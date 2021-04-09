---
title: DCOM-Sicherheitsverbesserungen in Windows XP Service Pack 2 und Windows Server 2003 Service Pack 1
description: Mit Windows Server XP Service Pack 2 (SP2) und Windows Server 2003 Service Pack 1 (SP1) werden erweiterte Standard Sicherheitseinstellungen für die verteilte Component Object Model (DCOM) eingeführt.
ms.assetid: 1917834c-5216-4ef3-a0c2-d8ca63cef53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ad51807e27a9b97e8b05e467d8a84881c3993a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102407"
---
# <a name="dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>DCOM-Sicherheitsverbesserungen in Windows XP Service Pack 2 und Windows Server 2003 Service Pack 1

Mit Windows Server XP Service Pack 2 (SP2) und Windows Server 2003 Service Pack 1 (SP1) werden erweiterte Standard Sicherheitseinstellungen für die verteilte Component Object Model (DCOM) eingeführt. Insbesondere führen Sie präziseere Rechte ein, die einem Administrator eine unabhängige Kontrolle über lokale und Remote Berechtigungen zum Starten, aktivieren und Zugreifen auf com-Server ermöglichen.

## <a name="what-does-dcom-do"></a>Was macht DCOM?

Das Microsoft Component Object Model (com) ist ein plattformunabhängiges, verteiltes, objektorientiertes System zum Erstellen von binären Softwarekomponenten, die interagieren können. Mit dem verteilten Component Object Model (DCOM) können Anwendungen Zwischenstand Orten verteilt werden, die für Sie und die Anwendung am sinnvollsten sind. Das DCOM-Wire-Protokoll bietet transparente Unterstützung für die zuverlässige, sichere und effiziente Kommunikation zwischen COM-Komponenten.

## <a name="who-does-this-feature-apply-to"></a>An welche Benutzer richtet sich Distributed Transaction Coordinator?

Wenn Sie com nur für Prozess interne com-Komponenten verwenden, gilt diese Funktion nicht für Sie.

Diese Funktion gilt für Sie, wenn Sie über eine COM-Serveranwendung verfügen, die eines der folgenden Kriterien erfüllt:

-   Die Zugriffsberechtigung für die Anwendung ist weniger streng als die Launch-Berechtigung, die zum Ausführen der Anwendung erforderlich ist.
-   Die Anwendung wird normalerweise von einem com-Remote Client aktiviert, ohne dass ein Administrator Konto verwendet wird.
-   Die Anwendung soll nur lokal verwendet werden. Dies bedeutet, dass Sie die COM-Serveranwendung einschränken können, sodass Sie nicht Remote zugänglich ist.

## <a name="what-new-functionality-is-added-to-this-feature-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>Welche neuen Funktionen werden diesem Feature in Windows XP Service Pack 2 und Windows Server 2003 Service Pack 1 hinzugefügt?

### <a name="computer-wide-restrictions"></a>Computer weite Einschränkungen

In com wurde eine Änderung vorgenommen, um Computer weite Zugriffs Steuerungen bereitzustellen, die den Zugriff auf alle Aufrufe, Aktivierungs-oder Start Anforderungen auf dem Computer steuern. Die einfachste Möglichkeit, diese Zugriffs Steuerungen zu übernehmen, ist ein zusätzlicher [**Access Check**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) -Befehl, der mit einer Computer weiten Zugriffs Steuerungs Liste (ACL) bei jedem aufrufen, aktivieren oder Starten eines beliebigen COM-Servers auf dem Computer ausgeführt wird. Wenn **Access Check** fehlschlägt, wird die Anforderung, die Aktivierung oder die Start Anforderung verweigert. Dies gilt zusätzlich zu allen **Access Check** -Daten, die für die serverspezifischen ACLs ausgeführt werden. Tatsächlich stellt Sie einen minimal Autorisierungs Standard bereit, der für den Zugriff auf jeden com-Server auf dem Computer weitergegeben werden muss. Es gibt eine Computer weite ACL für Start Berechtigungen zum abdecken von Aktivierungs-und Start rechten sowie eine Computer weite Zugriffs Steuerungs Liste für Zugriffsberechtigungen zum abdecken von aufrufsrechten. Diese können über die Komponenten Dienste Microsoft Management Console (MMC) konfiguriert werden.

Diese Computer weiten Zugriffs Steuerungs Listen bieten eine Möglichkeit, schwache Sicherheitseinstellungen zu überschreiben, die von einer bestimmten Anwendung mithilfe von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) oder anwendungsspezifischen Sicherheitseinstellungen festgelegt wurden. Dies bietet einen minimalen Sicherheitsstandard, der unabhängig von den Einstellungen des jeweiligen Servers übermittelt werden muss.

