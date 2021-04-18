---
title: Iwmpdvd-Back-Methode
description: Die Methode "Back" ändert die Anzeige von einem Untermenü in das übergeordnete Menü.
ms.assetid: 81d033d4-f570-44a5-898a-e419101c04fa
keywords:
- Windows-Media Player der Back-Methode
- Back-Methode, Windows Media Player, iwmpdvd-Schnittstelle
- Iwmpdvd Interface, Windows Media Player, Back-Methode
topic_type:
- apiref
api_name:
- IWMPDVD.back
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cd31cd6365843a6905760c4447ea679e15e70ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358748"
---
# <a name="iwmpdvdback-method"></a><span data-ttu-id="a2fb3-106">Iwmpdvd:: Back-Methode</span><span class="sxs-lookup"><span data-stu-id="a2fb3-106">IWMPDVD::back method</span></span>

<span data-ttu-id="a2fb3-107">Die Methode " **Back** " ändert die Anzeige von einem Untermenü in das übergeordnete Menü.</span><span class="sxs-lookup"><span data-stu-id="a2fb3-107">The **back** method changes the display from a submenu to its parent menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2fb3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2fb3-108">Syntax</span></span>


```CSharp
public void back();
```


```VB

Public Sub back()
Implements IWMPDVD.back
```





## <a name="parameters"></a><span data-ttu-id="a2fb3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2fb3-109">Parameters</span></span>

<span data-ttu-id="a2fb3-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a2fb3-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2fb3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a2fb3-111">Return value</span></span>

<span data-ttu-id="a2fb3-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a2fb3-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2fb3-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2fb3-113">Remarks</span></span>

<span data-ttu-id="a2fb3-114">Jede DVD wird unterschiedlich verfasst.</span><span class="sxs-lookup"><span data-stu-id="a2fb3-114">Every DVD is authored differently.</span></span> <span data-ttu-id="a2fb3-115">Einige DVDs werden so erstellt, dass die- `back` Methode über das Root-Menü verfügbar ist, aber wenn Sie aufgerufen wird, wird keine Aktion durchführen.</span><span class="sxs-lookup"><span data-stu-id="a2fb3-115">Some DVDs are authored so that the `back` method is available from the root menu, but when invoked, it will do nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2fb3-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2fb3-116">Requirements</span></span>



| <span data-ttu-id="a2fb3-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2fb3-117">Requirement</span></span> | <span data-ttu-id="a2fb3-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a2fb3-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2fb3-119">Version</span><span class="sxs-lookup"><span data-stu-id="a2fb3-119">Version</span></span><br/>   | <span data-ttu-id="a2fb3-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="a2fb3-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a2fb3-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="a2fb3-121">Namespace</span></span><br/> | <span data-ttu-id="a2fb3-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a2fb3-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a2fb3-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="a2fb3-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a2fb3-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a2fb3-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2fb3-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2fb3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2fb3-126">**Iwmpdvd-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="a2fb3-126">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





