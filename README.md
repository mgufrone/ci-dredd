## Hercule, Dredd, and Fury in one Image

This image is based on the use case when I need those three to do testing using dredd. But installing dredd is such a painful time so I would like to skip the compilation of those three in this image.


### HOW TO

    docker pull mgufrone/ci-dredd
    # Running Hercule
    docker run -v yourpath:/src --net=host mgufrone/ci-dredd:latest hercule blueprint/blueprint.apib -o apiary.apib
    # Running Fury
    # Running Dredd
    docker run -v yourpath:/src --net=host mgufrone/ci-dredd:latest fury --validate apiary.apib
    # Running Dredd
    docker run -v yourpath:/src --net=host mgufrone/ci-dredd:latest dredd
