---
description: Die Tabelle Directory gibt das Verzeichnislayout für das Produkt an. Jede Zeile der Tabelle gibt ein Verzeichnis sowohl an der Quelle als auch am Ziel an.
ms.assetid: eaca30cb-fec1-49ca-8b23-5e54c583e3e2
title: Verzeichnistabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f19e9b5994062ac55564799854fc36016fc6ddb9887bc36aa9a94652ef31aeb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947344"
---
# <a name="directory-table"></a>Verzeichnistabelle

Die Tabelle Directory gibt das Verzeichnislayout für das Produkt an. Jede Zeile der Tabelle gibt ein Verzeichnis sowohl an der Quelle als auch am Ziel an.

Die Tabelle Directory enthält die folgenden Spalten.



| Spalte            | Typ                         | Key | Nullwerte zulässig |
|-------------------|------------------------------|-----|----------|
| Verzeichnis         | [Identifier](identifier.md) | J   | N        |
| Übergeordnetes Verzeichnis \_ | [Identifier](identifier.md) | N   | J        |
| DefaultDir        | [DefaultDir](defaultdir.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Directory"></span><span id="directory"></span><span id="DIRECTORY"></span>Verzeichnis
</dt> <dd>

Die Spalte Verzeichnis enthält einen eindeutigen Bezeichner für ein Verzeichnis oder einen Verzeichnispfad. Diese Spalte kann den Namen einer Eigenschaft enthalten, die auf den vollständigen Pfad eines Zielverzeichnisses festgelegt ist. Wenn diese Spalte eine Eigenschaft enthält, verwendet das Zielverzeichnis den in der DefaultDir -Spalte angegebenen Namen und das übergeordnete Verzeichnis, das in der Spalte Directory \_ Parent angegeben ist.

Das Quellverzeichnis verwendet immer den in der Spalte DefaultDir angegebenen Namen und das übergeordnete Verzeichnis, das in der Spalte Directory \_ Parent angegeben ist.

Wenn die Spalte Directory Parent entweder NULL oder gleich dem Wert der Directory -Spalte ist, stellt die Directory -Spalte \_ ein Stammzielverzeichnis dar. In der Directory-Tabelle kann nur ein Stammverzeichnis angegeben werden.

</dd> <dt>

<span id="Directory_Parent"></span><span id="directory_parent"></span><span id="DIRECTORY_PARENT"></span>Übergeordnetes \_ Verzeichnis
</dt> <dd>

Diese Spalte ist ein Verweis auf das übergeordnete Verzeichnis des Verzeichnisses. Ein Datensatz mit einer übergeordneten Verzeichnisspalte gleich NULL oder gleich der Directory -Spalte \_ stellt ein Stammverzeichnis dar. Der vollständige Pfad des übergeordneten Verzeichnisses wird als Verweis in der Spalte Directory Parent (Übergeordnetes Verzeichnis) aufgelöst und ist ein externer Schlüssel \_ in der Spalte Directory. Wenn ein Ordner beispielsweise über ein übergeordnetes Verzeichnis namens PDIR verfügt, wird das übergeordnete Verzeichnis von PDIR in der Directory Parent -Spalte der Zeile mit PDIR in der \_ Directory -Spalte angegeben.

</dd> <dt>

<span id="DefaultDir"></span><span id="defaultdir"></span><span id="DEFAULTDIR"></span>DefaultDir
</dt> <dd>

Die Spalte DefaultDir enthält den Namen des Verzeichnisses (lokalisierbar) unter dem übergeordneten Verzeichnis. Standardmäßig ist dies der Name des Ziel- und des Quellverzeichnisses. Um unterschiedliche Quell- und Zielverzeichnisnamen anzugeben, trennen Sie die Ziel- und Quellnamen wie folgt durch einen \[ Doppelpunkt: Zielname \] : \[ Quellname \] .

Wenn der Wert der Übergeordneten Verzeichnisspalte NULL oder gleich der Spalte Directory ist, gibt die Spalte DefaultDir den Namen eines \_ Stammquellenverzeichnisses an.

Bei einem Quellverzeichnis, das kein Stammverzeichnis ist, gibt ein in der Spalte DefaultDir eingegebener Zeitraum (.) für den Quellverzeichnisnamen oder den Zielverzeichnisnamen an, dass sich das Verzeichnis im übergeordneten Verzeichnis ohne Unterverzeichnis befinden soll.

Die Verzeichnisnamen in dieser Spalte können als kurze Dateinamenpaare \| mit langen Dateinamen formatiert werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Jeder Datensatz in der Tabelle stellt ein Verzeichnis sowohl im Quell- als auch im Zielbild dar. Die Directory-Tabelle muss ein einzelnes Stammverzeichnis mit einem Directory-Spaltenwert angeben, der der [**TARGETDIR-Eigenschaft**](targetdir.md) entspricht.

Installieren Sie [bei einer Administratorinstallation](administrative-installation.md)das Administrative Image im Stammverzeichnis TARGETDIR, und verwenden Sie die Namen des Quellverzeichnisses, um die Zielverzeichnisse aufzulösen.

Beachten Sie, dass das Installationsprogramm eine Reihe von [Standardeigenschaften auf](properties.md) Systemordnerpfade fest legt. Eine Liste [der Eigenschaften, die](property-reference.md) auf Systemordner festgelegt sind, finden Sie in der Eigenschaftenreferenz.

Die Verzeichnisauflösung wird während der [Aktion CostFinalize](costfinalize-action.md) durchgeführt und erfolgt wie folgt:

### <a name="root-destination-directory"></a>Stammzielverzeichnis

Möglicherweise ist nur ein einzelnes Stammzielverzeichnis vorhanden. Um das Stammzielverzeichnis anzugeben, legen Sie die Directory-Spalte auf die [**TARGETDIR-Eigenschaft**](targetdir.md) und die DefaultDir -Spalte auf die [**SourceDir-Eigenschaft**](sourcedir.md) fest. Wenn die **TARGETDIR-Eigenschaft** definiert ist, wird das Zielverzeichnis in den Wert der Eigenschaft aufgelöst. Wenn die **TARGETDIR-Eigenschaft** nicht definiert ist, wird die [**ROOTDRIVE-Eigenschaft**](rootdrive.md) verwendet, um den Pfad aufzulösen.

### <a name="root-source-directory"></a>Stamm-Quellverzeichnis

Der Wert der DefaultDir-Spalte für den Stammverzeichniseintrag muss auf die [**SourceDir-Eigenschaft festgelegt**](sourcedir.md) werden.

### <a name="non-root-destination-directories"></a>Zielverzeichnisse ohne Stamm

Der Verzeichniswert für ein Nicht-Stammverzeichnis wird auch als Name einer Eigenschaft interpretiert, die den Speicherort des Ziels definiert. Wenn die Eigenschaft definiert ist, wird das Zielverzeichnis in den Wert der Eigenschaft aufgelöst. Wenn die Eigenschaft nicht definiert ist, wird das Zielverzeichnis in ein Unterverzeichnis unterhalb des aufgelösten Zielverzeichnisses für den Eintrag Übergeordnetes Verzeichnis \_ aufgelöst. Der DefaultDir-Wert definiert den Namen des Unterverzeichnisses.

### <a name="non-root-source-directories"></a>Quellverzeichnisse ohne Stamm

Das Quellverzeichnis für ein Nicht-Stammverzeichnis wird in ein Unterverzeichnis des aufgelösten Quellverzeichnisses für den Eintrag Übergeordnetes Verzeichnis \_ aufgelöst. Auch hier definiert der DefaultDir-Wert den Namen des Unterverzeichnisses.

### <a name="short-or-long-file-names"></a>Kurze oder lange Dateinamen

Beim Auflösen von Zielverzeichnissen werden die in der Spalte DefaultDir angegebenen kurzen Dateinamen verwendet, wenn entweder die [**SHORTFILENAMES-Eigenschaft**](shortfilenames.md) festgelegt ist oder das Volume, auf dem sich das Verzeichnis befindet, keine langen Dateinamen unterstützt. Andernfalls wird der lange Dateiname verwendet.

Beachten Sie Folgendes: Wenn die Verzeichnisse während der Aktion CostFinalize aufgelöst werden, werden die Schlüssel in der Directory-Tabelle zu Eigenschaften, die [auf](properties.md) Verzeichnispfade festgelegt sind.

[CreateFolder-Tabelle](createfolder-table.md)

Informationen zum Erstellen leerer Ordner während einer Installation finden Sie unter [CreateFolder Table](createfolder-table.md).

[Verwenden der Verzeichnistabelle](using-the-directory-table.md)

Weitere Informationen zur Verzeichnistabelle, einschließlich Beispielen, finden Sie unter [Verwenden der Verzeichnistabelle](using-the-directory-table.md).

## <a name="validation"></a>Überprüfung

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

 

 



