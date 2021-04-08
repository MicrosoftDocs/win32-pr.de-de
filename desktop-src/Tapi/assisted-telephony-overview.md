---
description: Ein nützliches Feature von Telefoniefunktionen ist die kleine Gruppe von Funktionen, die als unterstützte Telefonie bezeichnet werden.
ms.assetid: 1c41f52b-f8bf-410e-a966-9323a690a4d5
title: Übersicht über unterstützte Telefonie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6a8826fd0c273936204d9250fb91504333d807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960109"
---
# <a name="assisted-telephony-overview"></a>Übersicht über unterstützte Telefonie

Ein nützliches Feature von Telefoniefunktionen ist die kleine Gruppe von Funktionen, die als unterstützte Telefonie bezeichnet werden. Die unterstützte Telefoniefunktion ist darauf ausgelegt, Sprachanrufe und Medien Aufrufe für jede Anwendung verfügbar zu machen, nicht nur für diejenigen, die für die Telefonfunktion vorgesehen sind. Anders ausgedrückt: mit der unterstützten Telefonie können Anwendungen Telefonanrufe tätigen, ohne die Details der Dienste der vollständigen telefonieapi kennen zu müssen. Es erweitert die Telefonie auf Textverarbeitungsanwendungen, Kalkulations Tabellen, Datenbanken, persönliche Informationsmanager und andere nicht-Telefonieanwendungen.

Eine Liste mit den TAPI 2. x-unterstützten Telefoniefunktionen der Basic-Telefoniefunktion finden Sie unter [TAPI-schnell Funktionsreferenz](./tapi-quick-function-reference.md). TAPI 3. x unterstützt eine unterstützte Telefonie über die [**itrequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest) -Schnittstelle.

Die Nützlichkeit der unterstützten Telefonie kann im folgenden Beispiel veranschaulicht werden. Eine Tabellenkalkulationsanwendung kann Funktionen enthalten, die eine Telefonnummer für einen Sprachanruf wählen. Solange die Anwendung keines der detaillierten Anrufe erfordert, die von der vollständigen telefonieapi bereitgestellt werden, ist die unterstützte telefoniemethode die einfachste und effizienteste Methode, um ihr eine Telefon Funktionalität zu bieten.

![Unterstützte Telefonie mit einer Tabellenkalkulationsanwendung](images/assist4.png)

Unterstützte Telefonie und die vollständige telefonieapi werden auf unterschiedliche Weise verwendet und implementiert, sodass es nicht ratsam ist, unterstützte telefoniefunktionsaufrufe und Telefonie-API-Funktionsaufrufe innerhalb einer einzelnen Anwendung zu mischen.

## <a name="using-assisted-telephony"></a>Verwenden der unterstützten Telefonie

Anwendungen, die unterstützte Telefoniedienste verwenden, initiieren nur die von TAPI in die Warteschlange eingereihten Anforderungs Anforderungen. Die Anforderungs Empfänger Anwendung ruft diese Anforderungen ab und führt Sie im Namen der unterstützten Telefonieanwendung aus. Die [**tapirequestmakecall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall) -Funktion fordert die Einrichtung eines sprach Aufrufes an. Der-Befehl wird von der anfordernden Anwendung nicht gesteuert.

TAPI ermöglicht es dem Benutzer, für jeden dieser Dienste andere Anforderungs Empfänger Anwendungen zu erstellen. Eine Anwendung wird zu einem Anforderungs Empfänger, indem Sie sich bei [**lineregisterrequestrecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient)registriert, wobei **true** als Wert für den Parameter *benable* angegeben wird. (Durch Angabe von " **false** " wird die Anwendung als Anforderungs Empfänger registriert, was Sie tun sollte, wenn festgestellt wird, dass die Empfänger Aufgaben für die aktuelle Sitzung durchlaufen werden.) Die Anwendung wählt die zu behandelnden Dienste im *dwrequestmode* -Parameter von **lineregisterrequestrecipient** aus. Ein möglicher Wert für eine Anforderung ist linerequestmode \_ MakeCall, um anzuzeigen, dass die Anwendung [**tapirequestmakecall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall) -Anforderungen verarbeitet. Wenn sich mehrere Anwendungen für dieselben Dienste registrieren, wird ein Prioritäts Schema verwendet, um dem Benutzer zu ermöglichen, die für die Verarbeitung von Anforderungen bevorzugte Anwendung auszuwählen. Dieses Prioritäts Schema ist identisch mit dem, das für die Aufruf Übergabe und das Routing eingehender Aufrufe auf der Grundlage einer Liste von Dateinamen in **handoffpriority** in der Registrierung verwendet wird.

