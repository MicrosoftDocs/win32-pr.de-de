---
title: Verbindungs fähige Objekt Schnittstellen
description: Verbindungs fähige Objekt Schnittstellen
ms.assetid: 136fb7bd-7a38-4051-b47b-3d08f1dbee79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc2d747d7aabe25788c34d80bddb8ca1466e9c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856908"
---
# <a name="connectable-object-interfaces"></a>Verbindungs fähige Objekt Schnittstellen

Die Unterstützung für Verbindungs fähige Objekte erfordert die Unterstützung für vier Schnittstellen:

-   [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) für das Verbindungs fähigen-Objekt
-   [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) für das Verbindungspunkt Objekt
-   [**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints) für ein Enumeratorobjekt
-   [**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) für ein Enumeratorobjekt

Die beiden letzteren sind als standardenumeratoren für die Typen **IConnectionPoint \*** und [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata)definiert.

Außerdem kann das Verbindungs fähigen-Objekt optional [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) und [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) unterstützen, um für einen Client ausreichend Informationen bereitzustellen, damit der Client zur Laufzeit Unterstützung für die ausgehende Schnittstelle bereitstellen kann.

Schließlich muss der Client ein Sink-Objekt bereitstellen, das die ausgehende Schnittstelle implementiert. Dies ist eine benutzerdefinierte COM-Schnittstelle, die vom Verbindungs fähigen-Objekt definiert wird.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Verwenden von IConnectionPointContainer](using-iconnectionpointcontainer.md)
-   [Verwenden von IConnectionPoint](using-iconnectionpoint.md)
-   [Verwenden von IProvideClassInfo](using-iprovideclassinfo.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Architektur von Verbindungs fähigen Objekten](architecture-of-connectable-objects.md)
</dt> </dl>

 

 




