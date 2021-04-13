---
title: IDXCoreAdapterFactory::UnregisterEventNotification
description: Hebt die Registrierung bei einer Benachrichtigung auf, die Sie zuvor für registriert haben.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6bb12126769a914680ea17ac9e6060346001c795
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390808"
---
# <a name="idxcoreadapterfactoryunregistereventnotification-method"></a><span data-ttu-id="36ef3-103">Idxcoreadapterfactory:: unregistereventnotification-Methode</span><span class="sxs-lookup"><span data-stu-id="36ef3-103">IDXCoreAdapterFactory::UnregisterEventNotification method</span></span>

<span data-ttu-id="36ef3-104">Hebt die Registrierung bei einer Benachrichtigung auf, die Sie zuvor für registriert haben.</span><span class="sxs-lookup"><span data-stu-id="36ef3-104">Unregisters from a notification that you previously registered for.</span></span> <span data-ttu-id="36ef3-105">Programmieranleitungen und Codebeispiele finden [Sie unter Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="36ef3-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="36ef3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="36ef3-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE UnregisterEventNotification(
  uint32_t eventCookie) = 0;
```

## <a name="parameters"></a><span data-ttu-id="36ef3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="36ef3-107">Parameters</span></span>

### <a name="eventcookie"></a><span data-ttu-id="36ef3-108">eventcookie</span><span class="sxs-lookup"><span data-stu-id="36ef3-108">eventCookie</span></span>

<span data-ttu-id="36ef3-109">Typ: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="36ef3-109">Type: **uint32_t**</span></span>

<span data-ttu-id="36ef3-110">Der Cookie-Wert (zurückgegeben, wenn Sie [idxcoreadapterfactory:: registereventnotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)aufgerufen haben), der eine vorherige Registrierung darstellt, für die die Registrierung aufgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="36ef3-110">The cookie value (returned when you called [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)) representing a prior registration that you now wish to unregister for.</span></span>

## <a name="returns"></a><span data-ttu-id="36ef3-111">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="36ef3-111">Returns</span></span>

<span data-ttu-id="36ef3-112">Typ: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="36ef3-112">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="36ef3-113">Wenn die Funktion erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="36ef3-113">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="36ef3-114">Andernfalls wird ein [**HRESULT**](../../com/structure-of-com-error-codes.md) - [Fehlercode](../../com/com-error-codes-10.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="36ef3-114">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="36ef3-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="36ef3-115">Return value</span></span>|<span data-ttu-id="36ef3-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36ef3-116">Description</span></span>|
|-|-|
|<span data-ttu-id="36ef3-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="36ef3-117">E_INVALIDARG</span></span>|<span data-ttu-id="36ef3-118">Der Wert von *eventcookie* ist kein gültiges Cookie, das eine vorherige Registrierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="36ef3-118">The value of *eventCookie* is not a valid cookie representing a prior registration.</span></span>|

## <a name="remarks"></a><span data-ttu-id="36ef3-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36ef3-119">Remarks</span></span>

<span data-ttu-id="36ef3-120">**Unregistereventnotification** wird erst zurückgegeben, nachdem alle ausstehenden/in-Progress-Rückrufe für diese Registrierung abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="36ef3-120">**UnregisterEventNotification** returns only after all pending/in-progress callbacks for this registration have completed.</span></span> <span data-ttu-id="36ef3-121">DXCore stellt sicher, dass für diese Registrierung keine neuen Rückrufe auftreten, nachdem **unregistereventnotification** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="36ef3-121">DXCore guarantees that no new callbacks will occur for this registration after **UnregisterEventNotification** has returned.</span></span> <span data-ttu-id="36ef3-122">Um jedoch einen Deadlock zu vermeiden, wartet **unregistereventnotification** nicht auf den Abschluss des aktiven Rückrufs, wenn Sie **unregistereventnotification** innerhalb des Rückrufs aufrufen.</span><span class="sxs-lookup"><span data-stu-id="36ef3-122">However, to avoid a deadlock, if you call **UnregisterEventNotification** from within your callback, then **UnregisterEventNotification** doesn't wait for the active callback to complete.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36ef3-123">Bevor Sie das DXCore-Objekt zerstören, das durch das *dxcoreobject* -Argument dargestellt wird, das an [idxcoreadapterfactory:: registereventnotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)übermittelt wird, müssen Sie den Cookie-Wert verwenden, um die Registrierung dieses Objekts bei Benachrichtigungen aufzuheben, indem Sie **unregistereventnotification** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="36ef3-123">Before you destroy the DXCore object represented by the *dxCoreObject* argument passed to [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), you must use the cookie value to unregister that object from notifications by calling **UnregisterEventNotification**.</span></span> <span data-ttu-id="36ef3-124">Wenn Sie dies nicht tun, wird eine schwerwiegende Ausnahme ausgelöst, wenn die Situation erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="36ef3-124">If you don't do that, then a fatal exception is raised when the situation is detected.</span></span>

<span data-ttu-id="36ef3-125">Nachdem Sie die Registrierung eines cookienwerts aufgehoben haben, kann dieser Wert von einer nachfolgenden Registrierung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="36ef3-125">Once you unregister a cookie value, that value is then eligible for being returned by a subsequent registration</span></span>

## <a name="see-also"></a><span data-ttu-id="36ef3-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36ef3-126">See also</span></span>

<span data-ttu-id="36ef3-127">[Idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md), [idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md), [idxcoreadapterfactory:: unregistereventnotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="36ef3-127">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>