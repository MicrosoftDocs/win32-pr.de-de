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
# <a name="delegation-of-queryinterface"></a><span data-ttu-id="c92ff-103">Delegierung von QueryInterface</span><span class="sxs-lookup"><span data-stu-id="c92ff-103">Delegation of QueryInterface</span></span>

<span data-ttu-id="c92ff-104">Handler, die Zugriff auf einige der internen Schnittstellen im Proxy-Manager benötigen, müssen die [**iinternalunknown**](/windows/win32/api/objidlbase/nn-objidlbase-iinternalunknown) -Schnittstelle durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="c92ff-104">Handlers that require access to some of the internal interfaces on the proxy manager have to go through the [**IInternalUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-iinternalunknown) interface.</span></span> <span data-ttu-id="c92ff-105">Dadurch wird verhindert, dass Handler die internen Schnittstellen von aggregatee außerhalb des Aggregats Blind delegieren und verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="c92ff-105">This prevents handlers from blindly delegating and exposing the aggregatee's internal interfaces outside of the aggregate.</span></span> <span data-ttu-id="c92ff-106">Zu diesen Schnittstellen gehören [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) und [**imultiqi**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi).</span><span class="sxs-lookup"><span data-stu-id="c92ff-106">These interfaces include [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) and [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi).</span></span> <span data-ttu-id="c92ff-107">Wenn der Handler **IClientSecurity** oder **imultiqi** verfügbar machen möchte, sollte er Sie selbst implementieren.</span><span class="sxs-lookup"><span data-stu-id="c92ff-107">If the handler wants to expose **IClientSecurity** or **IMultiQI**, it should implement them itself.</span></span>

<span data-ttu-id="c92ff-108">Im Fall von [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity), wenn der Client versucht, die Sicherheit für eine Schnittstelle festzulegen, die der Handler verfügbar gemacht hat, sollte der Handler die Sicherheit für den zugrunde liegenden Netzwerkschnittstellen Proxy festlegen.</span><span class="sxs-lookup"><span data-stu-id="c92ff-108">In the case of [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity), if the client tries to set the security on an interface that the handler has exposed, the handler should set the security on the underlying network interface proxy.</span></span>

<span data-ttu-id="c92ff-109">Im Fall von [**imultiqi**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi)sollte der Handler die Schnittstellen, die ihm bekannt sind, ausfüllen und dann den-Befehl an den Proxy Manager weiterleiten, um die restlichen Schnittstellen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c92ff-109">In the case of [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi), the handler should fill in the interfaces it knows about and then forward the call to the proxy manager to get the rest of the interfaces filled in.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c92ff-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c92ff-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c92ff-111">Der Lightweight Client-Side-Handler</span><span class="sxs-lookup"><span data-stu-id="c92ff-111">The Lightweight Client-Side Handler</span></span>](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 