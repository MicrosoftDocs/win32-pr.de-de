---
title: Benutzerdefinierte Wählhilfen
description: Windows Betriebssystem 2000 und höher ermöglichen Es Entwicklern, ihre eigenen benutzerdefinierten Dialer bereitzustellen, die mit dem Ras-Ras-Dienst (RAS) arbeiten.
ms.assetid: ad94f38d-812f-4329-8055-6274a21a3242
keywords:
- Benutzerdefinierte Wählhilfen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69b23edd8501929181a54b1b511f365945f8e1c6277056e068cf58fb67bd26c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791500"
---
# <a name="custom-dialers"></a>Benutzerdefinierte Wählhilfen

Windows Betriebssystem 2000 und höher ermöglichen Es Entwicklern, ihre eigenen benutzerdefinierten Dialer bereitzustellen, die mit dem Ras-Ras-Dienst (RAS) arbeiten. Das benutzerdefinierte Dialer wird als einzelne DLL (Dynamic Link Library) implementiert, die die folgenden Einstiegspunkte exportiert:

-   [**RasCustomDial**](/windows/desktop/api/Ras/nc-ras-rascustomdialfn)
-   [**RasCustomDialDlg**](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomdialdlgfn)
-   [**RasCustomHangup**](/windows/desktop/api/Ras/nc-ras-rascustomhangupfn)
-   [**RasCustomEntryDlg**](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomentrydlgfn)
-   [**RasCustomDeleteEntryNotify**](/windows/desktop/api/Ras/nc-ras-rascustomdeleteentrynotifyfn)

Die DLL für benutzerdefiniertes Wählen muss alle diese Einstiegspunkte exportieren und die Einstiegspunkte als Unicode-Funktionen implementieren. Weitere Informationen zu diesen Funktionen finden Sie auf der Referenzseite für jede Funktion in der Referenz zum WINDOWS SDK-Remotezugriffsdienst.

Damit eine RAS-Verbindung das benutzerdefinierte Dialer verwenden kann, muss der Telefonbucheintrag für die Verbindung den Pfad zur DLL für benutzerdefiniertes Wählen enthalten. Verwenden Sie die RAS-API-Funktionen [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) und [**RasSetEntryProperties,**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) um diesen Pfad im **szCustomDialDll-Element** der [**RASENTRY-Struktur**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) für den Telefonbucheintrag festzulegen.

## <a name="updating-the-registry-for-custom-dialers"></a>Aktualisieren der Registrierung für benutzerdefinierte Wählhilfen

Damit das System eine Verbindung wählen kann, die ein benutzerdefiniertes Dialer verwendet, muss der Pfad zur DLL für benutzerdefinierte Wähle im folgenden Registrierungswert vorhanden sein.

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
<dd>                  REG_MULTI_SZ</dd>
</dl>
```

Da **CustomDLL** vom Typ **REG MULTI \_ \_ SZ** ist, kann es Pfade zu mehreren DLLs mit benutzerdefiniertem Wählvorgang enthalten. Sie müssen den Pfad zur DLL mit benutzerdefiniertem Wählvorgang in diesem Registrierungswert zusätzlich zum Telefonbucheintrag für die Verbindung festlegen.

Standardmäßig kann dieser Registrierungswert nur von einem Benutzer mit Administrator- oder Systemberechtigungen geschrieben werden. Ändern Sie aus Sicherheitsgründen nicht die Berechtigungen für diesen Registrierungsschlüssel.

## <a name="using-custom-dialers-at-system-logon"></a>Verwenden von benutzerdefinierten Wählern bei der Systemanmeldung

Windows Betriebssystem 2000 und höher ermöglicht es einem Benutzer, zum Zeitpunkt der Anmeldung eine RAS-Verbindung herzustellen. Dazu überprüft der Benutzer im Dialogfeld **Anmeldeinformationen** die Anmeldung mithilfe von **DFÜ-Netzwerken.** Nachdem der Benutzer auf die Schaltfläche Ok geklickt hat, zeigt das System die verfügbaren Verbindungen an.

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

In den meisten Fällen arbeitet ein benutzerdefiniertes Dialer mit den Sicherheitsberechtigungen des Benutzers, der es aufruft. Wenn das benutzerdefinierte Dialer jedoch bei der Anmeldung aufgerufen wird, wird es mit Systemberechtigungen betrieben. Entwerfen Sie daher das benutzerdefinierte Dialer so, dass es nicht verwendet werden kann, um die Systemsicherheit zu verletzen. Beispielsweise sollte die Wählhilfe keine Benutzeroberfläche darstellen, die dem Benutzer Schreibzugriff auf das Dateisystem des Computers ermöglicht. Zu den Benutzeroberflächen, die diesen Zugriff ermöglichen, gehören das Dialogfeld **"Datei suchen",** das dialogfeld **"Datei öffnen"** und Windows **Hilfe.**

## <a name="custom-dialer-user-interface-must-support-idcancel"></a>Benutzerdefinierte Wählhilfe Benutzeroberfläche IDCANCEL unterstützen muss

Wenn das benutzerdefinierte Wählfeld eine Benutzeroberfläche anzeigt, muss die Benutzeroberfläche WM \_ COMMAND-Meldungen unterstützen, bei denen LOWORD(*wParam*) gleich IDCANCEL ist.

 

 