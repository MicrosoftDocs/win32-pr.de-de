---
title: Iwmpcdromrip-startrip-Methode
description: Die startrip-Methode rippt die CD.
ms.assetid: 3569e29c-e593-4bdd-8afb-74e39721cf80
keywords:
- startrip-Methoden Fenster Media Player
- startrip-Methode, Windows Media Player, iwmpcdromrip-Schnittstelle
- Iwmpcdromrip-Schnittstelle, Windows Media Player, startrip-Methode
topic_type:
- apiref
api_name:
- IWMPCdromRip.startRip
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327ac9009cf1b8fb9ccfbcc460cde78ef40b3802
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355935"
---
# <a name="iwmpcdromripstartrip-method"></a><span data-ttu-id="a1707-106">Iwmpcdromrip:: startrip-Methode</span><span class="sxs-lookup"><span data-stu-id="a1707-106">IWMPCdromRip::startRip method</span></span>

<span data-ttu-id="a1707-107">Die **startrip** -Methode rippt die CD.</span><span class="sxs-lookup"><span data-stu-id="a1707-107">The **startRip** method rips the CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1707-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1707-108">Syntax</span></span>


```CSharp
public void startRip();
```


```VB

Public Sub startRip()
Implements IWMPCdromRip.startRip
```





## <a name="parameters"></a><span data-ttu-id="a1707-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1707-109">Parameters</span></span>

<span data-ttu-id="a1707-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a1707-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a1707-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1707-111">Return value</span></span>

<span data-ttu-id="a1707-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a1707-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1707-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1707-113">Remarks</span></span>

<span data-ttu-id="a1707-114">Das einreißen einer CD mithilfe der **iwmpcdromrip** -Schnittstelle hat die gleiche Wirkung wie das einreißen von Musik mithilfe der Windows Media Player-Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="a1707-114">Ripping a CD by using the **IWMPCdromRip** interface has the same effect as ripping music by using the Windows Media Player user interface.</span></span> <span data-ttu-id="a1707-115">Ausgerigter Inhalt wird der Bibliothek automatisch entsprechend den Einstellungen des Benutzers hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a1707-115">Ripped content is automatically added to the library according to the user's preferences.</span></span> <span data-ttu-id="a1707-116">Weitere Informationen zu den Benutzereinstellungen für das CD-Ripping finden Sie unter "Ripping Music from CDs" in der Windows Media Player-Hilfe.</span><span class="sxs-lookup"><span data-stu-id="a1707-116">For more information about user preferences for CD ripping, see "Ripping music from CDs" in Windows Media Player Help.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1707-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1707-117">Requirements</span></span>



| <span data-ttu-id="a1707-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1707-118">Requirement</span></span> | <span data-ttu-id="a1707-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a1707-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1707-120">Version</span><span class="sxs-lookup"><span data-stu-id="a1707-120">Version</span></span><br/>   | <span data-ttu-id="a1707-121">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="a1707-121">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="a1707-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="a1707-122">Namespace</span></span><br/> | <span data-ttu-id="a1707-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a1707-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a1707-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="a1707-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a1707-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a1707-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1707-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1707-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1707-127">**Iwmpcdromrip-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="a1707-127">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a1707-128">**Iwmpcdromrip. stoprip**</span><span class="sxs-lookup"><span data-stu-id="a1707-128">**IWMPCdromRip.stopRip**</span></span>](wmplibiwmpcdromrip-iwmpcdromrip-stoprip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a1707-129">**Ripping einer CD**</span><span class="sxs-lookup"><span data-stu-id="a1707-129">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> </dl>

 

 





