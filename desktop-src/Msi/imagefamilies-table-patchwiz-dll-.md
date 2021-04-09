---
description: Eine Bild Familie ist eine Gruppe von einem oder mehreren aktualisierten Images eines Produkts, die auf die neueste Version aktualisiert wurden.
ms.assetid: 06a77b35-b593-47e6-9083-46a6b65b7481
title: Tabelle "ImageFamilies" (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ece99e3c42626eb2155f16f2198703dc31b682
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959221"
---
# <a name="imagefamilies-table-patchwizdll"></a>Tabelle "ImageFamilies" (Patchwiz.dll)

Eine Bild Familie ist eine Gruppe von einem oder mehreren aktualisierten Images eines Produkts, die auf die neueste Version aktualisiert wurden. Jedes aktualisierte Image darf nur einer Familie angehören. Aktualisierte Images, die zu einer Abbild Familie gehören, nutzen eine oder mehrere Dateien gemeinsam. Jede Bild Familie verfügt über eine eigene CAB-Datei in der MSP-Datei, die die binären Patches und die neuen Dateien enthält, die zum Aktualisieren der Unterschiede Zwischenziel Dateien und aktualisierten Dateien erforderlich sind. Die CAB-Datei repliziert nicht die binären Patches und neuen Dateien, die von den freigegebenen Dateien verwendet werden.

Eine Tabelle "ImageFamilies", die mindestens einen Datensatz enthält, ist in jeder Datenbank der Patcherstellung (PCP-Datei) erforderlich. Diese Tabelle wird von der [uikreatepatchpackageex](uicreatepatchpackageex--patchwiz-dll-.md) -Funktion verwendet.

Die Tabelle "ImageFamilies" enthält die Patchinformationen, die der [Medien Tabelle](media-table.md)hinzugefügt werden sollen. Ein Patch fügt der Medien Tabelle einen Eintrag hinzu. Jeder Datensatz in den Tabellen "ImageFamilies" bezieht sich auf eine Gruppe verwandter Produkt Images, die auf die neueste Version des Produkts aktualisiert wurden.

Die Tabelle "ImageFamilies" weist die folgenden Spalten auf. Ein NULL-Wert kann in den Spalten mediasrcpropname, mediadiskid und filesequencestart verwendet werden, wenn der Patch mit Windows Installer und Patchwiz.dll Version 2,0 angewendet wird.



| Spalte            | Typ    | Schlüssel | Nullwerte zulässig |
|-------------------|---------|-----|----------|
| Familie            | text    | J   | N        |
| Mediasrcpropname  | text    |     | J        |
| Mediadiskid       | integer |     | J        |
| Filesequencestart | integer |     | J        |
| Diskprompt        | text    |     | J        |
| VolumeLabel       | text    |     | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Ärzte
</dt> <dd>

Der in diesem Feld eingegebene Wert ist ein Bezeichner für eine Gruppe verwandter Produkt Images, die auf die neueste Version des Produkts aktualisiert wurden. Auf insgesamt 8 alphanumerische Zeichen oder Unterstriche beschränkt. Das Installationsprogramm bettet einen CAB-Stream in der Windows Installer Patchdatei (MSP-Datei) für jede Familie in der Tabelle ein. Die CAB-Datei enthält die binären Patches und neuen Dateien, die zum Aktualisieren eines zielbilds in ein aktualisiertes Image des Produkts erforderlich sind. Das Installationsprogramm fügt den Familiennamen mit PCW \_ CAB \_ als Präfix ein, um den in das CAB-Feld des neuen [Medien Tabellen](media-table.md) Eintrags eingegebenen Datenstrom Namen zu generieren.

</dd> <dt>

<span id="MediaSrcPropName"></span><span id="mediasrcpropname"></span><span id="MEDIASRCPROPNAME"></span>Mediasrcpropname
</dt> <dd>

Der Wert, der in das Quellfeld des neuen [Medien Tabellen](media-table.md) Eintrags für das aktualisierte Image eingegeben wurde. Dieses Feld kann nur NULL sein, wenn Sie die Version 2,0 von Patchwiz.dll verwenden und die minimumrequirements dmsiversion in der [Properties-Tabelle (Patchwiz.dll)](properties-table-patchwiz-dll-.md) auf 200 festgelegt ist.

</dd> <dt>

<span id="MediaDiskId"></span><span id="mediadiskid"></span><span id="MEDIADISKID"></span>Mediadiskid
</dt> <dd>

Der Installer gibt diesen Wert in das DiskId-Feld des neuen [Medien Tabellen](media-table.md) Datensatzes ein. Der DiskId-Wert muss größer sein als jede aktuelle DiskId im Zielpaket. Der Grenzwert für mediadiskid ist 32767. Dieses Feld kann nur NULL sein, wenn Sie die Version 2,0 von Patchwiz.dll verwenden und die minimumrequirements dmsiversion in der [Properties-Tabelle (Patchwiz.dll)](properties-table-patchwiz-dll-.md) auf 200 festgelegt ist.

</dd> <dt>

<span id="FileSequenceStart"></span><span id="filesequencestart"></span><span id="FILESEQUENCESTART"></span>Filesequencestart
</dt> <dd>

Dieses Feld ist die Sequenznummer für die Startdatei. Dieselbe Datei Sequenznummer darf nicht in zwei Patches für dasselbe Produkt vorhanden sein. Um dies zu gewährleisten, muss der Wert in diesem Feld größer sein als alle Sequenznummern, die in vorherigen Patches oder im ursprünglichen Installationspaket verwendet wurden. Die größte Sequenznummer in einem Patch kann bestimmt werden, indem der filesequencestart-Nummer für diesen Patch die Gesamtanzahl der Einträge in der patchcab-Datei hinzugefügt wird. Eine Möglichkeit, dies zu ermitteln, besteht darin, die. ddf-Datei zu überprüfen, die während der Erstellung des Patches von [Patchwiz.dll](patchwiz-dll.md) generiert wurde. Der Grenzwert für filesequencestart ist 32767. Dieses Feld kann nur NULL sein, wenn Sie die Version 2,0 von Patchwiz.dll verwenden und die minimumrequirements dmsiversion in der [Properties-Tabelle (Patchwiz.dll)](properties-table-patchwiz-dll-.md) auf 200 festgelegt ist.

</dd> <dt>

<span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>Diskprompt
</dt> <dd>

Der Installer gibt diesen Wert in das Feld diskprompt des Datensatzes der neuen [Medien Tabelle](media-table.md) ein.

</dd> <dt>

<span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel
</dt> <dd>

Der Installer gibt diesen Wert in das Feld VolumeLabel des neuen Mediendaten Satzes ein.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Patch fügt dem CAB-Feld des neuen Datensatzes, der der [Medien Tabelle](media-table.md)hinzugefügt wurde, den Namen der CAB-Datei in der MSP-Datei hinzu. Da es sich um eine eingebettete CAB-Datei handelt, wird dem Namen ein Zeichen ' ' vorangestellt \# . Der Patch fügt dem Quellfeld des neuen Datensatzes in der Medien Tabelle eine Eigenschaft hinzu. Es können nicht zwei Patches die gleiche Quell Eigenschaft aufweisen.

Die Dateien, die in der Bild Familie freigegeben werden, müssen in jedem aktualisierten Image der Familie über denselben Datei Tabellenschlüssel verfügen. Alle Datei Tabellenschlüssel, die von den aktualisierten Images gemeinsam genutzt werden, müssen dieselbe Datei darstellen und müssen in allen aktualisierten Images identisch sein. Der Datei Tabellenschlüssel ist der Wert, der in der Datei Spalte der [Dateitabelle](file-table.md)eingegeben wurde.

Der Grenzwert für mediadiskid und filesequencestart ist 32767. Um dieses Limit zu erhöhen, exportieren Sie die Tabelle "ImageFamilies" in eine IDT-Datei mit [Msidb.exe](msidb-exe.md) und ändern Sie den Spaltentyp von "I2" in "I4" oder "I2" in "I4". importieren Sie dann die IDT-Datei zurück in die PCP-Datenbank. Transformationen und Patches können nicht zwischen zwei Paketen mit unterschiedlichen Spaltentypen erstellt werden.

 

 



