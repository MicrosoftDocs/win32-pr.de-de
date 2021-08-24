---
title: AppIDFlags
description: Eine Gruppe von Flags, die das Aktivierungsverhalten eines COM-Servers steuern.
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

Eine Gruppe von Flags, die das Aktivierungsverhalten eines COM-Servers steuern.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AppIDFlags = flags
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ DWORD-Wert.**



| Flagwert | Konstante                                              |
|------------|-------------------------------------------------------|
| 0x1        | APPIDREGFLAGS \_ ACTIVATE \_ IUSERVER \_ INDESKTOP          |
| 0x2        | APPIDREGFLAGS \_ SECURE SERVER PROCESS SD UND \_ \_ \_ \_ \_ BIND |
| 0x4        | APPIDREGFLAGS \_ ISSUE \_ ACTIVATION \_ RPC \_ AT \_ IDENTIFY   |



 

### <a name="appidregflags_activate_iuserver_indesktop-description"></a>APPIDREGFLAGS \_ ACTIVATE \_ IUSERVER \_ INDESKTOP Description

Wenn das **FLAG APPIDREGFLAGS \_ ACTIVATE \_ IUSERVER \_ INDESKTOP** in **AppIDFlags** gelöscht wird oder **AppIDFlags** nicht vorhanden ist, stellt der Client in einer Terminalserversitzung, die eine Aktivierungsanforderung für einen [COM-Server](interactive-user.md) eines interaktiven Benutzers stellt, entweder eine Bindung an den COM-Server auf dem "Standarddesktop" der [Fensterstation](/windows/desktop/winstation/window-stations) "winsta0" der Sitzung in der Aktivierungsanforderung oder wird gestartet und an diesen gebunden. Wenn der Client beispielsweise "winsta0 \\ desktop1" von Sitzung 3 ausführt, wird die Aktivierungsanforderung für Sitzung 3 entweder an den COM-Server in "winsta0 default" von Sitzung 3 gebunden oder gestartet und \\ gebunden, auch wenn eine Instanz des COM-Servers bereits in "winsta0 \\ desktop1" von Sitzung 3 ausgeführt wird.

Wenn das **FLAG APPIDREGFLAGS \_ ACTIVATE \_ IUSERVER \_ INDESKTOP** im **AppIDFlags-Wert** festgelegt ist, wird COM entweder an den Serverprozess, der auf dem Desktop des Clients ausgeführt wird, und die Sitzung in der Aktivierungsanforderung gebunden oder gestartet und an diesen gebunden. Wenn der Client beispielsweise "winsta0 \\ desktop1" in Sitzung 3 ausführt, wird die Aktivierungsanforderung für Sitzung 3 entweder an den COM-Server in "winsta0 desktop1" in Sitzung 3 gebunden oder gestartet und gebunden. Dies \\ gilt auch, wenn eine Instanz des COM-Servers in Sitzung 3 bereits in "winsta0 default" ausgeführt \\ wird.

Der Client kann den [Sitzungsmoniker](/windows/desktop/TermServ/session-monikers) verwenden, um eine andere Sitzung als die Sitzung des Clients anzugeben, wenn er die Aktivierungsanforderung vornimmt.

Das **FLAG APPIDREGFLAGS \_ ACTIVATE \_ IUSERVER \_ INDESKTOP** gilt nur für COM-Server, die für RunAs ["Interactive User"](interactive-user.md)konfiguriert sind.

### <a name="appidregflags_secure_server_process_sd_and_bind-description"></a>APPIDREGFLAGS \_ SECURE SERVER PROCESS SD UND BIND \_ \_ \_ \_ \_ Description

Wenn das **FLAG APPIDREGFLAGS \_ SECURE SERVER PROCESS SD AND \_ \_ \_ \_ \_ BIND** in **AppIDFlags** festgelegt ist, werden COM-Server, die für RunAs "Activator" konfiguriert sind, mit einem Prozesssicherheitsdeskriptor gestartet, der [PROCESS ALL ACCESS \_ \_ auf](/windows/desktop/ProcThread/process-security-and-access-rights) die LogonID-SID des Prozesstokens zulässt. Darüber hinaus wird der Besitzer des Sicherheitsdeskriptors auf die LogonID-SID des Prozesstokens festgelegt.

Wenn das FLAG **APPIDREGFLAGS \_ SECURE SERVER PROCESS SD UND \_ \_ \_ \_ \_ BIND** in **AppIDFlags** festgelegt ist, werden COM-Server, die für RunAs "This User" konfiguriert sind, mit einem Prozesssicherheitsdeskriptor gestartet, der [PROCESS ALL \_ \_ ACCESS](/windows/desktop/ProcThread/process-security-and-access-rights) in der Anmelde-ID des Prozesstokens zulässt. Darüber hinaus wird der Besitzer des Sicherheitsdeskriptors auf die LogonID-SID des Prozesstokens festgelegt. Darüber hinaus ändert der COM-Dienststeuerungs-Manager (SCM) das Token des COM-Serverprozesses wie folgt:

-   Dem Token wird eine APPID-SID hinzugefügt. Sie gewährt der APPID-SID Vollzugriff in der standardmäßigen DACL (Discretionary Access Control List) des Tokens. In Windows Vista und neueren Versionen von Windows wird die OwnerRights SID READ \_ CONTROL-Berechtigung in der Standardmäßigen DACL des Tokens gewährt. In versionen vor Windows Vista von Windows wird der Tokenbesitzer auf die APPID-SID festgelegt.

Bei Verwendung des FLAGS **APPIDREGFLAGS SECURE \_ \_ SERVER \_ PROCESS SD \_ UND \_ \_ BIND** müssen die folgenden Sicherheitsüberlegungen berücksichtigt werden:

-   Das **FLAG APPIDREGFLAGS \_ SECURE SERVER PROCESS SD UND \_ \_ \_ \_ \_ BIND** ist für COM-Server vorgesehen, die unter einem der integrierten Dienstsicherheitskontexte gestartet werden, z. B. networkService- oder LocalService-Konten. Wenn die Server die Identität privilegierter Clients annehmen und das **FLAG APPIDREGFLAGS \_ SECURE SERVER PROCESS SD AND \_ \_ \_ \_ \_ BIND** nicht festgelegt ist, kann bösartiger Code, der in anderen Prozessen mit demselben Sicherheitskontext ausgeführt wird, die Rechte erhöhen, indem die Identitätswechseltoken der privilegierten Clients aus dem COM-Serverprozess entwendet werden.
-   Wenn das FLAG **APPIDREGFLAGS \_ SECURE SERVER PROCESS SD UND \_ \_ \_ \_ \_ BIND** festgelegt ist, härtet COM die Sicherheitsbeschreibung des Prozessobjekts im Fall von RunAs-COM-Servern vom Typ "Activator". Für solche Server wird erwartet, dass der COM-Client das Token, das er für die COM-Aktivierung verwendet, härtet.
-   Wenn das **FLAG APPIDREGFLAGS \_ SECURE SERVER PROCESS SD UND \_ \_ \_ \_ \_ BIND** festgelegt ist, härtet COM die Sicherheitsbeschreibung des Prozessobjekts im Fall von RunAs-COM-Servern vom Typ "Dieser Benutzer". Außerdem wird das Prozesstoken des COM-Servers gehärtet, da der COM-SCM die Entität ist, die das Token erstellt.

Das FLAG **APPIDREGFLAGS \_ SECURE SERVER PROCESS SD AND \_ \_ \_ \_ \_ BIND** wird in Windows XP, Windows Server 2003, Windows Vista und Windows Server 2008 nur unterstützt, wenn der MSRC8322-Patch [(Sicherheitsbulletin MS09-012](https://support.microsoft.com/kb/959454)) angewendet wird. Sie wird in Windows 7 und neueren Versionen von Windows nativ unterstützt.

Das **FLAG APPIDREGFLAGS \_ SECURE SERVER PROCESS SD AND \_ \_ \_ \_ \_ BIND** gilt nur für COM-Server, die für RunAs "Activator" oder "This User" konfiguriert sind. Sie gilt nicht für COM-Server, die NT-Dienste sind.

### <a name="appidregflags_issue_activation_rpc_at_identify-description"></a>APPIDREGFLAGS \_ ISSUE \_ ACTIVATION \_ RPC \_ AT \_ IDENTIFY Description

Wenn das **FLAG APPIDREGFLAGS \_ ISSUE ACTIVATION RPC AT \_ \_ \_ \_ IDENTIFY** in **AppIDFlags** festgelegt ist, gibt der COM-SCM Objektaktivierungsanforderungen an den COM-Serverprozess aus, indem er die Identitätsebene [RPC C \_ \_ IMP LEVEL \_ \_ IDENTIFY](impersonation-levels.md)verwendet.

Wenn das **FLAG APPIDREGFLAGS \_ ISSUE ACTIVATION RPC AT \_ \_ \_ \_ IDENTIFY** nicht festgelegt ist, gibt der COM-SCM Objektaktivierungsanforderungen an die COM-Serverprozesse aus, indem er die Identitätsebene [RPC C \_ \_ IMP LEVEL \_ \_ IMPERSONATE](impersonation-levels.md)verwendet.

Bei Verwendung des **FLAGS APPIDREGFLAGS ISSUE \_ \_ ACTIVATION \_ RPC \_ AT \_ IDENTIFY** müssen die folgenden Sicherheitsüberlegungen berücksichtigt werden:

-   Das **FLAG APPIDREGFLAGS \_ ISSUE ACTIVATION RPC AT \_ \_ \_ \_ IDENTIFY** ist für COM-Server vorgesehen, die in Objektaktivierungsanforderungen keine Arbeit im Auftrag von Clients ausführen. Wenn für solche Server die COM SCM Objektaktivierungsanforderungen auf [RPC \_ C \_ IMP LEVEL \_ \_ IDENTIFY](impersonation-levels.md) ausgibt, wird die Wahrscheinlichkeit minimiert, dass privilegierte Token [**mit SE \_ IMPERSONATE \_ NAME-Ebene**](/windows/desktop/SecAuthZ/privilege-constants) im Prozess angezeigt werden.

Das **FLAG APPIDREGFLAGS \_ ISSUE ACTIVATION RPC AT \_ \_ \_ \_ IDENTIFY** wird in Windows 7 und höher von Windows unterstützt.

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

 

 