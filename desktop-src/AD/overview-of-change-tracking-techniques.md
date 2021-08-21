---
title: Übersicht über Änderungsnachverfolgung Techniken
description: Es gibt mehrere Möglichkeiten, wie Änderungsnachverfolgungsmechanismen den Bereich für die Nachverfolgung von Änderungen unterscheiden können. Eine Anwendung kann Änderungen an einem einzelnen Attribut eines einzelnen Objekts, an allen Objekten in einer Domäne usw. nachverfolgen.
ms.assetid: 7359e851-61b7-420d-beb0-f7f33f79b007
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036a16362a7f27da47fc086d8758b28619f34d1475c7bb911050deb20c86f08d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025508"
---
# <a name="overview-of-change-tracking-techniques"></a>Übersicht über Änderungsnachverfolgung Techniken

Änderungsnachverfolgungsmechanismen können sich auf verschiedene Weise unterscheiden:

-   Bereich für die Nachverfolgung von Änderungen: Eine Anwendung kann Änderungen an einem einzelnen Attribut eines einzelnen Objekts, an allen Objekten in einer Domäne usw. nachverfolgen. Wenn der Mechanismus den Anforderungen der Anwendung entspricht, erhält die Anwendung ein Minimum an irrelevanten Daten, wodurch die Leistung verbessert wird.
-   Zeitachsen: Eine Anwendung wird bei jeder Änderung während der Durchführung benachrichtigt oder kann über die Nettoeffekte von Änderungen über einen Zeitraum von Minuten oder Stunden benachrichtigt werden.

    Die Verarbeitung weniger zeitaufwändiger Daten kann effizienter sein, da mehrere Änderungen in eine reduziert werden können. Wenn sich beispielsweise ein Attribut innerhalb eines Intervalls von einer Stunde dreimal ändert, wird eine Anwendung, die über änderungen benachrichtigt wird, die sich über eine Stunde angesammelt haben, nur über eine Attributänderung benachrichtigt, nicht über drei.

    Berücksichtigen Sie bei der Betrachtung von Zeitachsen die Auswirkungen der Replikationslatenz. Ein Update, das von einem Domänencontroller stammt, wird nicht sofort auf einen anderen Domänencontroller repliziert. Das Erfordern von Zeitplänen für die Änderungsnachverfolgung, die viel besser als die erwartete Replikationslatenz ist, bietet häufig keinen echten Vorteil für die Anwendung.

-   Abruf im Vergleich zu Benachrichtigung: Beim Abruf stellt eine Anwendung in regelmäßigen Abständen eine Anforderung an einen Domänencontroller, um Änderungsnachverfolgungsdaten zu empfangen. Mit Benachrichtigung sendet der Domänencontroller Änderungen nur dann an die Anwendung, wenn Änderungen auftreten.

    Der Aufwand für das Abrufen ist offensichtlich: Die Anwendung kann Änderungsnachverfolgungsdaten anfordern, wenn nichts Wesentliches aufgetreten ist. Der Mehraufwand für Benachrichtigungen ist feiner. Der Server muss Daten zu Benachrichtigungsanforderungen verwalten und diese Daten abfragen, um zu entscheiden, ob eine Benachrichtigung gesendet werden soll. Dies kann zu zusätzlichem Mehraufwand für normale Updateanforderungen kommen.

-   Ausdrücken des Wissens der Anwendung: persistent im Vergleich zu temporär: Jeder Änderungsnachverfolgungsmechanismus muss eine Methode für den Server enthalten, der die nachverfolgten Daten enthält, um den Wissenszustand der Anwendung zu verstehen, sodass die Idee der "Änderung" klar definiert ist. Der Wissenszustand der Anwendung kann beispielsweise als "Aktualisiert mit allen Änderungen, die auf DC d vor der Zeit t aufgetreten sind" ausgedrückt werden. Ein Mechanismus, der auf dieser Methode zum Ausdrücken des Wissenszustands einer Anwendung basiert, bietet eine effiziente Möglichkeit für die Anwendung, Änderungen zu erhalten, die nach einem bestimmten Zeitpunkt aufgetreten sind.

    Wenn der Ausdruck des Anwendungswissens beibehalten werden kann, d. h. wie in einer Datei oder Datenbank wie in einer Datei oder Datenbank wiederherstellbar gespeichert werden kann, ist der Neustart der Anwendung weniger ressourcenintensiv als wenn dies nicht dere ist. Im obigen Beispiel kann der Ausdruck des Anwendungswissens beibehalten werden, indem der Domänencontroller d und die Uhrzeit t aufgezeichnet werden. Einige Änderungsbenachrichtigungsmechanismen lassen nicht zu, dass diese Daten beibehalten werden. Der Server und die Anwendung müssen beim Starten der Anwendung mit einem anderen Mechanismus synchronisiert werden. Dies ist ressourcenintensiv, wenn mehrere Objekte beteiligt sind, und kann eine komplexe Programmierung umfassen.

