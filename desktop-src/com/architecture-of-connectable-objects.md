---
title: Architektur von Verbindungs fähigen Objekten
description: Architektur von Verbindungs fähigen Objekten
ms.assetid: 69949a3b-3ab8-4054-84d8-9256fbf39c7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9d8d2909942d1c04aed972e7891a6f4ae3f730
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "106373402"
---
# <a name="architecture-of-connectable-objects"></a>Architektur von Verbindungs fähigen Objekten

Das Verbindungs fähigen-Objekt ist nur ein Teil der allgemeinen Architektur von Verbindungs fähigen Objekten. Diese Technologie umfasst die folgenden Elemente:

-   **Connectable-Objekt.** Implementiert die [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) -Schnittstelle. erstellt mindestens ein Verbindungspunkt Objekt. definiert eine ausgehende Schnittstelle für den Client.
-   **Ent.** Fragt das Objekt für [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) ab, um zu bestimmen, ob das Objekt eine Verbindung herstellt. erstellt ein Sink-Objekt, um die vom Verbindungs fähigen-Objekt definierte ausgehende Schnittstelle zu implementieren.
-   **Sink-Objekt.** Implementiert die ausgehende Schnittstelle. wird verwendet, um eine Verbindung mit dem Verbindungs fähigen-Objekt herzustellen.
-   **Verbindungspunkt Objekt.** Implementiert die [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) -Schnittstelle und verwaltet die Verbindung mit der Senke des Clients.

Die Beziehungen zwischen Client, Verbindungs fähiges Objekt, Verbindungspunkt und Senke werden im folgenden Diagramm veranschaulicht:

![Diagramm, das die Verbindungspunkte zwischen dem Client und dem Verbindungs fähigen Objekt anzeigt.](images/1cd44fec-5d2c-4427-846b-ccab7ec0b08a.png)

Bevor das Verbindungspunkt Objektmethoden in der Sink-Schnittstelle in Schritt 3 im vorangehenden Diagramm aufruft, muss es [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) für die jeweilige erforderliche Schnittstelle sein, auch wenn der Zeiger bereits im Schritt 2-Aufruf der Methode " [**Empfehlung**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) " weitergegeben wurde.

Zwei Enumeratorobjekte sind auch an dieser Architektur beteiligt, aber in der Abbildung nicht dargestellt. Eine wird von einer Methode in [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) erstellt, um die Verbindungspunkte innerhalb des Verbindungs fähigen Objekts aufzulisten. Der andere wird von einer Methode in [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) erstellt, um die Verbindungen aufzulisten, die derzeit mit diesem Verbindungspunkt hergestellt werden. Ein Verbindungspunkt kann mehrere verbundene Sink-Schnittstellen unterstützen und die Liste der Verbindungen jedes Mal durchlaufen, wenn ein Methodenaufruf an diese Schnittstelle erfolgt. Dieser Prozess wird als Multicasting bezeichnet.

Beim Arbeiten mit Verbindungs fähigen Objekten ist es wichtig zu verstehen, dass das Verbindungs fähige Objekt, jeder Verbindungspunkt, jede Senke und alle Enumeratoren separate Objekte mit separaten [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Implementierungen, separaten Verweis Zählungen und separaten Lebens dauern aufweisen. Ein Client, der diese Objekte verwendet, ist immer für die Freigabe aller Verweis Zähler zuständig, die er besitzt.

> [!Note]  
> Ein Verbindungs fähiges Objekt kann mehr als einen Client unterstützen und mehrere senken innerhalb eines Clients unterstützen. Ebenso kann eine Senke mit mehr als einem Verbindungs fähigen Objekt verbunden werden.

 

Die Schritte zum Herstellen einer Verbindung zwischen einem Client und einem Verbindungs fähigen Objekt lauten wie folgt:

1.  Der Client fragt [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) für das-Objekt ab, um zu bestimmen, ob das Objekt verbunden ist. Wenn dieser Vorgang erfolgreich ist, enthält der Client einen Zeiger auf die **IConnectionPointContainer** -Schnittstelle für das Verbindungs fähigen-Objekt, und der Verbindungs fähigen-Objekt Verweis-Counter wurde inkrementiert. Andernfalls ist das Objekt nicht Verbindungs fähigen und unterstützt keine ausgehenden Schnittstellen.
2.  Wenn das Objekt verbunden ist, versucht der Client als nächstes, einen Zeiger auf die [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) -Schnittstelle an einem Verbindungspunkt innerhalb des Verbindungs fähigen Objekts abzurufen. Es gibt zwei Methoden zum Abrufen dieses Zeigers: sowohl in [**IConnectionPointContainer:: FindConnectionPoint**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) als auch in [**IConnectionPointContainer:: EnumConnectionPoints**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-enumconnectionpoints). Wenn ' **EnumConnectionPoints** ' verwendet wird, sind einige zusätzliche Schritte erforderlich. (Weitere Informationen finden [Sie unter Verwenden von IConnectionPointContainer](using-iconnectionpointcontainer.md) .) Wenn der Vorgang erfolgreich ist, unterstützen das Verbindungs fähige Objekt und der Client die gleiche ausgehende Schnittstelle. Das Verbindungs fähige Objekt definiert es und ruft es auf, und der Client implementiert es. Der Client kann dann über den Verbindungspunkt innerhalb des Verbindungs fähigen Objekts kommunizieren.
3.  Der Client ruft dann die [**Empfehlung**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) auf dem Verbindungspunkt auf, um eine Verbindung zwischen der Senke-Schnittstelle und dem Verbindungspunkt des Objekts herzustellen. Nach diesem-Befehl enthält der Verbindungspunkt des Objekts einen Zeiger auf die ausgehende Schnittstelle in der Senke.
4.  Der Code in der [**Empfehlung**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) ruft [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) für den übergebenen Schnittstellen Zeiger auf und fragt den spezifischen Schnittstellen Bezeichner ab, mit dem eine Verbindung hergestellt wird.
5.  Das-Objekt ruft bei Bedarf Methoden auf der-Schnittstelle der Senke auf und verwendet dabei den Zeiger, der vom Verbindungspunkt gehalten wird.
6.  Der Client ruft [**unempfehlung**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-unadvise) auf, um die Verbindung zu beenden. Dann ruft der Client **IConnectionPoint:: Release** auf, um seinen Halt für den Verbindungspunkt freizugeben, und somit auch das Haupt Verbindungs fähige Objekt. Der Client muss auch **IConnectionPointContainer:: Release** anrufen, um seinen Halt für das zentrale Verbindungs fähigen-Objekt freizugeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbindungs fähige Objekt Schnittstellen](connectable-object-interfaces.md)
</dt> </dl>

 

 




