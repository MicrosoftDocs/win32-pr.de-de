---
title: Übersicht über Änderungsnachverfolgung Techniken
description: Es gibt mehrere Möglichkeiten, wie sich Änderungs nach Verfolgungs Mechanismen auf den Gültigkeitsbereich für die Nachverfolgung von Änderungen unterscheiden können. eine Anwendung kann Änderungen an einem einzelnen Attribut eines einzelnen Objekts, an allen Objekten in einer Domäne usw. nachverfolgen.
ms.assetid: 7359e851-61b7-420d-beb0-f7f33f79b007
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91fce20dc5e9fe8fe98937bb13885be577185e04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036350"
---
# <a name="overview-of-change-tracking-techniques"></a>Übersicht über Änderungsnachverfolgung Techniken

Es gibt mehrere Möglichkeiten, wie sich Änderungs nach Verfolgungs Mechanismen unterscheiden können:

-   Bereich für die Nachverfolgung von Änderungen: eine Anwendung kann Änderungen an einem einzelnen Attribut eines einzelnen Objekts, an allen Objekten in einer Domäne usw. nachverfolgen. Wenn der Mechanismus den Anforderungen der Anwendung entspricht, erhält die Anwendung mindestens irrelevante Daten, wodurch sich die Leistung verbessert.
-   Aktualität: eine Anwendung wird bei jeder Änderung benachrichtigt, oder Sie kann über einen Zeitraum von Minuten oder Stunden über den Nettoeffekt von Änderungen benachrichtigt werden.

    Die Verarbeitung weniger zeitgemäßer Daten ist möglicherweise effizienter, da ggf. einige Änderungen reduziert werden. Wenn ein Attribut z. b. dreimal innerhalb eines Zeitraums von einer Stunde geändert wird, wird eine Anwendung, die über eine Stunde kumulierte Änderungen benachrichtigt wird, nur über eine Attribut Änderung benachrichtigt, nicht über drei.

    Beachten Sie bei der Betrachtung der Aktualität die Auswirkung der Replikations Latenz. Ein Update, das von einem Domänen Controller stammt, wird nicht sofort auf einen anderen Domänen Controller repliziert. Das Verlangen der Zeit, dass die Änderungs Nachverfolgung wesentlich besser ist als die erwartete Replikations Wartezeit, bietet der Anwendung häufig keinen echten Vorteil.

-   Abruf und Benachrichtigung: bei der Abfrage sendet eine Anwendung regelmäßig eine Anforderung an einen Domänen Controller, um Änderungs nach Verfolgungs Daten zu empfangen. Bei einer Benachrichtigung sendet der Domänen Controller Änderungen nur dann an die Anwendung, wenn Änderungen auftreten.

    Der Aufwand für den Abruf ist offensichtlich: die Anwendung kann Änderungs nach Verfolgungs Daten anfordern, wenn nichts signifikanter ist. Der Aufwand für die Benachrichtigung ist sehr gering. Der Server muss Daten zu Benachrichtigungs Anforderungen verwalten und muss diese Daten überprüfen, um zu entscheiden, ob eine Benachrichtigung gesendet werden soll. Dies kann zu normalen Aktualisierungs Anforderungen mehr Aufwand verursachen.

-   Ausdrücken des Wissens der Anwendung: persistent und temporär: jeder Mechanismus für die Änderungs Nachverfolgung muss eine Methode für den Server mit den verfolgten Daten enthalten, um den Zustand des Wissens der Anwendung zu verstehen, sodass die Vorstellung von "ändern" wohl definiert ist. Beispielsweise kann der Zustand der Anwendung als "aktualisiert mit allen Änderungen, die vor der Zeit t auf DC d aufgetreten sind" ausgedrückt werden. Ein Mechanismus, der auf diesem Weg zum Ausdrücken des Wissens Wissens einer Anwendung basiert, bietet eine effiziente Möglichkeit für die Anwendung, Änderungen zu erhalten, die nach einem bestimmten Zeitpunkt aufgetreten sind.

    Wenn der Ausdruck des Wissens der Anwendung persistent gespeichert werden kann, d. h., wie in einer Datei oder Datenbank, ist die Anwendungs Neustarts weniger ressourcenintensiv, als wenn dies nicht möglich ist. Im obigen Beispiel kann der Ausdruck des Wissens der Anwendung persistent gespeichert werden, indem der DC d und die Uhrzeit t aufgezeichnet werden. Einige Änderungs Benachrichtigungsmechanismen lassen nicht zu, dass diese Daten persistent gespeichert werden. Der Server und die Anwendung müssen mit einem anderen Mechanismus synchronisiert werden, wenn die Anwendung gestartet wird. Dies ist ressourcenintensiv, wenn mehrere Objekte beteiligt sind und eine komplexe Programmierung umfassen können.