Diese ACLs werden geprüft, wenn auf die Schnittstellen zugegriffen wird, die von RPCSS verfügbar gemacht werden. Dadurch wird eine Methode zum Steuern des Zugriffs auf diesen Systemdienst bereitstellt.

Diese ACLs bieten einen zentralen Ort, an dem ein Administrator allgemeine Autorisierungs Richtlinien festlegen kann, die für alle com-Server auf dem Computer gelten.

> [!Note]  
> Das Ändern der Computer weiten Sicherheitseinstellungen wirkt sich auf alle com-Server Anwendungen aus und verhindert möglicherweise, dass Sie ordnungsgemäß funktionieren. Wenn es com-Server Anwendungen gibt, die Einschränkungen aufweisen, die weniger streng sind als die Computer weiten Einschränkungen, werden diese Anwendungen durch das Reduzieren der Computer weiten Einschränkungen möglicherweise für unerwünschte Zugriffe zugänglich gemacht. Wenn Sie dagegen die Computer weiten Einschränkungen erhöhen, können einige com-Server Anwendungen nicht mehr durch das Aufrufen von Anwendungen aufgerufen werden.

 

Standardmäßig lauten Windows XP SP2-Computer Einschränkungs Einstellungen wie folgt:



| Berechtigung        | Administrator                                                                                             | Jeder                                            | Anonym               |
|-------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------|-------------------------|
| Starten<br/> | Lokaler Start<br/> Lokale Aktivierung<br/> Remotestart<br/> Remoteaktivierung<br/> | Lokaler Start<br/> Lokale Aktivierung<br/> |                         |
| Access<br/> |                                                                                                           | Lokaler Zugriff<br/> Remotezugriff<br/>    | Lokaler Zugriff<br/> |



 

Standardmäßig lauten Windows Server 2003 SP 1-Einstellungen für die Computer Einschränkung wie folgt.



| Berechtigung        | Administrator                                                                                             | Verteilte com-Benutzer (integrierte Gruppe)                                                                    | Jeder                                            | Anonym                                        |
|-------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------|
| Starten<br/> | Lokaler Start<br/> Lokale Aktivierung<br/> Remotestart<br/> Remoteaktivierung<br/> | Lokaler Start<br/> Lokale Aktivierung<br/> Remotestart<br/> Remoteaktivierung<br/> | Lokaler Start<br/> Lokale Aktivierung<br/> | –<br/>                                   |
| Access<br/> | –<br/>                                                                                            | Lokaler Zugriff<br/> Remotezugriff<br/>                                                          | Lokaler Zugriff<br/> Remotezugriff<br/>    | Lokaler Zugriff<br/> Remotezugriff<br/> |



 

> [!Note]  
> Verteilte com-Benutzer sind eine neue integrierte Gruppe, die in Windows Server 2003 SP1 enthalten ist, um das Hinzufügen von Benutzern zu den Einstellungen für die Einschränkung der DCOM-Computer zu beschleunigen. Diese Gruppe ist Teil der ACL, die von den Einstellungen [machineaccesseinschränkung](machineaccessrestriction.md) und [machinelauncheinschränkungs](machinelaunchrestriction.md) verwendet wird. das Entfernen von Benutzern aus dieser Gruppe wirkt sich daher auf diese Einstellungen aus.

 

### <a name="why-is-this-change-important-what-threats-does-it-help-mitigate"></a>Warum ist diese Änderung so wichtig? Welche Bedrohungen werden damit gemindert?

Viele com-Anwendungen enthalten Sicherheits spezifischen Code (z. b. den Aufruf von [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)), verwenden jedoch schwache Einstellungen und ermöglichen häufig nicht authentifizierten Zugriff auf den Prozess. Es gibt derzeit keine Möglichkeit für einen Administrator, diese Einstellungen zu überschreiben, um eine höhere Sicherheit in früheren Versionen von Windows zu erzwingen.

Die com-Infrastruktur umfasst das RPCSS, einen Systemdienst, der beim Systemstart ausgeführt wird und danach immer ausgeführt wird. Sie verwaltet die Aktivierung von COM-Objekten und der ausgelaufenden Objekttabelle und stellt Hilfsdienste für DCOM-Remoting bereit. Er macht RPC-Schnittstellen verfügbar, die remote aufgerufen werden können. Da einige com-Server nicht authentifizierten Remote Zugriff zulassen, können diese Schnittstellen von beliebigen Benutzern, einschließlich nicht authentifizierter Benutzer, aufgerufen werden. Folglich kann RPCSS von böswilligen Benutzern auf nicht authentifizierten Remote Computern angegriffen werden.

