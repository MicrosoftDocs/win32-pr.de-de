---
description: Ein wertvolles Feature der Telefonie ist die kleine Gruppe von Funktionen, die als Unterstützte Telefonie bezeichnet werden.
ms.assetid: 1c41f52b-f8bf-410e-a966-9323a690a4d5
title: Übersicht über die unterstützte Telefonie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86adba883e558419731405c5b1274e812816944295c5743e8a91d343b42082c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117948844"
---
# <a name="assisted-telephony-overview"></a>Übersicht über die unterstützte Telefonie

Ein wertvolles Feature der Telefonie ist die kleine Gruppe von Funktionen, die als Unterstützte Telefonie bezeichnet werden. Die telefonunterstützte Telefonie ist darauf ausgelegt, die Einrichtung von Sprachanrufen und Medienanrufen für jede Anwendung verfügbar zu machen, nicht nur für telefonische Funktionen. Anders ausgedrückt: Mit der unterstützten Telefonie können Anwendungen Telefonanrufe tätigen, ohne die Details der Dienste der vollständigen Telefonie-API kennen zu müssen. Sie erweitert die Telefonie auf Anwendungen für die Wortverarbeitung, Tabellenkalkulationen, Datenbanken, Manager für persönliche Informationen und andere Nicht-Telefonieanwendungen.

Eine Liste der TAPI 2.x-gestützten Telefoniefunktionen der Einfachtelefonie finden Sie unter [TAPI Quick Function Reference (TAPI-Kurzfunktionsreferenz).](./tapi-quick-function-reference.md) TAPI 3.x unterstützt die unterstützte Telefonie über die [**ITRequest-Schnittstelle.**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest)

Die Nützlichkeit der unterstützten Telefonie kann im folgenden Beispiel veranschaulicht werden. Eine Tabellenkalkulationsanwendung kann Funktionen enthalten, die eine Telefonnummer für einen Sprachanruf wählen. Solange die Anwendung keine der detaillierten Anrufsteuerungen benötigt, die von der vollständigen Telefonie-API bereitgestellt werden, ist die unterstützte Telefonie die einfachste und effizienteste Möglichkeit, um ihr Telefoniefunktionen zu bieten.

![Unterstützte Telefonie mit einer Tabellenkalkulationsanwendung](images/assist4.png)

Die unterstützte Telefonie und die vollständige Telefonie-API werden auf unterschiedliche Weise verwendet und implementiert. Daher wird nicht empfohlen, Telefoniefunktionsaufrufe und Telefonie-API-Funktionsaufrufe innerhalb einer einzelnen Anwendung zu kombinieren.

## <a name="using-assisted-telephony"></a>Verwenden der unterstützten Telefonie

Anwendungen, die Die unterstützten Telefoniedienste verwenden, initiieren nur Aufrufanforderungen, die vorübergehend von TAPI in die Warteschlange eingereiht werden. Die Anwendung des Anforderungsempfängers ruft diese Anforderungen ab und führt sie im Namen der Anwendung Assisted Telefonie aus. Die [**tapiRequestMakeCall-Funktion**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall) fordert die Einrichtung eines Sprachanrufs an. Die anfordernde Anwendung steuert den Aufruf nicht.

TAPI ermöglicht es dem Benutzer, für jeden dieser Dienste unterschiedliche oder die gleiche Anwendung für den Anforderungsempfänger einzurichten. Eine Anwendung wird zu einem Anforderungsempfänger, indem sie sich bei [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient)registriert, in dem **TRUE** als Wert für den Parameter *bEnable* angegeben wird. (Durch Die Angabe von **FALSE** wird die Registrierung der Anwendung als Anforderungsempfänger aufgehoben. Dies sollte erfolgen, wenn festgestellt wurde, dass die Empfängeraufgaben für die aktuelle Sitzung erfüllt sind.) Die Anwendung wählt die Dienste aus, die sie im *dwRequestMode-Parameter* von **lineRegisterRequestRecipient** verarbeiten möchte. Ein möglicher Wert für eine Anforderung ist LINEREQUESTMODE \_ MAKECALL, um anzuzeigen, dass die Anwendung [**tapiRequestMakeCall-Anforderungen**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall) verarbeitet. Wenn sich mehrere Anwendungen für dieselben Dienste registrieren, wird ein Prioritätsschema verwendet, damit der Benutzer auswählen kann, welche Anwendung für die Verarbeitung von Anforderungen bevorzugt wird. Dieses Prioritätsschema ist identisch mit dem für die Anrufableitung und das Routing eingehender Aufrufe basierend auf einer Liste von Dateinamen in **HandoffPriorities** in der Registrierung.

