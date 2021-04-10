---
title: Benutzerdefinierte-diker
description: Windows 2000 und spätere Betriebssysteme ermöglichen es Entwicklern, eigene benutzerdefinierte dbugatoren bereitzustellen, die mit dem Remote Zugriffs Dienst (RAS) funktionieren.
ms.assetid: ad94f38d-812f-4329-8055-6274a21a3242
keywords:
- Benutzerdefinierte-diker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35293de408a2a0faa146b93f9b5d5ebccf447acc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209302"
---
# <a name="custom-dialers"></a>Benutzerdefinierte-diker

Windows 2000 und spätere Betriebssysteme ermöglichen es Entwicklern, eigene benutzerdefinierte dbugatoren bereitzustellen, die mit dem Remote Zugriffs Dienst (RAS) funktionieren. Die benutzerdefinierte Einwählprogramm ist als einzelne Dynamic Link Library (dll) implementiert, die die folgenden Einstiegspunkte exportiert:

-   [**Rascustomdial**](/windows/desktop/api/Ras/nc-ras-rascustomdialfn)
-   [**Rascustomdialdlg**](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomdialdlgfn)
-   [**Rascustomhangup**](/windows/desktop/api/Ras/nc-ras-rascustomhangupfn)
-   [**Rascustomentrydlg**](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomentrydlgfn)
-   [**Rascustomdeleteentrynotify**](/windows/desktop/api/Ras/nc-ras-rascustomdeleteentrynotifyfn)

Die benutzerdefinierte DFÜ-dll muss alle diese Einstiegspunkte exportieren und die Einstiegspunkte als Unicode-Funktionen implementieren. Weitere Informationen zu diesen Funktionen finden Sie auf der Referenzseite für jede Funktion in der Windows SDK RAS-Dienst Referenz.

Damit eine RAS-Verbindung die benutzerdefinierte Dialer verwendet, muss der Telefonbucheintrag für die Verbindung den Pfad zur benutzerdefinierten dll enthalten. Verwenden Sie die RAS-API-Funktionen " [**rasgetentryproperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) " und " [**rassetentryproperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) ", um diesen Pfad im **szcustomdialdll** -Member der " [**rasentry**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) "-Struktur für den Telefonbucheintrag festzulegen.

## <a name="updating-the-registry-for-custom-dialers"></a>Aktualisieren der Registrierung für benutzerdefinierte Dialekte

Damit das System eine Verbindung wählen kann, die eine benutzerdefinierte Dialer verwendet, muss der Pfad zur benutzerdefinierten DFÜ-dll im folgenden Registrierungs Wert vorhanden sein.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
                  CustomDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_MULTI_SZ</dd>
</dl>
```

Da **CustomDLL** den Typ **reg \_ \_ MultiSZ** hat, kann es Pfade zu mehreren benutzerdefinierten DLLs enthalten. Sie müssen den Pfad zu der benutzerdefinierten DFÜ-dll in diesem Registrierungs Wert zusätzlich zum Telefonbucheintrag für die Verbindung festlegen.

Standardmäßig kann dieser Registrierungs Wert nur von einem Benutzer mit Administrator-oder System Berechtigungen geschrieben werden. Ändern Sie die Berechtigungen für diesen Registrierungsschlüssel aus Sicherheitsgründen nicht.

## <a name="using-custom-dialers-at-system-logon"></a>Verwenden von benutzerdefinierten dialtoren bei der System Anmeldung

Windows 2000 und spätere Betriebssysteme ermöglichen es einem Benutzer, zum Zeitpunkt der Anmeldung eine RAS-Verbindung herzustellen. Zu diesem Zweck überprüft der Benutzer die **Anmeldung mithilfe des Einwählnetzwerks** im Dialogfeld **Anmelde Informationen** . Nachdem der Benutzer auf die Schaltfläche "OK" geklickt hat, zeigt das System die verfügbaren Verbindungen an.

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

In den meisten Fällen arbeitet eine benutzerdefinierte Einwählprogramm mit den Sicherheits Privilegien des Benutzers, der ihn aufruft. Wenn jedoch die benutzerdefinierte Einwählprogramm bei der Anmeldung aufgerufen wird, wird Sie mit System Privilegien betrieben. Daher sollten Sie die benutzerdefinierte Einwählprogramm so entwerfen, dass Sie nicht zur Verletzung der Systemsicherheit verwendet werden kann. Beispielsweise sollte die Einwählprogramm keine Benutzeroberfläche präsentieren, die dem Benutzer den Schreibzugriff auf das Dateisystem des Computers ermöglicht. Zu den Benutzeroberflächen, die diesen Zugriff bereitstellen, gehören das Dialogfeld " **Find-File** ", das Dialogfeld " **Datei öffnen** " und die Windows- **Hilfe**

## <a name="custom-dialer-user-interface-must-support-idcancel"></a>Benutzerdefinierte Dialer-Benutzeroberfläche muss IDCANCEL unterstützen

Wenn die benutzerdefinierte Einwählprogramm eine Benutzeroberfläche anzeigt, muss die Benutzeroberfläche die WM-befehlsnachrichten unterstützen, \_ wobei LoWord (*wParam*) gleich IDCANCEL ist.

 

 