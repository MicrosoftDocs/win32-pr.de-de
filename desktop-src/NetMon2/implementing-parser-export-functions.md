---
description: Die parserexportfunktionen stellen die gesamte Funktionalität der Parser in der Parser-dll bereit. Jede Parser-DLL muss parserautoinstallinfo und DllMain implementieren. Die verbleibenden Exportfunktionen müssen für jeden Parser implementiert werden, der in der Parser-DLL enthalten ist.
ms.assetid: be73623c-7ae7-4ca9-be6c-52f513cd38a4
title: Implementieren von parserexportfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b8eafb7e12c36a9413a320652e3d372ffbf51e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525109"
---
# <a name="implementing-parser-export-functions"></a>Implementieren von parserexportfunktionen

Die parserexportfunktionen stellen die gesamte Funktionalität der Parser in der Parser-dll bereit. Jede Parser-DLL muss [**parserautoinstallinfo**](parserautoinstallinfo.md) und [**DllMain**](dllmain-parser.md)implementieren. Die verbleibenden Exportfunktionen müssen für jeden Parser implementiert werden, der in der Parser-DLL enthalten ist.

In den folgenden Themen wird gezeigt, wie die Exportfunktionen implementiert werden.



| Begriff                                                                                                                                                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Implementing_ParserAutoInstallInfo"></span><span id="implementing_parserautoinstallinfo"></span><span id="IMPLEMENTING_PARSERAUTOINSTALLINFO"></span>[Implementieren von "parameserautoinstallinfo"](implementing-parserautoinstallinfo.md)<br/> | Enthält eine Beschreibung und ein Codebeispiel für die Implementierung der [**parserautoinstallinfo**](parserautoinstallinfo.md) -Funktion, die die Parser identifiziert, die sich in einer Parser-DLL befinden.<br/>                                                                                            |
| <span id="Implementing_DllMain_Parser"></span><span id="implementing_dllmain_parser"></span><span id="IMPLEMENTING_DLLMAIN_PARSER"></span>[Implementieren von DllMain-Parser](implementing-dllmain-parser.md)<br/>                                    | Enthält eine Beschreibung und ein Codebeispiel für die Implementierung der [**DllMain-Parser**](dllmain-parser.md) -Funktion, die das vorhanden sein eines Parsers identifiziert und dann Ressourcen freigibt, die von Netzwerkmonitor für den Parser verwendet werden.<br/>                                              |
| <span id="Implementing_Register"></span><span id="implementing_register"></span><span id="IMPLEMENTING_REGISTER"></span>[Implementieren von Register](implementing-register.md)<br/>                                                                  | Enthält eine Beschreibung und ein Codebeispiel für die Implementierung der [**Register**](register-parser.md) -Funktion, die alle Eigenschaften eines Protokolls aufzeichnet.<br/>                                                                                                                     |
| <span id="Implementing_RecognizeFrame"></span><span id="implementing_recognizeframe"></span><span id="IMPLEMENTING_RECOGNIZEFRAME"></span>[Implementieren von "erkenzeframe"](implementing-recognizeframe.md)<br/>                                    | Enthält eine Beschreibung und ein Codebeispiel für die Implementierung der Funktion " [**erkenzeframe**](recognizeframe.md) ", die eine Instanz eines Protokolls in einem Frame identifiziert.<br/>                                                                                                         |
| <span id="Implementing_AttachProperties"></span><span id="implementing_attachproperties"></span><span id="IMPLEMENTING_ATTACHPROPERTIES"></span>[Implementieren von attachproperties](implementing-attachproperties.md)<br/>                          | Enthält eine Beschreibung und ein Codebeispiel für die Implementierung der [**attachproperties**](attachproperties.md) -Funktion, die die vom Parser erkannten Daten trennt und dann Eigenschafts Beschreibungen an jede Protokoll Eigenschaft anfügt, die in den erkannten Daten vorhanden ist.<br/> |
| <span id="Implementing_FormatProperties"></span><span id="implementing_formatproperties"></span><span id="IMPLEMENTING_FORMATPROPERTIES"></span>[Implementieren von formatproperties](implementing-formatproperties.md)<br/>                          | Enthält eine Beschreibung und ein Codebeispiel für die Implementierung der [**formatproperties**](formatproperties.md) -Funktion, mit der die Daten formatiert werden, die im Detailbereich der Netzwerkmonitor-Benutzeroberfläche angezeigt werden.<br/>                                                                    |
| <span id="Implementing_Deregister"></span><span id="implementing_deregister"></span><span id="IMPLEMENTING_DEREGISTER"></span>[Implementieren von deregistern](implementing-deregister.md)<br/>                                                        | Enthält eine Beschreibung und ein Codebeispiel für die Implementierung der [**deregister**](deregister.md) -Funktion, die die zum Registrieren von Protokoll Eigenschaften verwendeten Ressourcen freigibt.<br/>                                                                                                     |



 

 

 