## <a name="call-requests"></a>Aufrufanforderungen

Die telefongestützte Telefonie bietet telefoniefähige Anwendungen mit einem benutzerfreundlichem Mechanismus zum Tätigen von Telefonanrufen, ohne dass der Entwickler die Telefonie vollständig literieren muss.

Die [**tapiRequestMakeCall-Funktion**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall) fordert einen Sprachanruf zwischen dem Benutzer und einer Remotepartei an, die durch seine Telefonnummer angegeben wird. Die Anforderung wird an TAPI gerichtet, die sie an eine Anwendung übergibt, die als Empfänger solcher Anforderungen registriert ist. Dieser Empfänger ist eine Anruf-Manager-Anwendung.

Nachdem die Anwendung die Anforderung gestellt hat, wird der Aufruf vollständig von der Aufruf-Manager-Anwendung aus gesteuert, da Assisted Telefonieanwendungen Keine Aufrufe verwalten können. Da die komplexeren Aspekte der Telefonie und alle Benutzeroberflächenvorgänge von der Call-Manager-Anwendung verarbeitet werden, müssen telefoniefähige Anwendungen nicht wesentlich geändert werden. Anwendungen, die diesen Vorgang über ihre integrierte Skriptsprache aufrufen können, müssen möglicherweise überhaupt nicht geändert werden.

Die [**tapiGetLocationInfo-Funktion**](/windows/win32/api/tapi/nf-tapi-tapigetlocationinfo) gibt an die Anwendung den Länder- oder Regionscode und den Ortscode (Gebiet) zurück, den der Benutzer in den aktuellen Standortparametern im Telefonie-Systemsteuerung festgelegt hat. Die Anwendung kann diese Informationen verwenden, um den Benutzer bei der Erstellung geeigneter kanonischer Telefonnummern zu unterstützen, z. B. indem sie diese als Standardwerte anbietet, wenn neue Nummern in einen Telefonbucheintrag oder einen Datenbankdatensatz eingegeben werden.

## <a name="request-recipients"></a>Anforderungsempfänger

Zwei Arten von Anwendungen sind erforderlich, um die unterstützte Telefonie auszuführen. Unterstützte *Telefonieclients* sind Anwendungen, die die unterstützte Telefonie verwenden, indem sie die Funktionen aufrufen, die das Präfix "tapi" aufweisen. Ein Beispiel für eine solche Clientanwendung wäre ein Arbeitsblatt, dem **ein** Menübefehl oder eine Symbolleistenschaltfläche hinzugefügt wird.

Unterstützte *Telefonieserver* sind Anwendungen, die Telefonie-API-Funktionen ausführen können, die sich aus dem Aufruf einer "tapi"-Funktion mit dem Präfix einer anderen Anwendung ergeben. Um sich selbst als Unterstützter Telefonieserver bekannt zu machen, wird eine solche Anwendung mithilfe der [**lineRegisterRequestRecipient-Funktion**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) als ein Server registriert.

Die Funktionen der unterstützten Telefonie (die mit dem Präfix "tapi" beginnen) werden als *Anforderungsfunktionen* bezeichnet. Unterstützte Telefonieanwendungen, die diese Anforderungen verarbeiten – unterstützte Telefonieserver – werden als *Anforderungsempfänger* bezeichnet.

## <a name="processing-assisted-telephony-requests"></a>Verarbeiten von unterstützten Telefonieanforderungen