## <a name="call-requests"></a>Aufrufe von Anforderungen

Die unterstützte Telefonie bietet telefoniefähigen Anwendungen einen leicht zu verwendenden Mechanismus für Telefonanrufe, ohne dass der Entwickler in Telefonieinformationen vollständig geschult werden muss.

Die [**tapirequestmakecall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall) -Funktion fordert einen Sprachanruf zwischen dem Benutzer und einem Remote Partei an, der durch seine Telefonnummer angegeben wird. Die Anforderung erfolgt an TAPI und übergibt sie an eine Anwendung, die als Empfänger solcher Anforderungen registriert ist. Dieser Empfänger ist eine Anwendungs-Manager-Anwendung.

Nachdem die Anwendung die Anforderung gestellt hat, wird der Aufruf vollständig von der Anwendung für den Aufruf-Manager gesteuert, da die unterstützten Telefonieanwendungen keine Aufrufe verwalten können. Da die komplizierteren Aspekte von Telefonie und alle Benutzeroberflächen Vorgänge von der Anwendung des Anwendungs Leiters verarbeitet werden, müssen telefonieaktivierte Anwendungen nicht auf irgendeine Weise geändert werden. Tatsächlich müssen Anwendungen, die diesen Vorgang von der integrierten Skriptsprache aus aufgerufen werden können, möglicherweise überhaupt nicht geändert werden.

Die [**tapigetlocationinfo**](/windows/win32/api/tapi/nf-tapi-tapigetlocationinfo) -Funktion gibt den Code des Landes oder der Region und den Ort (Bereich), den der Benutzer in den aktuellen Standort Parametern in der telefoniesteuerungskosten festgelegt hat, an die Anwendung zurück. Die Anwendung kann diese Informationen verwenden, um den Benutzer bei der Erstellung richtiger kanonischer Telefonnummern zu unterstützen, z. b. wenn diese als Standardwerte angeboten werden, wenn in einem Telefonbucheintrag oder einem Daten Bank Datensatz neue Zahlen eingegeben werden.

## <a name="request-recipients"></a>Anforderungs Empfänger

Zwei Arten von Anwendungen sind erforderlich, um eine unterstützte Telefonie auszuführen. Unterstützte *Telefonieclients* sind Anwendungen, die unterstützte Telefonie verwenden, indem Sie die Funktionen aufrufen, die das Präfix "TAPI" aufweisen. Ein Beispiel für eine solche Client Anwendung wäre eine Kalkulations Tabelle, der **ein Menübefehl** oder eine Symbolleisten Schaltfläche hinzugefügt wird.

Unterstützte *Telefonieserver* sind Anwendungen, die Telefonie-API-Funktionen ausführen können, die sich aus einem anderen Anwendungs Aufrufe einer "TAPI"-Präfix Funktion ergeben. Um sich selbst als einen unterstützten Telefonieserver bekannt zu machen, registriert sich eine Anwendung mithilfe der [**lineregisterrequestrecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) -Funktion als eine Anwendung.

Die Funktionen der unterstützten Telefonie (die mit dem Präfix "TAPI" beginnen) werden als *Anforderungs Funktionen* bezeichnet. Unterstützte Telefonieanwendungen, die diese Anforderungen verarbeiten – unterstützte Telefonieserver – werden als *Anforderungs Empfänger* bezeichnet.

## <a name="processing-assisted-telephony-requests"></a>Verarbeiten von unterstützten Telefonieanforderungen

Der Prozess, mit dem Anforderungen zugestellt und gewartet werden, lautet wie folgt:

