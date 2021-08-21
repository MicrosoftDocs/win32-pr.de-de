---
title: DCOM-Sicherheitsverbesserungen in Windows XP Service Pack 2 und Windows Server 2003 Service Pack 1
description: Windows Server XP Service Pack 2 (SP2) und Windows Server 2003 Service Pack 1 (SP1) führen erweiterte Standardsicherheitseinstellungen für distributed Component Object Model (DCOM) ein.
ms.assetid: 1917834c-5216-4ef3-a0c2-d8ca63cef53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d093186f3d0a028112248409b71e0d71ed084e15cc075a1aced7a589aa0733ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501330"
---
# <a name="dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>DCOM-Sicherheitsverbesserungen in Windows XP Service Pack 2 und Windows Server 2003 Service Pack 1

Windows Server XP Service Pack 2 (SP2) und Windows Server 2003 Service Pack 1 (SP1) führen erweiterte Standardsicherheitseinstellungen für distributed Component Object Model (DCOM) ein. Insbesondere führen sie präzisere Rechte ein, die es einem Administrator ermöglichen, unabhängige Kontrolle über lokale und Remoteberechtigungen zum Starten, Aktivieren und Zugreifen auf COM-Server zu haben.

## <a name="what-does-dcom-do"></a>Was macht DCOM?

Microsoft Component Object Model (COM) ist ein plattformunabhängiges, verteiltes, objektorientiertes System zum Erstellen binärer Softwarekomponenten, die interagieren können. DCOM (Distributed Component Object Model) ermöglicht die Verteilung von Anwendungen auf Standorte, die für Sie und die Anwendung am sinnvollsten sind. Das DCOM-Wire Protocol bietet transparent Unterstützung für eine zuverlässige, sichere und effiziente Kommunikation zwischen COM-Komponenten.

## <a name="who-does-this-feature-apply-to"></a>An welche Benutzer richtet sich Distributed Transaction Coordinator?

Wenn Sie COM nur für in-Process-COM-Komponenten verwenden, gilt dieses Feature nicht für Sie.

Dieses Feature gilt für Sie, wenn Sie über eine COM-Serveranwendung verfügen, die eines der folgenden Kriterien erfüllt:

-   Die Zugriffsberechtigung für die Anwendung ist weniger streng als die Startberechtigung, die zum Ausführen der Anwendung erforderlich ist.
-   Die Anwendung wird in der Regel ohne Administratorkonto von einem REMOTE-COM-Client aktiviert.
-   Die Anwendung soll nur lokal verwendet werden. Dies bedeutet, dass Sie Ihre COM-Serveranwendung so einschränken können, dass sie nicht remote zugänglich ist.

## <a name="what-new-functionality-is-added-to-this-feature-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>Welche neuen Funktionen werden diesem Feature in Windows XP Service Pack 2 und Windows Server 2003 Service Pack 1 hinzugefügt?

### <a name="computer-wide-restrictions"></a>Computerweite Einschränkungen

In COM wurde eine Änderung vorgenommen, um computerweite Zugriffssteuerungen zu bieten, die den Zugriff auf alle Aufruf-, Aktivierungs- oder Startanforderungen auf dem Computer steuern. Die einfachste Möglichkeit, sich diese Zugriffssteuerungen zu überlegen, ist ein zusätzlicher [**AccessCheck-Aufruf,**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) der für eine computerweite Zugriffssteuerungsliste (Access Control List, ACL) bei jedem Aufruf, jeder Aktivierung oder jedem Start eines COM-Servers auf dem Computer ausgeführt wird. Wenn **accessCheck fehlschlägt,** wird der Aufruf, die Aktivierung oder die Startanforderung verweigert. Dies gilt zusätzlich zu **allen AccessCheck-Kontrollkästchen,** die für die serverspezifischen ACLs ausgeführt werden. Tatsächlich stellt sie einen Minimalautorisierungsstandard zur Verfügung, der für den Zugriff auf einen com-Server auf dem Computer übergeben werden muss. Es gibt eine computerweite ACL für Startberechtigungen, um Aktivierungs- und Startrechte zu behandeln, und eine computerweite ACL für Zugriffsberechtigungen, um Aufrufrechte zu abdecken. Diese können über die Komponentendienste-Microsoft Management Console (MMC) konfiguriert werden.

Diese computerweiten ACLs bieten eine Möglichkeit, schwache Sicherheitseinstellungen außer Kraft zu setzen, die von einer bestimmten Anwendung über [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) oder anwendungsspezifische Sicherheitseinstellungen angegeben werden. Dies bietet einen Mindestsicherheitsstandard, der unabhängig von den Einstellungen des jeweiligen Servers übergeben werden muss.

