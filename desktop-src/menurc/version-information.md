---
title: Versionsinformationen
description: In diesem Abschnitt wird die Versionsinformationsressource erläutert.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\versioninformation.htm
keywords:
- Ressourcen,Versionsinformationen
- Versionsinformationen
- Versionsnummern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac69601c593c51a5a15a0af0706a019f135d855875f6e1ecabdb414a8a100045
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733095"
---
# <a name="version-information"></a>Versionsinformationen

Versionsinformationen erleichtern Es Anwendungen, Dateien ordnungsgemäß zu installieren, und ermöglichen Setupprogrammen die Analyse aktuell installierter Dateien. Die Versionsinformationsressource enthält die Versionsnummer der Datei, das vorgesehene Betriebssystem und den ursprünglichen Dateinamen.

### <a name="in-this-section"></a>In diesem Abschnitt



| Name                                                               | Beschreibung                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------|
| [Informationen zu Versionsinformationen](about-version-information.md)         | Erläutert die Versionsinformationsfunktionen.<br/>            |
| [Verwenden von Versionsinformationen](using-version-information.md)         | Erläutert die Verwendung der Versionsinformationsfunktionen.<br/> |
| [Versionsinformationsreferenz](version-information-reference.md) | Enthält die API-Referenz.<br/>                             |



 

### <a name="version-information-functions"></a>Versionsinformationsfunktionen



| Name                                                         | Beschreibung                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)             | Ruft Versionsinformationen für die angegebene Datei ab. <br/>                                                                                                                                                                                                                                                                                                     |
| [**GetFileVersionInfoEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoexa)         | Ruft Versionsinformationen für die angegebene Datei ab.<br/>                                                                                                                                                                                                                                                                                                      |
| [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea)     | Bestimmt, ob das Betriebssystem Versionsinformationen für eine angegebene Datei abrufen kann. Wenn Versionsinformationen verfügbar sind, [**gibt GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) die Größe dieser Informationen in Bytes zurück. <br/>                                                                                                             |
| [**GetFileVersionInfoSizeEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizeexa) | Bestimmt, ob das Betriebssystem Versionsinformationen für eine angegebene Datei abrufen kann. Wenn Versionsinformationen verfügbar sind, [**gibt GetFileVersionInfoSizeEx**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizeexa) die Größe dieser Informationen in Bytes zurück.<br/>                                                                                                          |
| [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea)                           | Bestimmt, wo eine Datei installiert werden soll, basierend darauf, ob eine andere Version der Datei im System gefunden wird. Die [**Werte, die VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea) in den angegebenen Puffern zurückgibt, werden in einem nachfolgenden Aufruf der [**VerInstallFile-Funktion**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) verwendet. <br/>                                                                          |
| [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea)                     | Installiert die angegebene Datei basierend auf Informationen, die von der [**VerFindFile-Funktion zurückgegeben**](/windows/desktop/api/Winver/nf-winver-verfindfilea) werden. [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) dekomprimiert die Datei bei Bedarf, weist einen eindeutigen Dateinamen zu und überprüft auf Fehler, z. B. veraltete Dateien. <br/>                                                                                   |
| [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea)                   | Ruft eine Beschreibungszeichenfolge für die Sprache ab, die einem angegebenen binären Microsoft-Sprachbezeichner zugeordnet ist.<br/>                                                                                                                                                                                                                                          |
| [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)                       | Ruft die angegebenen Versionsinformationen aus der angegebenen Versionsinformationsressource ab. Um die entsprechende Ressource abzurufen, müssen Sie vor dem Aufrufen von [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)zuerst die [**GetFileVersionInfoSize-Funktion**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) und dann die [**GetFileVersionInfo-Funktion**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa) aufrufen. <br/> |



 

### <a name="version-information-structures"></a>Versionsinformationsstrukturen



| Name                                          | Beschreibung                                                                                                                                                                                                                      |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Schnur**](string-str.md)                  | Zeigt die Organisation der Daten in einer Dateiversionsressource. Sie enthält eine Zeichenfolge, die einen bestimmten Aspekt einer Datei beschreibt, z. B. die Version einer Datei, ihre Urheberrechtshinweise oder ihre Marken.<br/>                |
| [**StringFileInfo**](stringfileinfo.md)      | Zeigt die Organisation der Daten in einer Dateiversionsressource. Sie enthält Versionsinformationen, die für eine bestimmte Sprache und Codepage angezeigt werden können.<br/>                                                           |
| [**Stringtable**](stringtable.md)            | Zeigt die Organisation der Daten in einer Dateiversionsressource. Sie enthält Informationen zur Sprach- und Codepageformatierung für die vom **Children-Member angegebenen** Zeichenfolgen. Eine Codepage ist ein geordneter Zeichensatz.<br/> |
| [**Var**](var-str.md)                        | Zeigt die Organisation der Daten in einer Dateiversionsressource. Sie enthält in der Regel eine Liste von Sprachen- und Codepage-Bezeichnerpaaren, die von der Version der Anwendung oder DLL unterstützt werden.<br/>                             |
| [**VarFileInfo**](varfileinfo.md)            | Zeigt die Organisation der Daten in einer Dateiversionsressource. Sie enthält Versionsinformationen, die nicht von einer bestimmten Kombination aus Sprache und Codepage abhängen.<br/>                                                        |
| [**VS \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) | Enthält Versionsinformationen zu einer Datei. Diese Informationen sind sprach- und codepageunabhängig. <br/>                                                                                                                   |
| [**VS \_ VERSIONINFO**](vs-versioninfo.md)     | Zeigt die Organisation der Daten in einer Dateiversionsressource. Es ist die Stammstruktur, die alle anderen Dateiversionsinformationsstrukturen enthält.<br/>                                                                    |



 

 

 





