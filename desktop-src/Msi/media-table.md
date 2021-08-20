---
description: In der Tabelle Medien werden die Datenträger beschrieben, aus denen sich die Quellmedien für die Installation zusammensetzen.
ms.assetid: f9789f1d-35bf-40d6-9724-d5a160a0d06d
title: Medientabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29939553e64fb6558aa6480fb69b7beab208a4ccb3e2c9ce55c4d8fcbfc18cc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805095"
---
# <a name="media-table"></a>Medientabelle

In der Tabelle Medien werden die Datenträger beschrieben, aus denen sich die Quellmedien für die Installation zusammensetzen.

Die Tabelle Media enthält die spalten, die in der folgenden Tabelle angezeigt werden.



| Spalte       | Typ                     | Key | Nullwerte zulässig |
|--------------|--------------------------|-----|----------|
| DiskId       | [Integer](integer.md)   | J   | N        |
| LastSequence | [Integer](integer.md)   | N   | N        |
| DiskPrompt   | [Text](text.md)         | N   | J        |
| Kabinett      | [Kabinett](cabinet.md)   | N   | J        |
| VolumeLabel  | [Text](text.md)         | N   | J        |
| Quelle       | [Eigenschaft](property.md) | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="DiskId"></span><span id="diskid"></span><span id="DISKID"></span>DiskId
</dt> <dd>

Bestimmt die Sortierreihenfolge für die Tabelle. Diese Zahl muss gleich oder größer als 1 sein.

</dd> <dt>

<span id="LastSequence"></span><span id="lastsequence"></span><span id="LASTSEQUENCE"></span>LastSequence
</dt> <dd>

Dateisequenznummer für die letzte Datei für dieses Medium. Die Zahlen in der Spalte LastSequence geben an, welche Dateien in der [Dateitabelle](file-table.md) auf einem bestimmten Quelldatenträger gefunden werden. Jeder Quelldatenträger enthält alle Dateien mit Sequenznummern (wie in der Spalte Sequenz der Dateitabelle gezeigt) kleiner oder gleich dem Wert in der Spalte LastSequence und größer als der LastSequence-Wert des vorherigen Datenträgers (oder größer als 0 für den ersten Eintrag in der Media-Tabelle). Diese Zahl muss nicht negativ sein. Der maximale Grenzwert beträgt 32767 Dateien. Weitere Informationen zum Erstellen eines Windows Installer-Pakets mit weiteren Dateien finden Sie unter [Erstellen eines großen Pakets.](authoring-a-large-package.md)

</dd> <dt>

<span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt
</dt> <dd>

Der Datenträgername, bei dem es sich in der Regel um den sichtbaren Text handelt, der auf dem Datenträger ausgegeben wird. Dieser lokalisierbare Text wird verwendet, um den Benutzer aufzufordern, wenn dieser Datenträger eingefügt werden muss.

</dd> <dt>

<span id="Cabinet"></span><span id="cabinet"></span><span id="CABINET"></span>Kabinett
</dt> <dd>

Der Name des Gehäuses, wenn einige oder alle auf dem Medium gespeicherten Dateien in eine Cab-Datei komprimiert werden. Wenn keine Schränke verwendet werden, muss diese Spalte leer sein. Der Name des Cab muss die Syntax des [Cabinet-Datentyps](cabinet.md) verwenden. Windows Das Installationsprogramm erfordert immer eine gültige Quelle, um Dateien zu reparieren, die in eingebetteten Cab-Dateien enthalten sind. Wenn Windows Installer ein Paket installiert, das eine eingebettete Cab-Datei enthält, kann eine Kopie der Cab-Datei vom System gespeichert werden. Diese Kopie kann nicht zum Reparieren der Schränkdatei verwendet werden. Um Speicherplatz zu sparen, verwenden Sie externe Cab-Dateien anstelle eingebetteter Cab-Dateien.

</dd> <dt>

<span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel
</dt> <dd>

Die bezeichnung, die dem Volume zugeordnet ist. Dies ist die Volumebezeichnung, die von der [**GetVolumeInformation-Funktion**](/windows/win32/api/fileapi/nf-fileapi-getvolumeinformationa) zurückgegeben wird. Wenn die [**SourceDir-Eigenschaft**](sourcedir.md) auf ein Wechseldatenträgervolume (Diskette oder CD-ROM) verweist, wird diese Volumebezeichnung verwendet, um zu überprüfen, ob sich der richtige Datenträger auf dem Laufwerk befindet, bevor versucht wird, Dateien zu installieren. Der Eintrag in dieser Spalte muss mit der Volumebezeichnung des physischen Mediums übereinstimmen.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Quelle
</dt> <dd>

Dieses Feld wird nur beim Patchen verwendet und wird andernfalls leer gelassen. Eine Patchtransformation kann hier eine Eigenschaft eingeben, bei der es sich um den Speicherort der Cab-Datei mit den Patchdateien oder um neue Dateien handelt, die vom Patch hinzugefügt wurden. Für diese Dateien muss eine andere Quelle angegeben werden, da die Quelle des Patchpakets getrennt von der Quelle des Produkts gespeichert werden kann. Wenn das Feld "Cabinet" leer ist, ignoriert das Installationsprogramm den Wert in dieser Spalte. Wenn dieses Feld leer ist, verwendet das Installationsprogramm den Wert der [**SourceDir-Eigenschaft**](sourcedir.md) als Quelle des Schränks.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn dem Cab-Namen ein Nummernzeichen ( ) vorangestellt \# ist, werden die Dateien, die auf diesen Medientabellendatensatz verweisen, in eine Cab-Datei gepackt, die in der Datenbank als separater Stream gespeichert ist.

Weitere Informationen zum Hinzufügen von Schränken zu Dateitabellen und Medientabellen finden Sie unter [Verwenden von Schränken und komprimierten Quellen.](using-cabinets-and-compressed-sources.md)

Windows Das Installationsprogramm erfordert, dass sich die .msi-Datei auf dem ersten Datenträger mit Wechselmedien (CD, DVD oder Diskette) befindet, die für die Installation des Produkts verwendet werden.

**Bestimmen des SourceMode**

Die [**Word Count Summary-Eigenschaft**](word-count-summary.md) bestimmt den Quellmodus für die aktuelle Installation. Wenn diese Eigenschaft auf 2 oder 3 festgelegt ist, wird von einer Installation des Gehäuses ausgegangen. In diesem Modus wird davon ausgegangen, dass die Cab-Dateien in dem Verzeichnis vorhanden sind, das durch die [**SourceDir-Eigenschaft**](sourcedir.md) angegeben wird. Wenn der Quelltypwert 0 oder 1 ist, wird davon ausgegangen, dass alle Quelldateien in der Struktur vorhanden sind, deren Stamm durch die **SourceDir-Eigenschaft** angegeben wird.

Beachten Sie, dass dies nur für Dateien in der Dateitabelle gilt, für die in der Attributspalte weder komprimierte noch unkomprimierte Bits festgelegt sind. Diese Bits überschreiben den Wert der [**Word Count Summary-Eigenschaft,**](word-count-summary.md) wenn bestimmt wird, ob eine bestimmte Datei komprimiert oder nicht komprimiert ist.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE04](ice04.md)  
[ICE06](ice06.md)  
[ICE35](ice35.md)  
[ICE58](ice58.md)  
[ICE71](ice71.md)  
[ICE81](ice81.md)  
</dl>

 

 