Diese ACLs werden überprüft, wenn auf die von RPCSS verfügbar gemachten Schnittstellen zugegriffen wird. Dies stellt eine Methode zum Steuern des Zugriffs auf diesen Systemdienst zur Verfügung.

Diese ACLs bieten einen zentralen Speicherort, an dem ein Administrator eine allgemeine Autorisierungsrichtlinie festlegen kann, die für alle COM-Server auf dem Computer gilt.

> [!Note]  
> Das Ändern der computerweiten Sicherheitseinstellungen wirkt sich auf alle COM-Serveranwendungen aus und verhindert möglicherweise, dass sie ordnungsgemäß funktionieren. Wenn es COM-Serveranwendungen mit Einschränkungen gibt, die weniger streng sind als die computerweiten Einschränkungen, kann eine Reduzierung der computerweiten Einschränkungen dazu führen, dass diese Anwendungen unerwünschtem Zugriff unterliegen. Wenn Sie hingegen die computerweiten Einschränkungen erhöhen, kann auf einige COM-Serveranwendungen möglicherweise nicht mehr durch Aufrufen von Anwendungen zugegriffen werden.

 

Standardmäßig sind Windows XP SP2-Computereinschränkungseinstellungen:



| Berechtigung        | Administrator                                                                                             | allen Beteiligten                                            | Anonym               |
|-------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------|-------------------------|
| Starten<br/> | Lokaler Start<br/> Lokale Aktivierung<br/> Remotestart<br/> Remoteaktivierung<br/> | Lokaler Start<br/> Lokale Aktivierung<br/> |                         |
| Zugriff<br/> |                                                                                                           | Lokaler Zugriff<br/> Remotezugriff<br/>    | Lokaler Zugriff<br/> |



 

Standardmäßig lauten Windows Server 2003 SP 1-Computereinschränkungseinstellungen wie folgt.



| Berechtigung        | Administrator                                                                                             | Verteilte COM-Benutzer (integrierte Gruppe)                                                                    | allen Beteiligten                                            | Anonym                                        |
|-------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------|
| Starten<br/> | Lokaler Start<br/> Lokale Aktivierung<br/> Remotestart<br/> Remoteaktivierung<br/> | Lokaler Start<br/> Lokale Aktivierung<br/> Remotestart<br/> Remoteaktivierung<br/> | Lokaler Start<br/> Lokale Aktivierung<br/> | Nicht zutreffend<br/>                                   |
| Zugriff<br/> | Nicht zutreffend<br/>                                                                                            | Lokaler Zugriff<br/> Remotezugriff<br/>                                                          | Lokaler Zugriff<br/> Remotezugriff<br/>    | Lokaler Zugriff<br/> Remotezugriff<br/> |



 

> [!Note]  
> Distributed COM Users ist eine neue integrierte Gruppe, die in Windows Server 2003 SP1 enthalten ist, um das Hinzufügen von Benutzern zu den DCOM-Computereinschränkungseinstellungen zu beschleunigen. Diese Gruppe ist Teil der ACL, die von den [Einstellungen MachineAccessRestriction](machineaccessrestriction.md) und [MachineLaunchRestriction](machinelaunchrestriction.md) verwendet wird. Das Entfernen von Benutzern aus dieser Gruppe wirkt sich daher auf diese Einstellungen aus.

 

### <a name="why-is-this-change-important-what-threats-does-it-help-mitigate"></a>Warum ist diese Änderung so wichtig? Welche Bedrohungen werden damit gemindert?

Viele COM-Anwendungen enthalten sicherheitsspezifischen Code (z. B. den Aufruf von [**CoInitializeSecurity),**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)verwenden jedoch schwache Einstellungen, wodurch häufig nicht authentifizierter Zugriff auf den Prozess ermöglicht wird. Es gibt derzeit keine Möglichkeit für einen Administrator, diese Einstellungen außer Kraft zu setzen, um eine höhere Sicherheit in früheren Versionen von Windows.

Die COM-Infrastruktur umfasst RPCSS, einen Systemdienst, der während des Systemstarts ausgeführt wird und danach immer ausgeführt wird. Er verwaltet die Aktivierung von COM-Objekten und der ausgeführten Objekttabelle und stellt Hilfsdienste für DCOM-Remoting zur Verfügung. Er macht RPC-Schnittstellen verfügbar, die remote aufgerufen werden können. Da einige COM-Server nicht authentifizierten Remotezugriff zulassen, können diese Schnittstellen von jedem aufgerufen werden, einschließlich nicht authentifizierter Benutzer. Daher kann RPCSS von böswilligen Benutzern auf nicht authentifizierten Remotecomputern angegriffen werden.

