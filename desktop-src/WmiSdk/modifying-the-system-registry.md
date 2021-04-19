---
description: Die Systemregistrierung enthält Konfigurationsdaten, die vom Betriebssystem, den Diensten und den Anwendungen verwendet werden.
ms.assetid: e16a5d4c-46a0-4798-894d-0af4cfa18f22
ms.tgt_platform: multiple
title: Ändern der System Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb274163999996267b5f1df62fb9352831763d4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342804"
---
# <a name="modifying-the-system-registry"></a>Ändern der System Registrierung

Die Systemregistrierung enthält Konfigurationsdaten, die vom Betriebssystem, den Diensten und den Anwendungen verwendet werden. Windows-Verwaltungsinstrumentation (WMI) verfügt über einen [System Registrierungs Anbieter](/previous-versions/windows/desktop/regprov/system-registry-provider) und die [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) -Klasse mit Methoden, die zum Überwachen oder Ändern der Registrierung auf dem lokalen Computer oder auf Remote Computern verwenden. Der [Win32-Anbieter](/windows/desktop/CIMWin32Prov/win32-provider) unterstützt die [**Win32- \_ Registrierungs**](/windows/desktop/CIMWin32Prov/win32-registry) Klasse, die statische Daten über die Größe einer Registrierung enthält.

Der System Registrierungs Anbieter ist eine Instanz, eine Eigenschaft und ein Ereignis Anbieter, die mit der Systemregistrierung über eine Schnittstelle verfügt. Der System Registrierungs Anbieter ist ein Standardanbieter mit der [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle. Sie können den System Registrierungs Anbieter für den Zugriff auf Registrierungsschlüssel und-Informationen auf lokalen Systemen und Remote Systemen verwenden. Weitere Informationen finden Sie unter [System Registrierungs Anbieter](/previous-versions/windows/desktop/regprov/system-registry-provider).

WMI platziert [**StdRegProv im Stamm**](/previous-versions/windows/desktop/regprov/stdregprov) - \\ Standard Namespace. Allerdings können Sie die Datei regevent. MOF in andere Namespaces kompilieren, damit Sie von anderen Anwendungen verwendet werden können.

Die in der folgenden Tabelle aufgeführten Themen veranschaulichen, wie die [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) -Klasse und der System Registrierungs Anbieter verwendet werden.



| Thema                                                                                              | BESCHREIBUNG                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Abrufen von Registrierungsdaten](obtaining-registry-data.md)                                             | Sie können Registrierungsdaten über Methoden der [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) -Klasse abrufen oder ändern, sodass Sie Registrierungsaktivitäten lokal oder Remote automatisieren können.                    |
| [Ändern von Registrierungsdaten](changing-registry-data.md)                                               | Sie können Schlüssel hinzufügen oder löschen und Registrierungs Eintrags Werte Unterschlüssel hinzufügen oder ändern.                                                                                                                    |
| [Programmieren mit dem System Registrierungs Anbieter](programming-with-the-system-registry-provider.md) | Sie können eigene Klassen definieren, die die System Registrierung mit Daten bereitstellt.                                                                                                                       |
| [Registrierung für System Registrierungs Ereignisse](registering-for-system-registry-events.md)               | Der System Registrierungs Anbieter kann Ereignisse an einen Consumer senden. Um Ereignisse zu empfangen, müssen Sie den Consumer registrieren, eine Abfrage erstellen und dann sicherstellen, dass der Anbieter ihre Ereignisse sendet – ordnungsgemäß. |
| [Der System Registrierungs Anbieter wird registriert.](registering-the-system-registry-provider.md)           | Der System Registrierungs Anbieter wird als Teil des WMI-Installationsvorgangs registriert.                                                                                                                |



 

 

 
