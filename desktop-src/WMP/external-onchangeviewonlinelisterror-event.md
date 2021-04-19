---
title: Externes. onchangeviewonlinelisterror-Ereignis
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Externes. onchangeviewonlinelisterror-Ereignis
ms.assetid: f53dfc80-a7d7-42b1-b390-e90aa108145f
keywords:
- Externes. onchangeviewonlinelisterror-Ereignisfenster Media Player
topic_type:
- apiref
api_name:
- External.OnChangeViewOnlineListError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09e9ff854893268a00cb7b5f2fb35409be2e70e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371685"
---
# <a name="externalonchangeviewonlinelisterror-event"></a><span data-ttu-id="7080e-105">Externes. onchangeviewonlinelisterror-Ereignis</span><span class="sxs-lookup"><span data-stu-id="7080e-105">External.OnChangeViewOnlineListError Event</span></span>

> [!Note]  
> <span data-ttu-id="7080e-106">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="7080e-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="7080e-107">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7080e-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="7080e-108">Das **onchangeviewonlinelisterror** -Ereignis tritt auf, wenn ein Aufrufen der [externen. changeviewonlinelist](external-changeviewonlinelist.md) -Methode zu einem Fehler führt.</span><span class="sxs-lookup"><span data-stu-id="7080e-108">The **OnChangeViewOnlineListError** event occurs when a call to the [External.changeViewOnlineList](external-changeviewonlinelist.md) method results in an error.</span></span>

``` syntax
window.external.OnChangeViewOnlineListError = functionname
```

## <a name="possible-values"></a><span data-ttu-id="7080e-109">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="7080e-109">Possible Values</span></span>

<span data-ttu-id="7080e-110">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die den Namen der Funktion im Skript angibt, die von Windows Media Player bei Auftreten des Ereignisses aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7080e-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="7080e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7080e-111">Parameters</span></span>

<span data-ttu-id="7080e-112">Die Funktion, die diesen Fehler behandelt, verfügt über die folgenden Parameter.</span><span class="sxs-lookup"><span data-stu-id="7080e-112">The function that handles this error has the following parameters.</span></span>

<dl> <dt>

<span data-ttu-id="7080e-113"><span id="hr"></span><span id="HR"></span>*HR*</span><span class="sxs-lookup"><span data-stu-id="7080e-113"><span id="hr"></span><span id="HR"></span>*hr*</span></span>
</dt> <dd>

<span data-ttu-id="7080e-114">Ein **HRESULT** -Fehlercode, der den Grund für den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="7080e-114">An **HRESULT** failure code that indicates the reason for the failure.</span></span>

</dd> <dt>

<span data-ttu-id="7080e-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*Librarylocationtype*</span><span class="sxs-lookup"><span data-stu-id="7080e-115"><span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*</span></span>
</dt> <dd>

<span data-ttu-id="7080e-116">Dieselbe Zeichenfolge, die im **librarylocationtype** -Parameter von **changeviewonlinelist** übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="7080e-116">The same string that was passed in the **LibraryLocationType** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="7080e-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*Librarylocationid*</span><span class="sxs-lookup"><span data-stu-id="7080e-117"><span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*</span></span>
</dt> <dd>

<span data-ttu-id="7080e-118">Dieselbe Zeichenfolge, die im **librarylocationid** -Parameter von **changeviewonlinelist** übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="7080e-118">The same string that was passed in the **LibraryLocationID** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="7080e-119"><span id="Params"></span><span id="params"></span><span id="PARAMS"></span>*Params*</span><span class="sxs-lookup"><span data-stu-id="7080e-119"><span id="Params"></span><span id="params"></span><span id="PARAMS"></span>*Params*</span></span>
</dt> <dd>

<span data-ttu-id="7080e-120">Dieselbe Zeichenfolge, die im Parameter **para** meters von **changeviewonlinelist** übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="7080e-120">The same string that was passed in the **Params** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="7080e-121"><span id="FriendlyName"></span><span id="friendlyname"></span><span id="FRIENDLYNAME"></span>*FriendlyName*</span><span class="sxs-lookup"><span data-stu-id="7080e-121"><span id="FriendlyName"></span><span id="friendlyname"></span><span id="FRIENDLYNAME"></span>*FriendlyName*</span></span>
</dt> <dd>

<span data-ttu-id="7080e-122">Dieselbe Zeichenfolge, die im **FriendlyName** -Parameter von **changeviewonlinelist** übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="7080e-122">The same string that was passed in the **FriendlyName** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="7080e-123"><span id="ListType"></span><span id="listtype"></span><span id="LISTTYPE"></span>*Listentyp*</span><span class="sxs-lookup"><span data-stu-id="7080e-123"><span id="ListType"></span><span id="listtype"></span><span id="LISTTYPE"></span>*ListType*</span></span>
</dt> <dd>

<span data-ttu-id="7080e-124">Dieselbe Zeichenfolge, die im **ListType** -Parameter von **changeviewonlinelist** übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="7080e-124">The same string that was passed in the **ListType** parameter of **changeViewOnlineList**.</span></span>

</dd> <dt>

<span data-ttu-id="7080e-125"><span id="ViewMode"></span><span id="viewmode"></span><span id="VIEWMODE"></span>*ViewMode*</span><span class="sxs-lookup"><span data-stu-id="7080e-125"><span id="ViewMode"></span><span id="viewmode"></span><span id="VIEWMODE"></span>*ViewMode*</span></span>
</dt> <dd>

<span data-ttu-id="7080e-126">Dieselbe Zeichenfolge, die im **ViewMode** -Parameter von **changeviewonlinelist** übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="7080e-126">The same string that was passed in the **ViewMode** parameter of **changeViewOnlineList**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7080e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7080e-127">Requirements</span></span>



| <span data-ttu-id="7080e-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7080e-128">Requirement</span></span> | <span data-ttu-id="7080e-129">Wert</span><span class="sxs-lookup"><span data-stu-id="7080e-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7080e-130">Version</span><span class="sxs-lookup"><span data-stu-id="7080e-130">Version</span></span><br/> | <span data-ttu-id="7080e-131">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="7080e-131">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="7080e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7080e-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="7080e-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7080e-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7080e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7080e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7080e-135">**Externes Objekt für den Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="7080e-135">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





