---
description: Sicherheit für Warteschlangenkomponenten
ms.assetid: 3fbeb81a-e3e4-495b-b891-896877fab92f
title: Sicherheit für Warteschlangenkomponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682a9b409df2f605c259a6af6741dcc6e59d9fc23852b950a13225b24386c010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547082"
---
# <a name="queued-components-security"></a>Sicherheit für Warteschlangenkomponenten

Wenn ein Client einen Methodenaufruf an ein Objekt in der Warteschlange sendet, erfolgt der Aufruf tatsächlich an die Aufzeichnung, die sie als Teil einer Nachricht an den Server verpackt. Der Listener liest die Nachricht aus der Warteschlange und übergibt sie an den Player. Der Player ruft die tatsächliche Serverkomponente auf und ruft denselben Methodenaufruf ab. Die Serverkomponente muss den Sicherheitsaufrufkontext des Clients (nicht des Sicherheitsaufrufkontexts des Players) beobachten, wenn der Player den Methodenaufruf sendet. Die Aufzeichnung marshallt den Sicherheitsaufrufkontext des Clients in die Nachricht, und der Player entmarshalsiert ihn auf dem Server, bevor der Methodenaufruf ausgeführt wird. Im Zusammenhang mit dem Serverobjekt gibt es keinen Unterschied im Sicherheitskontext zwischen einem direkten Aufruf vom Client und einem indirekten Aufruf vom Player. Insbesondere werden die aufgerufenen Methoden mit den Berechtigungen des Absenders ausgeführt.

Eine COM+-Komponente in der Warteschlange unterstützt die rollenbasierte Sicherheitssemantik genau wie andere Komponenten, die für die Verwendung mit COM+-Anwendungen entwickelt wurden. Komponenten einer Anwendung in der Warteschlange können daher programmgesteuerte Schnittstellen verwenden, um die Rollenmitgliedschaft ihres Aufrufers ([**ISecurityCallContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole)) oder eines bestimmten Benutzers ([**ISecurityCallContext::IsUserInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-isuserinrole)) zu finden. Es wird empfohlen, dass alle Komponenten in der Warteschlange mit potenziellen Sicherheitsrisiken diese Schnittstellen verwenden, um die Anmeldeinformationen des Absenders explizit zu überprüfen.

Die Aufruferidentität ist die Identität, die einem Methodenaufruf zugeordnet ist. Die Identität des Aufrufers wird von der rollenbasierten Sicherheit verwendet und ist im Sicherheitsaufrufkontext vorhanden. In Komponenten in der Warteschlange wird die Identität des Aufrufers als Daten in der Message Queuing dargestellt. Message Queuing authentifiziert die Absenderidentität der Nachricht. Wenn die Identität des Aufrufers und die Absenderidentität der Nachricht identisch sind, Message Queuing sowohl die Nachricht als auch den Aufrufer authentifiziert. Dies ist der übliche Fall.

> [!Note]  
> COM+-Komponenten in der Warteschlange unterstützen keine Sicherheit im Identitätswechselstil, die es einem Server ermöglicht, ein Zugriffstoken abzurufen, das der Clientidentität entspricht, und es entweder zum Durchführen von Zugriffssteuerungsüberprüfungen oder zum Ausführen von Aktionen im Clientsicherheitskontext zu verwenden.

 

Wenn der Aufrufer einer Komponente in der Warteschlange über eine Out-of-Process-Aufzeichnung mit der Komponente interagiert, können die Identitäten des Aufrufers und des Nachrichtensenders (Recorder) unterschiedlich sein. In diesem Fall überprüfen COM+-Komponenten in der Warteschlange, ob der Absender der Nachricht Mitglied der QC-Rolle "Vertrauenswürdiger Benutzer" auf dem Server ist. Darüber hinaus erfordert die Out-of-Process-Aufzeichnung ein Authentifizierungszertifikat, da es von einem Message Queuing.

Mitglieder der QC-Rolle "Vertrauenswürdiger Benutzer" dürfen eine beliebige Identität angeben. Dies bedeutet, dass ein böswilliges Mitglied einen Aufruf einer Warteschlangenkomponente mit erhöhten Rechten ausführen kann. Daher wird empfohlen, die Anzahl solcher Benutzer auf ein absolutes Minimum zu beschränken.

Aufgrund des Risikos eines komplexen Angriffs, der mit jedem Mechanismus verbunden ist, der die Identität über ein Netzwerk verteilt, sowie des Risikos eines einfachen Denial-of-Service-Angriffs durch Überflutung der Warteschlangen mit nicht aussetzbaren Anforderungen wird empfohlen, den COM+-Dienst für Warteschlangenkomponenten nur in einem Netzwerk vertrauenswürdiger Hosts bereitzustellen, z. B.  in einem privaten Netzwerk oder einem virtuellen privaten Netzwerk oder hinter einer entsprechend konfigurierten Firewall.

COM+-Komponenten in der Warteschlange werden über DCOM ausgeführt, sodass Sie die  Integrität und Vertraulichkeit von Methodenaufrufen in der Warteschlange schützen  können, indem Sie auf der Registerkarte Sicherheit auf dem Eigenschaftenblatt Ihrer Warteschlangenanwendung die Einstellung Paketdatenschutz als Einstellung Authentifizierungsebene **von** Aufrufen auswählen. 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Sicherheit](com--security.md)
</dt> <dt>

[Sicherheitseinschränkungen im Arbeitsgruppenmodus](security-limitations-in-workgroup-mode.md)
</dt> <dt>

[Angeben des Authentifizierungsprotokolls](specifying-the-authentication-protocol.md)
</dt> </dl>

 

 



