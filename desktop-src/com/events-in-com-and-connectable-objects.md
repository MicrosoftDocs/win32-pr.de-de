---
title: Ereignisse in com und Verbindungs fähigen Objekten
description: Wenn ein Programm etwas erkennt, das aufgetreten ist, kann es seine Clients benachrichtigen.
ms.assetid: f6ffbd1d-4bc1-4dc2-b3ed-ee12359e3d75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5115cfd08d57658eec879d44b4361e88965b3c
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "104038476"
---
# <a name="events-in-com-and-connectable-objects"></a>Ereignisse in com und Verbindungs fähigen Objekten

Wenn ein Programm etwas erkennt, das aufgetreten ist, kann es seine Clients benachrichtigen. Wenn z. b. ein Börsen Ticker Programm eine Änderung am Preis eines Aktien Ereignisses entdeckt, kann es alle Clients über die Änderung benachrichtigen. Dieser Benachrichtigungs Prozess wird als auslösen *eines Ereignisses* bezeichnet.

Mit com können Server Objekte com-Ereignisse verwenden, um Ereignisse ohne Informationen darüber auszulösen, welche Objekte benachrichtigt werden. Objekte können auch *Verbindungs fähige Objekte* verwenden, um ausführliche Informationen über Clients zu erhalten, die Benachrichtigungen angefordert haben.

COM-Verbindungs fähige Objekte stellen neben Ihren eingehenden Schnittstellen ausgehende Schnittstellen für Ihre Clients bereit. Demzufolge können Objekte und Ihre Clients an der bidirektionalen Kommunikation beteiligt sein. Eingehende Schnittstellen werden für ein Objekt implementiert und empfangen Aufrufe von externen Clients eines Objekts, während ausgehende Schnittstellen auf der Senke des Clients implementiert werden und Aufrufe vom-Objekt empfangen werden. Das-Objekt definiert eine Schnittstelle, die Sie verwenden möchten, und der Client implementiert diese.

Ein-Objekt definiert seine eingehenden Schnittstellen und stellt Implementierungen dieser Schnittstellen bereit. Eingehende Schnittstellen sind für Clients über die [**IUnknown:: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode des Objekts verfügbar. Clients Ruft die Methoden einer eingehenden Schnittstelle für das-Objekt auf, und das-Objekt führt gewünschte Aktionen im Namen des Clients aus.

Ausgehende Schnittstellen werden auch von einem Objekt definiert, aber der Client stellt die Implementierungen der ausgehenden Schnittstellen für ein Sink-Objekt bereit, das vom Client erstellt wird. Das-Objekt ruft dann Methoden der ausgehenden Schnittstelle für das sink-Objekt auf, um den Client über Änderungen im Objekt zu benachrichtigen, Ereignisse im Client zu lösen, etwas vom Client anzufordern, oder tatsächlich für einen beliebigen Zweck, mit dem der Objekt Ersteller kommt.

Ein Beispiel für eine ausgehende Schnittstelle ist eine ibuttonsink-Schnittstelle, die von einem Push-Schaltflächen-Steuerelement definiert wird, um die Clients über die Beispielsweise ruft das Schaltflächen Objekt ibuttonsink:: OnClick für das sink-Objekt des Clients auf, wenn der Benutzer auf die Schaltfläche auf dem Bildschirm klickt. Das Button-Steuerelement definiert die ausgehende Schnittstelle. Damit ein Client der Schaltfläche das Ereignis behandelt, muss der Client diese ausgehende Schnittstelle in einem Sink-Objekt implementieren und dann die Senke mit dem Schaltflächen-Steuerelement verbinden. Wenn dann Ereignisse in der Schaltfläche auftreten, ruft die Schaltfläche die Senke auf. zu diesem Zeitpunkt kann der Client jede beliebige Aktion ausführen, die diesem Schaltflächen Klick zugewiesen werden soll.

Verbindungs fähige Objekte bieten einen allgemeinen Mechanismus für die Kommunikation zwischen Objekten. Diese Technologie kann von jedem Objekt verwendet werden, das Ereignisse oder Benachrichtigungen verfügbar machen möchte. Zusätzlich zur allgemeinen Verbindungs fähigen Objekttechnologie bietet com viele besondere Zweck senken und Standort Schnittstellen, die von Objekten verwendet werden, um Clients über bestimmte Ereignisse zu benachrichtigen, die für den Client von Interesse sind. Beispielsweise kann [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) von Objekten verwendet werden, um Clients von Daten zu benachrichtigen und Änderungen im Objekt anzuzeigen.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Architektur von Verbindungs fähigen Objekten](architecture-of-connectable-objects.md)
-   [Verbindungs fähige Objekt Schnittstellen](connectable-object-interfaces.md)

 

 




