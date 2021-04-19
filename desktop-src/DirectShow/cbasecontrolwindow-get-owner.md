---
description: Mit der Methode "Get Owner" wird \_ der aktuelle Fenster Besitzer abgerufen.
ms.assetid: f0eea5e7-4dfa-4973-ae12-487657e6be80
title: CBaseControlWindow.get_Owner-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Owner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8f8e3d4a331dbc66397a7b0058fcefcede2cdbb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370710"
---
# <a name="cbasecontrolwindowget_owner-method"></a><span data-ttu-id="d5ba3-103">Cbasecontrolwindow. get \_ Owner-Methode</span><span class="sxs-lookup"><span data-stu-id="d5ba3-103">CBaseControlWindow.get\_Owner method</span></span>

<span data-ttu-id="d5ba3-104">Die- `get_Owner` Methode ruft den aktuellen Fenster Besitzer ab.</span><span class="sxs-lookup"><span data-stu-id="d5ba3-104">The `get_Owner` method retrieves the current window owner.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5ba3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5ba3-105">Syntax</span></span>


```C++
HRESULT get_Owner(
   OAHWND *Owner
);
```



## <a name="parameters"></a><span data-ttu-id="d5ba3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5ba3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5ba3-107">*Besitzer*</span><span class="sxs-lookup"><span data-stu-id="d5ba3-107">*Owner*</span></span> 
</dt> <dd>

<span data-ttu-id="d5ba3-108">Zeiger auf den Fenster Besitzer.</span><span class="sxs-lookup"><span data-stu-id="d5ba3-108">Pointer to the window owner.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5ba3-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5ba3-109">Return value</span></span>

<span data-ttu-id="d5ba3-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d5ba3-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5ba3-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5ba3-111">Remarks</span></span>

<span data-ttu-id="d5ba3-112">Das Videofenster kann innerhalb einer Dokument Umgebung wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d5ba3-112">The video window can play back within a document environment.</span></span> <span data-ttu-id="d5ba3-113">Zu diesem Zweck muss das Fenster als untergeordnetes Element eines anderen Fensters erstellt werden (sodass es abgeschnitten und entsprechend verschoben wird).</span><span class="sxs-lookup"><span data-stu-id="d5ba3-113">To do this, the window must be made a child of another window (so that it is clipped and moved appropriately).</span></span> <span data-ttu-id="d5ba3-114">Mit dieser Eigenschaft kann der Besitzer des Fensters festgelegt und abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d5ba3-114">This property allows the owner of the window to be set and retrieved.</span></span> <span data-ttu-id="d5ba3-115">Wenn das Fenster im Besitz eines anderen Fensters ist, wird einfach die Microsoft Win32-Funktion " **SetParent** " aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="d5ba3-115">When the window is owned by another window, it simply calls the Microsoft Win32 **SetParent** function.</span></span> <span data-ttu-id="d5ba3-116">Eine Anwendung, die diese Funktion aufrufen, ändert die Fenster Stile, um das untergeordnete WS-Bit festzulegen \_ .</span><span class="sxs-lookup"><span data-stu-id="d5ba3-116">An application calling this function will change the window styles to set the WS\_CHILD bit on.</span></span>

<span data-ttu-id="d5ba3-117">Wenn sich das Fenster im Besitz eines anderen Fensters befindet, werden automatisch bestimmte Nachrichten Sätze (insbesondere Maus-und Tastatur Meldungen) weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="d5ba3-117">When the window is owned by another window, it will automatically forward certain sets of messages (in particular, mouse and keyboard messages).</span></span> <span data-ttu-id="d5ba3-118">Dies ermöglicht es einer Anwendung, eine einfache Bearbeitung von Hot-Spot und andere Interaktionen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="d5ba3-118">This allows an application to do simple hot-spot editing and other interactions.</span></span>

<span data-ttu-id="d5ba3-119">Diese Member-Funktion soll von externen Objekten über die [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Schnittstelle aufgerufen werden und sperrt daher den kritischen Abschnitt, um mit dem zugeordneten Filter synchronisiert zu werden.</span><span class="sxs-lookup"><span data-stu-id="d5ba3-119">This member function is meant to be called by external objects through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, and therefore locks the critical section to synchronize with the associated filter.</span></span> <span data-ttu-id="d5ba3-120">Rufen Sie die Member-Funktion [**cbasecontrolwindow:: getownerwindow**](cbasecontrolwindow-getownerwindow.md) auf, um diese Eigenschaft abzurufen, wenn Sie nicht von einem externen Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d5ba3-120">Call the [**CBaseControlWindow::GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md) member function to retrieve this property if not calling from an external object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5ba3-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5ba3-121">Requirements</span></span>



| <span data-ttu-id="d5ba3-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5ba3-122">Requirement</span></span> | <span data-ttu-id="d5ba3-123">Wert</span><span class="sxs-lookup"><span data-stu-id="d5ba3-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5ba3-124">Header</span><span class="sxs-lookup"><span data-stu-id="d5ba3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d5ba3-125"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5ba3-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d5ba3-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d5ba3-126">Library</span></span><br/> | <dl> <span data-ttu-id="d5ba3-127">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d5ba3-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5ba3-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5ba3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5ba3-129">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d5ba3-129">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




