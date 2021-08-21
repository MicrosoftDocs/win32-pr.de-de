---
title: Zeigermoniker
description: Ein Zeigermoniker identifiziert ein Objekt, das nur im aktiven oder ausgeführten Zustand vorhanden sein kann. Dies unterscheidet sich von anderen Klassen von Monikern, die Objekte identifizieren, die entweder im passiven oder aktiven Zustand vorhanden sein können.
ms.assetid: 9895f03d-7110-41c1-a934-87010f9ad380
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcdf96497751b3f777c292c56d35b2c04432da84b352e20c4dd8b0917dedb16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047898"
---
# <a name="pointer-monikers"></a>Zeigermoniker

Ein *Zeigermoniker* identifiziert ein Objekt, das nur im aktiven oder ausgeführten Zustand vorhanden sein kann. Dies unterscheidet sich von anderen Klassen von Monikern, die Objekte identifizieren, die entweder im passiven oder aktiven Zustand vorhanden sein können.

Angenommen, eine Anwendung verfügt über ein -Objekt, das keine persistente Darstellung hat. Wenn ein Client Ihrer Anwendung Zugriff auf dieses Objekt benötigt, können Sie dem Client normalerweise einfach einen Zeiger auf das Objekt übergeben. Angenommen, Ihr Client erwartet einen Moniker. Das Objekt kann nicht mit einem Dateimoniker identifiziert werden, da es nicht in einer Datei gespeichert ist, noch mit einem Elementmoniker, da es nicht in einem anderen Objekt enthalten ist.

Stattdessen kann Ihre Anwendung einen Zeigermoniker erstellen, bei dem es sich um einen Moniker handelt, der einfach intern einen Zeiger enthält, und diesen an den Client übergeben. Der Client kann diesen Moniker wie jeden anderen behandeln. Wenn der Client jedoch [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) für den Zeigermoniker aufruft, überprüft der Monikercode weder die ausgeführte Objekttabelle (ROT) noch lädt er etwas aus dem Speicher. Stattdessen ruft der Monikercode einfach [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) für den im Moniker gespeicherten Zeiger auf.

Zeigermoniker ermöglichen es Objekten, die nur im aktiven oder ausgeführten Zustand vorhanden sind, an Monikervorgängen teilzunehmen und von Monikerclients verwendet zu werden. Ein wichtiger Unterschied zwischen Zeigermonikern und anderen Klassen von Monikern ist, dass Zeigermoniker nicht im persistenten Speicher gespeichert werden können. Wenn Sie dies tun, gibt der Aufruf der [**IMoniker::Save-Methode**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-save) einen Fehler zurück. Dies bedeutet, dass Zeigermoniker nur in speziellen Situationen nützlich sind. Sie können die [**CreatePointerMoniker-Funktion**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) verwenden, wenn Sie einen Zeigermoniker verwenden müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Antimoniker](anti-monikers.md)
</dt> <dt>

[Klassenmoniker](class-monikers.md)
</dt> <dt>

[Zusammengesetzte Moniker](composite-monikers.md)
</dt> <dt>

[Dateimoniker](file-monikers.md)
</dt> <dt>

[Elementmoniker](item-monikers.md)
</dt> </dl>

 

 




