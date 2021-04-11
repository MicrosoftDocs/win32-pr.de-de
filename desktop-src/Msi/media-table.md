---
description: In der Medien Tabelle wird der Satz von Datenträgern beschrieben, aus denen die-Quell Medien für die-Installation gemacht werden.
ms.assetid: f9789f1d-35bf-40d6-9724-d5a160a0d06d
title: Medien Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a59cd8bf864aa890891873ed92a39225c6eebdf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351258"
---
# <a name="media-table"></a>Medien Tabelle

In der Medien Tabelle wird der Satz von Datenträgern beschrieben, aus denen die-Quell Medien für die-Installation gemacht werden.

Die Medien Tabelle enthält die Spalten, die in der folgenden Tabelle aufgeführt sind.



| Spalte       | Typ                     | Schlüssel | Nullwerte zulässig |
|--------------|--------------------------|-----|----------|
| DiskId       | [Integer](integer.md)   | J   | N        |
| LastSequence | [Integer](integer.md)   | N   | N        |
| Diskprompt   | [Text](text.md)         | N   | J        |
| KEs      | [KEs](cabinet.md)   | N   | J        |
| VolumeLabel  | [Text](text.md)         | N   | J        |
| `Source`       | [Eigenschaft](property.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="DiskId"></span><span id="diskid"></span><span id="DISKID"></span>DiskId
</dt> <dd>

Bestimmt die Sortierreihenfolge für die Tabelle. Diese Zahl muss größer oder gleich 1 sein.

</dd> <dt>

<span id="LastSequence"></span><span id="lastsequence"></span><span id="LASTSEQUENCE"></span>LastSequence
</dt> <dd>

Datei Sequenznummer für die letzte Datei für dieses Medium. Die Zahlen in der Spalte LastSequence geben an, welche Dateien in der [Datei](file-table.md) Tabelle auf einem bestimmten Quell Datenträger gefunden werden. Jeder Quell Datenträger enthält alle Dateien mit Sequenznummern (wie in der Sequence-Spalte der File-Tabelle angezeigt), die kleiner oder gleich dem Wert in der LastSequence-Spalte sind, und größer als der LastSequence-Wert des vorherigen Datenträgers (oder größer als 0 für den ersten Eintrag in der Medien Tabelle). Diese Zahl darf nicht negativ sein. der maximale Grenzwert beträgt 32767 Dateien. Weitere Informationen zum Erstellen eines Windows Installer Pakets mit weiteren Dateien finden Sie unter Erstellen [eines großen Pakets](authoring-a-large-package.md).

</dd> <dt>

<span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>Diskprompt
</dt> <dd>

Der Datenträger Name, der in der Regel der auf dem Datenträger gedruckte sichtbare Text ist. Dieser lokalisierbare Text wird verwendet, um den Benutzer zur Eingabe aufzufordern, wenn dieser Datenträger eingefügt werden muss.

</dd> <dt>

<span id="Cabinet"></span><span id="cabinet"></span><span id="CABINET"></span>KEs
</dt> <dd>

Der Name der CAB-Datei, wenn einige oder alle Dateien, die auf dem Medium gespeichert sind, in eine CAB-Datei komprimiert werden. Wenn keine Schränke verwendet werden, muss diese Spalte leer sein. Der Name der CAB [-Datei muss](cabinet.md) die Syntax des CAB-Datentyps verwenden. Windows Installer benötigt immer eine gültige Quelle zum Reparieren von Dateien, die in eingebetteten CAB-Dateien enthalten sind. Wenn Windows Installer ein Paket installiert, das eine eingebettete CAB-Datei enthält, kann eine Kopie der CAB-Datei vom System gespeichert werden. Diese Kopie kann nicht verwendet werden, um die CAB-Datei zu reparieren. Um Speicherplatz zu sparen, verwenden Sie externe CAB-Dateien anstelle von eingebetteten CAB-Dateien.

</dd> <dt>

<span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel
</dt> <dd>

Die Bezeichnung, die dem Volume zugeordnet ist. Dies ist die Lautstärke Bezeichnung, die von der [**GetVolumeInformation**](/windows/win32/api/fileapi/nf-fileapi-getvolumeinformationa) -Funktion zurückgegeben wird. Wenn die [**SourceDir**](sourcedir.md) -Eigenschaft auf ein Wechsel Datenträger (Disketten oder CD-ROM) verweist, wird diese Volumebezeichnung verwendet, um zu überprüfen, ob sich der richtige Datenträger im Laufwerk befindet, bevor versucht wird, Dateien zu installieren. Der Eintrag in dieser Spalte muss mit der Volumebezeichnung des physischen Mediums identisch sein.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Ausgangs
</dt> <dd>

Dieses Feld wird nur durch Patchen verwendet und andernfalls leer gelassen. Eine patchtransformation kann hier eine Eigenschaft eingeben, bei der es sich um den Speicherort der CAB-Datei mit den Patchdateien oder um neue Dateien handelt, die vom Patch hinzugefügt werden. Für diese Dateien muss eine andere Quelle angegeben werden, da die Quelle des Patchpakets getrennt von der Produkt Quelle gespeichert werden kann. Wenn das CAB-Feld leer ist, ignoriert das Installationsprogramm den Wert in dieser Spalte. Wenn dieses Feld leer ist, verwendet das Installationsprogramm den Wert der [**SourceDir**](sourcedir.md) -Eigenschaft als Quelle der CAB-Datei.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn dem CAB-Namen ein Nummern Zeichen () vorangestellt ist \# , werden die Dateien, die auf diesen Medien Tabellendaten Satz verweisen, in einer CAB-Datei verpackt, die in der Datenbank als separater Stream gespeichert ist.

Weitere Informationen zum Hinzufügen von schränken zu den Datei Tabellen und Medien Tabellen finden Sie unter [Verwenden von Schränken und komprimierten Quellen](using-cabinets-and-compressed-sources.md).

Windows Installer erfordert, dass sich die MSI-Datei auf dem ersten Datenträger des Wechsel Datenträgers (CD, DVD oder Diskette) befindet, der für die Installation des Produkts verwendet wird.

**Bestimmen von sourcemode**

Die " [**Word Count Summary**](word-count-summary.md) "-Eigenschaft bestimmt den Quell Modus für die aktuelle Installation. Wenn diese Eigenschaft auf 2 oder 3 festgelegt ist, wird eine CAB-Installation angenommen. In diesem Modus wird davon ausgegangen, dass die CAB-Dateien im Verzeichnis vorhanden sind, das von der [**SourceDir**](sourcedir.md) -Eigenschaft angegeben wird. Wenn der Quelltyp "0" oder "1" ist, wird davon ausgegangen, dass alle Quelldateien in der Struktur vorhanden sind, deren Stamm durch die **SourceDir** -Eigenschaft angegeben wird.

Beachten Sie, dass dies nur für Dateien in der Dateitabelle gilt, für die in der Spalte Attribute weder das komprimierte als auch das unkomprimierte Bit festgelegt ist. Diese Bits überschreiben den Wert der [**Zusammenfassungs Eigenschaft der Wort Zählung**](word-count-summary.md) , wenn bestimmt wird, ob eine bestimmte Datei komprimiert oder unkomprimiert ist.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE04](ice04.md)  
[ICE06](ice06.md)  
[ICE35](ice35.md)  
[ICE58](ice58.md)  
[ICE71](ice71.md)  
[ICE81](ice81.md)  
</dl>

 

 
