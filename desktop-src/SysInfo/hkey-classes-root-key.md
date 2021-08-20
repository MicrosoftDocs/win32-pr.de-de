---
description: Der SCHLÜSSEL HKEY CLASSES ROOT (HKCR) enthält Dateinamenerweiterungszuordnungen und COM-Klassenregistrierungsinformationen wie \_ \_ ProgIDs, CLSIDs und IIDs. Sie ist hauptsächlich für die Kompatibilität mit der Registrierung in 16-Bit-Windows.
ms.assetid: b404875f-11e1-48f2-98d2-0378a0646ed3
title: HKEY_CLASSES_ROOT-Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca75fc0b736c156e2e0dbe8ad07ff84cbbaa0a9ee1484de74e4f670703b2d875
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885682"
---
# <a name="hkey_classes_root-key"></a>HKEY \_ CLASSES \_ ROOT Key

Der **Schlüssel HKEY \_ CLASSES \_ ROOT** (**HKCR**) enthält Dateinamenerweiterungszuordnungen und COM-Klassenregistrierungsinformationen wie [ProgIDs,](../com/-progid--key.md) [CLSIDs](../com/clsid-key-hklm.md)und [IIDs.](../com/interface-key.md) Sie ist hauptsächlich für die Kompatibilität mit der Registrierung in 16-Bit-Windows.

Klassenregistrierungs- und Dateierweiterungsinformationen werden sowohl unter den **Schlüsseln HKEY \_ LOCAL \_ MACHINE** als auch **HKEY \_ CURRENT \_ USER** gespeichert. Der **Schlüssel HKEY \_ LOCAL MACHINE Software Classes \_ \\ \\ enthält** Standardeinstellungen, die für alle Benutzer auf dem lokalen Computer gelten können. Der **Schlüssel HKEY \_ CURRENT USER Software Classes \_ \\ \\ enthält** Einstellungen, die nur für den interaktiven Benutzer gelten. Der **HKEY \_ CLASSES \_ ROOT-Schlüssel** bietet eine Ansicht der Registrierung, in der die Informationen aus diesen beiden Quellen zusammengeführt werden. **HKEY \_ CLASSES \_ ROOT** stellt diese zusammengeführte Ansicht auch für Anwendungen zur Verfügung, die für frühere Versionen von Windows.

Die benutzerspezifischen Einstellungen haben Vorrang vor den Standardeinstellungen. Die Standardeinstellung kann z. B. eine bestimmte Anwendung für die .doc angeben. Benutzer können diese Einstellung jedoch überschreiben, indem sie eine andere Anwendung in der Registrierung angeben.

Mit Registrierungsfunktionen wie [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) oder [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) können Sie den **HKEY \_ CLASSES \_ ROOT-Schlüssel** angeben. Wenn Sie diese Funktionen von einem Prozess aufrufen, der im interaktiven Benutzerkonto ausgeführt wird, führt das System die Standardeinstellungen in **HKEY \_ LOCAL MACHINE \_ Software \\ \\ Classes** mit den Einstellungen des interaktiven Benutzers unter **HKEY CURRENT USER Software \_ \_ Classes \\ \\ zusammen.** Weitere Informationen dazu, wie diese Einstellungen zusammengeführt werden, finden Sie unter [Merged View of HKEY CLASSES \_ \_ ROOT](merged-view-of-hkey-classes-root.md).

Um die Einstellungen für den interaktiven Benutzer zu ändern, speichern Sie die Änderungen unter **HKEY \_ CURRENT USER Software \_ \\ \\ Classes** statt **HKEY CLASSES \_ \_ ROOT**.

Um die Standardeinstellungen zu ändern, speichern Sie die Änderungen unter **HKEY \_ LOCAL MACHINE Software \_ \\ \\ Classes**. Wenn Sie Schlüssel in einen Schlüssel unter **HKEY \_ CLASSES \_ ROOT** schreiben, speichert das System die Informationen unter **HKEY \_ LOCAL MACHINE \_ \\ Software \\ Classes**. Wenn Sie Werte in einen Schlüssel unter **HKEY \_ CLASSES \_ ROOT** schreiben und der Schlüssel bereits unter **HKEY CURRENT USER Software Classes (HKEY \_ CURRENT \_ \\ \\ USER-Softwareklassen)** vorhanden ist, werden die Informationen vom System dort statt unter **HKEY LOCAL MACHINE Software Classes (HKEY LOCAL \_ \_ \\ MACHINE-Softwareklassen) \\ gespeichert.**

Prozesse, die in einem anderen Sicherheitskontext als dem des interaktiven Benutzers ausgeführt werden, sollten den **HKEY \_ CLASSES \_ ROOT-Schlüssel** nicht mit den Registrierungsfunktionen verwenden. Stattdessen können solche Prozesse explizit den **Schlüssel HKEY \_ LOCAL MACHINE \_ Software \\ \\ Classes** öffnen, um auf die Standardeinstellungen zu zugreifen. Um einen Registrierungsschlüssel zu öffnen, der den Inhalt der **HKEY \_ LOCAL \_ \\ \\ MACHINE-Softwareklassen** mit den Einstellungen für einen angegebenen Benutzer zusammenführung, können diese Prozesse die [**RegOpenUserClassesRoot-Funktion**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot) aufrufen. Beispielsweise kann ein Thread, der die Identität eines Clients anpersoniert, **RegOpenUserClassesRoot** aufrufen, wenn er eine zusammengeführte Sicht für den Client abrufen muss, für den die Identität angenommen wird. [](/windows/desktop/SecAuthZ/client-impersonation) Beachten **Sie, dass RegOpenUserClassesRoot fehlschlägt,** wenn das Benutzerprofil für den angegebenen Benutzer nicht geladen wurde. Das System lädt bei der Anmeldung automatisch das Profil für den interaktiven Benutzer. Für andere Benutzer müssen Sie die [**LoadUserProfile-Funktion**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) aufrufen, um das Profil des Benutzers explizit zu laden.

Wenn eine Anwendung mit Administratorrechten ausgeführt wird und die Benutzerkontensteuerung deaktiviert ist, ignoriert die COM-Runtime die BENUTZERSPEZIFISCHE COM-Konfiguration und greifen nur auf die COMPUTERspezifische COM-Konfiguration zu. Anwendungen, die Administratorrechte erfordern, sollten abhängige COM-Objekte während der Installation im COM-Konfigurationsspeicher pro Computer registrieren (**HKEY \_ LOCAL MACHINE Software \_ \\ \\ Classes**). Weitere Informationen finden Sie unter [AC: UAC: COM Per-User Configuration](/previous-versions/bb756926(v=msdn.10)).

**Windows Server 2003 und Windows XP/2000:** Anwendungen können abhängige COM-Objekte entweder im COMPUTER- oder benutzerspezifischen COM-Konfigurationsspeicher registrieren (**HKEY \_ LOCAL \_ \\ MACHINE-Softwareklassen \\** oder **HKEY \_ CURRENT USER \_ Software \\ \\ Classes**).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[HKEY \_ CLASSES \_ ROOT (Referenz zur Resource Kit-Registrierung)](/previous-versions/windows/it-pro/windows-server-2003/cc739822(v=ws.10))
</dt> </dl>

 

 