In früheren Versionen von Windows gab es für einen Administrator keine Möglichkeit, die Gefährdungsstufe der COM-Server auf einem Computer zu verstehen. Ein Administrator hat sich einen Überblick über den Grad der Gefährdung gemacht, indem er systematisch die konfigurierten Sicherheitseinstellungen für alle registrierten COM-Anwendungen auf dem Computer überprüft hat. Da es jedoch ungefähr 150 COM-Server in einer Standardinstallation von Windows gibt, war diese Aufgabe entmutigend. Es gab keine Möglichkeit, die Einstellungen für einen Server, der die Sicherheit in die Software integriert, und nicht den Quellcode für diese Software zu überprüfen.

Diese drei Probleme werden durch computerweite DCOM-Einschränkungen entschärft. Außerdem erhalten Administratoren die Möglichkeit, eingehende DCOM-Aktivierung, -Start und -Aufrufe zu deaktivieren.

### <a name="what-works-differently"></a>Worin bestehen die Unterschiede?

Standardmäßig werden der Gruppe Jeder berechtigungen für den lokalen Start, die lokale Aktivierung und den lokalen Zugriff gewährt. Dadurch können alle lokalen Szenarien ohne Änderungen an der Software oder am Betriebssystem funktionieren.

Standardmäßig werden der Gruppe Jeder Windows XP SP2 Remotezugriffsaufrufberechtigungen erteilt. In Windows Server 2003 SP1 werden den Gruppen "Jeder" und "Anonym" Remotezugriffsberechtigungen erteilt. Dies ermöglicht die meisten COM-Clientszenarien, einschließlich des allgemeinen Falls, in dem ein COM-Client einen lokalen Verweis an einen Remoteserver übergibt und den Client in einen Server umschließt. In Windows XP SP2 können dadurch Szenarien deaktiviert werden, die nicht authentifizierte Remotezugriffsaufrufe erfordern.

Außerdem werden standardmäßig nur Mitgliedern der Gruppe Administratoren Remoteaktivierungs- und Startberechtigungen erteilt. Dadurch werden Remoteaktivierungen durch Nichtadministratoren für installierte COM-Server deaktiviert.

### <a name="how-do-i-resolve-these-issues"></a>Gewusst wie diese Probleme beheben?

Wenn Sie einen COM-Server implementieren und erwarten, dass die Remoteaktivierung durch einen nicht administrativen COM-Client unterstützt wird, sollten Sie berücksichtigen, ob das Risiko, das mit der Aktivierung dieses Prozesses verbunden ist, akzeptabel ist, oder ob Sie Ihre Implementierung so ändern sollten, dass keine Remoteaktivierung durch einen nicht administrativen COM-Client oder remote nicht authentifizierte Aufrufe erforderlich ist.

Wenn das Risiko akzeptabel ist und Sie die Remoteaktivierung durch einen nicht administrativen COM-Client oder nicht authentifizierte Remoteaufrufe aktivieren möchten, müssen Sie die Standardkonfiguration für dieses Feature ändern.

> [!Note]  
> Das Ändern der computerweiten Sicherheitseinstellungen wirkt sich auf alle COM-Serveranwendungen aus und verhindert möglicherweise, dass sie ordnungsgemäß funktionieren. Wenn ES COM-Serveranwendungen mit Einschränkungen gibt, die weniger streng sind als die computerweiten Einschränkungen, kann eine Reduzierung der computerweiten Einschränkungen zu unerwünschtem Zugriff für diese Anwendungen führen. Wenn Sie hingegen die computerweiten Einschränkungen erhöhen, kann auf einige COM-Serveranwendungen möglicherweise nicht mehr durch Aufrufen von Anwendungen zugegriffen werden.

 

Sie können die Konfigurationseinstellungen entweder mithilfe des Komponentendienste-Microsoft Management Console (MMC) oder der Windows ändern.

Wenn Sie das MMC-Snap-In für Komponentendienste verwenden, können diese  Einstellungen auf der Registerkarte **COM-Sicherheit** des Dialogfelds Eigenschaften für den Computer konfiguriert werden, den Sie verwalten. Der **Bereich Zugriffsberechtigungen** wurde geändert, damit Sie computerweite Grenzwerte zusätzlich zu den Standardeinstellungen für COM-Server festlegen können. Darüber hinaus können Sie separate ACL-Einstellungen für den lokalen und Remotezugriff sowohl unter den Grenzwerten als auch den Standardeinstellungen bereitstellen.

Im Bereich **Start- und** Aktivierungsberechtigungen können Sie die lokalen und Remoteberechtigungen sowie die computerweiten Grenzwerte und Die Standardwerte steuern. Sie können sowohl lokale als auch Remoteaktivierungs- und Startberechtigungen unabhängig voneinander angeben.

Alternativ können Sie diese ACL-Einstellungen mithilfe der Registrierung konfigurieren.

