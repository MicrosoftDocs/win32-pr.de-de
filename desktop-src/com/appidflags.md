---
title: Appidflags
description: Ein Satz von Flags, die das Aktivierungs Verhalten eines COM-Servers steuern.
ms.assetid: ab98e7d3-85c6-4328-84c4-1d4583df69ce
keywords:
- Appidflags-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdad2b80625d6a60460d43f242d7897e0ae7eb40
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106339517"
---
# <a name="appidflags"></a>Appidflags

Ein Satz von Flags, die das Aktivierungs Verhalten eines COM-Servers steuern.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AppIDFlags = flags
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ DWORD** -Wert.



| Flagwert | Konstante                                              |
|------------|-------------------------------------------------------|
| 0x1        | appidregflags \_ Aktivieren von \_ iuserver \_ indesktop          |
| 0x2        | appidregflags \_ Secure \_ Server \_ Process \_ SD \_ und \_ Bind |
| 0x4        | appidregflags- \_ Ausgabe- \_ \_ RPC \_ bei \_ Identifizierung   |



 

### <a name="appidregflags_activate_iuserver_indesktop-description"></a>Appidregflags \_ Aktivieren Sie \_ iuserver \_ indesktop Description.

Wenn **appidregflags das \_ iuserver-Flag " \_ \_ indesktop" aktivieren** , wird es in **appidflags** gelöscht, oder **appidflags** ist nicht vorhanden. der Client in einer Terminal Server Sitzung, die eine Aktivierungs Anforderung für einen [interaktiven Benutzer](interactive-user.md) -com-Server durchführt, bindet entweder an den com-Server im "Standard"-Desktop der "WinSta0"- [Fenster Station](/windows/desktop/winstation/window-stations) der Sitzung in der Aktivierungs Anforderung und bindet ihn an. Wenn z. b. auf dem Client "WinSta0 \\ desktop1" der Sitzung 3 ausgeführt wird, wird die Aktivierungs Anforderung für Sitzung 3 entweder an den com-Server in "WinSta0 default" der Sitzung 3 gebunden oder gestartet und an diesen gebunden, \\ auch wenn eine Instanz des COM-Servers bereits in "WinSta0 \\ desktop1" der Sitzung 3 ausgeführt wird.

Wenn das **appidregflags-Flag " \_ \_ iuserver \_ indesktop** " im **appidflags** -Wert aktiviert ist, bindet com entweder den Server Prozess, der auf dem Desktop des Clients ausgeführt wird, und bindet ihn an den Server Prozess, der in der Aktivierungs Anforderung ausgeführt wird. Wenn z. b. auf dem Client "WinSta0 \\ desktop1" in Sitzung 3 ausgeführt wird, wird die Aktivierungs Anforderung für Sitzung 3 entweder an den com-Server in "WinSta0 desktop1" in Sitzung 3 gebunden oder gestartet und an diesen gebunden \\ , auch wenn eine Instanz des COM-Servers bereits in "WinSta0 \\ default" in Sitzung 3 ausgeführt wird.

Der-Client kann den [sitzungsmoniker](/windows/desktop/TermServ/session-monikers) verwenden, um eine andere Sitzung als die Sitzung des Clients anzugeben, wenn die Aktivierungs Anforderung erfolgt.

Das Flag " **\_ \_ iuserver \_ indesktop aktivieren" von "appidregflags** " gilt nur für com-Server, die als "[interaktiver Benutzer](interactive-user.md)" konfiguriert sind.

### <a name="appidregflags_secure_server_process_sd_and_bind-description"></a>Appidregflags \_ Secure \_ Server \_ Process \_ SD \_ und \_ Bind Description

Wenn **appidregflags \_ Secure \_ Server \_ Process \_ SD und das \_ \_ Bind-** Flag in **appidflags** festgelegt sind, werden com-Server, die für die Ausführung von "Activator" konfiguriert sind, mit einem Prozess Sicherheits Deskriptor gestartet, der den [ \_ gesamten \_ Zugriff](/windows/desktop/ProcThread/process-security-and-access-rights) auf die LogonId-SID des Prozess Tokens ermöglicht. Außerdem wird der Besitzer der Sicherheits Beschreibung auf die LogonId-SID des Prozess Tokens festgelegt.

Wenn **appidregflags \_ Secure \_ Server \_ Process \_ SD und das \_ \_ Bind-** Flag in **appidflags** festgelegt sind, werden com-Server, die für die Ausführung von "this user" konfiguriert sind, mit einer Prozess Sicherheits Beschreibung gestartet, die den [ \_ gesamten \_ Zugriff](/windows/desktop/ProcThread/process-security-and-access-rights) in der LogonId-SID des Prozess Tokens ermöglicht. Außerdem wird der Besitzer der Sicherheits Beschreibung auf die LogonId-SID des Prozess Tokens festgelegt. Außerdem ändert der com-Dienststeuerungs-Manager (SCM) das Token des com-Server Prozesses wie folgt:

-   Dem Token wird eine AppID-sid hinzugefügt. Sie gewährt der AppID-sid Vollzugriff in der standardmäßigen Zugriffs Steuerungs Liste (DACL) des Tokens. In Windows Vista und höheren Versionen von Windows wird die Berechtigung "Besitzer Rechte-sid lesen" \_ in der tokenstandarddacl erteilt. In Versionen von Windows Vista vor Windows Vista wird der Tokenbesitzer auf die AppID-sid festgelegt.