1.  Wenn TAPI eine unterstützte Telefonieanforderung empfängt, überprüft er, ob ein Anforderungs Empfänger, d. h. eine zurzeit für die Verarbeitung des Anforderungs Typs registrierte Anwendung, registriert ist. Wenn ein Anforderungs Empfänger vorhanden ist, wird die Anforderung in die Warteschlange eingereiht, und die Anwendung mit der höchsten Priorität, die sich für den Dienst der Anforderung registriert hat, wird als [**Zeilen \_ Anforderungs**](./line-request.md) Nachricht gesendet. Die Meldung benachrichtigt den Anforderungs Empfänger, dass eine neue Anforderung eingetroffen ist, und weist einen Hinweis auf den Modus der Anforderung auf.
2.  Wenn TAPI eine aktuell laufende Anwendung nicht finden kann, um eine solche Anforderung zu verarbeiten, wird versucht, eine Anwendung zu starten, die als fähig registriert wurde. Diese Registrierungsinformationen werden in **handoffprioritäten** in der Registrierung aufgezeichnet. TAPI versucht, Anwendungen in der Reihenfolge zu starten, in der Sie im Abschnitt " **handoffprioritäten** " aufgeführt sind. (Weitere Informationen finden Sie im folgenden Schritt.)

    Wenn derzeit keine Anwendung registriert ist, prüft TAPI die Liste der Anwendungen zur Anforderungs Verarbeitung auf den zugehörigen Eintrag in **handoffprioritäten**. Wenn die zugehörige Zeile in der Datei nicht vorhanden ist, wenn keine Anwendungen aufgeführt sind oder keine der Anwendungen in der Liste gestartet werden kann, wird die Anforderung mit dem Fehler tapierr \_ norequestrecipient abgelehnt.

    Wenn ein Anforderungs Empfänger gestartet wird (unabhängig davon, ob er von TAPI gestartet wurde), ist es seine Aufgabe, [**lineregisterrequestrecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) während des Startvorgangs aufzurufen und sich selbst als Anforderungs Empfänger zu registrieren.

3.  Wenn eine oder mehrere Anwendungen im Eintrag aufgeführt sind, beginnt TAPI mit der ersten aufgelisteten Anwendung (höchste Priorität) und versucht, Sie mit der Funktion " [**deateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) " zu starten. Wenn der Versuch, die Anwendung zu starten, fehlschlägt, versucht TAPI, die nächste Anwendung in der Liste zu starten. Wenn eine Anwendung erfolgreich gestartet wird, fügt TAPI die Anforderung einfach in die Warteschlange ein und gibt eine Erfolgsmeldung an die Anwendung zurück, obwohl die Anforderung dem Anforderungs Empfänger noch nicht signalisiert wurde.

    Nachdem die Anforderungs Empfänger Anwendung gestartet wurde, wird [**lineregisterrequestrecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient)aufgerufen, wodurch eine [**Zeilen \_ Anforderungs**](./line-request.md) Nachricht gesendet wird, die signalisiert, dass die Anforderung in die Warteschlange eingereiht wird. Wenn die gestartete Anwendung aus irgendeinem Grund nie registriert wird, bleibt die Anforderung in die Warteschlange eingereiht und bleibt unbegrenzt in der Warteschlange, bis eine Anwendung für diese Art von Anforderung registriert wird.

4.  Wenn TAPI feststellt, dass eine solche registrierte Anwendung bereits ausgeführt wird oder gestartet wird, wird die Anforderung in die Warteschlange eingereiht, eine Zeilen \_ Anforderungs Nachricht an die Serveranwendung gesendet und eine Erfolgsmeldung für den Funktions Aufrufder unterstützten Telefonieanwendung zurückgegeben. Diese Erfolgsmeldung gibt nur an, dass die Anforderung akzeptiert und in die Warteschlange eingereiht wurde, und nicht, dass Sie erfolgreich ausgeführt wurde.

