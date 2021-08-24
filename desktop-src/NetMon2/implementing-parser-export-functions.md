---
description: Die Parser-Exportfunktionen stellen alle Funktionen der Parser in der Parser-DLL bereit. Jede Parser-DLL muss ParserAutoInstallInfo und DllMain implementieren. Die verbleibenden Exportfunktionen müssen für jeden Parser implementiert werden, der in der Parser-DLL enthalten ist.
ms.assetid: be73623c-7ae7-4ca9-be6c-52f513cd38a4
title: Implementieren von Parser-Exportfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e32b3b1aa807a604f058ed8965ef11728f6c12fecb34e27a337682361f8dd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778840"
---
# <a name="implementing-parser-export-functions"></a>Implementieren von Parser-Exportfunktionen

Die Parser-Exportfunktionen stellen alle Funktionen der Parser in der Parser-DLL bereit. Jede Parser-DLL muss [**ParserAutoInstallInfo**](parserautoinstallinfo.md) und [**DllMain**](dllmain-parser.md)implementieren. Die verbleibenden Exportfunktionen müssen für jeden Parser implementiert werden, der in der Parser-DLL enthalten ist.

In den folgenden Themen erfahren Sie, wie Sie die Exportfunktionen implementieren.



| Begriff                                                                                                                                                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Implementing_ParserAutoInstallInfo"></span><span id="implementing_parserautoinstallinfo"></span><span id="IMPLEMENTING_PARSERAUTOINSTALLINFO"></span>[Implementieren von ParserAutoInstallInfo](implementing-parserautoinstallinfo.md)<br/> | Enthält eine Beschreibung und ein Codebeispiel für die Implementierung der [**ParserAutoInstallInfo-Funktion,**](parserautoinstallinfo.md) die die Parser identifiziert, die sich in einer Parser-DLL befinden.<br/>                                                                                            |
| <span id="Implementing_DllMain_Parser"></span><span id="implementing_dllmain_parser"></span><span id="IMPLEMENTING_DLLMAIN_PARSER"></span>[Implementieren des DllMain-Parsers](implementing-dllmain-parser.md)<br/>                                    | Enthält eine Beschreibung und ein Codebeispiel für die Implementierung der [**DllMain Parser-Funktion,**](dllmain-parser.md) die das Vorhandensein eines Parsers identifiziert und dann Ressourcen freigibt, die Netzwerkmonitor für den Parser verwendet.<br/>                                              |
| <span id="Implementing_Register"></span><span id="implementing_register"></span><span id="IMPLEMENTING_REGISTER"></span>[Implementieren von Registern](implementing-register.md)<br/>                                                                  | Enthält eine Beschreibung und ein [](register-parser.md) Codebeispiel für die Implementierung der Register-Funktion, die alle Eigenschaften eines Protokolls aufzeichnet.<br/>                                                                                                                     |
| <span id="Implementing_RecognizeFrame"></span><span id="implementing_recognizeframe"></span><span id="IMPLEMENTING_RECOGNIZEFRAME"></span>[Implementieren von RecognizeFrame](implementing-recognizeframe.md)<br/>                                    | Enthält eine Beschreibung und ein Codebeispiel für die Implementierung der [**RecognizeFrame-Funktion,**](recognizeframe.md) die eine Instanz eines Protokolls in einem Frame identifiziert.<br/>                                                                                                         |
| <span id="Implementing_AttachProperties"></span><span id="implementing_attachproperties"></span><span id="IMPLEMENTING_ATTACHPROPERTIES"></span>[Implementieren von AttachProperties](implementing-attachproperties.md)<br/>                          | Enthält eine Beschreibung und ein Codebeispiel für die Implementierung der [**AttachProperties-Funktion,**](attachproperties.md) die die vom Parser erkannten Daten trennt und dann Eigenschaftenbeschreibungen an jede Protokolleigenschaft anfügt, die in den erkannten Daten vorhanden ist.<br/> |
| <span id="Implementing_FormatProperties"></span><span id="implementing_formatproperties"></span><span id="IMPLEMENTING_FORMATPROPERTIES"></span>[Implementieren von FormatProperties](implementing-formatproperties.md)<br/>                          | Enthält eine Beschreibung und ein Codebeispiel für die Implementierung der [**FormatProperties-Funktion,**](formatproperties.md) die die Daten formatiert, die im Detailbereich der Netzwerkmonitor Ui angezeigt werden.<br/>                                                                    |
| <span id="Implementing_Deregister"></span><span id="implementing_deregister"></span><span id="IMPLEMENTING_DEREGISTER"></span>[Implementieren der Registrierung](implementing-deregister.md)<br/>                                                        | Enthält eine Beschreibung und ein Codebeispiel für die Implementierung der [**Deregister-Funktion,**](deregister.md) die die Ressourcen freigibt, die zum Registrieren von Protokolleigenschaften verwendet werden.<br/>                                                                                                     |



 

 

 




