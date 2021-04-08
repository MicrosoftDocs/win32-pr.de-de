---
description: Das Windows-Betriebssystem stellt Mechanismen bereit, um die Kommunikation und die Datenfreigabe zwischen Anwendungen zu vereinfachen. Gemeinsam werden die durch diese Mechanismen aktivierten Aktivitäten als prozessübergreifende Kommunikation (prozessübergreifende Communications, IPC) bezeichnet.
ms.assetid: ad3fb0d9-d0ab-479e-b9a6-22a463b6728c
title: Prozessübergreifende Kommunikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca9789da756ae5449e77237c1140386a6f5cfd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865588"
---
# <a name="interprocess-communications"></a>Prozessübergreifende Kommunikation

Das Windows-Betriebssystem stellt Mechanismen bereit, um die Kommunikation und die Datenfreigabe zwischen Anwendungen zu vereinfachen. Gemeinsam werden die durch diese Mechanismen aktivierten Aktivitäten als *prozessübergreifende Kommunikation (prozessübergreifende Communications* , IPC) bezeichnet. Einige Arten von IPC vereinfachen die Division von Arbeit zwischen mehreren spezialisierten Prozessen. Andere Arten von IPC vereinfachen die Division von Arbeitsaufwand zwischen Computern in einem Netzwerk.

In der Regel können Anwendungen IPC als Clients oder Server verwenden. Bei einem *Client* handelt es sich um eine Anwendung oder einen Prozess, der einen Dienst von einer anderen Anwendung oder einem anderen Prozess anfordert. Bei einem *Server* handelt es sich um eine Anwendung oder einen Prozess, der auf eine Client Anforderung antwortet. Viele Anwendungen fungieren abhängig von der Situation sowohl als Client als auch als Server. Beispielsweise kann eine Textverarbeitungsanwendung als Client fungieren, um eine Zusammenfassungs Tabelle mit Herstellungskosten aus einer Tabellenkalkulationsanwendung anzufordern, die als-Server fungiert. Die Tabellenkalkulationsanwendung könnte wiederum als Client beim Anfordern der aktuellen Inventur Ebenen von einer automatisierten Bestands Steuerungsanwendung fungieren.

Nachdem Sie entschieden haben, dass Ihre Anwendung von IPC profitieren würde, müssen Sie entscheiden, welche der verfügbaren IPC-Methoden verwendet werden sollen. Es ist wahrscheinlich, dass eine Anwendung mehrere IPC-Mechanismen verwendet. Die Antworten auf diese Fragen bestimmen, ob eine Anwendung durch die Verwendung eines oder mehrerer IPC-Mechanismen profitieren kann.

-   Soll die Anwendung mit anderen Anwendungen kommunizieren können, die auf anderen Computern in einem Netzwerk ausgeführt werden, oder ist es für die Anwendung ausreichend, nur mit Anwendungen auf dem lokalen Computer zu kommunizieren?
-   Soll die Anwendung mit Anwendungen kommunizieren können, die auf anderen Computern ausgeführt werden, die unter verschiedenen Betriebssystemen ausgeführt werden können (z. b. 16-Bit-Windows oder Unix)?
-   Soll der Benutzer der Anwendung die anderen Anwendungen auswählen, mit denen die Anwendung kommuniziert, oder kann die Anwendung die Zusammenarbeit der Anwendung implizit finden?
-   Sollte die Anwendung auf allgemeine Weise mit vielen verschiedenen Anwendungen kommunizieren, wie z. b. das Zulassen von Ausschneide-und Einfügevorgängen mit einer beliebigen anderen Anwendung oder, wenn die Kommunikationsanforderungen auf einen eingeschränkten Satz von Interaktionen mit bestimmten anderen Anwendungen beschränkt werden sollen?
-   Ist die Leistung ein wichtiger Aspekt der Anwendung? Alle IPC-Mechanismen beinhalten einen gewissen Aufwand.
-   Soll die Anwendung eine GUI-Anwendung oder eine Konsolenanwendung sein? Einige IPC-Mechanismen erfordern eine GUI-Anwendung.