Diese ACLs werden in der Registrierung an den folgenden Speicherorten gespeichert:

``` syntax
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole\MachineAccessRestriction=ACL
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole\MachineLaunchRestriction=ACL
```

Hierbei handelt es sich um benannte Werte vom Typ REG BINARY, die Daten enthalten, die die Zugriffssteuerungsliste der Prinzipale beschreiben, die auf eine beliebige COM-Klasse oder ein COM-Objekt auf \_ dem Computer zugreifen können. Die Zugriffsrechte in der Zugriffssteuerungsliste sind:

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

Diese ACLs können mit normalen Sicherheitsfunktionen erstellt werden.

> [!Note]  
> Um Abwärtskompatibilität zu gewährleisten, kann eine Zugriffssteuerungsliste in dem Format vorhanden sein, das vor Windows XP SP2 und Windows Server 2003 SP1 verwendet wird, die nur das Zugriffsrecht COM RIGHTS EXECUTE verwendet, oder sie kann im neuen Format vorhanden sein, das in Windows XP SP2 und \_ Windows Server 2003 SP1 verwendet wird, das COM RIGHTS EXECUTE zusammen mit einer Kombination aus \_ COM RIGHTS EXECUTE \_ \_ \_ \_ \_ LOCAL, COM RIGHTS EXECUTE REMOTE, COM RIGHTS ACTIVATE LOCAL und \_ COM RIGHTS ACTIVATE REMOTE \_ \_ \_ \_ \_ \_ \_ \_ verwendet. Beachten Sie, dass COM RIGHTS EXECUTE> immer vorhanden sein muss. Wenn dieses Recht nicht vorhanden ist, wird ein \_ \_ ungültiger Sicherheitsdeskriptor generiert. Beachten Sie außerdem, dass Sie das alte format und das neue Format nicht in einer einzelnen ACL mischen dürfen. Entweder müssen alle Zugriffssteuerungseinträge (ACCESS Control Entries, ACEs) nur das COM RIGHTS EXECUTE-Zugriffsrecht gewähren, oder alle müssen COM RIGHTS EXECUTE zusammen mit einer Kombination aus \_ \_ COM RIGHTS EXECUTE \_ \_ \_ \_ \_ LOCAL, COM RIGHTS EXECUTE REMOTE, COM RIGHTS ACTIVATE LOCAL und \_ COM RIGHTS ACTIVATE \_ REMOTE \_ \_ \_ \_ \_ \_ \_ gewähren.

 

> [!Note]  
> Nur Benutzer mit Administratorrechten können diese Einstellungen ändern.

 

## <a name="what-existing-functionality-is-changing-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>Welche vorhandenen Funktionen ändern sich in Windows XP Service Pack 2 und Windows Server 2003 Service Pack 1?

### <a name="rpcss-runs-as-a-network-service"></a>RPCSS wird als Netzwerkdienst ausgeführt

RPCSS ist ein wichtiger Dienst für die RPC-Endpunktzuordnung und die DCOM-Infrastruktur. Dieser Dienst wurde in früheren Versionen von als lokales System Windows. Um die Angriffsfläche der Windows zu reduzieren und eine tiefgehende Verteidigung zu bieten, wurde die RPCSS-Dienstfunktionalität in zwei Dienste aufgeteilt. Der RPCSS-Dienst mit allen ursprünglichen Funktionen, für die keine lokalen Systemberechtigungen erforderlich waren, wird jetzt unter dem Netzwerkdienstkonto ausgeführt. Ein neuer DCOMLaunch-Dienst, der Funktionen enthält, die lokale Systemberechtigungen erfordern, wird unter dem Lokalen Systemkonto ausgeführt.

### <a name="why-is-this-change-important"></a>Warum ist diese Änderung so wichtig?

Durch diese Änderung wird die Angriffsfläche reduziert, und der RPCSS-Dienst wird tiefgehender Schutz bieten, da eine Rechteerweiterung im RPCSS-Dienst jetzt auf die Netzwerkdienstberechtigung beschränkt ist.

### <a name="what-works-differently"></a>Worin bestehen die Unterschiede?

Diese Änderung sollte für Benutzer transparent sein, da die Kombination der RPCSS- und DCOMLaunch-Dienste dem vorherigen RPCSS-Dienst entspricht, der in früheren Versionen von Windows.

### <a name="more-specific-com-permissions"></a>Spezifischere COM-Berechtigungen

