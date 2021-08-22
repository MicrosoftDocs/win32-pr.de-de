---
title: Client Shell-API-Strukturen und -Definitionen
description: Die folgende Tabelle enthält eine Übersicht über die Strukturen und anderen Definitionen für die Clientshell-API Windows Remoteverwaltung (WinRM).
ms.assetid: b7a3c92e-6796-482f-9d70-18a48cce4ad8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c9c3d1f6f9f9d476e9b49ef309e5236e4421e0b5afa77fa1072b92f2060cfcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643260"
---
# <a name="client-shell-api-structures-and-definitions"></a>Client Shell-API-Strukturen und -Definitionen

Die folgende Tabelle enthält eine Übersicht über die Strukturen und anderen Definitionen für die Clientshell-API Windows Remoteverwaltung (WinRM).



| Funktion                                                                      | Beschreibung                                                                                  |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_VERVOLLSTÄNDIGUNGSFUNKTION DER WSMAN-SHELL \_ \_**](/windows/win32/api/wsman/nc-wsman-wsman_shell_completion_function) | Die Rückruffunktion, die für Shellvorgänge aufgerufen wird, die zu einer Remoteanforderung führen. |



 



| Struktur                                                                      | Beschreibung                                                                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ANMELDEINFORMATIONEN FÜR DIE \_ WSMAN-AUTHENTIFIZIERUNG \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_authentication_credentials) | Definiert die Authentifizierungsmethode und die Anmeldeinformationen, die für die Server- oder Proxyauthentifizierung verwendet werden.                                              |
| [**WSMAN \_ DATA**](/windows/desktop/api/Wsman/ns-wsman-wsman_data)                                              | Speichert eingehende und ausgehende Daten, die in der WinRM-API verwendet werden.                                                                                     |
| [**WSMAN \_ DATA \_ BINARY**](/windows/desktop/api/Wsman/ns-wsman-wsman_data_binary)                               | Speichert Binärdaten für die Verwendung mit verschiedenen WinRM-API-Funktionen.                                                                                |
| [**\_WSMAN-DATENTEXT \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_data_text)                                   | Speichert textbasierte Daten für die Verwendung mit verschiedenen WinRM-API-Funktionen.                                                                            |
| [**\_WSMAN-UMGEBUNGSVARIABLE \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_environment_variable)             | Definiert eine einzelne Umgebungsvariable mithilfe eines Name-Wert-Paars.                                                                  |
| [**WSMAN \_ ENVIRONMENT \_ VARIABLE \_ SET**](/windows/desktop/api/Wsman/ns-wsman-wsman_environment_variable_set)    | Definiert ein Array von Umgebungsvariablen.                                                                                                  |
| [**\_WSMAN-FEHLER**](/windows/desktop/api/Wsman/ns-wsman-wsman_error)                                     | Enthält Fehlerinformationen.                                                                                                                 |
| [**\_WSMAN-SCHLÜSSEL**](/windows/desktop/api/Wsman/ns-wsman-wsman_key)                                                | Stellt ein Schlüssel-Wert-Paar innerhalb eines Selektorsatzes dar und wird verwendet, um eine bestimmte Ressource zu identifizieren.                                       |
| [**\_WSMAN-OPTION**](/windows/desktop/api/Wsman/ns-wsman-wsman_option)                                          | Stellt ein bestimmtes Optionsnamen- und Wertpaar dar.                                                                                           |
| [**\_WSMAN-OPTIONSSATZ \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_option_set)                                 | Stellt einen Satz von Optionen dar.                                                                                                                |
| [**\_WSMAN-PROXYINFORMATIONEN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_proxy_info)                                 | Legt die Proxyinformationen für jede Sitzung fest.                                                                                                |
| [**WSMAN \_ RECEIVE \_ DATA \_ RESULT**](/windows/desktop/api/Wsman/ns-wsman-wsman_receive_data_result)              | Stellt die von der [**WSManReceiveShellOutput-API empfangenen**](/windows/desktop/api/Wsman/nf-wsman-wsmanreceiveshelloutput) Ausgabedaten dar.                                |
| [**\_WSMAN-ANTWORTDATEN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_response_data)                           | Stellt die Ausgabedaten dar, die von einem [**WSMan-Vorgang**](wsman.md) empfangen werden.                                                                |
| [**WSMAN \_ SELECTOR \_ SET**](/windows/desktop/api/Wsman/ns-wsman-wsman_selector_set)                             | Definiert einen Satz von Schlüsseln, die die Identität einer Ressource darstellen.                                                                            |
| [**WSMAN \_ SHELL \_ ASYNC**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_async)                               | Definiert eine asynchrone Struktur, die an alle Shellvorgänge übergeben wird.                                                                   |
| [**WSMAN \_ SHELL \_ DISCONNECT \_ INFO**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_disconnect_info)          | TBD                                                                                                                                         |
| [**\_WSMAN \_ SHELL-STARTINFORMATIONEN \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_startup_info_v10)                | Speichert alle shellspezifischen Daten, die zum Erstellen einer Shell mithilfe des [**WSManCreateShell-Plug-In-Aufrufs**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell) erforderlich sind. |
| [**WSMAN \_ STREAM \_ ID \_ SET**](/windows/desktop/api/Wsman/ns-wsman-wsman_stream_id_set)                          | Listet alle Streams auf, die entweder für die Eingabe oder Ausgabe für die Shell und befehle verwendet werden.                                                  |
| [**WSMAN \_ USERNAME \_ PASSWORD \_ CREDS**](/windows/desktop/api/Wsman/ns-wsman-wsman_username_password_creds)      | Definiert die anmeldeinformationen, die für die Authentifizierung verwendet werden.                                                                                            |



 

 

 