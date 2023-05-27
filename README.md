# diarization_khoekhoe
Репозиторий для курсовой работы на тему «Диаризация говорящих на данных малоресурсных языков» (англ. «Speaker Diarization on the data of Low-Resource languages») 

- creatingprotocol.ipynb получает на вход аннотированные в ELAN файлы с расширением .eaf (сами файлы и список их названий в csv) и делает из них базу данных database.yml. В базе данных лежат ссылки на три типа файлов: .rttm (файлы с аннотированными сегментами каждого аудио), .uem (границы аннотации), .lst (список названий аудио).
- finetuningandoptimizing.ipynb: получает на вход database.yml и на имеющихся данных файнтюнит модель и оптимизирует параметры. Код данного файла адаптирован с туториала https://github.com/pyannote/pyannote-audio/blob/develop/tutorials/adapting_pretrained_pipeline.ipynb
- correlations.ipynb: считает корреляции DER и параметров, которые могут быть значимыми (общая продолжительность речи в файле, язык говорения и количество говорящих)
