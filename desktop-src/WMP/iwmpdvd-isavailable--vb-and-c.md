---
title: Iwmpdvd. IsAvailable (VB und C)
description: Die IsAvailable-Eigenschaft (die get \_ IsAvailable-Methode in C \) Ruft einen Wert ab, der angibt, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann.
ms.assetid: 55690783-df2f-473d-a6f2-a4907b7e8a78
keywords:
- Iwmpdvd. IsAvailable (VB und C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPDVD.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e3409da619f337b61606baaf546cebbb438087c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365703"
---
# <a name="iwmpdvdisavailable-vb-and-c"></a><span data-ttu-id="04564-104">Iwmpdvd. IsAvailable (VB und c#)</span><span class="sxs-lookup"><span data-stu-id="04564-104">IWMPDVD.isAvailable (VB and C#)</span></span>

<span data-ttu-id="04564-105">Die **IsAvailable** -Eigenschaft (die **get \_ IsAvailable** -Methode in c#) Ruft einen Wert ab, der angibt, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="04564-105">The **isAvailable** property (the **get\_isAvailable** method in C#) gets a value that indicates whether a specified type of information is available or a specified action can be performed.</span></span>


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
)
```



## <a name="parameters"></a><span data-ttu-id="04564-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="04564-106">Parameters</span></span>

<span data-ttu-id="04564-107">*bstritem*</span><span class="sxs-lookup"><span data-stu-id="04564-107">*bstrItem*</span></span>

<span data-ttu-id="04564-108">Ein System. String-Wert, der einem der folgenden Werte entspricht.</span><span class="sxs-lookup"><span data-stu-id="04564-108">A System.String that is one of the following values.</span></span>



| <span data-ttu-id="04564-109">Wert</span><span class="sxs-lookup"><span data-stu-id="04564-109">Value</span></span>      | <span data-ttu-id="04564-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04564-110">Description</span></span>                                                                                   |
|------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="04564-111">back (Zurück)</span><span class="sxs-lookup"><span data-stu-id="04564-111">back</span></span>       | <span data-ttu-id="04564-112">Ermittelt, ob die **iwmpdvd. Back** -Methode verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="04564-112">Discovers whether the **IWMPDVD.back** method is available.</span></span>                                   |
| <span data-ttu-id="04564-113">DVD</span><span class="sxs-lookup"><span data-stu-id="04564-113">dvd</span></span>        | <span data-ttu-id="04564-114">Ermittelt, ob die DVD geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="04564-114">Discovers whether the DVD is loaded.</span></span>                                                          |
| <span data-ttu-id="04564-115">dvddecoder</span><span class="sxs-lookup"><span data-stu-id="04564-115">dvdDecoder</span></span> | <span data-ttu-id="04564-116">Ermittelt, ob der DVD-Decoder auf dem System installiert ist.</span><span class="sxs-lookup"><span data-stu-id="04564-116">Discovers whether the DVD decoder is installed on system.</span></span>                                     |
| <span data-ttu-id="04564-117">resume</span><span class="sxs-lookup"><span data-stu-id="04564-117">resume</span></span>     | <span data-ttu-id="04564-118">Ermittelt, ob die **iwmpdvd. Resume** -Methode verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="04564-118">Discovers whether the **IWMPDVD.resume** method is available.</span></span>                                 |
| <span data-ttu-id="04564-119">titlemenu</span><span class="sxs-lookup"><span data-stu-id="04564-119">titleMenu</span></span>  | <span data-ttu-id="04564-120">Ermittelt, ob die **iwmpdvd. titlemenu** -Methode verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="04564-120">Discovers whether the **IWMPDVD.titleMenu** method is available.</span></span>                              |
| <span data-ttu-id="04564-121">topmenu</span><span class="sxs-lookup"><span data-stu-id="04564-121">topMenu</span></span>    | <span data-ttu-id="04564-122">Ermittelt, ob die **iwmpdvd. topmenu** -Methode verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="04564-122">Discovers whether the **IWMPDVD.topMenu** method is available.</span></span> <span data-ttu-id="04564-123">Wird üblicherweise als Stamm Menü bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="04564-123">Commonly called the root menu.</span></span> |



 

## <a name="property-value"></a><span data-ttu-id="04564-124">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="04564-124">Property Value</span></span>

<span data-ttu-id="04564-125">**System.Boolean**</span><span class="sxs-lookup"><span data-stu-id="04564-125">**System.Boolean**</span></span>

<span data-ttu-id="04564-126">Ein **System. boolescher** Wert, der angibt, ob ein angegebener Informationstyp verfügbar ist oder eine bestimmte Aktion ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="04564-126">A **System.Boolean** that indicates whether a specified type of information is available or a specified action can be performed.</span></span>

## <a name="remarks"></a><span data-ttu-id="04564-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04564-127">Remarks</span></span>

<span data-ttu-id="04564-128">Die DVD-Features von Windows Media Player können nicht auf Computern verwendet werden, auf denen kein DVD-Decoder installiert ist.</span><span class="sxs-lookup"><span data-stu-id="04564-128">The DVD features of Windows Media Player will not work on computers that do not have a DVD decoder installed.</span></span> <span data-ttu-id="04564-129">Sie können bestimmen, ob ein Decoder verfügbar ist, indem Sie die **IsAvailable** -Eigenschaft (die **get \_ IsAvailable** -Methode in c#) aufrufen und den **System. String** -Wert "dvddecoder" übergeben.</span><span class="sxs-lookup"><span data-stu-id="04564-129">You can determine whether a decoder is available by calling the **isAvailable** property (the **get\_isAvailable** method in C#) and passing in the **System.String** value "dvdDecoder".</span></span>

<span data-ttu-id="04564-130">Jede DVD wird unterschiedlich verfasst.</span><span class="sxs-lookup"><span data-stu-id="04564-130">Every DVD is authored differently.</span></span> <span data-ttu-id="04564-131">Die während der DVD-Wiedergabe und-Navigation verfügbaren Methoden hängen davon ab, wie die DVD erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="04564-131">The methods available during DVD playback and navigation depend on how the DVD is authored.</span></span>

## <a name="requirements"></a><span data-ttu-id="04564-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04564-132">Requirements</span></span>



| <span data-ttu-id="04564-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04564-133">Requirement</span></span> | <span data-ttu-id="04564-134">Wert</span><span class="sxs-lookup"><span data-stu-id="04564-134">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04564-135">Version</span><span class="sxs-lookup"><span data-stu-id="04564-135">Version</span></span><br/>   | <span data-ttu-id="04564-136">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="04564-136">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="04564-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="04564-137">Namespace</span></span><br/> | <span data-ttu-id="04564-138">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="04564-138">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="04564-139">Assembly</span><span class="sxs-lookup"><span data-stu-id="04564-139">Assembly</span></span><br/>  | <dl> <span data-ttu-id="04564-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="04564-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04564-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04564-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04564-142">**Iwmpdvd-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="04564-142">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="04564-143">**Iwmpdvd. Back (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="04564-143">**IWMPDVD.back (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-back--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="04564-144">**Iwmpdvd. Resume (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="04564-144">**IWMPDVD.resume (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-resume--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="04564-145">**Iwmpdvd. titlemenu (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="04564-145">**IWMPDVD.titleMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="04564-146">**Iwmpdvd. topmenu (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="04564-146">**IWMPDVD.topMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