In früheren Versionen von Windows gab es für einen Administrator keine Möglichkeit, die Integritätsebene der com-Server auf einem Computer zu verstehen. Ein Administrator hat eine Idee des Expositionsniveaus erhalten, indem er systematisch die konfigurierten Sicherheitseinstellungen für alle registrierten COM-Anwendungen auf dem Computer prüft, aber da in einer Standardinstallation von Windows ungefähr 150 com-Server vorhanden sind, war dieser Task beängstigend. Es gab keine Möglichkeit, die Einstellungen für einen Server anzuzeigen, der Sicherheit in der Software umfasst, kurz bevor der Quellcode für diese Software überprüft wird.

Durch DCOM-Computer weite Einschränkungen werden diese drei Probleme minimiert. Außerdem bietet der Administrator die Möglichkeit, eingehende DCOM-Aktivierung,-Starts und-Aufrufe zu deaktivieren.

### <a name="what-works-differently"></a>Worin bestehen die Unterschiede?

Standardmäßig werden der Gruppe jeder die Berechtigungen Local Launch, local Activation und Local Access callerteilt. Dadurch können alle lokalen Szenarien ohne Änderung an der Software oder dem Betriebssystem funktionieren.

Standardmäßig werden in Windows XP SP2 der Gruppe jeder die Berechtigungen für den Remote Zugriff aufgerufen. In Windows Server 2003 SP1 werden den Gruppen "jeder" und "Anonymous" Remote Zugriffsberechtigungen erteilt. Dies ermöglicht die meisten com-Client Szenarien, einschließlich des häufigen Falls, bei dem ein com-Client einen lokalen Verweis an einen Remote Server übergibt, wodurch der Client auf einen Server verwandelt wird. In Windows XP SP2 können dadurch Szenarios deaktiviert werden, die nicht authentifizierte Remote Zugriffs Aufrufe erfordern.

Standardmäßig werden nur Mitgliedern der Gruppe "Administratoren" Berechtigungen zum Remote Aktivierungs-und Start Zugriff erteilt. Hierdurch werden Remote Aktivierungen durch nicht Administratoren für die Installation von com-Servern deaktiviert.

### <a name="how-do-i-resolve-these-issues"></a>Gewusst wie diese Probleme beheben?

Wenn Sie einen com-Server implementieren und davon ausgehen, dass die Remote Aktivierung durch einen nicht administrativen com-Client unterstützt wird, sollten Sie in Erwägung ziehen, ob das mit dem Aktivieren dieses Prozesses verbundene Risiko akzeptabel ist oder ob Sie die Implementierung so ändern müssen, dass keine Remote Aktivierung durch einen nicht administrativen com-Client oder Remote-nicht authentifizierte Aufrufe erforderlich ist.

Wenn das Risiko akzeptabel ist und Sie die Remote Aktivierung durch einen nicht administrativen com-Client oder Remote-nicht authentifizierte Aufrufe aktivieren möchten, müssen Sie die Standardkonfiguration für dieses Feature ändern.

> [!Note]  
> Das Ändern der Computer weiten Sicherheitseinstellungen wirkt sich auf alle com-Server Anwendungen aus und verhindert möglicherweise, dass Sie ordnungsgemäß funktionieren. Wenn es com-Server Anwendungen gibt, die Einschränkungen aufweisen, die weniger streng sind als die Computer weiten Einschränkungen, können diese Anwendungen durch eine Reduzierung der Computer weiten Einschränkungen für unerwünschte Zugriffe zugänglich gemacht werden. Wenn Sie dagegen die Computer weiten Einschränkungen erhöhen, können einige com-Server Anwendungen nicht mehr durch das Aufrufen von Anwendungen aufgerufen werden.

 

Sie können die Konfigurationseinstellungen entweder mit den Komponenten Diensten Microsoft Management Console (MMC) oder der Windows-Registrierung ändern.

Wenn Sie das MMC-Snap-in "Komponenten Dienste" verwenden, können diese Einstellungen auf der Registerkarte **com-Sicherheit** im Dialogfeld **Eigenschaften** für den Computer, den Sie verwalten, konfiguriert werden. Der Bereich **Zugriffsberechtigungen** wurde geändert, damit Sie zusätzlich zu den standardmäßigen Standardeinstellungen für com-Server Computer weite Grenzen festlegen können. Darüber hinaus können Sie separate ACL-Einstellungen für lokalen und Remote Zugriff unter Grenzwerte und Standardeinstellungen bereitstellen.

Im Bereich **Start-und Aktivierungs Berechtigungen** können Sie die lokalen und Remote Berechtigungen sowie die Computer weiten Grenzwerte und die Standardwerte steuern. Sie können sowohl lokale als auch Remote Aktivierung und Start Berechtigungen unabhängig voneinander angeben.

