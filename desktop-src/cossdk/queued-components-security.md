---
description: Sicherheit in der Warteschlange befindliche Komponenten
ms.assetid: 3fbeb81a-e3e4-495b-b891-896877fab92f
title: Sicherheit in der Warteschlange befindliche Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b51592f6216d7380e877f2cd582a277f1583b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127141"
---
# <a name="queued-components-security"></a>Sicherheit in der Warteschlange befindliche Komponenten

Wenn ein Client einen Methoden aufzurufen an ein Objekt in der Warteschlange sendet, wird der-Befehl tatsächlich an die Aufzeichnung gerichtet, die ihn als Teil einer Nachricht an den Server verpackt. Der Listener liest die Nachricht aus der Warteschlange und übergibt sie an den Player. Der Player Ruft die tatsächliche Serverkomponente auf und führt denselben Methodenaufruf aus. Die Serverkomponente muss den Sicherheitskontext des Clients (nicht den Sicherheits Aufrufkontext des Players) beobachten, wenn der Player den Methoden aufzurufen. Die Aufzeichnung Marshalls den Sicherheitskontext des Clients in die Nachricht, und der Player entmarshalls Sie auf dem Server, bevor Sie den Methoden aufzurufen. Wenn es um das Server Objekt geht, gibt es keinen Unterschied im Sicherheitskontext zwischen einem direkten-Client und einem indirekten-Rückruf des Players. Insbesondere die Methoden, die aufgerufen werden, werden mit den Berechtigungen des Absenders ausgeführt.

Eine in der Warteschlange befindliche COM+-Komponente unterstützt die rollenbasierte Sicherheits Semantik wie andere Komponenten, die für die Verwendung mit com+-Anwendungen erstellt wurden. Komponenten einer Anwendung in der Warteschlange können daher programmgesteuerte Schnittstellen verwenden, um die Rollen Mitgliedschaft Ihres Aufrufers ([**ISecurityCallContext:: isCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole)) oder einen bestimmten Benutzer ([**ISecurityCallContext:: IsUserInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-isuserinrole)) zu ermitteln. Es wird empfohlen, dass alle Komponenten in der Warteschlange mit einer potenziellen Sicherheits Auswirkung diese Schnittstellen verwenden, um die Anmelde Informationen des Absenders explizit zu überprüfen.

Die Identität des Aufrufers ist die Identität, die einem Methodenaufruf zugeordnet ist. Die Identität des Aufrufers wird von der rollenbasierten Sicherheit verwendet und ist im Sicherheits Aufruf Kontext vorhanden. In in der Warteschlange befindlichen Komponenten wird die Identität des Aufrufers als Daten in der Message Queuing Nachricht dargestellt. Message Queuing authentifiziert die Absender Identität der Nachricht. Wenn die Identität des Aufrufers und die Identität des Nachrichten Absenders identisch sind, werden Message Queuing die Nachricht und den Aufrufer authentifiziert. Dies ist der übliche Fall.

> [!Note]  
> Die in der Warteschlange befindlichen Komponenten von com+ unterstützen die Sicherheit im Identitätswechsel Format nicht, wodurch ein Server ein Zugriffs Token abrufen kann, das der Client Identität entspricht, und es entweder zum Durchführen von Zugriffs Steuerungs Prüfungen oder zum Verwenden des Client Sicherheits Kontexts verwenden.

 

Wenn der Aufrufer einer in der Warteschlange befindlichen Komponente über eine Out-of-Process-Aufzeichnung mit der Komponente interagiert, können sich die Identitäten des Aufrufers und der Nachrichten Absender (Recorder) unterscheiden. In diesem Fall überprüft com+ in der Warteschlange befindliche Komponenten, ob der Absender der Nachricht ein Mitglied der vertrauten QC-Benutzerrolle auf dem Server ist. Außerdem erfordert die Out-of-Process-Aufzeichnung ein Authentifizierungszertifikat, da Sie durch Message Queuing authentifiziert wird.

Mitglieder der Benutzerrolle "QC Trusted" können eine beliebige Identität angeben, was bedeutet, dass ein böswilliger Member einen in der Warteschlange befindlichen Komponenten aufrufmit erhöhten Rechten ausführen könnte. Daher wird empfohlen, dass die Anzahl der Benutzer auf ein absolutes Minimum beschränkt wird.

Aufgrund des Risikos eines anspruchsvollen Angriffs in Verbindung mit einem Mechanismus, der Identität über ein Netzwerk verteilt, und dem Risiko eines einfachen Denial-of-Service-Angriffs durch das überfluten der Warteschlangen mit nicht ausführbaren Anforderungen wird empfohlen, den com+-Dienst in der Warteschlange nur in einem Netzwerk vertrauenswürdiger Hosts bereitzustellen – beispielsweise in einem privaten Netzwerk oder einem virtuellen privaten Netzwerk. oder hinter einer entsprechend konfigurierten Firewall.

Die **in der Warte** Schlange befindlichen Komponenten von com+ werden über DCOM ausgeführt, sodass Sie die Integrität **und das Geheimnis** von Methoden aufrufen **in der** Warteschlange schützen können, indem Sie auf der Registerkarte Sicherheit auf der Registerkarte Sicherheit auf der Registerkarte Sicherheit auf der Registerkarte Sicherheit auf der Registerkarte **Sicherheit** die Einstellung

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-Sicherheit](com--security.md)
</dt> <dt>

[Sicherheitseinschränkungen im Arbeitsgruppen Modus](security-limitations-in-workgroup-mode.md)
</dt> <dt>

[Angeben des Authentifizierungs Protokolls](specifying-the-authentication-protocol.md)
</dt> </dl>

 

 



