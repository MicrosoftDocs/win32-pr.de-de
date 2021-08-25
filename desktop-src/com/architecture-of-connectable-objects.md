---
title: Architektur von miteinander verbundenen Objekten
description: Architektur von miteinander verbundenen Objekten
ms.assetid: 69949a3b-3ab8-4054-84d8-9256fbf39c7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1215b013c3db751e90b07ed21d5f897ef0332000ce2cd2b3b167cbe86798927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993955"
---
# <a name="architecture-of-connectable-objects"></a>Architektur von miteinander verbundenen Objekten

Das verbindungsfähige Objekt ist nur ein Teil der Gesamtarchitektur von miteinander verbundenen Objekten. Diese Technologie umfasst die folgenden Elemente:

-   **Verbindungsfähiges Objekt.** Implementiert die [**IConnectionPointContainer-Schnittstelle.**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) erstellt mindestens ein Verbindungspunktobjekt. definiert eine ausgehende Schnittstelle für den Client.
-   **Kunde.** Fragt das -Objekt nach [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) ab, um zu bestimmen, ob das Objekt verbunden werden kann. erstellt ein Senkenobjekt, um die ausgehende Schnittstelle zu implementieren, die durch das verbindungsfähige Objekt definiert wird.
-   **Senkenobjekt.** Implementiert die ausgehende Schnittstelle. wird verwendet, um eine Verbindung mit dem verbindungsfähigen Objekt herzustellen.
-   **Verbindungspunktobjekt.** Implementiert die [**IConnectionPoint-Schnittstelle**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) und verwaltet die Verbindung mit der Senke des Clients.

Die Beziehungen zwischen Client, verbindungsfähigem Objekt, Einem Verbindungspunkt und einer Senke sind im folgenden Diagramm dargestellt:

![Diagramm, das die Verbindungspunkte zwischen dem Client und dem verbindungsfähigen Objekt zeigt.](images/1cd44fec-5d2c-4427-846b-ccab7ec0b08a.png)

Bevor das Verbindungspunktobjekt Methoden in der Senkenschnittstelle in Schritt 3 im vorherigen Diagramm aufruft, muss es [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) für die spezifische erforderliche Schnittstelle verwenden, auch wenn der Zeiger bereits im Schritt 2-Aufruf der [**Advise-Methode**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) übergeben wurde.

Zwei Enumeratorobjekte sind auch an dieser Architektur beteiligt, aber nicht in der Abbildung dargestellt. Eine wird von einer Methode in [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) erstellt, um die Verbindungspunkte innerhalb des verbindungsfähigen Objekts aufzuzählen. Der andere wird von einer Methode in [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) erstellt, um die verbindungen aufzuzählen, die derzeit mit diesem Verbindungspunkt hergestellt werden. Ein Verbindungspunkt kann mehrere verbundene Senkenschnittstellen unterstützen und sollte die Liste der Verbindungen jedes Mal durchlaufen, wenn er einen Methodenaufruf für diese Schnittstelle vornimmt. Dieser Prozess wird als Multicasting bezeichnet.

Bei der Arbeit mit miteinander verbundenen Objekten ist es wichtig zu verstehen, dass das verbindungsfähige Objekt, jeder Verbindungspunkt, jede Senke und alle Enumeratoren separate Objekte mit separaten [**IUnknown-Implementierungen,**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) separaten Verweiszählern und separaten Lebensdauern sind. Ein Client, der diese Objekte verwendet, ist immer für die Freigabe aller Verweisanzahlen verantwortlich, die er besitzt.

> [!Note]  
> Ein verbindungsfähiges Objekt kann mehrere Clients und mehrere Senken innerhalb eines Clients unterstützen. Ebenso kann eine Senke mit mehreren miteinander verbundenen Objekten verbunden werden.

 

Die Schritte zum Herstellen einer Verbindung zwischen einem Client und einem verbindungsfähigen Objekt sind wie folgt:

1.  Der Client fragt [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) für das Objekt ab, um zu bestimmen, ob das Objekt verbunden werden kann. Wenn dieser Aufruf erfolgreich ist, enthält der Client einen Zeiger auf die **IConnectionPointContainer-Schnittstelle** für das verbindungsfähige Objekt, und der Verweiszähler für das verbindungsfähige Objekt wurde erhöht. Andernfalls ist das Objekt nicht verbindungsfähig und unterstützt keine ausgehenden Schnittstellen.
2.  Wenn das Objekt verbunden werden kann, versucht der Client als Nächstes, einen Zeiger auf die [**IConnectionPoint-Schnittstelle**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) auf einem Verbindungspunkt innerhalb des verbindungsfähigen Objekts abzurufen. Es gibt zwei Methoden zum Abrufen dieses Zeigers, sowohl in [**IConnectionPointContainer::FindConnectionPoint**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) als auch in [**IConnectionPointContainer::EnumConnectionPoints.**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-enumconnectionpoints) Wenn **EnumConnectionPoints** verwendet wird, sind einige zusätzliche Schritte erforderlich. (Weitere Informationen finden Sie unter [Verwenden von IConnectionPointContainer.)](using-iconnectionpointcontainer.md) Bei Erfolg unterstützen das verbindungsfähige Objekt und der Client die gleiche ausgehende Schnittstelle. Das verbindungsfähige Objekt definiert es und ruft es auf, und der Client implementiert es. Der Client kann dann über den Verbindungspunkt innerhalb des verbindungsfähigen Objekts kommunizieren.
3.  Der Client ruft dann [**Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) für den Verbindungspunkt auf, um eine Verbindung zwischen seiner Senkenschnittstelle und dem Verbindungspunkt des Objekts herzustellen. Nach diesem Aufruf enthält der Verbindungspunkt des Objekts einen Zeiger auf die ausgehende Schnittstelle in der Senke.
4.  Der Code in [**Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) ruft [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) für den übergebenen Schnittstellenzeiger auf und fragt nach dem spezifischen Schnittstellenbezeichner, mit dem eine Verbindung hergestellt wird.
5.  Das -Objekt ruft methoden für die Schnittstelle der Senke nach Bedarf auf, wobei der von seinem Verbindungspunkt gehaltene Zeiger verwendet wird.
6.  Der Client ruft [**Unadvise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-unadvise) auf, um die Verbindung zu beenden. Anschließend ruft der Client **IConnectionPoint::Release** auf, um die Aufbewahrung auf dem Verbindungspunkt und somit auch im Hauptverbindungsobjekt freizugeben. Der Client muss auch **IConnectionPointContainer::Release** aufrufen, um die Aufbewahrung für das main connectable-Objekt freizugeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbindende Objektschnittstellen](connectable-object-interfaces.md)
</dt> </dl>

 

 




