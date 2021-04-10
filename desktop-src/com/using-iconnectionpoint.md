---
title: Verwenden von IConnectionPoint
description: Verwenden von IConnectionPoint
ms.assetid: afd50b84-1fd6-47ad-a3ef-e8b4a725b72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7aa758ec1bd40233b1cc41a6c375ed296fc167
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039633"
---
# <a name="using-iconnectionpoint"></a>Verwenden von IConnectionPoint

Wenn der Client einen Zeiger auf einen Verbindungspunkt hat, kann er die folgenden Vorgänge ausführen, wie über [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint)ausgedrückt:

-   Zuerst ruft [**IConnectionPoint:: GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) die IID der ausgehenden Schnittstelle ab, die vom Verbindungspunkt unterstützt wird. Bei Verwendung in Verbindung mit [**IEnumConnectionPoints**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints)ermöglicht diese Methode dem Client, die IIDs aller ausgehenden Schnittstellen zu überprüfen, die für das Verbindungs fähige Objekt unterstützt werden.
-   Zweitens kann ein Client über die [**IConnectionPoint:: GetConnectionPointContainer**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectionpointcontainer) -Methode vom Verbindungspunkt zurück zur [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) -Schnittstelle des Verbindungs fähigen-Objekts navigieren.
-   Drittens sind die interessantesten Methoden für den Client [**IConnectionPoint:: Rat**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) und [**IConnectionPoint:: Unrat**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-unadvise). Wenn ein Client ein eigenes Sink-Objekt mit dem Verbindungs fähigen-Objekt verbinden möchte, übergibt der Client den [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Zeiger der Senke (oder einen anderen Schnittstellen Zeiger auf das gleiche Objekt), um zu **informieren**. Der Verbindungspunkt fragt die Senke nach der spezifischen ausgehenden Schnittstelle ab, die erwartet wird. Wenn diese Schnittstelle in der Senke verfügbar ist, speichert der Verbindungspunkt den Schnittstellen Zeiger. Ab diesem **Punkt führt das** Verbindungs fähigen-Objekt über diese Schnittstelle Aufrufe an die Senke, wenn Ereignisse auftreten. Um die Senke vom Verbindungspunkt aus zu trennen, übergibt der Client einen von der **Empfehlung** zurückgegebenen Schlüssel an die **unempfehlung** -Methode. **Nicht Empfehlung** muss [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) auf der Senke-Schnittstelle aufzurufen.
-   Zum Schluss kann ein Client einen Verbindungspunkt anweisen, alle Verbindungen mit ihm aufzulisten, die über [**IConnectionPoint:: EnumConnections**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-enumconnections)vorhanden sind. Diese Methode erstellt ein Enumeratorobjekt (mit einem separaten Verweis Zähler), das einen [**IEnumConnections**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) -Zeiger darauf zurückgibt. Der Client muss [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) aufzurufen, wenn der Enumerator nicht mehr benötigt wird. Außerdem gibt der Enumerator eine Reihe von [**CONNECTDATA**](/windows/win32/api/ocidl/ns-ocidl-connectdata) -Strukturen zurück, jeweils eine für jede Verbindung. Jede Struktur beschreibt eine Verbindung mithilfe des [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Zeigers der Senke und des ursprünglich von der [**Empfehlung**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise)zurückgegebenen Verbindungs Schlüssels. Wenn diese Senke-Schnittstellen Zeiger erreicht werden, muss der Client **Release** für jeden Zeiger, der in einer **CONNECTDATA** -Struktur zurückgegeben wird, abrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbindungs fähige Objekt Schnittstellen](connectable-object-interfaces.md)
</dt> </dl>

 

 