Alternativ können Sie diese ACL-Einstellungen mithilfe der Registrierung konfigurieren.

Diese ACLs werden in der Registrierung an den folgenden Speicherorten gespeichert:

``` syntax
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole\MachineAccessRestriction=ACL
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole\MachineLaunchRestriction=ACL
```

Dabei handelt es sich um benannte Werte vom Typ "reg \_ Binary", die Daten enthalten, die die ACL der Prinzipale beschreiben, die auf beliebige com-Klassen oder COM-Objekte auf dem Computer zugreifen können. Die Zugriffsrechte in der ACL lauten:

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

Diese ACLs können mit normalen Sicherheitsfunktionen erstellt werden.

> [!Note]  
> Um Abwärtskompatibilität zu gewährleisten, kann eine ACL in dem Format vorhanden sein, das vor Windows XP SP2 und Windows Server 2003 SP1 verwendet wurde. in der nur die Zugriffsrechte für com \_ \_ -Rechte ausführen verwendet werden, oder Sie können im neuen Format vorhanden sein, das in Windows XP SP2 und Windows Server 2003 SP1 verwendet wird, das com- \_ Rechte \_ zusammen mit einer Kombination aus com- \_ Rechten ausführen \_ \_ lokal, com- \_ Rechte \_ Execute \_ Remote, com \_ \_ -Rechte Aktivierung \_ lokal und com- \_ Rechte \_ Aktivierung Remote verwendet \_ . Beachten Sie, dass com- \_ Rechte \_ Execute> immer vorhanden sein müssen. das Fehlen dieses Rechts generiert eine ungültige Sicherheits Beschreibung. Beachten Sie außerdem, dass Sie das alte Format und das neue Format nicht innerhalb einer einzelnen ACL mischen dürfen. entweder müssen alle Zugriffs Steuerungs Einträge (ACEs) nur die com- \_ Rechte \_ Execute Access Right gewähren, oder Sie müssen alle com- \_ Rechte \_ mit einer Kombination aus com- \_ rechten Execute \_ \_ local, com- \_ Rechte \_ Execute \_ Remote, com \_ \_ -Rechte lokal aktivieren \_ und com- \_ Rechte für \_ Remote Aktivierung gewähren \_ .

 

> [!Note]  
> Diese Einstellungen können nur von Benutzern mit Administrator Rechten geändert werden.

 

## <a name="what-existing-functionality-is-changing-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>Welche vorhandenen Funktionen ändern sich in Windows XP Service Pack 2 und Windows Server 2003 Service Pack 1?

### <a name="rpcss-runs-as-a-network-service"></a>RPCSS wird als Netzwerkdienst ausgeführt.

RPCSS ist ein Schlüsseldienst für die RPC-Endpunkt Zuordnung und die DCOM-Infrastruktur. Dieser Dienst wurde in früheren Versionen von Windows als lokales System ausgeführt. Um die Angriffsfläche von Fenstern zu verringern und eine gründliche Abwehr zu gewährleisten, wurde die RPCSS-Dienst Funktionalität in zwei Dienste aufgeteilt. Der RPCSS-Dienst mit sämtlicher ursprünglicher Funktionalität, die keine lokalen System Berechtigungen erforderte, wird jetzt unter dem Netzwerkdienst Konto ausgeführt. Ein neuer DCOMLAUNCH-Dienst, der Funktionen enthält, die lokale System Berechtigungen erfordern, wird unter dem Konto Lokales System ausgeführt.

### <a name="why-is-this-change-important"></a>Warum ist diese Änderung so wichtig?

Diese Änderung verringert die Angriffsfläche und bietet umfassende Schutzmaßnahmen für den RPCSS-Dienst, da eine Erhöhung der Berechtigungen im RPCSS-Dienst jetzt auf die Netzwerkdienst Berechtigung beschränkt ist.

### <a name="what-works-differently"></a>Worin bestehen die Unterschiede?

Diese Änderung sollte für Benutzer transparent sein, da die Kombination der Dienste RPCSS und DCOMLAUNCH dem vorherigen RPCSS-Dienst entspricht, der in früheren Versionen von Windows bereitgestellt wurde.

### <a name="more-specific-com-permissions"></a>Spezifischere com-Berechtigungen

COM-Server Anwendungen haben zwei Arten von Berechtigungen: Start Berechtigungen und Zugriffsberechtigungen. Start Berechtigungen steuern die Autorisierung zum Starten eines COM-Servers während der com-Aktivierung, wenn der Server nicht bereits ausgeführt wird. Diese Berechtigungen werden als Sicherheits Deskriptoren definiert, die in den Registrierungs Einstellungen angegeben werden. Zugriffsberechtigungen steuern die Autorisierung zum Aufrufen eines laufenden com-Servers. Diese Berechtigungen werden als Sicherheits Deskriptoren definiert, die der com-Infrastruktur über die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) -API oder mithilfe von Registrierungs Einstellungen bereitgestellt werden. Sowohl die Start-als auch die Zugriffsberechtigungen gewähren oder verweigern den Zugriff basierend auf Prinzipale und unterscheiden sich nicht, ob der Aufrufer lokal auf dem Server oder Remote ist.