Der Prozess, mit dem Anforderungen übermittelt und verarbeitet werden, lautet wie folgt:

1.  Wenn TAPI eine Anforderung vom Typ "Unterstützte Telefonie" empfängt, wird nach einem Anforderungsempfänger gesucht, d. h. nach einer Anwendung, die derzeit für die Verarbeitung dieser Art von Anforderung registriert ist. Wenn ein Anforderungsempfänger vorhanden ist, wird die Anforderung in die Warteschlange eingereiht, und die Anwendung mit der höchsten Priorität, die für den Dienst dieser Anforderung registriert wurde, erhält eine [**LINE \_ REQUEST-Nachricht.**](./line-request.md) Die Nachricht benachrichtigt den Empfänger der Anforderung, dass eine neue Anforderung eingetroffen ist, und enthält einen Hinweis auf den Modus der Anforderung.
2.  Wenn TAPI eine derzeit ausgeführte Anwendung zum Verarbeiten einer solchen Anforderung nicht finden kann, wird versucht, eine Anwendung zu starten, die dafür registriert wurde. Diese Registrierungsinformationen werden in **HandoffPriorities** in der Registrierung aufgezeichnet. TAPI versucht, Anwendungen in der Reihenfolge zu starten, in der sie im Abschnitt **HandoffPriorities** aufgeführt sind. (Weitere Informationen finden Sie im folgenden Schritt.)

    Wenn derzeit keine Anwendung registriert ist, überprüft TAPI die Liste der Anwendungen zur Anforderungsverarbeitung für den zugeordneten Eintrag in **HandoffPriorities.** Wenn die zugeordnete Zeile in der Datei fehlt, keine Anwendungen darin aufgeführt sind oder keine der Anwendungen in der Liste gestartet werden kann, wird die Anforderung mit dem Fehler TAPIERR \_ NOREQUESTRECIPIENT abgelehnt.

    Wenn ein Anforderungsempfänger gestartet wird (unabhängig davon, ob er von TAPI gestartet wurde), ist es seine Aufgabe, während des Startvorgangs [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) aufzurufen und sich selbst als Anforderungsempfänger zu registrieren.

3.  Wenn eine oder mehrere Anwendungen im Eintrag aufgeführt sind, beginnt TAPI mit der ersten aufgeführten Anwendung (höchste Priorität) und versucht, sie mit der [**CreateProcess-Funktion**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) zu starten. Wenn der Versuch, die Anwendung zu starten, fehlschlägt, versucht TAPI, die nächste Anwendung in der Liste zu starten. Wenn eine Anwendung erfolgreich gestartet wird, stellt TAPI die Anforderung einfach in die Warteschlange und gibt eine Erfolgsanzeige an die Anwendung zurück, obwohl die Anforderung noch nicht an den Empfänger der Anforderung gesendet wurde.

    Nachdem die Anwendung des Anforderungsempfängers gestartet wurde, ruft sie [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient)auf, wodurch eine [**LINE \_ REQUEST-Nachricht**](./line-request.md) gesendet wird, die angibt, dass die Anforderung in die Warteschlange eingereiht wird. Wenn die gestartete Anwendung aus irgendeinem Grund nie registriert wird, bleibt die Anforderung in der Warteschlange und bleibt unbegrenzt in der Warteschlange, bis sich eine Anwendung für diesen Anforderungstyp registriert.

4.  Wenn TAPI feststellt, dass eine solche registrierte Anwendung bereits ausgeführt wird oder erfolgreich gestartet wird, wird die Anforderung in die Warteschlange gestellt, und es wird eine LINE \_ REQUEST-Nachricht an die Serveranwendung gesendet, und es wird eine Erfolgsanzeige für den Funktionsaufruf an die Anwendung Assisted Telefonie zurückgegeben. Diese Erfolgsmeldung gibt nur an, dass die Anforderung akzeptiert und in die Warteschlange eingereiht wurde, nicht dass sie erfolgreich ausgeführt wurde.

