---
title: Verwenden von IConnectionPointContainer
description: Verwenden von IConnectionPointContainer
ms.assetid: a87afb25-4d45-4ce2-9b27-840da5107bce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a8d53e9051796cafa4a8c7825d810b18784d58a4dd5d531eb38872b87cb32c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992030"
---
# <a name="using-iconnectionpointcontainer"></a>Verwenden von IConnectionPointContainer

Ein verbindungsfähiges Objekt implementiert [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) (und macht es über [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))verfügbar), um das Vorhandensein ausgehender Schnittstellen anzugeben. Für jede ausgehende Schnittstelle verwaltet das verbindungsfähige Objekt ein Unterobjekt des Verbindungspunkts, das [**selbst IConnectionPoint implementiert.**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) Das verbindungsfähige Objekt enthält daher die Verbindungspunkte, daher die Benennung von **IConnectionPointContainer** und **IConnectionPoint**.

Über [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer)kann ein Client zwei Vorgänge ausführen. Erstens: Wenn der Client bereits über die IID für eine ausgehende Schnittstelle verfügt, die er unterstützt, kann er den entsprechenden Verbindungspunkt für die IID mithilfe von [**IConnectionPointContainer::FindConnectionPoint suchen.**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) Der Client kann den Verbindungspunkt aufgrund der Container-/Contained-Beziehung zwischen dem verbindungsierbaren Objekt und seinen enthaltenen Verbindungspunkten nicht direkt abfragen. Im Grunde **ist FindConnectionPoint** das [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) für ausgehende Schnittstellen, wenn die IID dem Client bekannt ist.

Zweitens kann der Client alle Verbindungspunkte innerhalb des verbindungsbaren Objekts über [**IConnectionPointContainer::EnumConnectionPoints aufzählen.**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-enumconnectionpoints) Diese Methode gibt einen [**IEnumConnectionPoints-Schnittstellenzeiger**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) für ein separates Enumeratorobjekt zurück. Über [**IEnumConnectionPoints::Next**](/windows/desktop/api/ocidl/nf-ocidl-ienumconnectionpoints-next)kann der Client [**IConnectionPoint-Schnittstellenzederherstellungen**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) auf jeden Verbindungspunkt abrufen.

Nachdem der Client die [**IConnectionPoint-Schnittstelle**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) erhalten hat, muss er [**IConnectionPoint::GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) aufrufen, um die IID der ausgehenden Schnittstelle zu bestimmen, die von jedem Verbindungspunkt unterstützt wird. Wenn der Client diese ausgehende Schnittstelle bereits unterstützt, kann er eine Verbindung herstellen. Andernfalls kann die ausgehende Schnittstelle möglicherweise weiterhin unterstützt werden, indem Informationen aus der Typbibliothek des verbindungsierbaren Objekts verwendet werden, um zur Laufzeit Unterstützung zu bieten. Diese Technik erfordert, dass das verbindungsfähige Objekt die [**IProvideClassInfo-Schnittstelle**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) unterstützt. (Siehe [Verwenden von IProvideClassInfo](using-iprovideclassinfo.md).)

Da der Enumerator ein separates Objekt ist, muss der Client **IEnumConnectionPoints::Release** aufrufen, wenn der Enumerator nicht mehr benötigt wird. Darüber hinaus ist jeder Verbindungspunkt ein Objekt mit einem separaten Verweiszähler vom enthaltenden verbindungsierbaren Objekt. Daher muss der Client auch IConnectionPoint::Release für jeden Verbindungspunkt aufrufen, auf den entweder über den Enumerator oder über [**FindConnectionPoint zugegriffen wird.**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schnittstellen für verbindende Objekte](connectable-object-interfaces.md)
</dt> </dl>

 

 