Wenn die Serveranwendung bereit ist, eine Anforderung zu verarbeiten, ruft Sie die [**linegetrequest**](/windows/win32/api/tapi/nf-tapi-linegetrequest) -Funktion auf. Dadurch erhalten Sie alle benötigten Informationen, z. b. eine Adresse, die Sie wählen können. Anschließend wird die Anforderung mithilfe der TAPI-Funktionen (z. b. [**linemakecall**](/windows/win32/api/tapi/nf-tapi-linemakecall) und [**linedrop**](/windows/win32/api/tapi/nf-tapi-linedrop)) verarbeitet, die andernfalls zum Platzieren des Aufrufes verwendet werden. Wenn Sie **linegetrequest** aufrufen, wird die Anforderung aus TAPI entfernt, und die Anforderungs Parameter werden in einen von der Anwendung zugewiesenen Anforderungs Puffer kopiert. Die Größe und die Interpretation der Inhalte des Puffers richten sich nach dem Anforderungs Modus.

Der Server muss beim Ausführen von Anforderungen sicherstellen, dass die richtigen Parameter verwendet werden. Dabei werden die folgenden Schritte ausgeführt:

1.  Der Anforderungs Empfänger empfängt zuerst eine [**Zeilen \_ Anforderungs**](./line-request.md) Nachricht, in der er darüber informiert wird, dass in der Anforderungs Warteschlange Anforderungen vorhanden sein können. Dadurch wird die Anwendung aufgefordert, [**linegetrequest**](/windows/win32/api/tapi/nf-tapi-linegetrequest) aufzurufen und fortzusetzen, bis die Warteschlange entladen wird (wenn die Anforderung zum Erstellen eines neuen Aufrufs dient), oder einen vorhandenen Aufruf zu löschen. Diese Meldung enthält nicht die Parameter für die Anforderung, es sei denn, eine Anforderung zum Löschen eines vorhandenen Aufrufes.
2.  Wenn die Anforderung ist, einen neuen-Befehl zu erstellen, verwendet der unterstützte Telefonieserver die [**linegetrequest**](/windows/win32/api/tapi/nf-tapi-linegetrequest) -Funktion, um die vollständige Anforderung abzurufen, einschließlich der Parameter der Anforderung. Der Server verfügt nun über alle Informationen, die er benötigt, z. b. die zu wählende Zahl oder die Identifizierung des Herstellers der Anforderung. Zuerst muss der Server jedoch den Arbeitsspeicher zuordnen, der zum Speichern dieser Informationen benötigt wird.
3.  Schließlich führt der Server die Anforderung aus, indem er die entsprechende TAPI-Funktion oder eine Reihe von Funktionen aufruft.

Wenn TAPI eine Anwendung nicht starten kann, die als Anforderungs Empfänger fungieren kann, schlägt der gestützte telefonierückruf fehl und gibt den Fehler tapierr \_ norequestrecipient zurück.

## <a name="notes-on-request-recipient-operations"></a>Hinweise zu Anforderungs Empfänger Vorgängen

Die folgenden Informationen betreffen Systeme, bei denen unterstützte Telefonieanforderungen verarbeitet werden:

-   In der Standard Registrierung sollte eine Anwendung zum Aufrufen des Managers in der Prioritäts Liste für [**tapirequestmakecall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall)aufgelistet werden. Es wäre hilfreich, aber nicht wichtig, dass die Anwendung für den Anwendungs Leiter über eine Menüoption verfügt, die es Benutzern ermöglicht, Sie auf die höchste Priorität festzulegen.
-   Wenn eine unterstützte telefonieempfängeranwendung automatisch von TAPI gestartet wird und die einzige TAPI-Anwendung im System ist, initialisiert diese Aktion TAPI. Wenn die unterstützte telefonieempfängeranwendung das liniengerät initialisiert und herunterfährt, bevor es für unterstützte Telefonieanforderungen registriert wird, wird TAPI ebenfalls heruntergefahren, und die unterstützte Telefonieanforderung geht verloren. Unterstützte Telefonieanforderungen können auch verloren gehen, wenn eine andere TAPI-Anwendung, die gestartet wird, initialisiert und heruntergefahren wird.

 

 
