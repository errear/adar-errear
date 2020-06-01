# Atividades do Curso ADAR (adar-errear) com o swirl

O **adar-errear** é um curso que usa a abordagem prática do pacote swirl. Ele serve para você praticar R (ou "errear") e para eu poder acompanhar seu andamento nas tarefas. A maioria das lições deste curso inclui diversos tópicos vistos no curso ADAR. As lições disponibilizadas estão sendo traduzidas do curso [Programando em R](https://github.com/swirldev/swirl_courses/tree/master/R_Programming). 

Este curso está em construção e você pode encontrar problemas durante a execução. Qualquer problema, por gentileza, avise-me para que possa corrigi-lo e adaptá-lo da melhor forma possível para o nosso curso.

## Instalação deste curso

```{r install-adar-errear}
install.packages(c("devtools", "base64enc", "httr"))
library(devtools)
install_course_github("errear", "adar-errear")
swirl()
```

## Use Google Forms in Your Course

Follow these steps in order to set up a Google
Form that can collect student's swirl progress:

1. Create a new form by clicking "New" on https://drive.google.com
2. Name your form something memorable.
3. Your form should have only one question which should be a paragraph type 
question.
4. In the upper right corner of the form there should be three vertical white
dots. Click on that icon and then click "Get pre-filled link." This will open
a new window.
5. Click "Submit" and copy the generated link.
6. Paste the generated link into `customTests.R` where indicated, so that a
string containing the link is assigned to the `pre_fill_link` variable in the
function `submit_log()`.

## Key Points in this Repo:

- swirl logging is disabled by default. Add the line 
`swirl_options(swirl_logging = TRUE)` to `initLesson.R` in order to enable 
logging.
- Copy my customTest.R file and edit the assignment of `pre_fill_link` as
described above.
- The last question of the lesson should look very similar to the last question
in this `lesson.yaml`. Of course you should feel free to edit the output.
- `dependson.txt` must at least contain `base64enc`.

## Decoding the Google Forms Submission

1. Install [swirlify](https://github.com/swirldev/swirlify). You must use a
version of swirlify later than 0.4.1.
2. Download the `csv` results from Google Forms.
3. Run `swirlify::google_form_decode()` and select the `csv` you downloaded.
4. `google_form_decode()` will return a data frame containing how each of your
students performed on every question.

## Help

Open an issue here or email us: info@swirlstats.com

---

## License

[CC0](https://creativecommons.org/publicdomain/zero/1.0/)