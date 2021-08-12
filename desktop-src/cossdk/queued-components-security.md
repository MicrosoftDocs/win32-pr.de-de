---
description: Sicherheit von Komponenten in der Warteschlange
ms.assetid: 3fbeb81a-e3e4-495b-b891-896877fab92f
title: Sicherheit von Komponenten in der Warteschlange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682a9b409df2f605c259a6af6741dcc6e59d9fc23852b950a13225b24386c010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547082"
---
# <a name="queued-components-security"></a>Sicherheit von Komponenten in der Warteschlange

Wenn ein Client einen Methodenaufruf an ein Objekt in der Warteschlange vornimmt, erfolgt der Aufruf tatsächlich an den Aufzeichnungsserver, der ihn als Teil einer Nachricht an den Server packt. Der Listener liest die Nachricht aus der Warteschlange und übergibt sie an den Player. Der Player ruft die tatsächliche Serverkomponente auf und ruft die gleiche Methode auf. Die Serverkomponente muss den Sicherheitsaufrufkontext des Clients (nicht den Sicherheitsaufrufkontext des Players) beobachten, wenn der Player den Methodenaufruf ausführt. Die Aufzeichnung marshallt den Sicherheitsaufrufkontext des Clients in die Nachricht, und der Player entmarshaliert sie auf dem Server, bevor er den Methodenaufruf vornimmt. Im Hinblick auf das Serverobjekt gibt es keinen Unterschied im Sicherheitskontext zwischen einem direkten Aufruf vom Client und einem indirekten Aufruf vom Player. Insbesondere werden die aufgerufenen Methoden mit den Berechtigungen des Absenders ausgeführt.

Eine COM+-Komponente in der Warteschlange unterstützt rollenbasierte Sicherheitssemantik genau wie andere Komponenten, die für die Verwendung mit COM+-Anwendungen erstellt wurden. Komponenten einer Anwendung in der Warteschlange können daher programmgesteuerte Schnittstellen verwenden, um die Rollenmitgliedschaft ihres Aufrufers ([**ISecurityCallContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole)) oder eines bestimmten Benutzers ([**ISecurityCallContext::IsUserInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-isuserinrole)) zu ermitteln. Es wird empfohlen, dass jede Komponente in der Warteschlange mit potenziellen Sicherheitsauswirkungen diese Schnittstellen verwendet, um die Anmeldeinformationen des Absenders explizit zu überprüfen.

Die Aufruferidentität ist die Identität, die einem Methodenaufruf zugeordnet ist. Die Aufruferidentität wird von der rollenbasierten Sicherheit verwendet und ist im Kontext des Sicherheitsaufrufs vorhanden. In Komponenten in der Warteschlange wird die Aufruferidentität als Daten in der Message Queuing Meldung dargestellt. Message Queuing authentifiziert die Absenderidentität der Nachricht. Wenn die Identität des Aufrufers und die Absenderidentität der Nachricht identisch sind, authentifiziert Message Queuing sowohl die Nachricht als auch den Aufrufer. Dies ist der übliche Fall.

> [!Note]  
> Com+-Komponenten in der Warteschlange unterstützen keine Identitätswechselsicherheit, die es einem Server ermöglicht, ein Zugriffstoken zu erhalten, das der Clientidentität entspricht, und es entweder zum Durchführen von Zugriffssteuerungsprüfungen oder zum Agieren im Clientsicherheitskontext zu verwenden.

 

Wenn der Aufrufer einer Komponente in der Warteschlange über einen Out-of-Process-Recorder mit der Komponente interagiert, können sich die Identitäten des Aufrufers und des Absenders der Nachricht (Aufzeichnung) unterscheiden. In diesem Fall überprüfen COM+-Komponenten in der Warteschlange, ob der Nachrichtensender Mitglied der Rolle "Vertrauenswürdiger QC-Benutzer" auf dem Server ist. Darüber hinaus erfordert die Out-of-Process-Aufzeichnung ein Authentifizierungszertifikat, da sie von Message Queuing authentifiziert wird.

Mitglieder der Rolle "Vertrauenswürdiger QC-Benutzer" dürfen eine beliebige Identität angeben. Dies bedeutet, dass ein böswilliges Mitglied einen Aufruf einer Komponente in der Warteschlange mit erhöhten Rechten ausführen kann. Daher wird empfohlen, die Anzahl solcher Benutzer auf ein absolutes Minimum zu beschränken.

Aufgrund des Risikos eines komplexen Angriffs, der mit einem Mechanismus verbunden ist, der die Identität über ein Netzwerk weitergibt, sowie des Risikos eines einfachen Denial-of-Service-Angriffs durch Überfluten der Warteschlangen mit nicht erstellbaren Anforderungen wird empfohlen, den COM+-Komponentendienst nur in einem Netzwerk von vertrauenswürdigen Hosts bereitzustellen, z. B.  in einem privaten Netzwerk oder einem virtuellen privaten Netzwerk oder hinter einer entsprechend konfigurierten Firewall.

COM+-Komponenten in der Warteschlange werden über DCOM ausgeführt, sodass Sie die Integrität und Vertraulichkeit von Methodenaufrufen in der Warteschlange schützen können, indem Sie auf der Registerkarte **Sicherheit** des **Eigenschaftenblatts** Ihrer Anwendung in der Warteschlange die Einstellung **Paketdatenschutz** als Einstellung für die **Authentifizierungsebene von Aufrufen** auswählen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Sicherheit](com--security.md)
</dt> <dt>

[Sicherheitseinschränkungen im Arbeitsgruppenmodus](security-limitations-in-workgroup-mode.md)
</dt> <dt>

[Angeben des Authentifizierungsprotokolls](specifying-the-authentication-protocol.md)
</dt> </dl>

 

 