Verwenden Sie die folgenden Verfahren, um Änderungen in Active Directory Domain Services zu verfolgen:

-   Verwenden Sie das Steuerelement für die Änderungs Benachrichtigung, um eine persistente asynchrone Suche nach Änderungen zu initiieren, die einem angegebenen Filter entsprechen. Weitere Informationen finden Sie unter [Ändern von Benachrichtigungen in Active Directory Domain Services](change-notifications-in-active-directory-domain-services.md).
-   Verwenden Sie eine Verzeichnis Synchronisierungs Suche (Dirsync), um Änderungen abzurufen, die seit der vorherigen Dirsync-Suche aufgetreten sind. Weitere Informationen finden Sie unter Abrufen [von Änderungen mithilfe des Dirsync-Steuer](polling-for-changes-using-the-dirsync-control.md)Elements.
-   Verwenden Sie das Attribut "attributschanged", um nach Objekten zu suchen, die seit der vorherigen Suche geändert wurden. Weitere Informationen finden Sie unter Abrufen [von Änderungen mithilfe von "US-nchanged](polling-for-changes-using-usnchanged.md)".

Das Änderungs Benachrichtigungs Steuerelement wurde für Anwendungen oder Dienste entwickelt, die eine Benachrichtigung über seltene Änderungen erfordern. Ein Beispiel hierfür ist ein Dienst oder ein Programm, das Konfigurationsdaten auf dem Active Directory Server speichert und umgehend benachrichtigt werden muss, wenn eine Änderung auftritt. Beachten Sie, dass es Einschränkungen für das Benachrichtigungs Steuerelement gibt.

-   Die Promptheit von Benachrichtigungen hängt von der Replikations Latenz und dem Speicherort der Änderung ab. Sie werden möglicherweise umgehend benachrichtigt, wenn eine Änderung in das zu überwachende Replikat repliziert wird, die Änderung jedoch möglicherweise schon viel früher auf einem anderen Replikat entstanden ist.
-   Das-Steuerelement ist auf die Überwachung eines einzelnen Objekts oder der unmittelbaren untergeordneten Elemente eines Containers beschränkt. Anwendungen, die mehrere Container oder nicht verbundene Objekte überwachen müssen, können bis zu fünf Benachrichtigungs Anforderungen registrieren.
-   Wenn zu viele Clients auf häufig auftretenden Änderungen lauschen, wirkt sich dies auf die Serverleistung aus. Im Allgemeinen sollten Anwendungen die Verwendung dieses Steuer Elements aus Leistungsgründen auf dem Server einschränken. Wenn Sie nicht sofort über Änderungen informiert werden müssen, kann es am besten sein, regelmäßig nach Änderungen abzufragen, anstatt Änderungs Benachrichtigungen zu verwenden.

Die Dirsync-und die aktualisierbaren Suchtechniken sind für Anwendungen konzipiert, die die Konsistenz zwischen den Daten auf dem Active Directory Server und den entsprechenden Daten in einem anderen Speicher aufrechterhalten. Diese Techniken werden von Anwendungen verwendet, die regelmäßig Änderungen Abfragen. Die Dirsync-Technik basiert auf einem LDAP-Server Steuerelement, das Sie über ADSI-oder LDAP-APIs verwenden können. Die Nachteile des Dirsync-Steuer Elements bestehen darin, dass es nur von einem Konto mit hohen Berechtigungen verwendet werden kann, z. b. einem Domänen Administrator. Im folgenden finden Sie eine Liste der Einschränkungen des Dirsync-Steuer Elements:

-   Das DirSync-Steuerelement kann nur von einem Konto mit hohen Berechtigungen verwendet werden, z. b. einem Domänen Administrator.
-   Das DirSync-Steuerelement kann nur einen gesamten namens Kontext überwachen. Sie können den Gültigkeitsbereich einer Dirsync-Suche nicht einschränken, um nur eine bestimmte Unterstruktur, einen Container oder ein Objekt in einem namens Kontext zu überwachen.

Die Methode "Methode" hat diese Einschränkungen nicht, obwohl die Verwendung von "DirSync" etwas komplizierter ist.

 

 