Durch die erste Änderung werden die com-Zugriffsrechte basierend auf der Entfernung unterschieden. Die beiden definierten Entfernungen sind lokal und Remote. Eine lokale com-Nachricht wird über das lokale Protokoll für Remote Prozedur Aufrufe (Remote Procedure Aufruf, LRPC) empfangen, während eine Remote-com-Nachricht über ein RPC-Host Protokoll (Remote Procedure Aufruf) wie TCP (Transmission Control Protocol) eingeht.

Com-Aktivierung ist das Abrufen eines COM-Schnittstellen Proxys auf einem Client durch Aufrufen von [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) oder einer seiner Varianten. Als Nebeneffekt dieses Aktivierungs Vorgangs muss manchmal ein com-Server gestartet werden, um die Anforderung des Clients zu erfüllen. Eine Start Berechtigungs-ACL bestätigt, wer einen com-Server starten darf. Eine Zugriffs Berechtigungs-ACL bestätigt, wer ein COM-Objekt aktivieren oder dieses Objekt aufrufen kann, sobald der com-Server bereits ausgeführt wird.

Die zweite Änderung besteht darin, dass die Aufrufe und Aktivierungs Rechte getrennt sind, um zwei unterschiedliche Vorgänge widerzuspiegeln und die Aktivierung direkt von der Zugriffs Berechtigungs-ACL in die ACL für die Startberechtigung zu verschieben. Da sowohl die Aktivierung als auch das Starten mit dem Erwerb eines Schnittstellen Zeigers verknüpft sind, gehören Aktivierungs-und Start Zugriffsrechte logisch zu einer ACL. Und da Sie immer Start Berechtigungen über die Konfiguration angeben (im Vergleich zu Zugriffsberechtigungen, die oft Programm gesteuert angegeben werden), bietet der Administrator durch das Platzieren der Aktivierungs Rechte in der ACL für die Startberechtigung eine Kontrolle über die Aktivierung.

Die Zugriffs Steuerungs Einträge für die Startberechtigung (ACEs) werden in vier Zugriffsrechte unterteilt:

-   Lokaler Start (LL)
-   Remote Start (RL)
-   Lokale Aktivierung (La)
-   Remote Aktivierung (RA)

Der Sicherheits Deskriptor für die Zugriffsberechtigung wird in zwei Zugriffsrechte aufgeteilt:

-   Lokale Zugriffs Aufrufe (LC)
-   Remote Zugriffs Aufrufe (RC)

Dadurch kann der Administrator sehr spezifische Sicherheits Konfigurationen anwenden. Beispielsweise können Sie einen com-Server so konfigurieren, dass er lokale Zugriffs Aufrufe von allen akzeptiert, während Sie nur Remote Zugriffs Aufrufe von Administratoren akzeptieren. Diese Unterschiede können durch Änderungen an den Sicherheits Deskriptoren für COM-Berechtigungen angegeben werden.

### <a name="why-is-this-change-important-what-threats-does-it-help-mitigate"></a>Warum ist diese Änderung so wichtig? Welche Bedrohungen werden damit gemindert?

Frühere Versionen der COM-Serveranwendung haben keine Möglichkeit, eine Anwendung so einzuschränken, dass Sie nur lokal verwendet werden kann, ohne die Anwendung über DCOM im Netzwerk verfügbar zu machen. Wenn ein Benutzer Zugriff auf eine COM-Serveranwendung hat, haben Sie Zugriff auf lokale und Remote Verwendung.

Eine COM-Serveranwendung kann sich selbst für nicht authentifizierte Benutzer zur Implementierung eines com-Rückruf Szenarios verfügbar machen. In diesem Szenario muss die Anwendung ihre Aktivierung auch für nicht authentifizierte Benutzer verfügbar machen, was möglicherweise nicht wünschenswert ist.

Präzise com-Berechtigungen bieten dem Administrator Flexibilität, die com-Berechtigungs Richtlinie eines Computers zu steuern. Diese Berechtigungen ermöglichen die Sicherheit für die beschriebenen Szenarien.

### <a name="what-works-differently-are-there-any-dependencies"></a>Worin bestehen die Unterschiede? Gibt es Abhängigkeiten?

