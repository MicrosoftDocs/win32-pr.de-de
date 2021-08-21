---
title: Benutzerdefinierte Telefone
description: Windows Betriebssystemen 2000 und höher können Entwickler ihre eigenen benutzerdefinierten Telefone bereitstellen, die mit dem Ras-Dienst (RAS) arbeiten.
ms.assetid: ad94f38d-812f-4329-8055-6274a21a3242
keywords:
- Benutzerdefinierte Telefone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69b23edd8501929181a54b1b511f365945f8e1c6277056e068cf58fb67bd26c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791500"
---
# <a name="custom-dialers"></a>Benutzerdefinierte Telefone

Windows Betriebssystemen 2000 und höher können Entwickler ihre eigenen benutzerdefinierten Telefone bereitstellen, die mit dem Ras-Dienst (RAS) arbeiten. Das benutzerdefinierte Dialer wird als einzelne DLL (Dynamic Link Library) implementiert, die die folgenden Einstiegspunkte exportiert:

-   [**RasCustomDial**](/windows/desktop/api/Ras/nc-ras-rascustomdialfn)
-   [**RasCustomDialDlg**](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomdialdlgfn)
-   [**RasCustomHangup**](/windows/desktop/api/Ras/nc-ras-rascustomhangupfn)
-   [**RasCustomEntryDlg**](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomentrydlgfn)
-   [**RasCustomDeleteEntryNotify**](/windows/desktop/api/Ras/nc-ras-rascustomdeleteentrynotifyfn)

Die CUSTOM DIAL-DLL muss alle diese Einstiegspunkte exportieren und die Einstiegspunkte als Unicode-Funktionen implementieren. Weitere Informationen zu diesen Funktionen finden Sie auf der Referenzseite für jede Funktion in der Windows SDK-Remotezugriffsdienstreferenz.

Damit eine RAS-Verbindung das benutzerdefinierte Telefon verwenden kann, muss der Telefonbucheintrag für die Verbindung den Pfad zur CUSTOM DIAL-DLL enthalten. Verwenden Sie die RAS-API-Funktionen [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) und [**RasSetEntryProperties,**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) um diesen Pfad im **szCustomDialDll-Member** der [**RASENTRY-Struktur**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) für den Eintrag phone-book fest zu legen.

## <a name="updating-the-registry-for-custom-dialers"></a>Aktualisieren der Registrierung für benutzerdefinierte Wähler

Damit das System eine Verbindung wählen kann, die ein benutzerdefiniertes Wählfeld verwendet, muss der Pfad zur CUSTOM DIAL-DLL im folgenden Registrierungswert vorhanden sein.

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

Da **CustomDLL vom** Typ **REG MULTI \_ \_ SZ** ist, kann es Pfade zu mehreren DLLs mit benutzerdefinierten DFÜ-Datenhalten. Sie müssen den Pfad zur CUSTOM DIAL-DLL in diesem Registrierungswert zusätzlich zum Telefonbucheintrag für die Verbindung festlegen.

Standardmäßig kann dieser Registrierungswert nur von einem Benutzer mit Administrator- oder Systemberechtigungen geschrieben werden. Ändern Sie aus Sicherheitsgründen die Berechtigungen für diesen Registrierungsschlüssel nicht.

## <a name="using-custom-dialers-at-system-logon"></a>Verwenden benutzerdefinierter Wähler bei der Systemanmeldung

Windows Betriebssystemen 2000 und höher können Benutzer zum Zeitpunkt der Anmeldung eine RAS-Verbindung herstellen. Hierzu überprüft der Benutzer  im Dialogfeld Anmeldeinformationen die Anmeldung mithilfe von **DFÜ-Netzwerken.** Nachdem der Benutzer auf die Schaltfläche Ok geklickt hat, zeigt das System die verfügbaren Verbindungen an.

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

In den meisten Fällen arbeitet ein benutzerdefiniertes Telefon mit den Sicherheitsberechtigungen des Benutzers, der ihn aufruft. Wenn der benutzerdefinierte Telefonwähler jedoch bei der Anmeldung aufgerufen wird, wird er mit Systemberechtigungen ausgeführt. Entwerfen Sie daher das benutzerdefinierte Telefon so, dass es nicht verwendet werden kann, um die Systemsicherheit zu verletzen. Beispielsweise sollte das Telefon keine Benutzeroberfläche präsentieren, die dem Benutzer Schreibzugriff auf das Dateisystem des Computers ermöglicht. Benutzeroberflächen, die einen  solchen Zugriff ermöglichen, umfassen das Dialogfeld Datei suchen, das allgemeine Dialogfeld Datei öffnen und Windows **Hilfe.** 

## <a name="custom-dialer-user-interface-must-support-idcancel"></a>Custom Dialer Benutzeroberfläche Muss IDCANCEL unterstützen

Wenn das benutzerdefinierte Telefon eine Benutzeroberfläche anzeigt, muss die Benutzeroberfläche WM COMMAND-Nachrichten unterstützen, bei denen \_ LOWORD(*wParam*) IDCANCEL entspricht.

 

 