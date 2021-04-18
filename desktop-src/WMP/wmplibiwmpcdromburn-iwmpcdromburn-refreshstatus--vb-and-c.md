---
title: Iwmpcdromburn-aktuasestatus-Methode
description: Die Aktualisierungs Status-Methode aktualisiert die Statusinformationen für die aktuelle Burn-Wiedergabeliste.
ms.assetid: 4dd90e76-92b5-4a00-b027-b54502e56804
keywords:
- aktuasestatusmethode Windows Media Player
- aktuasestatusmethode Windows Media Player, iwmpcdromburn-Schnittstelle
- Iwmpcdromburn Interface, Windows Media Player, aktuaktuasestatusmethode
topic_type:
- apiref
api_name:
- IWMPCdromBurn.refreshStatus
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55205e684d055d20c8e8f218ba58716de8472916
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364778"
---
# <a name="iwmpcdromburnrefreshstatus-method"></a><span data-ttu-id="7e0d2-106">Iwmpcdromburn:: erfrischendes Status-Methode</span><span class="sxs-lookup"><span data-stu-id="7e0d2-106">IWMPCdromBurn::refreshStatus method</span></span>

<span data-ttu-id="7e0d2-107">Die Aktualisierungs **Status** -Methode aktualisiert die Statusinformationen für die aktuelle Burn-Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="7e0d2-107">The **refreshStatus** method updates the status information for the current burn playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e0d2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e0d2-108">Syntax</span></span>


```CSharp
public void refreshStatus();
```


```VB

Public Sub refreshStatus()
Implements IWMPCdromBurn.refreshStatus
```





## <a name="parameters"></a><span data-ttu-id="7e0d2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e0d2-109">Parameters</span></span>

<span data-ttu-id="7e0d2-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7e0d2-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7e0d2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e0d2-111">Return value</span></span>

<span data-ttu-id="7e0d2-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7e0d2-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e0d2-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e0d2-113">Remarks</span></span>

<span data-ttu-id="7e0d2-114">Rufen Sie diese Methode auf, nachdem Sie eine Burn-Wiedergabeliste erstellt oder geändert haben, bevor Sie die Statusinformationen lesen oder die CD brennen.</span><span class="sxs-lookup"><span data-stu-id="7e0d2-114">You should call this method after you create or change a burn playlist before reading status information or burning the CD.</span></span> <span data-ttu-id="7e0d2-115">Sie können testen, ob eine Aktualisierung erforderlich ist, indem Sie den Wert von **burnstate** und die Überprüfung auf wmpbsrefresh statuausgaben durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="7e0d2-115">You can test whether a refresh is required by getting the value of **burnState** and checking for wmpbsRefreshStatusPending.</span></span>

<span data-ttu-id="7e0d2-116">Das Aktualisieren des Status ist ein synchroner Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7e0d2-116">Refreshing the status is a synchronous operation.</span></span> <span data-ttu-id="7e0d2-117">Dies bedeutet, dass eine lange Zeitspanne vergehen kann, bevor diese Methode zurückgibt, wenn die aktuelle Burn-Wiedergabeliste groß ist und viele Änderungen enthält.</span><span class="sxs-lookup"><span data-stu-id="7e0d2-117">This means that a lengthy period of time might elapse before this method returns if the current burn playlist is large and contains many changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e0d2-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e0d2-118">Requirements</span></span>



| <span data-ttu-id="7e0d2-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e0d2-119">Requirement</span></span> | <span data-ttu-id="7e0d2-120">Wert</span><span class="sxs-lookup"><span data-stu-id="7e0d2-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e0d2-121">Version</span><span class="sxs-lookup"><span data-stu-id="7e0d2-121">Version</span></span><br/>   | <span data-ttu-id="7e0d2-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="7e0d2-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="7e0d2-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="7e0d2-123">Namespace</span></span><br/> | <span data-ttu-id="7e0d2-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="7e0d2-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7e0d2-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="7e0d2-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7e0d2-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7e0d2-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e0d2-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e0d2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e0d2-128">**Iwmpcdromburn-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="7e0d2-128">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e0d2-129">**Iwmpcdromburn. burnstate (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="7e0d2-129">**IWMPCdromBurn.burnState (VB and C#)**</span></span>](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e0d2-130">**Wmpburnstate**</span><span class="sxs-lookup"><span data-stu-id="7e0d2-130">**WMPBurnState**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