Die folgenden Sicherheitsaspekte müssen berücksichtigt werden, wenn die **appidregflags \_ Secure \_ Server \_ Process \_ SD und das \_ \_ Bind-** Flag verwendet werden:

-   Die **appidregflags \_ Secure \_ Server \_ Process \_ SD \_ und das \_ Bind-** Flag sollen von com-Servern festgelegt werden, die unter einem der integrierten Dienst Sicherheits Kontexte gestartet werden, entweder dem NetworkService-Konto oder dem LocalService-Konto. Wenn die Server die Identität privilegierter Clients annehmen und der **appidregflags \_ Secure \_ Server \_ Process \_ SD \_ -und \_ Bind-** Flag nicht festgelegt ist, kann bösartiger Code, der in anderen Prozessen mit demselben Sicherheitskontext ausgeführt wird, die Berechtigung erhöhen, indem die Identitätswechsel Token der privilegierten Clients vom com-Server Prozess übernommen werden.
-   Wenn **appidregflags \_ Secure \_ Server \_ Process \_ SD \_ und \_ Bind** Flag festgelegt ist, wird die Sicherheits Beschreibung des Process-Objekts von com bei der Ausführung von "Activator"-com-Servern mit com vergrößert. Bei solchen Servern soll der com-Client das Token, das für die COM-Aktivierung verwendet wird, Härten.
-   Wenn die **appidregflags \_ Secure \_ Server \_ Process \_ SD \_ -und \_ Bind-** Flag festgelegt ist, wird die Sicherheits Beschreibung des Prozess Objekts von com bei den com-Servern des runas "this user" festgelegt. Außerdem wird das Prozess Token des COM-Servers festgeschrieben, da es sich bei dem com-SCM um die Entität handelt, die das Token erstellt.

**Appidregflags \_ Secure \_ Server \_ Process \_ SD \_ und \_ Bind-** Flag werden in Windows XP, Windows Server 2003, Windows Vista und Windows Server 2008 nur unterstützt, wenn der MSRC8322-Patch ([Sicherheitsbulletin MS09-012](https://support.microsoft.com/kb/959454)) angewendet wird. Sie wird in Windows 7 und höheren Versionen von Windows nativ unterstützt.

**Appidregflags \_ Secure \_ Server \_ Process \_ SD \_ und \_ Bind-** Flag gelten nur für com-Server, die für die Ausführung von "Activator" oder "this user" konfiguriert sind. Es gilt nicht für com-Server, bei denen es sich um NT-Dienste handelt.

### <a name="appidregflags_issue_activation_rpc_at_identify-description"></a>Appidregflags- \_ Problem \_ Aktivierung \_ RPC \_ bei Identifizierung der \_ Beschreibung

Wenn das **appidregflags- \_ Problem \_ bei der Aktivierung von \_ RPC \_ unter \_ identifizierungsflag** in **appidflags** festgelegt ist, gibt der com-SCM Objekt Aktivierungs Anforderungen an den com-Server Prozess mit einer Identitätswechsel Ebene der [RPC-C- \_ \_ \_ Ebene \_ Identifizierung](impersonation-levels.md)aus.

Wenn das **appidregflags- \_ Problem \_ bei der Aktivierung der RPC-Aktivierung bei einem \_ \_ \_ identifizierungsflag** nicht festgelegt ist, gibt der com-SCM Objekt Aktivierungs Anforderungen an die com-Server Prozesse mithilfe einer Identitätswechsel Ebene von RPC-C- [ \_ \_ \_ Ebene \_](impersonation-levels.md)für Identitätswechsel aus.

Die folgenden Sicherheitsüberlegungen müssen berücksichtigt werden, wenn die **appidregflags- \_ \_ Aktivierungs- \_ RPC \_ bei der \_ identifizierungsflag** verwendet wird:

-   Das **appidregflags- \_ Problem \_ bei der Aktivierung der RPC- \_ \_ unter \_ Identifizierung** ist für die Verwendung durch com-Server vorgesehen, die keine Arbeit im Auftrag von Clients in Objekt Aktivierungs Anforderungen ausführen. Bei solchen Servern wird durch das vorhanden sein von com SCM-Objekt Aktivierungs Anforderungen auf [RPC- \_ C- \_ IMP- \_ Ebene \_](impersonation-levels.md) die Wahrscheinlichkeit minimiert, dass privilegierte Token mit der [**\_ \_ namens**](/windows/desktop/SecAuthZ/privilege-constants) Ebene "SE Identitätswechsel" im Prozess angezeigt werden.

Das Flag zur **\_ Aktivierung der RPC- \_ Ausgabe \_ \_ von \_ appidregflags** in Windows 7 und höheren Versionen von Windows wird unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Desktops](/windows/desktop/winstation/desktops)
</dt> <dt>

[Identitätswechsel Ebenen](impersonation-levels.md)
</dt> <dt>

[Interaktiver Benutzer](interactive-user.md)
</dt> <dt>

[Sitzungsmoniker](/windows/desktop/TermServ/session-monikers)
</dt> <dt>

[Fenster Stationen](/windows/desktop/winstation/window-stations)
</dt> </dl>

 

 