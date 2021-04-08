---
description: Die Verzeichnis Tabelle gibt das Verzeichnis Layout für das Produkt an. Jede Zeile der Tabelle gibt ein Verzeichnis an, das sowohl an der Quelle als auch am Ziel liegt.
ms.assetid: eaca30cb-fec1-49ca-8b23-5e54c583e3e2
title: Verzeichnis Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273445aef67e3f166255321d0ac0ccf1aee37515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960058"
---
# <a name="directory-table"></a>Verzeichnis Tabelle

Die Verzeichnis Tabelle gibt das Verzeichnis Layout für das Produkt an. Jede Zeile der Tabelle gibt ein Verzeichnis an, das sowohl an der Quelle als auch am Ziel liegt.

Die Verzeichnis Tabelle enthält die folgenden Spalten.



| Spalte            | Typ                         | Schlüssel | Nullwerte zulässig |
|-------------------|------------------------------|-----|----------|
| Verzeichnis         | [Bezeichner](identifier.md) | J   | N        |
| Über \_ geordnetes Verzeichnis | [Bezeichner](identifier.md) | N   | J        |
| DefaultDir        | [DefaultDir](defaultdir.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>Befinden
</dt> <dd>

Die Verzeichnis Spalte enthält einen eindeutigen Bezeichner für ein Verzeichnis oder einen Verzeichnispfad. Diese Spalte kann den Namen einer Eigenschaft enthalten, die auf den vollständigen Pfad eines Zielverzeichnisses festgelegt ist. Wenn diese Spalte eine Eigenschaft enthält, übernimmt das Zielverzeichnis den in der Spalte DefaultDir angegebenen Namen und übernimmt das übergeordnete Verzeichnis, das in der übergeordneten Spalte des Verzeichnisses angegeben ist \_ .

Das Quellverzeichnis nimmt immer den in der Spalte DefaultDir angegebenen Namen an und übernimmt das übergeordnete Verzeichnis, das in der übergeordneten Spalte des Verzeichnisses angegeben ist \_ .

Wenn die \_ übergeordnete Spalte des Verzeichnisses entweder NULL oder gleich dem Wert der Verzeichnis Spalte ist, stellt die Verzeichnis Spalte ein Stammverzeichnis dar. In der Verzeichnis Tabelle kann nur ein Stammverzeichnis angegeben werden.

</dd> <dt>

<span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>Über \_ geordnetes Verzeichnis
</dt> <dd>

Diese Spalte ist ein Verweis auf das übergeordnete Verzeichnis des Verzeichnisses. Ein Datensatz mit einer über \_ geordneten Verzeichnis Spalte, die gleich NULL oder gleich der Verzeichnis Spalte ist, stellt ein Stammverzeichnis dar. Der vollständige Pfad des übergeordneten Verzeichnisses wird in der übergeordneten Spalte des Verzeichnisses als Verweis aufgelöst \_ . ist ein externer Schlüssel in der Verzeichnis Spalte. Wenn ein Ordner z. b. über ein übergeordnetes Verzeichnis namens pdir verfügt, wird das übergeordnete Verzeichnis von pdir in der über \_ geordneten Spalte des Verzeichnisses der Zeile mit pdir in der Spalte Verzeichnis angegeben.

</dd> <dt>

<span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>DefaultDir
</dt> <dd>

Die DefaultDir-Spalte enthält den Namen des Verzeichnisses (lokalisierbar) unter dem übergeordneten Verzeichnis. Standardmäßig ist dies der Name des Zielverzeichnisses und des Quell Verzeichnisses. Um verschiedene Quell-und Zielverzeichnis Namen anzugeben, trennen Sie die Ziel-und Quellnamen durch einen Doppelpunkt wie folgt: \[ TargetName \] : \[ SourceName \] .

Wenn der Wert der über \_ geordneten Verzeichnis Spalte NULL oder gleich der Verzeichnis Spalte ist, gibt die DefaultDir-Spalte den Namen eines Stamm Quell Verzeichnisses an.

Bei einem nicht stammenden Quellverzeichnis gibt ein Punkt (.), der in der DefaultDir-Spalte für den Quellverzeichnis Namen oder den Zielverzeichnis Namen eingegeben wird, an, dass sich das Verzeichnis in seinem übergeordneten Verzeichnis ohne Unterverzeichnis befinden soll.

Die Verzeichnisnamen in dieser Spalte können als kurze \| Dateiname-Paare mit langer Dateiname formatiert werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Jeder Datensatz in der Tabelle stellt ein Verzeichnis sowohl im Quell-als auch im Ziel Abbild dar. Die Verzeichnis Tabelle muss ein einzelnes Stammverzeichnis mit einem Verzeichnis Spaltenwert angeben, der der [**TARGETDIR**](targetdir.md) -Eigenschaft entspricht.

Installieren Sie für eine [Administrative Installation](administrative-installation.md)das administrative image im Stammverzeichnis TARGETDIR, und verwenden Sie die Quellverzeichnis Namen, um die Zielverzeichnisse aufzulösen.

Beachten Sie, dass das Installationsprogramm eine Reihe von Standard [Eigenschaften](properties.md) für Systemordner Pfade festlegt. Eine Liste der Eigenschaften, die auf Systemordner festgelegt sind, finden Sie in der [Eigenschafts Referenz](property-reference.md) .

Die Verzeichnis Auflösung erfolgt während der [Aktion "costfinalize](costfinalize-action.md) " und wird wie folgt ausgeführt:

### <a name="root-destination-directory"></a>Stammverzeichnis

Es darf nur ein einzelnes Stammverzeichnis vorhanden sein. Zum Angeben des Stammverzeichnis Verzeichnisses legen Sie die Spalte Verzeichnis auf die Eigenschaft [**TARGETDIR**](targetdir.md) und die Spalte DefaultDir auf die Eigenschaft [**SourceDir**](sourcedir.md) fest. Wenn die Eigenschaft **TARGETDIR** definiert ist, wird das Zielverzeichnis in den Wert der Eigenschaft aufgelöst. Wenn die **TARGETDIR** -Eigenschaft nicht definiert ist, wird der Pfad mithilfe der [**ROOTDRIVE**](rootdrive.md) -Eigenschaft aufgelöst.

### <a name="root-source-directory"></a>Stamm Quellverzeichnis

Der Wert der DefaultDir-Spalte für den Stammverzeichnis Eintrag muss auf die [**SourceDir**](sourcedir.md) -Eigenschaft festgelegt werden.

### <a name="non-root-destination-directories"></a>Nicht Stamm Verzeichnisse (Ziel)

Der Verzeichnis Wert für ein nicht-Stammverzeichnis wird auch als Name einer Eigenschaft interpretiert, die den Speicherort des Ziels definiert. Wenn die Eigenschaft definiert ist, wird das Zielverzeichnis in den Wert der Eigenschaft aufgelöst. Wenn die Eigenschaft nicht definiert ist, wird das Zielverzeichnis in ein Unterverzeichnis unter dem aufgelösten Zielverzeichnis für den über \_ geordneten Verzeichniseintrag aufgelöst. Der DefaultDir-Wert definiert den Namen des Unterverzeichnisses.

### <a name="non-root-source-directories"></a>Nicht Stamm Quellverzeichnisse

Das Quellverzeichnis für ein nicht-Stammverzeichnis wird in ein Unterverzeichnis des aufgelösten Quell Verzeichnisses für den über \_ geordneten Verzeichniseintrag aufgelöst. Der DefaultDir-Wert definiert den Namen des Unterverzeichnisses.

### <a name="short-or-long-file-names"></a>Kurze oder lange Dateinamen

Beim Auflösen von Zielverzeichnissen werden die in der DefaultDir-Spalte angegebenen kurzen Dateinamen verwendet, wenn entweder die [**shortfileames**](shortfilenames.md) -Eigenschaft festgelegt ist oder das Volume, auf dem sich das Verzeichnis befindet, keine langen Dateinamen unterstützt. Andernfalls wird der lange Dateiname verwendet.

Beachten Sie Folgendes: Wenn die Verzeichnisse während der costfinalize-Aktion aufgelöst werden, werden die Schlüssel in der Verzeichnis Tabelle zu [Eigenschaften](properties.md) , die auf Verzeichnispfade festgelegt sind.

[Tabelle "Buildordner"](createfolder-table.md)

Informationen zum Erstellen von leeren Ordnern während einer Installation finden Sie in der [Tabelle "Tabelle](createfolder-table.md)".

[Verwenden der Verzeichnis Tabelle](using-the-directory-table.md)

Weitere Informationen zur Verzeichnis Tabelle, einschließlich Beispielen, finden Sie unter [Verwenden der Verzeichnis Tabelle](using-the-directory-table.md).

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE07](ice07.md)  
[ICE30](ice30.md)  
[ICE32](ice32.md)  
[ICE38](ice38.md)  
[ICE46](ice46.md)  
[ICE48](ice48.md)  
[ICE56](ice56.md)  
[ICE57](ice57.md)  
[ICE64](ice64.md)  
[ICE88](ice88.md)  
[ICE90](ice90.md)  
[ICE91](ice91.md)  
[ICE99](ice99.md)  
</dl>

 

 