Zum Bereitstellen der Abwärtskompatibilität werden vorhandene com-Sicherheits Deskriptoren so interpretiert, dass sowohl der lokale als auch der Remote Zugriff gleichzeitig zugelassen oder verweigert werden. Das heißt, ein Zugriffs Steuerungs Eintrag (ACE) erlaubt sowohl lokale als auch Remote oder verweigert sowohl lokale als auch Remote.

Es sind keine abwärts Kompatibilitätsprobleme für die Berechtigungen zum Aufrufen oder starten aufgetreten. Es gibt jedoch ein Problem mit der Kompatibilität der Aktivierungs Rechte. Wenn die konfigurierten Start Berechtigungen in den vorhandenen Sicherheits Beschreibungen für einen com-Server restriktiver sind als die Zugriffsberechtigungen und restriktiver sind, als für Client Aktivierungs Szenarien minimal erforderlich sind, muss die Start Berechtigungs-ACL geändert werden, um den autorisierten Clients die entsprechenden Aktivierungs Berechtigungen zu geben.

Bei com-Anwendungen, die die Standard Sicherheitseinstellungen verwenden, sind keine Kompatibilitätsprobleme aufgetreten. Bei Anwendungen, die mit der com-Aktivierung dynamisch gestartet werden, haben die meisten keine Kompatibilitätsprobleme, da die Start Berechtigungen bereits alle Personen einschließen müssen, die ein Objekt aktivieren können. Andernfalls generieren solche Anwendungen Aktivierungs Fehler, auch vor der Anwendung von Windows XP SP2 oder Windows Server 2003 SP1, wenn Aufrufer ohne Startberechtigung versuchen, ein Objekt zu aktivieren, und der com-Server nicht bereits ausgeführt wird.

Die Anwendungen, die für Kompatibilitätsprobleme am meisten von Interesse sind, sind com-Anwendungen, die bereits von einem anderen Mechanismus gestartet werden, z. b. Windows-Explorer oder Service Control Manager. Sie können diese Anwendungen auch durch eine vorherige com-Aktivierung starten, die die standardmäßigen Zugriffs-und Start Berechtigungen überschreibt und Start Berechtigungen angibt, die restriktiver sind als die aufrufen Berechtigungen. Weitere Informationen zum Beheben dieses Kompatibilitäts Problems finden Sie unter "Gewusst wie lösen Sie diese Probleme?". im nächsten Abschnitt.

Wenn ein System, das auf Windows XP SP2 oder Windows Server 2003 SP1 aktualisiert wird, auf einen früheren Status zurückgesetzt wird, wird jeder ACE, der so bearbeitet wurde, dass er lokalen Zugriff, Remote Zugriff oder beides ermöglicht, so interpretiert, dass sowohl der lokale als auch der Remote Zugriff zugelassen werden. Jeder ACE, der zum Verweigern von lokalem Zugriff, Remote Zugriff oder beides bearbeitet wurde, wird so interpretiert, dass sowohl der lokale als auch der Remote Zugriff verweigert werden. Wenn Sie eine Service Pack deinstallieren, sollten Sie sicherstellen, dass keine neuen ACEs dazu führen, dass Anwendungen nicht mehr funktionieren.

### <a name="how-do-i-resolve-these-issues"></a>Gewusst wie diese Probleme beheben?

Wenn Sie einen com-Server implementieren und die Standard Sicherheitseinstellungen außer Kraft setzen, vergewissern Sie sich, dass die anwendungsspezifische ACL für die Start Berechtigungen die Aktivierungs Berechtigung für entsprechende Benutzer erteilt. Wenn dies nicht der Fall ist, müssen Sie die anwendungsspezifische ACL für die Startberechtigung ändern, um den entsprechenden Benutzern Aktivierungs Rechte zu erteilen, damit Anwendungen und Windows-Komponenten, die DCOM verwenden, nicht ausfallen. Diese anwendungsspezifischen Start Berechtigungen werden in der Registrierung gespeichert.

Die com-ACLs können mit normalen Sicherheitsfunktionen erstellt oder geändert werden.

## <a name="what-settings-are-added-or-changed-in-windows-xp-service-pack-2"></a>Welche Einstellungen werden in Windows XP Service Pack 2 hinzugefügt oder geändert?

> [!Caution]  
> Eine falsche Verwendung dieser Einstellungen kann dazu führen, dass Anwendungen und Windows-Komponenten, die DCOM verwenden, fehlschlagen.

 

In der folgenden Tabelle werden diese Abkürzungen verwendet:

LL-lokaler Start

Lokale Aktivierung (La)

RL-Remote Start

RA-Remote Aktivierung

LC-lokale Zugriffs Aufrufe

RC-Remote Zugriffs Aufrufe

ACL-Access Control Liste



