---
description: Der \_ \_ HKCR-Schlüssel (HKEY Classes root) enthält Dateinamen Erweiterungs Zuordnungen und com-Klassen Registrierungsinformationen wie z. b. ProgIDs, CLSIDs und IIDs. Sie ist in erster Linie für die Kompatibilität mit der Registrierung in 16-Bit-Windows vorgesehen.
ms.assetid: b404875f-11e1-48f2-98d2-0378a0646ed3
title: HKEY_CLASSES_ROOT-Taste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e7aebe0e59424eb5ff7584fe61c2c5089eb887b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868164"
---
# <a name="hkey_classes_root-key"></a>Stamm Schlüssel der HKEY- \_ Klassen \_

Der **HKCR**-Schlüssel ( **HKEY \_ Classes \_ root** ) enthält Dateinamen Erweiterungs Zuordnungen und com-Klassen Registrierungsinformationen wie z. b. [ProgIDs](../com/-progid--key.md), [CLSIDs](../com/clsid-key-hklm.md)und [IIDs](../com/interface-key.md). Sie ist in erster Linie für die Kompatibilität mit der Registrierung in 16-Bit-Windows vorgesehen.

Die Informationen zur Klassen Registrierung und zur Dateinamenerweiterung werden unter den aktuellen **HKEY \_ \_** -Computern und **aktuellen HKEY- \_ \_ Benutzer** Schlüsseln gespeichert. Der Schlüssel für die **\_ \_ \\ Software \\ Klassen des lokalen HKEY** -Computers enthält Standardeinstellungen, die für alle Benutzer auf dem lokalen Computer gelten können. Der Schlüssel **HKEY \_ Current \_ User- \\ Software \\ Klassen** enthält Einstellungen, die nur für den interaktiven Benutzer gelten. Der Stamm Schlüssel der **HKEY- \_ Klassen \_** bietet eine Ansicht der Registrierung, mit der die Informationen aus diesen beiden Quellen zusammengeführt werden. **HKEY \_ Klassen \_** Stamm stellt außerdem diese zusammengeführte Ansicht für Anwendungen bereit, die für frühere Versionen von Windows entwickelt wurden.

Die benutzerspezifischen Einstellungen haben Vorrang vor den Standardeinstellungen. Beispielsweise kann mit der Standardeinstellung eine bestimmte Anwendung für die Verarbeitung von doc-Dateien angegeben werden. Benutzer können diese Einstellung jedoch außer Kraft setzen, indem Sie in der Registrierung eine andere Anwendung angeben.

Mit Registrierungsfunktionen wie [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) oder [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) können Sie den Stamm Schlüssel der **HKEY- \_ Klassen \_** angeben. Wenn Sie diese Funktionen von einem Prozess aus abrufen, der im interaktiven Benutzerkonto ausgeführt wird, führt das System die Standardeinstellungen in den **HKEY- \_ \_ \\ Software \\ Klassen für lokale Computer** mit den interaktiven Benutzereinstellungen unter **HKEY \_ Current \_ User \\ Software \\ Classes** zusammen. Weitere Informationen dazu, wie diese Einstellungen zusammengeführt werden, finden Sie unter [zusammengeführte Ansicht von HKEY \_ Classes \_ root](merged-view-of-hkey-classes-root.md).

Um die Einstellungen für den interaktiven Benutzer zu ändern, speichern Sie die Änderungen unter **HKEY \_ Current \_ User \\ Software \\ Classes** anstelle von **HKEY \_ Classes \_ root**.

Um die Standardeinstellungen zu ändern, speichern Sie die Änderungen unter **HKEY- \_ \_ \\ Software \\ Klassen für lokale Computer**. Wenn Sie Schlüssel in einen Schlüssel unter **HKEY- \_ Klassen \_** Stamm schreiben, speichert das System die Informationen unter **HKEY- \_ \_ \\ Software \\ Klassen für lokale Computer**. Wenn Sie Werte in einen Schlüssel unter **HKEY \_ Classes \_ root** schreiben und der Schlüssel bereits unter **HKEY \_ Current \_ User \\ Software \\ Classes** vorhanden ist, speichert das System die Informationen dort anstelle von **HKEY- \_ \_ \\ Software \\ Klassen für lokale Computer**.

Prozesse, die in einem anderen Sicherheitskontext als dem des interaktiven Benutzers ausgeführt werden, sollten den **HKEY- \_ Klassen \_** Stamm Schlüssel nicht mit den Registrierungsfunktionen verwenden. Stattdessen können solche Prozesse explizit den HKEY-Schlüssel für die **\_ \_ \\ Software \\ Klassen der lokalen Computer** öffnen, um auf die Standardeinstellungen zuzugreifen. Um einen Registrierungsschlüssel zu öffnen, der den Inhalt von **HKEY- \_ \_ \\ Software \\ Klassen für lokale Computer** mit den Einstellungen für einen angegebenen Benutzer zusammenfasst, können diese Prozesse die [**regopenuserclassesroot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot) -Funktion aufzurufen. Beispielsweise kann ein Thread, der die Identität eines Clients annimmt, **regopenuserclassesroot** aufrufen, wenn er eine zusammengeführte Ansicht für den Client abrufen muss, für [den ein Identitäts](/windows/desktop/SecAuthZ/client-impersonation) Wechsel durchgeführt wird. Beachten Sie, dass **regopenuserclassesroot** fehlschlägt, wenn das Benutzerprofil für den angegebenen Benutzer nicht geladen wurde. Das System lädt das Profil für den interaktiven Benutzer automatisch, wenn sich die Anmeldung anmeldet. Für andere Benutzer müssen Sie die Funktion [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) anrufen, um das Profil des Benutzers explizit zu laden.

Wenn eine Anwendung mit Administratorrechten ausgeführt wird und die Benutzerkontensteuerung deaktiviert ist, ignoriert die com-Laufzeit die com-Konfiguration pro Benutzer und greift nur auf die com-Konfiguration pro Computer zu. Anwendungen, für die Administratorrechte erforderlich sind, sollten abhängige com-Objekte während der Installation im com-Konfigurations Speicher pro Computer (**HKEY \_ local \_ Machine \\ Software \\ Classes**) registrieren. Weitere Informationen finden Sie unter [AC: UAC: com-Per-User Konfiguration](/previous-versions/bb756926(v=msdn.10)).

**Windows Server 2003 und Windows XP/2000:** Anwendungen können abhängige com-Objekte entweder für den pro-Computer-oder benutzerspezifischen com-Konfigurations Speicher (**HKEY \_ local \_ Machine \\ Software \\ Classes** oder **HKEY \_ Current \_ User \\ Software \\ Classes**) registrieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[HKEY- \_ Klassen Stamm \_ (Ressourcenkit-Registrierungs Verweis)](/previous-versions/windows/it-pro/windows-server-2003/cc739822(v=ws.10))
</dt> </dl>

 

 