COM-Serveranwendungen verfügen über zwei Arten von Berechtigungen: Startberechtigungen und Zugriffsberechtigungen. Startberechtigungen steuern die Autorisierung zum Starten eines COM-Servers während der COM-Aktivierung, wenn der Server noch nicht ausgeführt wird. Diese Berechtigungen werden als Sicherheitsdeskriptoren definiert, die in den Registrierungseinstellungen angegeben werden. Zugriffsberechtigungen steuern die Autorisierung zum Aufrufen eines ausgeführten COM-Servers. Diese Berechtigungen werden als Sicherheitsdeskriptoren definiert, die der COM-Infrastruktur über die [**CoInitializeSecurity-API**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) oder mithilfe von Registrierungseinstellungen bereitgestellt werden. Sowohl Start- als auch Zugriffsberechtigungen ermöglichen oder verweigern den Zugriff basierend auf Prinzipals und machen keinen Unterschied, ob der Aufrufer lokal auf dem Server oder remote ist.

Die erste Änderung unterscheidet die COM-Zugriffsrechte basierend auf der Entfernung. Die beiden definierten Abstände sind Lokal und Remote. Eine lokale COM-Nachricht wird über das LRPC-Protokoll (Local Remote Procedure Call) empfangen, während eine Remote-COM-Nachricht über ein RPC-Hostprotokoll (Remote Procedure Call, Remoteprozeduraufruf) wie tcp (Transmission Control Protocol) eintrifft.

Com-Aktivierung ist das Abrufen eines COM-Schnittstellenproxys auf einem Client durch Aufrufen von [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) oder einer seiner Varianten. Als Nebeneffekt dieses Aktivierungsprozesses muss manchmal ein COM-Server gestartet werden, um die Clientanforderung zu erfüllen. Eine Startberechtigungs-ACL gibt an, wer einen COM-Server starten darf. Eine Zugriffsberechtigungs-ACL gibt an, wer ein COM-Objekt aktivieren oder aufrufen darf, sobald der COM-Server bereits ausgeführt wird.

Die zweite Änderung ist, dass die Aufruf- und Aktivierungsrechte so getrennt sind, dass sie zwei unterschiedliche Vorgänge widerspiegeln und die Aktivierung von der Zugriffsberechtigungs-ACL auf die Zugriffsberechtigungs-ACL verschieben. Da Aktivierung und Start beide mit dem Abrufen eines Schnittstellenzeigers verknüpft sind, gehören Aktivierungs- und Startzugriffsrechte logisch zu einer ACL zusammen. Und da Sie startberechtigungen immer über die Konfiguration angeben (im Vergleich zu Zugriffsberechtigungen, die häufig programmgesteuert angegeben werden), bietet das Festlegen der Aktivierungsrechte in der Zugriffsberechtigungs-ACL dem Administrator die Kontrolle über die Aktivierung.

Die Zugriffssteuerungseinträge für Startberechtigungen sind in vier Zugriffsrechte unterbrochen:

-   Lokaler Start (LL)
-   Remotestart (RL)
-   Lokale Aktivierung (LA)
-   Remote Activate (RA)

Der Sicherheitsdeskriptor für Zugriffsberechtigungen ist in zwei Zugriffsrechte aufgeteilt:

-   Aufrufe des lokalen Zugriffs (LOCAL Access Calls, LC)
-   Remotezugriffsaufrufe (RC)

Dadurch kann der Administrator sehr spezifische Sicherheitskonfigurationen anwenden. Beispielsweise können Sie einen COM-Server so konfigurieren, dass er lokale Zugriffsaufrufe von allen Akzeptiert, während nur Remotezugriffsaufrufe von Administratoren akzeptiert werden. Diese Unterschiede können durch Änderungen an den Sicherheitsdeskriptoren für COM-Berechtigungen angegeben werden.

### <a name="why-is-this-change-important-what-threats-does-it-help-mitigate"></a>Warum ist diese Änderung so wichtig? Welche Bedrohungen werden damit gemindert?

Frühere Versionen der COM-Serveranwendung haben keine Möglichkeit, eine Anwendung so einzuschränken, dass sie nur lokal verwendet werden kann, ohne die Anwendung über DCOM im Netzwerk verfügbar zu machen. Wenn ein Benutzer Zugriff auf eine COM-Serveranwendung hat, hat er Zugriff sowohl für die lokale als auch für die Remotenutzung.

Eine COM-Serveranwendung kann sich für nicht authentifizierte Benutzer zur Implementierung eines COM-Rückrufszenarios verfügbar machen. In diesem Szenario muss die Anwendung auch ihre Aktivierung für nicht authentifizierte Benutzer verfügbar machen, was möglicherweise nicht wünschenswert ist.

Präzise COM-Berechtigungen bieten dem Administrator die Flexibilität, die COM-Berechtigungsrichtlinie eines Computers zu steuern. Diese Berechtigungen ermöglichen die Sicherheit für die beschriebenen Szenarien.

