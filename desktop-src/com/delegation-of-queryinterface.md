---
title: Delegierung von QueryInterface
description: Delegierung von QueryInterface
ms.assetid: c5c1b584-9ca3-4dc4-a769-0142e5d8790a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e062f3d063d4f23c941182d80170cec0a680c6f3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102399"
---
# <a name="delegation-of-queryinterface"></a>Delegierung von QueryInterface

Handler, die Zugriff auf einige der internen Schnittstellen im Proxy-Manager benötigen, müssen die [**iinternalunknown**](/windows/win32/api/objidlbase/nn-objidlbase-iinternalunknown) -Schnittstelle durchlaufen. Dadurch wird verhindert, dass Handler die internen Schnittstellen von aggregatee außerhalb des Aggregats Blind delegieren und verfügbar machen. Zu diesen Schnittstellen gehören [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) und [**imultiqi**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi). Wenn der Handler **IClientSecurity** oder **imultiqi** verfügbar machen möchte, sollte er Sie selbst implementieren.

Im Fall von [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity), wenn der Client versucht, die Sicherheit für eine Schnittstelle festzulegen, die der Handler verfügbar gemacht hat, sollte der Handler die Sicherheit für den zugrunde liegenden Netzwerkschnittstellen Proxy festlegen.

Im Fall von [**imultiqi**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi)sollte der Handler die Schnittstellen, die ihm bekannt sind, ausfüllen und dann den-Befehl an den Proxy Manager weiterleiten, um die restlichen Schnittstellen zu erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Der Lightweight Client-Side-Handler](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 