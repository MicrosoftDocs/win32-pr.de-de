---
title: Zeigermoniker
description: Ein zeigermoniker identifiziert ein Objekt, das nur im aktiven oder aktiven Zustand vorhanden sein kann. Dies unterscheidet sich von anderen Klassen von Monikern, die Objekte identifizieren, die im passiven oder aktiven Zustand vorhanden sein können.
ms.assetid: 9895f03d-7110-41c1-a934-87010f9ad380
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebebfce908571b69a5b8ce05f589a4ca4b30977
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "104389745"
---
# <a name="pointer-monikers"></a>Zeigermoniker

Ein *zeigermoniker* identifiziert ein Objekt, das nur im aktiven oder aktiven Zustand vorhanden sein kann. Dies unterscheidet sich von anderen Klassen von Monikern, die Objekte identifizieren, die im passiven oder aktiven Zustand vorhanden sein können.

Angenommen, eine Anwendung verfügt über ein Objekt, das über keine permanente Darstellung verfügt. Wenn ein Client der Anwendung Zugriff auf dieses Objekt benötigt, können Sie den Client in der Regel einfach einem Zeiger auf das-Objekt übergeben. Angenommen, der Client erwartet einen Moniker. Das Objekt kann nicht mit einem dateimoniker identifiziert werden, weil es nicht in einer Datei gespeichert ist, und nicht mit einem elementmoniker, weil es nicht in einem anderen Objekt enthalten ist.

Stattdessen kann die Anwendung einen zeigermoniker erstellen, bei dem es sich um einen Moniker handelt, der intern einen Zeiger enthält, und diesen an den Client übergibt. Dieser Moniker kann vom Client wie jeder andere behandelt werden. Wenn der Client jedoch [**IMoniker:: bindungobject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) für den zeigermoniker aufruft, überprüft der monikercode nicht die laufende Objekttabelle (rot) oder lädt nichts aus dem Speicher. Stattdessen ruft der monikercode einfach [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) für den im Moniker gespeicherten Zeiger auf.

Zeiger Moniker erlauben, dass Objekte, die nur im Status aktiv oder wird ausgeführt werden, an monikervorgängen teilnehmen und von monikerclients verwendet werden. Ein wichtiger Unterschied zwischen Zeiger Monikern und anderen Klassen von Monikern besteht darin, dass Zeiger Moniker nicht im persistenten Speicher gespeichert werden können. Wenn Sie dies tun, gibt der Aufruf der [**IMoniker:: Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-save) -Methode einen Fehler zurück. Dies bedeutet, dass Zeiger Moniker nur in speziellen Situationen nützlich sind. Sie können die Funktion " [**kreatepointermoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) " verwenden, wenn Sie einen zeigermoniker verwenden müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anti-Moniker](anti-monikers.md)
</dt> <dt>

[Klassenmoniker](class-monikers.md)
</dt> <dt>

[Zusammengesetzte Moniker](composite-monikers.md)
</dt> <dt>

[Dateimoniker](file-monikers.md)
</dt> <dt>

[Elementmoniker](item-monikers.md)
</dt> </dl>

 

 