| Name der Einstellung                                                                                         | Standort                                                                                                       | Vorheriger Standardwert                                                                                                                                                                     | Standardwert                                                                                                                                                                                                                                                                                                                                                             | Mögliche Werte                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MachineLaunchRestriction**<br/>                                                              | **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ OLE**<br/>                                                 | Jeder-ll, La, RL, RA<br/> Anonymous<br/> LL, La, RL, RA<br/> (Dies ist ein neuer Registrierungsschlüssel. Basierend auf dem vorhandenen Verhalten sind dies die effektiven Werte.)<br/> | Administrator: ll, La, RL, RA<br/>                                                                                                                                                                                                                                                                                                                                  | ACL<br/>                                                                                                                                                                                                               |
| **MachineAccessRestriction**<br/>                                                              | **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ OLE**<br/>                                                 | Alle-LC, RC<br/> Anonymous-LC, RC<br/> (Dies ist ein neuer Registrierungsschlüssel. Basierend auf dem vorhandenen Verhalten sind dies die effektiven Werte.)<br/>                            | Alle: LC, RC<br/> Anonym: LC<br/>                                                                                                                                                                                                                                                                                                                      | ACL<br/>                                                                                                                                                                                                               |
| **CallFailureLoggingLevel**<br/>                                                               | **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ OLE**<br/>                                                 | Nicht zutreffend<br/>                                                                                                                                                                 | Dieser Registrierungsschlüssel ist nicht vorhanden. ein fehlender Schlüssel oder Wert wird jedoch als 2 interpretiert.<br/> Dieses Ereignis wird standardmäßig nicht protokolliert. Wenn Sie diesen Wert auf 1 setzen, um die Protokollierung dieser Informationen zu starten, um die Problembehandlung zu erleichtern, achten Sie darauf, die Größe des Ereignis Protokolls zu überwachen, da es sich hierbei um ein Ereignis handelt, das eine große Anzahl von Einträgen generieren kann.<br/> | 1: protokolliert stets Ereignisprotokoll Fehler während eines Aufrufes im com-Server Prozess.<br/> 2: protokolliert niemals Ereignisprotokoll Fehler während eines Aufrufes im Server Prozess.<br/>                                                  |
| **Invalidsecuritydescriptor LoggingLevel**<br/>                                                 | **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ OLE**<br/>                                                 | Nicht zutreffend<br/>                                                                                                                                                                 | Dieser Registrierungsschlüssel ist nicht vorhanden. ein fehlender Schlüssel oder Wert wird jedoch als 1 interpretiert.<br/> Dieses Ereignis wird standardmäßig protokolliert. Es sollte selten vorkommen.<br/>                                                                                                                                                                                                    | 1: protokolliert stets Ereignisprotokoll Fehler, wenn die com-Infrastruktur einen ungültigen Sicherheits Deskriptor findet.<br/> 2: protokolliert niemals Ereignisprotokoll Fehler, wenn die com-Infrastruktur eine ungültige Sicherheits Beschreibung findet.<br/> |
| DCOM: Computer Start Einschränkungen in der Security Descriptor Definition Language (SDDL)-Syntax<br/> | (Gruppenrichtlinie Objekt) Computer Konfiguration \\ Windows-Einstellungen \\ lokale Richtlinien \\ Sicherheitsoptionen<br/>  | Nicht zutreffend<br/>                                                                                                                                                                 | Nicht definiert<br/>                                                                                                                                                                                                                                                                                                                                                    | Zugriffs Steuerungs Liste im SDDL-Format. Das vorhanden sein dieser Richtlinie überschreibt Werte in machinelauncheinschränkungs, bisher.<br/>                                                                                            |
| DCOM: Computer Zugriffs Einschränkungen in SDDL-Syntax (Security Descriptor Definition Language)<br/> | (Gruppenrichtlinie Objekt) Computer Konfiguration \\ Windows-Einstellungen \\ lokale Richtlinien \\ Sicherheitsoptionen<br/> | Nicht zutreffend<br/>                                                                                                                                                                 | Nicht definiert<br/>                                                                                                                                                                                                                                                                                                                                                    | Zugriffs Steuerungs Liste im SDDL-Format. Das vorhanden sein dieser Richtlinie überschreibt Werte in machineaccesseinschränkung, bisher.<br/>                                                                                            |



 

## <a name="what-settings-are-added-or-changed-in-windows-server-2003-service-pack-1"></a>Welche Einstellungen werden in Windows Server 2003 Service Pack 1 hinzugefügt oder geändert?

> [!Note]  
> Eine falsche Verwendung dieser Einstellungen kann dazu führen, dass Anwendungen und Windows-Komponenten, die DCOM verwenden, fehlschlagen.

 

In der folgenden Tabelle werden diese Abkürzungen verwendet:

LL-lokaler Start

