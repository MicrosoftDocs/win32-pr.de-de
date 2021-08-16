---
title: AppIDFlags
description: Ein Satz von Flags, die das Aktivierungsverhalten eines COM-Servers steuern.
ms.assetid: ab98e7d3-85c6-4328-84c4-1d4583df69ce
keywords:
- AppIDFlags-Registrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44ecf7d0d112d2ceff913f3de6250c130e16455c1810cc6234db63a6aaf463fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048868"
---
# <a name="appidflags"></a>AppIDFlags

Ein Satz von Flags, die das Aktivierungsverhalten eines COM-Servers steuern.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AppIDFlags = flags
```

## <a name="remarks"></a>Hinweise

Dies ist ein **\_ REG-DWORD-Wert.**



| Flagwert | Konstante                                              |
|------------|-------------------------------------------------------|
| 0x1        | APPIDREGFLAGS \_ AKTIVIEREN \_ IUSERVER \_ INDESKTOP          |
| 0x2        | APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ AND \_ BIND |
| 0x4        | APPIDREGFLAGS-PROBLEM: \_ \_ AKTIVIERUNGS-RPC \_ BEI \_ \_ IDENTIFIZIERUNG   |



 

### <a name="appidregflags_activate_iuserver_indesktop-description"></a>APPIDREGFLAGS \_ ACTIVATE \_ IUSERVER \_ INDESKTOP Description

Wenn das [](/windows/desktop/winstation/window-stations) **APPIDREGFLAGS ACTIVATE \_ \_ IUSERVER \_ INDESKTOP-Flag** in **AppIDFlags** gelöscht wird oder **AppIDFlags** nicht vorhanden ist, bindet der Client in einer Terminalserversitzung eine Aktivierungsanforderung für einen Interactive [User](interactive-user.md) COM-Server und bindet ihn entweder an den COM-Server auf dem "Standarddesktop" der Winsta0-Fensterstation der Sitzung in der Aktivierungsanforderung oder startet und bindet ihn an ihn. Wenn auf dem Client beispielsweise "winsta0 desktop1" von Sitzung 3 ausgeführt wird, wird die Aktivierungsanforderung für Sitzung 3 entweder an den COM-Server in "winsta0 default" von Sitzung 3 gebunden oder gestartet und an ihn gebunden, auch wenn bereits eine Instanz des \\ \\ COM-Servers in "winsta0 desktop1" von Sitzung \\ 3 ausgeführt wird.

Wenn das **APPIDREGFLAGS \_ ACTIVATE \_ IUSERVER \_ INDESKTOP-Flag** im **AppIDFlags-Wert** festgelegt ist, bindet COM entweder den Serverprozess, der auf dem Clientdesktop ausgeführt wird, und die Sitzung in der Aktivierungsanforderung an den Serverprozess, der auf dem Clientdesktop ausgeführt wird, oder startet und bindet ihn an ihn. Wenn auf dem Client beispielsweise "winsta0 desktop1" in Sitzung 3 ausgeführt wird, wird die Aktivierungsanforderung für Sitzung 3 entweder an den COM-Server in "winsta0 desktop1" in Sitzung 3 gebunden oder gestartet und an ihn gebunden, auch wenn bereits eine Instanz des COM-Servers in Sitzung 3 in \\ \\ "winsta0 default" ausgeführt \\ wird.

Der Client kann den [Sitzungsmoniker](/windows/desktop/TermServ/session-monikers) verwenden, um eine Sitzung anzugeben, die sich von der Sitzung des Clients unterscheidet, wenn er die Aktivierungsanforderung stellt.

Das **APPIDREGFLAGS \_ ACTIVATE \_ IUSERVER \_ INDESKTOP-Flag** gilt nur für COM-Server, die für RunAs ["Interactive User" konfiguriert](interactive-user.md)sind.

### <a name="appidregflags_secure_server_process_sd_and_bind-description"></a>APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ AND \_ BIND Description

Wenn das **APPIDREGFLAGS \_ SECURE SERVER PROCESS SD AND \_ \_ \_ \_ \_ BIND-Flag** in **AppIDFlags** festgelegt ist, werden COM-Server, die für RunAs "Activator" konfiguriert sind, mit einem Prozesssicherheitsdeskriptor gestartet, der [PROCESS ALL \_ \_ ACCESS](/windows/desktop/ProcThread/process-security-and-access-rights) auf die LogonID-SID des Prozesstokens zulässt. Darüber hinaus wird der Besitzer des Sicherheitsdeskriptors auf die LogonID-SID des Prozesstokens festgelegt.

Wenn das **APPIDREGFLAGS \_ SECURE SERVER PROCESS SD AND \_ \_ \_ \_ \_ BIND-Flag** in **AppIDFlags** festgelegt ist, werden COM-Server, die für RunAs "This User" konfiguriert sind, mit einem Prozesssicherheitsdeskriptor gestartet, der [PROCESS ALL \_ \_ ACCESS](/windows/desktop/ProcThread/process-security-and-access-rights) in der LogonID-SID des Prozesstokens zulässt. Darüber hinaus wird der Besitzer des Sicherheitsdeskriptors auf die LogonID-SID des Prozesstokens festgelegt. Darüber hinaus ändert der COM Service Control Manager (SCM) das Token des COM-Serverprozesses wie folgt:

-   Sie fügt dem Token eine APPID-SID hinzu. Sie gewährt der APPID-SID Vollzugriff in der Token-DACL (Discretionary Access Control List). In Windows Vista und neueren Versionen von Windows wird die OwnerRights SID READ \_ CONTROL-Berechtigung in der Token-Standard-DACL erteilt. In Versionen vor Windows Vista von Windows wird der Tokenbesitzer auf die APPID-SID fest.

Bei verwendung des FLAGS APPIDREGFLAGS SECURE SERVER PROCESS SD AND BIND müssen die folgenden **\_ \_ \_ \_ \_ \_ Sicherheitsüberlegungen berücksichtigt** werden:

-   Das **APPIDREGFLAGS \_ SECURE SERVER PROCESS SD AND \_ \_ \_ \_ \_ BIND-Flag** soll von COM-Servern festgelegt werden, die unter einem der integrierten Dienstsicherheitskontexte gestartet werden: networkservice- oder localservice-Konten. Wenn die Server die Identität privilegierter Clients imitieren und das **FLAG APPIDREGFLAGS \_ SECURE SERVER PROCESS SD AND \_ \_ \_ \_ \_ BIND** nicht festgelegt ist, kann bösartiger Code, der in anderen Prozessen mit demselben Sicherheitskontext ausgeführt wird, die Berechtigungen erhöhen, indem die Identitätswechseltoken der privilegierten Clients aus dem COM-Serverprozess übertragen werden.
-   Wenn **das APPIDREGFLAGS \_ SECURE SERVER PROCESS SD AND \_ \_ \_ \_ \_ BIND-Flag** festgelegt ist, härtet COM den Sicherheitsdeskriptor des Prozessobjekts im Fall von COM-RunAs-"Activator"-Servern. Für solche Server wird erwartet, dass der COM-Client das Token härtet, das er für die COM-Aktivierung verwendet.
-   Wenn **das APPIDREGFLAGS \_ SECURE SERVER PROCESS SD AND \_ \_ \_ \_ \_ BIND-Flag** festgelegt ist, härtet COM die Sicherheitsbeschreibung des Prozessobjekts im Fall von COM-Servern mit den RunAs "This User". Außerdem wird das Prozesstoken des COM-Servers gehärtet, da der COM-SCM die Entität ist, die das Token erstellt.

Das **APPIDREGFLAGS \_ SECURE SERVER PROCESS SD AND \_ \_ \_ \_ \_ BIND-Flag** wird in Windows XP, Windows Server 2003, Windows Vista und Windows Server 2008 nur unterstützt, wenn der MSRC8322-Patch ( Sicherheitsbulletin [MS09-012](https://support.microsoft.com/kb/959454)) angewendet wird. Es wird nativ in version Windows 7 und neueren Versionen von Windows.

Das **APPIDREGFLAGS \_ SECURE SERVER PROCESS SD AND \_ \_ \_ \_ \_ BIND-Flag** gilt nur für COM-Server, die für RunAs "Activator" oder "This User" konfiguriert sind. Dies gilt nicht für COM-Server, die NT-Dienste sind.

### <a name="appidregflags_issue_activation_rpc_at_identify-description"></a>APPIDREGFLAGS \_ PROBLEM AKTIVIERUNG RPC AT IDENTIFY \_ \_ \_ \_ Description

Wenn das **FLAG APPIDREGFLAGS \_ ISSUE ACTIVATION RPC AT \_ \_ \_ \_ IDENTIFY** in **AppIDFlags** festgelegt ist, gibt der COM-SCM Objektaktivierungsanforderungen an den COM-Serverprozess aus. Dabei wird die Identitätswechselebene [RPC C IMP LEVEL IDENTIFY \_ \_ \_ \_ verwendet.](impersonation-levels.md)

Wenn das **RPC \_ AT \_ \_ \_ \_ IDENTIFY-Flag APPIDREGFLAGS ISSUE ACTIVATION** NICHT festgelegt ist, gibt der COM-SCM Objektaktivierungsanforderungen an die COM-Serverprozesse aus, indem die Identitätswechselebene RPC C IMP LEVEL [ \_ \_ \_ \_ IMPERSONATE](impersonation-levels.md)verwendet wird.

Die folgenden Sicherheitsüberlegungen müssen bei Verwendung des **FLAGs APPIDREGFLAGS \_ ISSUE ACTIVATION RPC AT IDENTIFY \_ \_ \_ \_ berücksichtigt** werden:

-   Das **FLAG APPIDREGFLAGS \_ ISSUE ACTIVATION RPC AT \_ \_ \_ \_ IDENTIFY** ist für die Verwendung durch COM-Server gedacht, die in Objektaktivierungsanforderungen keine Aufgaben im Auftrag von Clients ausführen. Wenn der COM-SCM für solche Server Objektaktivierungsanforderungen auf [RPC C IMP LEVEL \_ \_ \_ \_ IDENTIFY](impersonation-levels.md) ausstelle, wird die Wahrscheinlichkeit von privilegierten Token minimiert, wenn SE [**\_ IMPERSONATE \_ NAME-Ebene**](/windows/desktop/SecAuthZ/privilege-constants) im Prozess angezeigt wird.

Das **RPC AT \_ \_ \_ \_ \_ IDENTIFY-Flag APPIDREGFLAGS ISSUE ACTIVATION** wird in Windows 7 und neueren Versionen von Windows.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Desktops](/windows/desktop/winstation/desktops)
</dt> <dt>

[Identitätswechselebenen](impersonation-levels.md)
</dt> <dt>

[Interaktiver Benutzer](interactive-user.md)
</dt> <dt>

[Sitzungsmoniker](/windows/desktop/TermServ/session-monikers)
</dt> <dt>

[Fensterstationen](/windows/desktop/winstation/window-stations)
</dt> </dl>

 

 