# to get the list of input files, go to the root of the document folder, and:
# grep -r '\\input{' * | cut -d ':' -f 2 | cut -c 8- | rev | cut -c 2- | rev | sed 's|^|  ${PROJECT_SOURCE_DIR}/acknowledgments/|g' | sed 's/$/.tex/g'
set(INCLUDED_TEX
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/../header.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/auxiliary-programs.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/auxiliary-energyplus-programs.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/weather-converter-program.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/weather-converter-program/background.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/weather-converter-program/weather-format-for-simulation-programs.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/weather-converter-program/weather-data-availability.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/weather-converter-program/using-the-weather-converter.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/weather-converter-program/definitions-file-custom-file-processing.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/weather-converter-program/reports-files-produced-by-the-weather.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/weather-converter-program/k-ppen-climate-classification.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/weather-converter-program/ashrae-climate-classification.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/weather-converter-program/energyplus-weather-file-epw-data-dictionary.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/weather-converter-program/epw-csv-format-in-out.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/weather-converter-program/missing-weather-file-data.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/weather-converter-program/source-weather-data-formats.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/weather-converter-program/data-sources-uncertainty.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/weather-converter-program/advanced-use-accessing-weather-conversion.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/weather-converter-program/references.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/weather-converter-program/web-resources.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/ground-heat-transfer-in-energyplus.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/ground-heat-transfer-in-energyplus/use-of-the-ground-temperatures-with-slabs.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/ground-heat-transfer-in-energyplus/slab-configuration-drawing.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/ground-heat-transfer-in-energyplus/running-the-slab-program.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/ground-heat-transfer-in-energyplus/technical-details-on-files-for-ground-heat.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/ground-heat-transfer-in-energyplus/slab-program-output-files.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/ground-heat-transfer-in-energyplus/description-of-the-objects-in-the-e-slabght.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/ground-heat-transfer-in-energyplus/using-ground-temperatures-with-basements.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/ground-heat-transfer-in-energyplus/running-the-basement-program.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/ground-heat-transfer-in-energyplus/technical-details-on-files-for-ground-heat-001.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/ground-heat-transfer-in-energyplus/basement-program-output-files.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/ground-heat-transfer-in-energyplus/the-basement-idd.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/ground-heat-transfer-in-energyplus/description-of-the-objects-in-the-basementght.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/ground-heat-transfer-in-energyplus/using-the-interface-surface-temperature.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/ground-heat-transfer-in-energyplus/references-001.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/view-factor-calculation-program.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/view-factor-calculation-program/using-the-view-factor-interface-program.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/view-factor-calculation-program/additional-information.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/using-older-version-input-files-transition.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/using-older-version-input-files-transition/idf-version-updater.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/using-older-version-input-files-transition/transition-console-program-details.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/using-older-version-input-files-transition/idf-version-converter-transition-file-lists.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/using-older-version-input-files-transition/converting-imf-files.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/epdrawgui.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/epdrawgui/main-tab.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/epdrawgui/option-tab.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/input-macros.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/input-macros/introduction-001.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/input-macros/running-the-ep-macro-program.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/input-macros/incorporating-external-files.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/input-macros/selectively-accepting-or-skipping-lines-of.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/input-macros/defining-blocks-of-input.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/input-macros/macro-debugging-and-listing-control.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/input-macros/listing-format.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/hvac-diagram.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/hvac-diagram/introduction-002.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/coeffconv-coeffcheck.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/coeffconv-coeffcheck/coeffconv.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/coeffconv-coeffcheck/coeffcheck.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/coeffconv-coeffcheck/running-the-coeffconv-or-coeffcheck-programs.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/expandobjects.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/expandobjects/introduction-003.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/expandobjects/hvac-template-objects-processed.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/expandobjects/ground-heat-transfer-objects-processed.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/expandobjects/building-surface-objects-processed.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/csvproc.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/convertesomtr.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/calcsoilsurftemp-program.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/calcsoilsurftemp-program/running-the-program.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/calcsoilsurftemp-program/program-inputs.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/calcsoilsurftemp-program/program-outputs.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/hvac-performance-curve-fit-tool.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/hvac-performance-curve-fit-tool/introduction-004.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/hvac-performance-curve-fit-tool/inputs.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/hvac-performance-curve-fit-tool/rated-data.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/hvac-performance-curve-fit-tool/performance-data.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/hvac-performance-curve-fit-tool/outputs.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/hvac-performance-curve-fit-tool/error-message.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/hvac-performance-curve-fit-tool/notes.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/hvac-performance-curve-fit-tool/references-002.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/parametric-spreadsheets.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/parametric-spreadsheets/water-to-water-heat-pump-parameter.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/parametric-spreadsheets/water-to-air-heat-pump-parameter-coefficient.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/parametric-spreadsheets/water-to-air-heat-pump-parameter-coefficient-001.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/parametric-spreadsheets/g-function-spreadsheet.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/parametricpreprocessor.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/appgpostprocess-appendix-g-postprocessing.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/running-console-applications.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/running-console-applications/modifying-the-batch-file.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/technical-details-of-running-energyplus.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/technical-details-of-running-energyplus/ep-launch-program.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/technical-details-of-running-energyplus/ep-launch-lite.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/technical-details-of-running-energyplus/energyplus-file-extensions.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/technical-details-of-running-energyplus/runeplus-batch-file.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/technical-details-of-running-energyplus/running-energyplus-by-hand.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/technical-details-of-running-energyplus/runeplus-details.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/technical-details-of-running-energyplus/rundirmulti-batch-file.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/technical-details-of-running-energyplus/energyplus-files.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/creating-input-files.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/creating-input-files/idd-conventions.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/creating-input-files/idfeditor.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/manipulating-output-files.tex
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/src/manipulating-output-files/ep-compare.tex
    ${PROJECT_SOURCE_DIR}/title.tex)

# to get the list of inluded images, go to the root of the document folder and:
# grep -r '\\includegraphics' * | cut -d ':' -f 2 | rev | cut -d '{' -f 1 | rev | cut -d '}' -f 1 | sed 's/^/  /g' | sort -n -t'.' -k 1.14
set(INCLUDED_IMAGES
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image001.jpg
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image002.jpg
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image003.jpg
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image006.jpg
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image007.jpg
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image008.jpg
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image009.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image010.jpg
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image011.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image012.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image015.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image016.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image018.jpg
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image019.jpg
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image020.jpg
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image021.jpg
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image022.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image023.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image024.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image025.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image026.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image027.jpg
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image028.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image029.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image030.jpg
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image034.jpg
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image036.jpg
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image037.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image038.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image039.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image040.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image041.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image041.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image041.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image042.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image043.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image044.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image045.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image046.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image047.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image048.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image049.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image050.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image051.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image052.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image053.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image054.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image055.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image056.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image057.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image058.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image059.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image059.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image060.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image101.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image102.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image103.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image104.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image105.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image106.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image107.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image108.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image109.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image110.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image111.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image112.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image113.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image114.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image115.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image116.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image117.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image118.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image119.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image120.png
    ${PROJECT_SOURCE_DIR}/auxiliary-programs/media/image121.png)

create_doc_target("auxiliary-programs" "AuxiliaryPrograms")
