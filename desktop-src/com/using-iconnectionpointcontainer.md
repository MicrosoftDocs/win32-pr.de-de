---
title: Verwenden von IConnectionPointContainer
description: Verwenden von IConnectionPointContainer
ms.assetid: a87afb25-4d45-4ce2-9b27-840da5107bce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d0b7c691e1ba6a8445af56978b43a2ccbf33e7
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "106341701"
---
# <a name="using-iconnectionpointcontainer"></a>Verwenden von IConnectionPointContainer

Ein Verbindungs fähigen-Objekt implementiert [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) (und macht es über [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))verfügbar), um anzugeben, dass ausgehende Schnittstellen vorhanden sind. Für jede ausgehende Schnittstelle verwaltet das Verbindungs fähigen-Objekt ein Verbindungspunkt-unter Objekt, das [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint)implementiert. Das Verbindungs fähigen-Objekt enthält daher die Verbindungspunkte, daher die Benennung von **IConnectionPointContainer** und **IConnectionPoint**.

Über [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer)kann ein Client zwei Vorgänge ausführen. Wenn der Client bereits über die IID für eine ausgehende Schnittstelle verfügt, die er unterstützt, kann er zunächst den entsprechenden Verbindungspunkt für die IID mithilfe von [**IConnectionPointContainer:: FindConnectionPoint**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint)finden. Der Client kann den Verbindungspunkt nicht direkt Abfragen, weil die Container/enthaltene Beziehung zwischen dem Verbindungs fähigen-Objekt und den darin enthaltenen Verbindungs Punkten besteht. Im Grunde ist **FindConnectionPoint** die [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) für ausgehende Schnittstellen, wenn die IID dem Client bekannt ist.

Zweitens kann der Client alle Verbindungspunkte innerhalb des Verbindungs fähigen Objekts über [**IConnectionPointContainer:: EnumConnectionPoints**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-enumconnectionpoints)auflisten. Diese Methode gibt einen [**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) -Schnittstellen Zeiger für ein separates Enumeratorobjekt zurück. Über [**IEnumConnectionPoints:: Next**](/windows/desktop/api/ocidl/nf-ocidl-ienumconnectionpoints-next)kann der Client [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) -Schnittstellen Zeiger auf jeden Verbindungspunkt abrufen.

Nachdem der Client die [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) -Schnittstelle abgerufen hat, muss er [**IConnectionPoint:: GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) aufrufen, um die IID der ausgehenden Schnittstelle zu ermitteln, die von den einzelnen Verbindungs Punkten unterstützt wird. Wenn der Client diese ausgehende Schnittstelle bereits unterstützt, kann er eine Verbindung herstellen. Andernfalls kann die ausgehende Schnittstelle weiterhin unterstützt werden, indem Informationen aus der Typbibliothek des Verbindungs fähigen-Objekts verwendet werden, um zur Laufzeit Unterstützung bereitzustellen. Diese Technik erfordert, dass das Verbindungs fähigen-Objekt die [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) -Schnittstelle unterstützt. (Weitere Informationen finden [Sie unter Verwenden von IProvideClassInfo](using-iprovideclassinfo.md).)

Da der Enumerator ein separates Objekt ist, muss der Client **IEnumConnectionPoints:: Release** abrufen, wenn der Enumerator nicht mehr benötigt wird. Außerdem ist jeder Verbindungspunkt ein Objekt mit einem separaten Verweis Zähler aus dem enthaltenden Verbindungs fähigen-Objekt. Daher muss der Client auch IConnectionPoint:: Release für jeden Verbindungspunkt aufrufen, auf den über den Enumerator oder durch [**FindConnectionPoint**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint)zugegriffen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbindungs fähige Objekt Schnittstellen](connectable-object-interfaces.md)
</dt> </dl>

 

 




