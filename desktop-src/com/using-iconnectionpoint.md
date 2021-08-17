---
title: Verwenden von IConnectionPoint
description: Verwenden von IConnectionPoint
ms.assetid: afd50b84-1fd6-47ad-a3ef-e8b4a725b72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2449be5f1711457807666e9e2068d13defd8437bedee93402f7b974d5298d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129422"
---
# <a name="using-iconnectionpoint"></a>Verwenden von IConnectionPoint

Wenn der Client über einen Zeiger auf einen Verbindungspunkt verfügt, kann er die folgenden Vorgänge ausführen, wie durch [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint)ausgedrückt:

-   Zuerst ruft [**IConnectionPoint::GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) die vom Verbindungspunkt unterstützte IID der ausgehenden Schnittstelle ab. Bei Verwendung in Verbindung mit [**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints)ermöglicht diese Methode dem Client, die IIDs aller ausgehenden Schnittstellen zu untersuchen, die für das verbindungsfähige Objekt unterstützt werden.
-   Zweitens kann ein Client über die [**IConnectionPoint::GetConnectionPointContainer-Methode**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectionpointcontainer) vom Verbindungspunkt zurück zur [**IConnectionPointContainer-Schnittstelle**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) des verbindungsfähigen Objekts navigieren.
-   Drittens sind die interessantesten Methoden für den Client [**IConnectionPoint::Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) und [**IConnectionPoint::Unadvise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-unadvise). Wenn ein Client sein eigenes Senkenobjekt mit dem verbindungsfähigen Objekt verbinden möchte, übergibt der Client den [**IUnknown-Zeiger**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) der Senke (oder einen anderen Schnittstellenzeiger auf demselben Objekt) an **Advise**. Der Verbindungspunkt fragt die Senke nach der spezifischen ausgehenden Schnittstelle ab, die erwartet wird. Wenn diese Schnittstelle in der Senke verfügbar ist, speichert der Verbindungspunkt den Schnittstellenzeiger. Von diesem Punkt bis zum Aufruf von **Unadvise** führt das verbindungsfähige Objekt über diese Schnittstelle Aufrufe an die Senke aus, wenn Ereignisse auftreten. Um die Senke vom Verbindungspunkt zu trennen, übergibt der Client einen von **Advise** zurückgegebenen Schlüssel an die **Unadvise-Methode.** **Unadvise** muss [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für die Senkenschnittstelle aufrufen.
-   Schließlich kann ein Client einen Verbindungspunkt bitten, alle Verbindungen mit ihm aufzuzählen, die über [**IConnectionPoint::EnumConnections**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-enumconnections)vorhanden sind. Diese Methode erstellt ein Enumeratorobjekt (mit einem separaten Verweiszähler), das einen [**IEnumConnections-Zeiger**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) darauf zurückgibt. Der Client muss [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) aufrufen, wenn der Enumerator nicht mehr benötigt wird. Darüber hinaus gibt der Enumerator eine Reihe von [**CONNECTDATA-Strukturen**](/windows/win32/api/ocidl/ns-ocidl-connectdata) zurück, eine für jede Verbindung. Jede Struktur beschreibt eine Verbindung mithilfe des [**IUnknown-Zeigers**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) der Senke sowie des Verbindungsschlüssels, der ursprünglich von [**Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise)zurückgegeben wurde. Wenn diese Senkenschnittstellenzeiger verwendet werden, muss der Client **Release** für jeden Zeiger aufrufen, der in einer **CONNECTDATA-Struktur** zurückgegeben wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbindende Objektschnittstellen](connectable-object-interfaces.md)
</dt> </dl>

 

 