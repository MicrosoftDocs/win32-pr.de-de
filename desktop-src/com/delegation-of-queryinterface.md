---
title: Delegierung von QueryInterface
description: Delegierung von QueryInterface
ms.assetid: c5c1b584-9ca3-4dc4-a769-0142e5d8790a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c63a9eb336bcf049877957bd55523ee70de489263bd19e0ebece8b65fbdd0ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501210"
---
# <a name="delegation-of-queryinterface"></a>Delegierung von QueryInterface

Handler, die Zugriff auf einige der internen Schnittstellen im Proxy-Manager benötigen, müssen die [**IInternalUnknown-Schnittstelle**](/windows/win32/api/objidlbase/nn-objidlbase-iinternalunknown) verwenden. Dadurch wird verhindert, dass Handler die internen Schnittstellen des Aggregats außerhalb des Aggregats blind delegieren und verfügbar machen. Zu diesen Schnittstellen [**gehören IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) und [**IMultiQI.**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi) Wenn der Handler **IClientSecurity** oder **IMultiQI verfügbar** machen möchte, sollte er sie selbst implementieren.

Im Fall von [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)sollte der Handler die Sicherheit für den zugrunde liegenden Netzwerkschnittstellenproxy festlegen, wenn der Client versucht, die Sicherheit für eine Schnittstelle, die der Handler verfügbar gemacht hat, zu erhöhen.

Im Fall von [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi)sollte der Handler die Schnittstellen ausfüllen, über die er weiß, und dann den Aufruf an den Proxy-Manager weiterversetzen, um die restlichen Schnittstellen ausgefüllt zu erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Der LightweightClient-Side Handler](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 