Lokale Aktivierung (La)

RL-Remote Start

RA-Remote Aktivierung

LC-lokale Zugriffs Aufrufe

RC-Remote Zugriffs Aufrufe

ACL-Access Control Liste



| Name der Einstellung                                                                                         | Standort                                                                                                       | Vorheriger Standardwert                                                                                                                                                             | Standardwert                                                                                                                                                                                                                                                                                                                                                             | Mögliche Werte                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MachineLaunchRestriction**<br/>                                                              | **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ OLE**<br/>                                                 | Jeder: ll, La, RL, RA<br/> Anonym: ll, La, RL, RA<br/> (Dies ist ein neuer Registrierungsschlüssel. Basierend auf dem vorhandenen Verhalten wären dies die effektiven Werte.)<br/> | Administrator: ll, La, RL, RA<br/> Jeder: ll, La<br/> Verteilte com-Benutzer: ll, La, RL, RA<br/>                                                                                                                                                                                                                                                     | ACL<br/>                                                                                                                                                                                                               |
| **MachineAccessRestriction**<br/>                                                              | **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ OLE**<br/>                                                 | Alle: LC, RC<br/> Anonym: LC, RC<br/> (Dies ist ein neuer Registrierungsschlüssel. Basierend auf dem vorhandenen Verhalten wären dies die effektiven Werte.)<br/>                 | Alle: LC, RC<br/> Anonym: LC, RC<br/>                                                                                                                                                                                                                                                                                                                  | ACL<br/>                                                                                                                                                                                                               |
| **CallFailureLoggingLevel**<br/>                                                               | **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ OLE**<br/>                                                 | Nicht zutreffend<br/>                                                                                                                                                         | Dieser Registrierungsschlüssel ist nicht vorhanden. ein fehlender Schlüssel oder Wert wird jedoch als 2 interpretiert.<br/> Dieses Ereignis wird standardmäßig nicht protokolliert. Wenn Sie diesen Wert auf 1 setzen, um die Protokollierung dieser Informationen zu starten, um die Problembehandlung zu erleichtern, achten Sie darauf, die Größe des Ereignis Protokolls zu überwachen, da es sich hierbei um ein Ereignis handelt, das eine große Anzahl von Einträgen generieren kann.<br/> | 1: protokolliert stets Ereignisprotokoll Fehler, wenn die com-Infrastruktur einen ungültigen Sicherheits Deskriptor findet.<br/> 2: protokolliert niemals Ereignisprotokoll Fehler, wenn die com-Infrastruktur eine ungültige Sicherheits Beschreibung findet.<br/> |
| **Invalidsecuritydescriptor LoggingLevel**<br/>                                                 | **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ OLE**<br/>                                                 | Nicht zutreffend<br/>                                                                                                                                                         | Dieser Registrierungsschlüssel ist nicht vorhanden. ein fehlender Schlüssel oder Wert wird jedoch als 1 interpretiert.<br/> Dieses Ereignis wird standardmäßig protokolliert. Es sollte selten vorkommen.<br/>                                                                                                                                                                                                    | 1: protokolliert stets Ereignisprotokoll Fehler, wenn die com-Infrastruktur eine ungültige Sicherheits Beschreibung findet.<br/> 2: protokolliert niemals Ereignisprotokoll Fehler, wenn die com-Infrastruktur eine ungültige Sicherheits Beschreibung findet.<br/>         |
| DCOM: Computer Start Einschränkungen in der Security Descriptor Definition Language (SDDL)-Syntax<br/> | (Gruppenrichtlinie Objekt) Computer Konfiguration \\ Windows-Einstellungen \\ lokale Richtlinien \\ Sicherheitsoptionen<br/> | Nicht zutreffend<br/>                                                                                                                                                         | Nicht definiert.<br/>                                                                                                                                                                                                                                                                                                                                                   | Zugriffs Steuerungs Liste im SDDL-Format. Das vorhanden sein dieser Richtlinie überschreibt Werte in machinelauncheinschränkungs, bisher.<br/>                                                                                            |
| DCOM: Computer Zugriffs Einschränkungen in SDDL-Syntax (Security Descriptor Definition Language)<br/> | (Gruppenrichtlinie Objekt) Computer Konfiguration \\ Windows-Einstellungen \\ lokale Richtlinien \\ Sicherheitsoptionen<br/> | Nicht zutreffend<br/>                                                                                                                                                         | Nicht definiert.<br/>                                                                                                                                                                                                                                                                                                                                                   | Zugriffs Steuerungs Liste im SDDL-Format. Das vorhanden sein dieser Richtlinie überschreibt Werte in machineaccesseinschränkung, bisher.<br/>                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheit in com](security-in-com.md)
</dt> </dl>

 