### <a name="what-works-differently-are-there-any-dependencies"></a>Worin bestehen die Unterschiede? Gibt es Abhängigkeiten?

Um Abwärtskompatibilität zu gewährleisten, werden vorhandene COM-Sicherheitsdeskriptoren interpretiert, um sowohl lokalen als auch Remotezugriff gleichzeitig zu ermöglichen oder zu verweigern. Das heißt, ein ACE (Access Control Entry) lässt entweder sowohl lokale als auch Remotezugriff zu oder verweigert sowohl lokale als auch Remotezugriffe.

Es gibt keine Abwärtskompatibilitätsprobleme für Aufruf- oder Startrechte. Es besteht jedoch ein Problem mit der Kompatibilität von Aktivierungsrechten. Wenn die konfigurierten Startberechtigungen in den vorhandenen Sicherheitsbeschreibungen für einen COM-Server restriktiver als die Zugriffsberechtigungen sind und restriktiver sind als dies für Clientaktivierungsszenarien minimal erforderlich ist, muss die Zugriffssteuerungsliste für Startberechtigungen geändert werden, um den autorisierten Clients die entsprechenden Aktivierungsberechtigungen zu erteilen.

Für COM-Anwendungen, die die Standardsicherheitseinstellungen verwenden, gibt es keine Kompatibilitätsprobleme. Bei Anwendungen, die dynamisch mit der COM-Aktivierung gestartet werden, haben die meisten keine Kompatibilitätsprobleme, da die Startberechtigungen bereits alle Benutzer enthalten müssen, die ein Objekt aktivieren können. Andernfalls generieren solche Anwendungen Aktivierungsfehler, noch bevor sie Windows XP SP2 oder Windows Server 2003 SP1 anwenden, wenn Aufrufer ohne Startberechtigung versuchen, ein Objekt zu aktivieren, und der COM-Server nicht bereits ausgeführt wird.

Die Anwendungen, die bei Kompatibilitätsproblemen am wichtigsten sind, sind COM-Anwendungen, die bereits von einem anderen Mechanismus gestartet wurden, z. B. Windows Explorer oder Dienststeuerungs-Manager. Sie können diese Anwendungen auch durch eine vorherige COM-Aktivierung starten, die die Standardzugriffs- und Startberechtigungen außer Kraft setzt und Startberechtigungen angibt, die restriktiver als die Aufrufberechtigungen sind. Weitere Informationen zum Beheben dieses Kompatibilitätsproblems finden Sie unter "Gewusst wie beheben sie diese Probleme?" im nächsten Abschnitt.

Wenn für ein System, das auf Windows XP SP2 oder Windows Server 2003 SP1 aktualisiert wurde, ein Rollback auf einen früheren Zustand ausgeführt wird, wird jeder ACE, der bearbeitet wurde, um lokalen Zugriff, Remotezugriff oder beides zu ermöglichen, interpretiert, um sowohl lokalen als auch Remotezugriff zu ermöglichen. Jeder ACE, der bearbeitet wurde, um lokalen Zugriff, Remotezugriff oder beides zu verweigern, wird interpretiert, um sowohl lokalen als auch Remotezugriff zu verweigern. Wenn Sie ein Service Pack deinstallieren, sollten Sie sicherstellen, dass keine neu festgelegten ACEs dazu führen, dass Anwendungen nicht mehr funktionieren.

### <a name="how-do-i-resolve-these-issues"></a>Gewusst wie diese Probleme beheben?

Wenn Sie einen COM-Server implementieren und die Standardsicherheitseinstellungen außer Kraft setzen, vergewissern Sie sich, dass die anwendungsspezifische Zugriffssteuerungsliste den entsprechenden Benutzern Aktivierungsberechtigungen erteilt. Wenn dies nicht der Fehler ist, müssen Sie die anwendungsspezifische Zugriffsberechtigungs-ACL ändern, um den entsprechenden Benutzern Aktivierungsrechte zu erteilen, damit Anwendungen und Windows-Komponenten, die DCOM verwenden, nicht fehlschlagen. Diese anwendungsspezifischen Startberechtigungen werden in der Registrierung gespeichert.

Die COM-ACLs können mithilfe normaler Sicherheitsfunktionen erstellt oder geändert werden.

## <a name="what-settings-are-added-or-changed-in-windows-xp-service-pack-2"></a>Welche Einstellungen werden in XP Service Pack 2 Windows oder geändert?

> [!Caution]  
> Eine nicht ordnungsgemäße Verwendung dieser Einstellungen kann dazu führen, dass Anwendungen und Windows, die DCOM verwenden, fehlschlagen.

 

In der folgenden Tabelle werden diese Abkürzungen verwendet:

LL – Lokaler Start

LA – Lokale Aktivierung

RL – Remotestart

RA – Remoteaktivierung

