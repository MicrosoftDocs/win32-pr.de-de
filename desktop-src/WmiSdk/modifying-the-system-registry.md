---
description: Die Systemregistrierung enthält Konfigurationsdaten, die vom Betriebssystem, den Diensten und Anwendungen verwendet werden.
ms.assetid: e16a5d4c-46a0-4798-894d-0af4cfa18f22
ms.tgt_platform: multiple
title: Ändern der Systemregistrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33562e2747d63d8531ff2b23d07eadac33d830ef3ecf3b8613f22170c0b735ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992840"
---
# <a name="modifying-the-system-registry"></a>Ändern der Systemregistrierung

Die Systemregistrierung enthält Konfigurationsdaten, die vom Betriebssystem, den Diensten und Anwendungen verwendet werden. Windows Die Verwaltungsinstrumentation (Management Instrumentation, WMI) verfügt über einen [Systemregistrierungsanbieter](/previous-versions/windows/desktop/regprov/system-registry-provider) und die [**StdRegProv-Klasse**](/previous-versions/windows/desktop/regprov/stdregprov) mit Methoden, die zum Überwachen oder Ändern der Registrierung auf dem lokalen Computer oder remoten Computern verwenden. Der [Win32-Anbieter unterstützt](/windows/desktop/CIMWin32Prov/win32-provider) die [**Win32 \_ Registry-Klasse,**](/windows/desktop/CIMWin32Prov/win32-registry) die statische Daten zur Größe einer Registrierung enthält.

Der Systemregistrierungsanbieter ist eine Instanz, Eigenschaft und ein Ereignisanbieter, die mit der Systemregistrierung verbunden sind. Der Systemregistrierungsanbieter ist ein Standardanbieter mit der [**IWbemServices-Schnittstelle.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) Sie können den Systemregistrierungsanbieter verwenden, um auf Registrierungsschlüssel und Informationen auf lokalen und Remotesystemen zu zugreifen. Weitere Informationen finden Sie unter [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider).

WMI platziert [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) im \\ Standardnamespace des Stamms. Sie können die Datei Regevent.mof jedoch in andere Namespaces kompilieren, damit sie von anderen Anwendungen verwendet werden kann.

Die in der folgenden Tabelle genannten Themen können Ihnen zeigen, wie Sie die [**StdRegProv-Klasse**](/previous-versions/windows/desktop/regprov/stdregprov) und den Systemregistrierungsanbieter verwenden.



| Thema                                                                                              | BESCHREIBUNG                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Abrufen von Registrierungsdaten](obtaining-registry-data.md)                                             | Sie können Registrierungsdaten über Methoden der [**StdRegProv-Klasse**](/previous-versions/windows/desktop/regprov/stdregprov) abrufen oder ändern, wodurch Sie Registrierungsaktivitäten lokal oder remote automatisieren können.                    |
| [Ändern von Registrierungsdaten](changing-registry-data.md)                                               | Sie können Schlüssel hinzufügen oder löschen und Registrierungseintragswerte unter Schlüsseln hinzufügen oder ändern.                                                                                                                    |
| [Programmieren mit dem Systemregistrierungsanbieter](programming-with-the-system-registry-provider.md) | Sie können eigene Klassen definieren, die die Systemregistrierung mit Daten liefert.                                                                                                                       |
| [Registrieren für Systemregistrierungsereignisse](registering-for-system-registry-events.md)               | Der Systemregistrierungsanbieter kann Ereignisse an einen Consumer senden. Um Ereignisse zu empfangen, müssen Sie Ihren Consumer registrieren, eine Abfrage erstellen und dann sicherstellen, dass der Anbieter Ihnen Ereignisse sendet – richtig. |
| [Registrieren des Systemregistrierungsanbieters](registering-the-system-registry-provider.md)           | Der Systemregistrierungsanbieter wird im Rahmen des WMI-Installationsprozesses registriert.                                                                                                                |



 

 

 