Wenn die Serveranwendung bereit ist, eine Anforderung zu verarbeiten, ruft sie die [**funktion lineGetRequest**](/windows/win32/api/tapi/nf-tapi-linegetrequest) auf. Dadurch kann er alle benötigten Informationen empfangen, z. B. eine Wähladresse. Anschließend wird die Anforderung mithilfe der TAPI-Funktionen (z. B. [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) und [**lineDrop)**](/windows/win32/api/tapi/nf-tapi-linedrop)verarbeitet, die andernfalls zum Platzieren des Aufrufs verwendet würden. Beim Aufrufen von **lineGetRequest** wird die Anforderung aus TAPI entfernt, und die Anforderungsparameter werden in einen von der Anwendung zugeordneten Anforderungspuffer kopiert. Die Größe und Interpretation des Inhalts des Puffers hängt vom Anforderungsmodus ab.

Der Server muss sicherstellen, dass er beim Ausführen von Anforderungen die richtigen Parameter verwendet. Dabei werden die folgenden Schritte befolgt:

1.  Der Anforderungsempfänger empfängt zunächst eine [**LINE \_ REQUEST-Nachricht,**](./line-request.md) in der er darüber informiert wird, dass anforderungen für ihn in der Anforderungswarteschlange vorhanden sein können. Dies weist die Anwendung an, [**lineGetRequest**](/windows/win32/api/tapi/nf-tapi-linegetrequest) aufzurufen und weiterhin aufzurufen, bis die Warteschlange entladen wird (wenn die Anforderung einen neuen Aufruf tätigen soll) oder einen vorhandenen Aufruf zu löschen. Diese Nachricht enthält nicht die Parameter für die Anforderung, außer im Fall einer Anforderung zum Löschen eines vorhandenen Aufrufs.
2.  Wenn die Anforderung einen neuen Aufruf tätigen soll, verwendet der Server für die unterstützte Telefonie die [**Funktion lineGetRequest,**](/windows/win32/api/tapi/nf-tapi-linegetrequest) um die vollständige Anforderung abzurufen, die die Parameter der Anforderung enthält. Der Server verfügt jetzt über alle benötigten Informationen, z. B. die Zuwahlnummer oder die Identifikation des Erstellers der Anforderung. Zunächst muss der Server jedoch den Arbeitsspeicher zuordnen, der zum Speichern dieser Informationen erforderlich ist.
3.  Schließlich führt der Server die Anforderung aus, indem er die entsprechende TAPI-Funktion oder den entsprechenden Funktionssatz aufruft.

Wenn TAPI keine Anwendung starten kann, die als Anforderungsempfänger dienen kann, schlägt der Telefonieaufruf fehl und gibt den Fehler TAPIERR \_ NOREQUESTRECIPIENT zurück.

## <a name="notes-on-request-recipient-operations"></a>Hinweise zu Anforderungsempfängervorgängen

Die folgenden Informationen beziehen sich auf Systeme, in denen gestützte Telefonieanforderungen verarbeitet werden:

-   Die Standardregistrierung sollte eine Aufruf-Manager-Anwendung in der Prioritätsliste für [**tapiRequestMakeCall auflisten.**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall) Es wäre hilfreich, aber nicht wichtig, wenn die Aufruf-Manager-Anwendung über eine Menüoption verfügen würde, mit der Benutzer sie auf die höchste Priorität festlegen können.
-   Wenn eine Empfängeranwendung für gestützte Telefonie automatisch von TAPI gestartet wird und es sich um die einzige TAPI-Anwendung im System handelt, initialisiert diese Aktion TAPI. Wenn die Empfängeranwendung für die gestützte Telefonie das Liniengerät initialisiert und herunterfährt, bevor sie sich für Unterstützte Telefonieanforderungen registriert, wird TAPI ebenfalls heruntergefahren, und die Anforderung der unterstützten Telefonie geht verloren. Unterstützte Telefonieanforderungen können auch verlorengehen, wenn eine andere gestartete TAPI-Anwendung initialisiert und heruntergefahren wird.

 

 