LC – Aufrufe des lokalen Zugriffs

RC – Remotezugriffsaufrufe

ACL – Access Control Liste



| Name der Einstellung                                                                                         | Standort                                                                                                       | Vorheriger Standardwert                                                                                                                                                                     | Standardwert                                                                                                                                                                                                                                                                                                                                                             | Mögliche Werte                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MachineLaunchRestriction**<br/>                                                              | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | Jeder – LL, LA, RL, RA<br/> Anonym:<br/> LL, LA, RL, RA<br/> (Dies ist ein neuer Registrierungsschlüssel. Basierend auf vorhandenem Verhalten sind dies die effektiven Werte.)<br/> | Administrator: LL, LA, RL, RA<br/>                                                                                                                                                                                                                                                                                                                                  | ACL<br/>                                                                                                                                                                                                               |
| **MachineAccessRestriction**<br/>                                                              | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | Jeder – LC, RC<br/> Anonym : LC, RC<br/> (Dies ist ein neuer Registrierungsschlüssel. Basierend auf vorhandenem Verhalten sind dies die effektiven Werte.)<br/>                            | Alle: LC, RC<br/> Anonym: LC<br/>                                                                                                                                                                                                                                                                                                                      | ACL<br/>                                                                                                                                                                                                               |
| **CallFailureLoggingLevel**<br/>                                                               | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | Nicht zutreffend<br/>                                                                                                                                                                 | Dieser Registrierungsschlüssel ist nicht vorhanden. Ein fehlender Schlüssel oder Wert wird jedoch als 2 interpretiert.<br/> Dieses Ereignis wird standardmäßig nicht protokolliert. Wenn Sie diesen Wert in 1 ändern, um mit der Protokollierung dieser Informationen zu beginnen, um ein Problem zu beheben, achten Sie darauf, die Größe Ihres Ereignisprotokolls zu überwachen, da dies ein Ereignis ist, das eine große Anzahl von Einträgen generieren kann.<br/> | 1 : Protokolliert immer Ereignisprotokollfehler während eines Aufrufs im COM-Serverprozess.<br/> 2 : Protokollieren Sie niemals Fehler im Ereignisprotokoll während eines Aufrufs im Aufrufserverprozess.<br/>                                                  |
| **InvalidSecurityDescriptorLoggingLevel**<br/>                                                 | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | Nicht zutreffend<br/>                                                                                                                                                                 | Dieser Registrierungsschlüssel ist nicht vorhanden. Ein fehlender Schlüssel oder Wert wird jedoch als 1 interpretiert.<br/> Dieses Ereignis wird standardmäßig protokolliert. Dies sollte selten vorkommen.<br/>                                                                                                                                                                                                    | 1 : Protokolliert immer Ereignisprotokollfehler, wenn die COM-Infrastruktur einen ungültigen Sicherheitsdeskriptor findet.<br/> 2 : Protokollieren Sie niemals Ereignisprotokollfehler, wenn die COM-Infrastruktur einen ungültigen Sicherheitsdeskriptor findet.<br/> |
| DCOM:Machine Launch Restrictions in Security Descriptor Definition Language (SDDL)-Syntax<br/> | (Gruppenrichtlinie-Objekt) Computerkonfiguration \\ Windows Einstellungen \\ Sicherheitsoptionen für lokale \\ Richtlinien<br/>  | Nicht zutreffend<br/>                                                                                                                                                                 | Nicht definiert<br/>                                                                                                                                                                                                                                                                                                                                                    | Zugriffssteuerungsliste im SDDL-Format. Das Vorhandensein dieser Richtlinie überschreibt zuvor Werte in MachineLaunchRestriction.<br/>                                                                                            |
| DCOM:Machine Access Restrictions in Security Descriptor Definition Language (SDDL)-Syntax<br/> | (Gruppenrichtlinie-Objekt) Computerkonfiguration \\ Windows Einstellungen \\ Sicherheitsoptionen für lokale \\ Richtlinien<br/> | Nicht zutreffend<br/>                                                                                                                                                                 | Nicht definiert<br/>                                                                                                                                                                                                                                                                                                                                                    | Zugriffssteuerungsliste im SDDL-Format. Das Vorhandensein dieser Richtlinie überschreibt zuvor Werte in MachineAccessRestriction.<br/>                                                                                            |



 

## <a name="what-settings-are-added-or-changed-in-windows-server-2003-service-pack-1"></a>Welche Einstellungen werden in Windows Server 2003 Service Pack 1 hinzugefügt oder geändert?

> [!Note]  
> Eine nicht ordnungsgemäße Verwendung dieser Einstellungen kann dazu führen, dass Anwendungen und Windows, die DCOM verwenden, fehlschlagen.

 

