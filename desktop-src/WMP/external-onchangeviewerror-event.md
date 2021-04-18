---
title: Externes. onchangeviewerror-Ereignis
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Externes. onchangeviewerror-Ereignis
ms.assetid: d6370629-5f50-434d-8eb5-5b43d1b2f7fe
keywords:
- Externe. onchangeviewerror-Ereignisfenster Media Player
topic_type:
- apiref
api_name:
- External.OnChangeViewError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91bcbb71e1c5324a9907d735492364561be49a60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354715"
---
# <a name="externalonchangeviewerror-event"></a><span data-ttu-id="f9526-105">Externes. onchangeviewerror-Ereignis</span><span class="sxs-lookup"><span data-stu-id="f9526-105">External.OnChangeViewError Event</span></span>

> [!Note]  
> <span data-ttu-id="f9526-106">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="f9526-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="f9526-107">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f9526-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="f9526-108">Das **onchangeviewerror** -Ereignis tritt auf, wenn ein Aufrufvorgang der [externen. changeView](external-changeview.md) -Methode zu einem Fehler führt.</span><span class="sxs-lookup"><span data-stu-id="f9526-108">The **OnChangeViewError** event occurs when a call to the [External.changeView](external-changeview.md) method results in an error.</span></span>

``` syntax
window.external.OnChangeViewError = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="f9526-109">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="f9526-109">Possible Values</span></span>

<span data-ttu-id="f9526-110">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die den Namen der Funktion im Skript angibt, die von Windows Media Player bei Auftreten des Ereignisses aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f9526-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="f9526-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9526-111">Parameters</span></span>

<span data-ttu-id="f9526-112">Die Funktion, die dieses Ereignis behandelt, verfügt über die folgenden Parameter.</span><span class="sxs-lookup"><span data-stu-id="f9526-112">The function that handles this event has the following parameters.</span></span>

<dl> <dt>

<span data-ttu-id="f9526-113"><span id="hr"></span><span id="HR"></span>*HR*</span><span class="sxs-lookup"><span data-stu-id="f9526-113"><span id="hr"></span><span id="HR"></span>*hr*</span></span>
</dt> <dd>

<span data-ttu-id="f9526-114">Ein **HRESULT** -Fehlercode, der den Grund für den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="f9526-114">An **HRESULT** failure code that indicates the reason for the failure.</span></span>

</dd> <dt>

<span data-ttu-id="f9526-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*Librarylocationtype*</span><span class="sxs-lookup"><span data-stu-id="f9526-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span></span>
</dt> <dd>

<span data-ttu-id="f9526-116">Dieselbe Zeichenfolge, die im **librarylocationtype** -Parameter von **changeView** übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f9526-116">The same string that was passed in the **LibraryLocationType** parameter of **changeView**.</span></span>

</dd> <dt>

<span data-ttu-id="f9526-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*Librarylocationid*</span><span class="sxs-lookup"><span data-stu-id="f9526-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span></span>
</dt> <dd>

<span data-ttu-id="f9526-118">Dieselbe Zeichenfolge, die im **librarylocationid** -Parameter von **changeView** übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f9526-118">The same string thatwas passed in the **LibraryLocationID** parameter of **changeView**.</span></span>

</dd> <dt>

<span data-ttu-id="f9526-119"><span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>*Filter*</span><span class="sxs-lookup"><span data-stu-id="f9526-119"><span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>*Filter*</span></span>
</dt> <dd>

<span data-ttu-id="f9526-120">Dieselbe Zeichenfolge, die im **Filter** -Parameter von **changeView** übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f9526-120">The same string that was passed in the **Filter** parameter of **changeView**.</span></span>

</dd> <dt>

<span data-ttu-id="f9526-121"><span id="ViewParams"></span><span id="viewparams"></span><span id="VIEWPARAMS"></span>*Viewparametriams*</span><span class="sxs-lookup"><span data-stu-id="f9526-121"><span id="ViewParams"></span><span id="viewparams"></span><span id="VIEWPARAMS"></span>*ViewParams*</span></span>
</dt> <dd>

<span data-ttu-id="f9526-122">Dieselbe Zeichenfolge, die in den **viewparameams** -Parameter von **changeView** übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f9526-122">The same string that was passed in the **ViewParams** parameter of **changeView**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9526-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9526-123">Requirements</span></span>



| <span data-ttu-id="f9526-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9526-124">Requirement</span></span> | <span data-ttu-id="f9526-125">Wert</span><span class="sxs-lookup"><span data-stu-id="f9526-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f9526-126">Version</span><span class="sxs-lookup"><span data-stu-id="f9526-126">Version</span></span><br/> | <span data-ttu-id="f9526-127">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="f9526-127">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="f9526-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f9526-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="f9526-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9526-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9526-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9526-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9526-131">**Externalobject für Typ 1 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="f9526-131">**ExternalObject for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