Verwenden Sie die folgenden Verfahren, um Änderungen in Active Directory Domain Services nachzuverfolgen:

-   Verwenden Sie das Änderungsbenachrichtigungssteuerelement, um eine persistente asynchrone Suche nach Änderungen zu initiieren, die mit einem angegebenen Filter übereinstimmen. Weitere Informationen finden Sie unter [Änderungsbenachrichtigungen in Active Directory Domain Services](change-notifications-in-active-directory-domain-services.md).
-   Verwenden Sie eine Verzeichnissynchronisierungssuche (DirSync), um Änderungen abzurufen, die seit der vorherigen DirSync-Suche aufgetreten sind. Weitere Informationen finden Sie unter [Abfragen von Änderungen mithilfe des DirSync-Steuerelements.](polling-for-changes-using-the-dirsync-control.md)
-   Verwenden Sie das USNChanged-Attribut, um nach Objekten zu suchen, die sich seit der vorherigen Suche geändert haben. Weitere Informationen finden Sie unter [Polling for Changes Using USNChanged](polling-for-changes-using-usnchanged.md).

Die Änderungsbenachrichtigungssteuerung ist für Anwendungen oder Dienste konzipiert, die eine angemessen schnelle Benachrichtigung über seltene Änderungen erfordern. Ein Beispiel ist ein Dienst oder Programm, der Konfigurationsdaten auf dem Active Directory-Server speichert und bei einer Änderung sofort benachrichtigt werden muss. Beachten Sie, dass es Einschränkungen des Benachrichtigungssteuerelements gibt.

-   Die Eingabeaufforderung von Benachrichtigungen hängt von der Replikationslatenz und dem Ort ab, an dem die Änderung aufgetreten ist. Sie werden möglicherweise sofort benachrichtigt, wenn eine Änderung in das replikat repliziert wird, das Sie überwachen, aber die Änderung ist möglicherweise viel früher auf einem anderen Replikat aufgetreten.
-   Das Steuerelement ist auf die Überwachung eines einzelnen Objekts oder der unmittelbar untergeordneten Elemente eines Containers beschränkt. Anwendungen, die mehrere Container oder nicht verbundene Objekte überwachen müssen, können bis zu fünf Benachrichtigungsanforderungen registrieren.
-   Wenn zu viele Clients häufig auftretende Änderungen überwachen, wirkt sich dies auf die Leistung des Servers aus. Im Allgemeinen sollten Anwendungen die Verwendung dieses Steuerelements aus Leistungsgründen auf dem Server einschränken. Wenn Sie änderungen nicht sofort kennen müssen, ist es möglicherweise am besten, änderungen in regelmäßigen Abständen abzufragen, anstatt eine Änderungsbenachrichtigung zu verwenden.

Die Suchtechniken DirSync und USNChanged sind für Anwendungen konzipiert, die die Konsistenz zwischen Daten auf dem Active Directory-Server und den entsprechenden Daten in einem anderen Speicher gewährleisten. Diese Techniken werden von Anwendungen verwendet, die in regelmäßigen Abständen Änderungen abfragen. Die DirSync-Technik basiert auf einem LDAP-Serversteuerelement, das Sie über ADSI oder LDAP-APIs verwenden können. Die Nachteile des DirSync-Steuerelements sind, dass es nur von einem Konto mit hohen Berechtigungen verwendet werden kann, z. B. einem Domänenadministrator. Im Folgenden sind die Einschränkungen des DirSync-Steuerelements aufgeführt:

-   Das DirSync-Steuerelement kann nur von einem Konto mit hohen Berechtigungen verwendet werden, z. B. einem Domänenadministrator.
-   Das DirSync-Steuerelement kann nur einen gesamten Namenskontext überwachen. Sie können den Bereich einer DirSync-Suche nicht einschränken, um nur eine bestimmte Teilstruktur, einen Container oder ein Objekt in einem Namenskontext zu überwachen.

Die USNChanged-Technik hat diese Einschränkungen nicht, obwohl die Verwendung etwas komplizierter ist als DirSync.

 

 




