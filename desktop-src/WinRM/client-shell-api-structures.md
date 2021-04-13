---
title: Client-Shell-API-Strukturen und-Definitionen
description: In der folgenden Tabelle finden Sie eine Übersicht über die Strukturen und andere Definitionen für die-Windows-Remoteverwaltung (WinRM)-ClientShell-API.
ms.assetid: b7a3c92e-6796-482f-9d70-18a48cce4ad8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c00a908856a6df8233e377d917ff28029dc8468e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390472"
---
# <a name="client-shell-api-structures-and-definitions"></a>Client-Shell-API-Strukturen und-Definitionen

In der folgenden Tabelle finden Sie eine Übersicht über die Strukturen und andere Definitionen für die-Windows-Remoteverwaltung (WinRM)-ClientShell-API.



| Funktion                                                                      | BESCHREIBUNG                                                                                  |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**Funktion zum Abschluss der WSMAN- \_ Shell \_ \_**](/windows/win32/api/wsman/nc-wsman-wsman_shell_completion_function) | Die Rückruffunktion, die für Shellvorgänge aufgerufen wird, was zu einer Remote Anforderung führt. |



 



| Struktur                                                                      | BESCHREIBUNG                                                                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Anmelde Informationen für WSMAN- \_ Authentifizierung \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_authentication_credentials) | Definiert die Authentifizierungsmethode und die Anmelde Informationen, die für die Server-oder Proxy Authentifizierung verwendet werden.                                              |
| [**WSMAN- \_ Daten**](/windows/desktop/api/Wsman/ns-wsman-wsman_data)                                              | Speichert eingehende und ausgehende Daten, die in der WinRM-API verwendet werden.                                                                                     |
| [**WSMAN- \_ Daten \_ Binärdatei**](/windows/desktop/api/Wsman/ns-wsman-wsman_data_binary)                               | Speichert Binärdaten für die Verwendung mit verschiedenen WinRM-API-Funktionen.                                                                                |
| [**WSMAN \_ - \_ Datentext**](/windows/desktop/api/Wsman/ns-wsman-wsman_data_text)                                   | Speichert textbasierte Daten für die Verwendung mit verschiedenen WinRM-API-Funktionen.                                                                            |
| [**WSMAN- \_ Umgebungs \_ Variable**](/windows/desktop/api/Wsman/ns-wsman-wsman_environment_variable)             | Definiert eine einzelne Umgebungsvariable mithilfe eines Name-Wert-Paars.                                                                  |
| [**WSMAN- \_ Umgebungs \_ Variable \_ festgelegt**](/windows/desktop/api/Wsman/ns-wsman-wsman_environment_variable_set)    | Definiert ein Array von Umgebungsvariablen.                                                                                                  |
| [**WSMAN- \_ Fehler**](/windows/desktop/api/Wsman/ns-wsman-wsman_error)                                     | Enthält Fehlerinformationen.                                                                                                                 |
| [**WSMAN- \_ Schlüssel**](/windows/desktop/api/Wsman/ns-wsman-wsman_key)                                                | Stellt ein Schlüssel-Wert-Paar innerhalb eines Selektor Satzes dar und wird zum Identifizieren einer bestimmten Ressource verwendet.                                       |
| [**WSMAN- \_ Option**](/windows/desktop/api/Wsman/ns-wsman-wsman_option)                                          | Stellt einen bestimmten Options Name und ein Wert-Paar dar.                                                                                           |
| [**WSMAN- \_ options \_ Satz**](/windows/desktop/api/Wsman/ns-wsman-wsman_option_set)                                 | Stellt einen Satz von Optionen dar.                                                                                                                |
| [**WSMAN- \_ Proxy \_ Informationen**](/windows/desktop/api/Wsman/ns-wsman-wsman_proxy_info)                                 | Legt die Proxy Informationen für jede Sitzung fest.                                                                                                |
| [**Ergebnis der WSMAN- \_ Empfangs \_ Daten \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_receive_data_result)              | Stellt die Ausgabedaten dar, die von der [**wsmanreceiveshelloutput**](/windows/desktop/api/Wsman/nf-wsman-wsmanreceiveshelloutput) -API empfangen werden.                                |
| [**WSMAN- \_ Antwort \_ Daten**](/windows/desktop/api/Wsman/ns-wsman-wsman_response_data)                           | Stellt die Ausgabedaten dar, die von einem [**WSMAN**](wsman.md) -Vorgang empfangen wurden.                                                                |
| [**WSMAN- \_ Auswahl \_ Satz**](/windows/desktop/api/Wsman/ns-wsman-wsman_selector_set)                             | Definiert einen Satz von Schlüsseln, die die Identität einer Ressource darstellen.                                                                            |
| [**WSMAN- \_ Shell \_ Async**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_async)                               | Definiert eine asynchrone-Struktur, die an alle Shellvorgänge übermittelt wird.                                                                   |
| [**WSMAN- \_ shelltrennungs \_ \_ Informationen**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_disconnect_info)          | TBD                                                                                                                                         |
| [**WSMAN \_ - \_ \_ shellstartinformationen**](/windows/desktop/api/Wsman/ns-wsman-wsman_shell_startup_info_v10)                | Speichert alle shellspezifischen Daten, die zum Erstellen einer Shell mithilfe des [**wsmankreateshell**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell) -Plug-in-Aufrufes benötigt werden. |
| [**WSMAN- \_ Stream- \_ ID- \_ Satz**](/windows/desktop/api/Wsman/ns-wsman-wsman_stream_id_set)                          | Listet alle Streams auf, die für die Eingabe oder Ausgabe für die Shell und Befehle verwendet werden.                                                  |
| [**Benutzername des WSMAN- \_ Benutzernamens \_ Kennwort \_**](/windows/desktop/api/Wsman/ns-wsman-wsman_username_password_creds)      | Definiert die Anmelde Informationen, die für die Authentifizierung verwendet werden.                                                                                            |



 

 

 