Die folgenden IPC-Mechanismen werden von Windows unterstützt:

-   [Zwischenablage](#using-the-clipboard-for-ipc)
-   [COM](#using-com-for-ipc)
-   [Datenkopie](#using-data-copy-for-ipc)
-   [DDE](#using-dde-for-ipc)
-   [Datei Zuordnung](#using-a-file-mapping-for-ipc)
-   [Postslots](#using-a-mailslot-for-ipc)
-   [Pipes](#using-pipes-for-ipc)
-   [RPC](#using-rpc-for-ipc)
-   [Windows-Sockets](#using-windows-sockets-for-ipc)

## <a name="using-the-clipboard-for-ipc"></a>Verwenden der Zwischenablage für IPC

Die Zwischenablage fungiert als zentrales Depot für die Datenfreigabe zwischen Anwendungen. Wenn ein Benutzer einen Ausschneide-oder Kopiervorgang in einer Anwendung ausführt, fügt die Anwendung die ausgewählten Daten in einem oder mehreren standardmäßigen oder Anwendungs definierten Formaten in die Zwischenablage ein. Alle anderen Anwendungen können dann die Daten aus der Zwischenablage abrufen und aus den verfügbaren Formaten auswählen, die Sie versteht. Die Zwischenablage ist ein sehr locker gekoppeltes Austausch Medium, bei dem Anwendungen nur das Datenformat akzeptieren müssen. Die Anwendungen können sich auf demselben Computer oder auf unterschiedlichen Computern in einem Netzwerk befinden.

**Schlüsselpunkt:** Alle Anwendungen sollten die Zwischenablage für die Datenformate unterstützen, die Sie verstehen. Beispielsweise sollte ein Text-Editor oder ein Textverarbeitungsprogramm mindestens in der Lage sein, Zwischenablage Daten im reinen Textformat zu liefern und zu akzeptieren. Weitere Informationen finden Sie unter [Zwischenablage](../dataxchg/clipboard.md).

## <a name="using-com-for-ipc"></a>Verwenden von com für IPC

Anwendungen, die OLE verwenden, verwalten *Verbund Dokumente*, d. –. Dokumente, die aus einer Vielzahl verschiedener Anwendungen besteht. OLE bietet Dienste, die es Anwendungen erleichtern, andere Anwendungen für die Datenbearbeitung aufzurufen. Ein Textverarbeitungs Tool, das OLE verwendet, könnte z. b. ein Diagramm aus einer Kalkulations Tabelle einbetten. Der Benutzer kann die Kalkulations Tabelle automatisch aus dem Textverarbeitungs Tool starten, indem Sie das eingebettete Diagramm für die Bearbeitung auswählen. OLE kümmert sich um das Starten der Tabelle und die Darstellung des Diagramms für die Bearbeitung. Wenn der Benutzer die Kalkulations Tabelle beendet, wird das Diagramm im ursprünglichen textprozessordokument aktualisiert. Die Kalkulations Tabelle scheint eine Erweiterung des Textprozessors zu sein.

Die Grundlage von OLE ist die Component Object Model (com). Eine Softwarekomponente, die com verwendet, kann mit einer Vielzahl anderer Komponenten kommunizieren, auch solche, die noch nicht geschrieben wurden. Die Komponenten interagieren als Objekte und Clients. Verteiltes com erweitert das COM-Programmiermodell so, dass es in einem Netzwerk funktioniert.

**Schlüsselpunkt:** OLE unterstützt zusammengesetzte Dokumente und ermöglicht einer Anwendung das Einschließen von eingebetteten oder verknüpften Daten, die automatisch eine andere Anwendung für die Datenbearbeitung startet, wenn Sie ausgewählt wird. Dadurch kann die Anwendung von jeder anderen Anwendung, die OLE verwendet, erweitert werden. COM-Objekte ermöglichen den Zugriff auf die Daten eines Objekts über eine oder mehrere Sätze verwandter Funktionen, die als *Schnittstellen* bezeichnet werden. Weitere Informationen finden Sie unter com-und ActiveX-Object Services.

## <a name="using-data-copy-for-ipc"></a>Verwenden der Datenkopie für IPC

Die Datenkopie ermöglicht einer Anwendung das Senden von Informationen an eine andere Anwendung mithilfe der [**WM- \_ CopyData**](../dataxchg/wm-copydata.md) -Nachricht. Diese Methode erfordert die Zusammenarbeit zwischen der sendenden Anwendung und der empfangenden Anwendung. Die empfangende Anwendung muss das Format der Informationen kennen und den Absender identifizieren können. Die sendende Anwendung kann den Speicher nicht ändern, auf den von einem Zeiger verwiesen wird.

**Schlüsselpunkt:** Die Datenkopie kann verwendet werden, um schnell Informationen mithilfe von Windows-Messaging an eine andere Anwendung zu senden. Weitere Informationen finden Sie unter [Kopieren von Daten](../dataxchg/data-copy.md).

## <a name="using-dde-for-ipc"></a>Verwenden von DDE für IPC

DDE ist ein Protokoll, mit dem Anwendungen Daten in einer Vielzahl von Formaten austauschen können. Anwendungen können DDE für einen einmaligen Datenaustausch oder für einen laufenden Austausch verwenden, bei dem die Anwendungen einander aktualisieren, sobald neue Daten verfügbar sind.

Die von DDE verwendeten Datenformate sind identisch mit denen, die von der Zwischenablage verwendet werden. DDE kann als Erweiterung des Zwischenablage Mechanismus betrachtet werden. Die Zwischenablage wird fast immer für eine einmalige Antwort auf einen Benutzer Befehl verwendet, wie z. b. das Auswählen des Einfüge Befehls in einem Menü. DDE wird in der Regel auch durch einen Benutzer Befehl initiiert, funktioniert jedoch oft ohne weitere Benutzerinteraktion. Sie können auch benutzerdefinierte DDE-Datenformate für ein spezielles IPC zwischen Anwendungen mit stärker gekoppelten Kommunikationsanforderungen definieren.

DDE-Austausch Vorgänge können zwischen Anwendungen erfolgen, die auf demselben Computer oder auf unterschiedlichen Computern in einem Netzwerk ausgeführt werden.

**Schlüsselpunkt:** DDE ist nicht so effizient wie neuere Technologien. Sie können DDE jedoch weiterhin verwenden, wenn andere IPC-Mechanismen nicht geeignet sind oder wenn Sie eine Schnittstelle mit einer vorhandenen Anwendung benötigen, die nur DDE unterstützt. Weitere Informationen finden Sie unter [dynamischer Datenaustausch](../dataxchg/dynamic-data-exchange.md) und [dynamischer Datenaustausch Verwaltungs Bibliothek](../dataxchg/dynamic-data-exchange-management-library.md).

## <a name="using-a-file-mapping-for-ipc"></a>Verwenden einer Datei Zuordnung für IPC

Die *Datei Zuordnung* ermöglicht einem Prozess, den Inhalt einer Datei so zu behandeln, als handele es sich um einen Speicherblock im Adressraum des Prozesses. Der Prozess kann einfache Zeiger Vorgänge verwenden, um den Inhalt der Datei zu überprüfen und zu ändern. Wenn zwei oder mehr Prozesse auf dieselbe Datei Zuordnung zugreifen, empfängt jeder Prozess einen Zeiger auf den Arbeitsspeicher in seinem eigenen Adressraum, der zum Lesen oder Ändern des Datei Inhalts verwendet werden kann. Die Prozesse müssen ein Synchronisierungs Objekt (z. b. ein Semaphor) verwenden, um Daten Beschädigungen in einer Multitasking-Umgebung zu verhindern.

Sie können einen Sonderfall der Datei Zuordnung verwenden, um *benannten gemeinsam genutzten Arbeitsspeicher* zwischen Prozessen bereitzustellen. Wenn Sie beim Erstellen eines Datei Mapping-Objekts die Datei für das System austauschen angeben, wird das Datei Zuordnung-Objekt als frei gegebener Speicherblock behandelt. Andere Prozesse können auf denselben Speicherblock zugreifen, indem Sie das gleiche Datei Zuordnungsobjekt öffnen.

Die Datei Zuordnung ist recht effizient und bietet auch Betriebssystem – unterstützte Sicherheits Attribute, die dazu beitragen können, dass unbefugte Daten beschädigt werden. Die Datei Zuordnung kann nur zwischen Prozessen auf einem lokalen Computer verwendet werden. Sie kann nicht über ein Netzwerk verwendet werden.

**Schlüsselpunkt:** Die Datei Zuordnung ist eine effiziente Möglichkeit für zwei oder mehr Prozesse auf demselben Computer, Daten gemeinsam zu nutzen, aber Sie müssen die Synchronisierung zwischen den Prozessen bereitstellen. Weitere Informationen finden Sie unter [Datei Zuordnung](/windows/desktop/Memory/file-mapping) und- [Synchronisierung](/windows/desktop/Sync/synchronization).

## <a name="using-a-mailslot-for-ipc"></a>Verwenden eines postslots für IPC

Mailslots bieten unidirektionale Kommunikation. Jeder Prozess, der einen Mailslot erstellt, ist ein *Mailslot-Server*. Andere Prozesse, die als *postslotclients* bezeichnet werden, senden Nachrichten an den Mailslot-Server, indem Sie eine Nachricht in ihren Mailslot schreiben. Eingehende Nachrichten werden immer an den postslot angehängt. Der postslot speichert die Nachrichten, bis der Mailslot-Server Sie gelesen hat. Bei einem Prozess kann es sich um einen Mailslot-Server und einen Mailslot-Client handeln, sodass die bidirektionale Kommunikation mithilfe mehrerer Postfächer möglich ist.

Ein Mailslot-Client kann eine Nachricht an einen Mailslot auf seinem lokalen Computer, an einen Mailslot auf einem anderen Computer oder an alle Postfächer mit demselben Namen auf allen Computern in einer angegebenen Netzwerk Domäne senden. Nachrichten, die an alle Postfächer in einer Domäne gesendet werden, können nicht mehr als 400 Bytes betragen, während an einen einzelnen Mailslot gesendete Nachrichten nur durch die maximale Nachrichtengröße beschränkt werden, die beim Erstellen des postslots vom Mailslot-Server festgelegt wurde.

**Schlüsselpunkt:** Mailslots bieten eine einfache Möglichkeit für Anwendungen, kurze Nachrichten zu senden und zu empfangen. Sie bieten außerdem die Möglichkeit, Nachrichten auf allen Computern in einer Netzwerk Domäne zu übertragen. Weitere Informationen finden Sie unter [Mailslots](mailslots.md).

## <a name="using-pipes-for-ipc"></a>Verwenden von Pipes für IPC

Es gibt zwei Arten von Pipes für die bidirektionale Kommunikation: Anonyme Pipes und Named Pipes. Mit *anonymen Pipes* können verwandte Prozesse Informationen untereinander übertragen. In der Regel wird eine anonyme Pipe verwendet, um die Standardeingabe oder-Ausgabe eines untergeordneten Prozesses umzuleiten, sodass Daten mit dem übergeordneten Prozess ausgetauscht werden können. Zum Austauschen von Daten in beiden Richtungen (Duplex Vorgang) müssen zwei anonyme Pipes erstellt werden. Der übergeordnete Prozess schreibt Daten mithilfe seines Schreib Handles in eine Pipe, während der untergeordnete Prozess die Daten mithilfe seines Lese Handles aus dieser Pipe liest. Entsprechend schreibt der untergeordnete Prozessdaten in die andere Pipe, und der übergeordnete Prozess liest aus diesem Prozess. Anonyme Pipes können nicht über ein Netzwerk verwendet werden, und Sie können auch nicht zwischen nicht verknüpften Prozessen verwendet werden.

*Named Pipes* werden zum Übertragen von Daten zwischen Prozessen verwendet, bei denen es sich nicht um verwandte Prozesse handelt, und zwischen Prozessen auf verschiedenen Computern. In der Regel erstellt ein Named Pipe-Server Prozess eine Named Pipe mit einem bekannten Namen oder einem Namen, der an seine Clients übermittelt werden soll. Ein Named Pipe-Client Prozess, der den Namen der Pipe kennt, kann das andere Ende öffnen und unterliegt den Zugriffsbeschränkungen, die durch den Named Pipe-Server Prozess angegeben werden. Nachdem sowohl der Server als auch der Client eine Verbindung mit der Pipe hergestellt haben, können Sie Daten austauschen, indem Sie Lese-und Schreibvorgänge auf der Pipe ausführen.

**Schlüsselpunkt:** Anonyme Pipes bieten eine effiziente Möglichkeit, die Standardeingabe oder-Ausgabe zu untergeordneten Prozessen auf demselben Computer umzuleiten. Named Pipes stellen eine einfache Programmierschnittstelle zum Übertragen von Daten zwischen zwei Prozessen bereit, unabhängig davon, ob Sie sich auf demselben Computer oder über ein Netzwerk befinden. Weitere Informationen finden Sie unter [Pipes](pipes.md).

## <a name="using-rpc-for-ipc"></a>Verwenden von RPC für IPC

RPC ermöglicht Anwendungen das Remote Aufruf von Funktionen. Daher vereinfacht RPC das Aufrufen einer Funktion. RPC funktioniert zwischen Prozessen auf einem einzelnen Computer oder auf verschiedenen Computern in einem Netzwerk.

Der von Windows bereitgestellte RPC ist mit der Open Software Foundation (OSF)-DCE (DCE) kompatibel. Dies bedeutet, dass Anwendungen, die RPC verwenden, mit Anwendungen kommunizieren können, die mit anderen Betriebssystemen ausgeführt werden, die DCE unterstützen. RPC unterstützt automatisch die Datenkonvertierung, um unterschiedliche Hardwarearchitekturen und die Byte-Reihenfolge zwischen unterschiedlichen Umgebungen zu berücksichtigen.

RPC-Clients und-Server sind eng gekoppelt, behalten jedoch weiterhin hohe Leistung bei. Das System nutzt RPC umfassend, um eine Client/Server-Beziehung zwischen verschiedenen Teilen des Betriebssystems zu ermöglichen.

**Schlüsselpunkt:** RPC ist eine Schnittstelle auf Funktionsebene mit Unterstützung für die automatische Datenkonvertierung und für die Kommunikation mit anderen Betriebssystemen. Mithilfe von RPC können Sie leistungsstarke, eng gekoppelte verteilte Anwendungen erstellen. Weitere Informationen finden Sie unter [Microsoft-RPC-Komponenten](/windows/desktop/Rpc/microsoft-rpc-components).

## <a name="using-windows-sockets-for-ipc"></a>Verwenden von Windows Sockets für IPC

Windows Sockets ist eine Protokoll unabhängige Schnittstelle. Es nutzt die Kommunikationsfunktionen der zugrunde liegenden Protokolle. In Windows Sockets 2 kann ein Sockethandle optional als Datei Handle mit den standardmäßigen Datei-e/a-Funktionen verwendet werden.

Windows Sockets basieren auf den Sockets, die zuerst von der Berkeley Software Distribution (BSD) populär gemacht wurden. Eine Anwendung, die Windows Sockets verwendet, kann mit einer anderen Socketimplementierung auf anderen Systemtypen kommunizieren. Allerdings werden nicht alle verfügbaren Optionen von allen Transport Dienstanbietern unterstützt.

**Schlüsselpunkt:** Windows Sockets ist eine Protokoll unabhängige Schnittstelle, die aktuelle und neue Netzwerkfunktionen unterstützen kann. Weitere Informationen finden Sie unter [Windows Sockets 2](/windows/desktop/WinSock/windows-sockets-start-page-2).

 

 