In der folgenden Tabelle werden diese Abkürzungen verwendet:

LL – Lokaler Start

LA – Lokale Aktivierung

RL – Remotestart

RA – Remoteaktivierung

LC – Aufrufe des lokalen Zugriffs

RC – Remotezugriffsaufrufe

ACL – Access Control Liste



| Name der Einstellung                                                                                         | Standort                                                                                                       | Vorheriger Standardwert                                                                                                                                                             | Standardwert                                                                                                                                                                                                                                                                                                                                                             | Mögliche Werte                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MachineLaunchRestriction**<br/>                                                              | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | Jeder: LL, LA, RL, RA<br/> Anonym: LL, LA, RL, RA<br/> (Dies ist ein neuer Registrierungsschlüssel. Basierend auf dem vorhandenen Verhalten sind dies die effektiven Werte.)<br/> | Administrator: LL, LA, RL, RA<br/> Jeder: LL, LA<br/> Verteilte COM-Benutzer: LL, LA, RL, RA<br/>                                                                                                                                                                                                                                                     | ACL<br/>                                                                                                                                                                                                               |
| **MachineAccessRestriction**<br/>                                                              | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | Alle: LC, RC<br/> Anonym: LC, RC<br/> (Dies ist ein neuer Registrierungsschlüssel. Basierend auf dem vorhandenen Verhalten sind dies die effektiven Werte.)<br/>                 | Alle: LC, RC<br/> Anonym: LC, RC<br/>                                                                                                                                                                                                                                                                                                                  | ACL<br/>                                                                                                                                                                                                               |
| **CallFailureLoggingLevel**<br/>                                                               | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | Nicht zutreffend<br/>                                                                                                                                                         | Dieser Registrierungsschlüssel ist nicht vorhanden. Ein fehlender Schlüssel oder Wert wird jedoch als 2 interpretiert.<br/> Dieses Ereignis wird standardmäßig nicht protokolliert. Wenn Sie diesen Wert in 1 ändern, um mit der Protokollierung dieser Informationen zu beginnen, um ein Problem zu beheben, achten Sie darauf, die Größe Ihres Ereignisprotokolls zu überwachen, da dies ein Ereignis ist, das eine große Anzahl von Einträgen generieren kann.<br/> | 1 : Protokolliert immer Ereignisprotokollfehler, wenn die COM-Infrastruktur einen ungültigen Sicherheitsdeskriptor findet.<br/> 2 : Protokollieren Sie niemals Ereignisprotokollfehler, wenn die COM-Infrastruktur einen ungültigen Sicherheitsdeskriptor findet.<br/> |
| **InvalidSecurityDescriptorLoggingLevel**<br/>                                                 | **HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Ole**<br/>                                                 | Nicht zutreffend<br/>                                                                                                                                                         | Dieser Registrierungsschlüssel ist nicht vorhanden. Ein fehlender Schlüssel oder Wert wird jedoch als 1 interpretiert.<br/> Dieses Ereignis wird standardmäßig protokolliert. Dies sollte selten vorkommen.<br/>                                                                                                                                                                                                    | 1 : Protokollieren Sie immer Ereignisprotokollfehler, wenn die COM-Infrastruktur einen ungültigen Sicherheitsdeskriptor findet.<br/> 2: Protokollieren Sie niemals Fehler im Ereignisprotokoll, wenn die COM-Infrastruktur einen ungültigen Sicherheitsdeskriptor findet.<br/>         |
| DCOM:Machine Launch Restrictions in Security Descriptor Definition Language (SDDL)-Syntax<br/> | (Gruppenrichtlinie-Objekt) Computerkonfiguration \\ Windows Einstellungen \\ Sicherheitsoptionen für lokale \\ Richtlinien<br/> | Nicht zutreffend<br/>                                                                                                                                                         | Nicht definiert.<br/>                                                                                                                                                                                                                                                                                                                                                   | Zugriffssteuerungsliste im SDDL-Format. Das Vorhandensein dieser Richtlinie überschreibt zuvor Werte in MachineLaunchRestriction.<br/>                                                                                            |
| DCOM:Machine Access Restrictions in Security Descriptor Definition Language (SDDL)-Syntax<br/> | (Gruppenrichtlinie-Objekt) Computerkonfiguration \\ Windows Einstellungen \\ Sicherheitsoptionen für lokale \\ Richtlinien<br/> | Nicht zutreffend<br/>                                                                                                                                                         | Nicht definiert.<br/>                                                                                                                                                                                                                                                                                                                                                   | Zugriffssteuerungsliste im SDDL-Format. Das Vorhandensein dieser Richtlinie überschreibt zuvor Werte in MachineAccessRestriction.<br/>                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheit in COM](security-in-com.md)
</dt> </dl>

 

