---
title: Versionsinformationen
description: In diesem Abschnitt wird die Ressource "Version-Information" erläutert.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\versioninformation.htm
keywords:
- Ressourcen, Versionsinformationen
- Versionsinformationen
- Versionsnummern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78e43de27f18f89a5f240242b63ade057f57ec92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310104"
---
# <a name="version-information"></a>Versionsinformationen

Versionsinformationen erleichtern Anwendungen die ordnungsgemäße Installation von Dateien und ermöglichen Setup Programmen das Analysieren von Dateien, die derzeit installiert sind. Die Ressource Version-Information enthält die Versionsnummer der Datei, das beabsichtigte Betriebssystem und den ursprünglichen Dateinamen.

### <a name="in-this-section"></a>In diesem Abschnitt



| Name                                                               | BESCHREIBUNG                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------|
| [Informationen zu Versionsinformationen](about-version-information.md)         | Erläutert die Versions Informationsfunktionen.<br/>            |
| [Verwenden von Versionsinformationen](using-version-information.md)         | Erläutert, wie die Versions Informationsfunktionen verwendet werden.<br/> |
| [Versions Informations Referenz](version-information-reference.md) | Enthält die API-Referenz.<br/>                             |



 

### <a name="version-information-functions"></a>Versions Informationsfunktionen



| Name                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)             | Ruft Versionsinformationen für die angegebene Datei ab. <br/>                                                                                                                                                                                                                                                                                                     |
| [**Getfileversioninfoex**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoexa)         | Ruft Versionsinformationen für die angegebene Datei ab.<br/>                                                                                                                                                                                                                                                                                                      |
| [**Fehler bei GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea)     | Bestimmt, ob das Betriebssystem Versionsinformationen für eine angegebene Datei abrufen kann. Wenn Versionsinformationen verfügbar sind, gibt [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) die Größe dieser Informationen in Byte zurück. <br/>                                                                                                             |
| [**Getfileversioninfosizeex**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizeexa) | Bestimmt, ob das Betriebssystem Versionsinformationen für eine angegebene Datei abrufen kann. Wenn Versionsinformationen verfügbar sind, gibt [**getfileversioninfosizeex**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizeexa) die Größe dieser Informationen in Byte zurück.<br/>                                                                                                          |
| [**Verfindfile**](/windows/desktop/api/Winver/nf-winver-verfindfilea)                           | Bestimmt, wo eine Datei installiert werden soll, je nachdem, ob eine andere Version der Datei im System lokalisiert wird. Die Werte, die [**verfindfile**](/windows/desktop/api/Winver/nf-winver-verfindfilea) in den angegebenen Puffern zurückgibt, werden in einem nachfolgenden Rückruf der [**verinstallfile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) -Funktion verwendet. <br/>                                                                          |
| [**Verinstallfile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea)                     | Installiert die angegebene Datei auf der Grundlage von Informationen, die von der [**verfindfile**](/windows/desktop/api/Winver/nf-winver-verfindfilea) -Funktion zurückgegeben werden. [**Verinstallfile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) dekomprimiert die Datei bei Bedarf, weist einen eindeutigen Dateinamen zu und überprüft auf Fehler, wie z. b. veraltete Dateien. <br/>                                                                                   |
| [**Verlanguagename**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea)                   | Ruft eine Beschreibungs Zeichenfolge für die Sprache ab, die einem angegebenen binären Microsoft-sprach Bezeichner zugeordnet ist.<br/>                                                                                                                                                                                                                                          |
| [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)                       | Ruft die angegebenen Versionsinformationen aus der angegebenen Version-Information-Ressource ab. Zum Abrufen der entsprechenden Ressource müssen Sie vor dem Aufrufen von [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)zuerst die [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) -Funktion und dann die [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa) -Funktion aufrufen. <br/> |



 

### <a name="version-information-structures"></a>Versions Informationsstrukturen



| Name                                          | BESCHREIBUNG                                                                                                                                                                                                                      |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Schnür**](string-str.md)                  | Zeigt die Organisation der Daten in einer Datei Versions Ressource an. Sie enthält eine Zeichenfolge, die einen bestimmten Aspekt einer Datei beschreibt, z. b. die Version einer Datei, die Copyright Hinweise oder ihre Marken.<br/>                |
| [**Stringfileingefo**](stringfileinfo.md)      | Zeigt die Organisation der Daten in einer Datei Versions Ressource an. Sie enthält Versionsinformationen, die für eine bestimmte Sprache und Codepage angezeigt werden können.<br/>                                                           |
| [**STRINGTABLE**](stringtable.md)            | Zeigt die Organisation der Daten in einer Datei Versions Ressource an. Sie enthält sprach-und Code Page Formatierungsinformationen für die Zeichen folgen, die vom **Children** -Member angegeben werden. Eine Codepage ist ein geordneter Zeichensatz.<br/> |
| [**Kreis**](var-str.md)                        | Zeigt die Organisation der Daten in einer Datei Versions Ressource an. Sie enthält in der Regel eine Liste der Sprachen-und Codepage-bezeichnerpaare, die von der Version der Anwendung oder DLL unterstützt werden.<br/>                             |
| [**Varfileingefo**](varfileinfo.md)            | Zeigt die Organisation der Daten in einer Datei Versions Ressource an. Sie enthält Versionsinformationen, die nicht von einer bestimmten Sprache und Codepage kombiniert werden.<br/>                                                        |
| [**VS \_ fixedfileingefo**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) | Enthält Versionsinformationen zu einer Datei. Diese Informationen sind sprach-und Codepage-unabhängig. <br/>                                                                                                                   |
| [**VS \_ VERSIONINFO**](vs-versioninfo.md)     | Zeigt die Organisation der Daten in einer Datei Versions Ressource an. Dabei handelt es sich um die Stamm Struktur, die alle anderen Datei Versions Informationsstrukturen enthält.<br/>                                                                    |



 

 

 





