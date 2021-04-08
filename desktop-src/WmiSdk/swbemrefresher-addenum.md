---
description: Fügt dem Objekt "Swap-Aktualisierungs Programm" einen neuen Enumerator hinzu. Dieser Enumerator gilt für alle Instanzen der-Klasse, die im Parameter "-Parameter" angegeben sind.
ms.assetid: 0fa22a47-4050-43ae-aad3-3a8ebbf5e9b2
ms.tgt_platform: multiple
title: Slibemaktusher. AddEnum-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cffa406a3a45869038f5e6fed12b23b6b84fde27
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761400"
---
# <a name="swbemrefresheraddenum-method"></a><span data-ttu-id="9f18a-104">Methode ' slibemfreshsher. AddEnum '</span><span class="sxs-lookup"><span data-stu-id="9f18a-104">SWbemRefresher.AddEnum method</span></span>

<span data-ttu-id="9f18a-105">Die Methode " **Swap. AddEnum** " fügt dem Objekt "slibemaktusher" [](swbemrefresher.md) einen neuen Enumerator hinzu.</span><span class="sxs-lookup"><span data-stu-id="9f18a-105">The **SWbemRefresher.AddEnum** method adds a new enumerator to the [**SWbemRefresher**](swbemrefresher.md) object.</span></span> <span data-ttu-id="9f18a-106">Dieser Enumerator gilt für alle Instanzen der-Klasse *, die im Parameter "* -Parameter" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="9f18a-106">This enumerator is for all the instances of the class that is specified in the *strClass* parameter.</span></span>

<span data-ttu-id="9f18a-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9f18a-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9f18a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f18a-108">Syntax</span></span>


```VB
objRefreshEnum = .AddEnum( _
  ByVal objWbemService, _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9f18a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f18a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f18a-110">*objwbemservice*</span><span class="sxs-lookup"><span data-stu-id="9f18a-110">*objWbemService*</span></span> 
</dt> <dd>

<span data-ttu-id="9f18a-111">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9f18a-111">Required.</span></span> <span data-ttu-id="9f18a-112">Ein-Objekt, [**das eine Verbindung**](swbemservices.md) mit dem Namespace darstellt, in dem sich das dem Aktualisierungs Programm hinzugefügte Objekt befindet.</span><span class="sxs-lookup"><span data-stu-id="9f18a-112">An [**SWbemServices**](swbemservices.md) object that represents a connection to the namespace in which the object that is being added to the refresher resides.</span></span>

</dd> <dt>

<span data-ttu-id="9f18a-113">*Klasse*</span><span class="sxs-lookup"><span data-stu-id="9f18a-113">*strClass*</span></span> 
</dt> <dd>

<span data-ttu-id="9f18a-114">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9f18a-114">Required.</span></span> <span data-ttu-id="9f18a-115">Eine Zeichenfolge, die die Klasse enthält, die dem Aktualisierungs Programm hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="9f18a-115">String that contains the class that is being added to the refresher.</span></span> <span data-ttu-id="9f18a-116">Diese Klasse wird als Enumerator der Instanzen der-Klasse verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f18a-116">This class is used as an enumerator of the instances of the class.</span></span> <span data-ttu-id="9f18a-117">Die [**Index**](swbemrefreshableitem-index.md) -Eigenschaft des zurückgegebenen " [**taubemfreshableitem**](swbemrefreshableitem.md) "-Elements stellt den Index des Enumerators in der Aktualisierungs-Auflistung dar.</span><span class="sxs-lookup"><span data-stu-id="9f18a-117">The [**Index**](swbemrefreshableitem-index.md) property of the returned [**SWbemRefreshableItem**](swbemrefreshableitem.md) represents the index of the enumerator in the refresher collection.</span></span>

</dd> <dt>

<span data-ttu-id="9f18a-118">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="9f18a-118">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9f18a-119">Eine Zeichenfolge, die den Objekt Pfad des Objekts enthält, für das die Methode ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9f18a-119">String that contains the object path of the object for which the method is executed.</span></span>

</dd> <dt>

<span data-ttu-id="9f18a-120">*objwbemnamedvalueset* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="9f18a-120">*objWbemNamedvalueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9f18a-121">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="9f18a-121">Typically, this is undefined.</span></span> <span data-ttu-id="9f18a-122">Andernfalls handelt es sich hierbei um ein Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f18a-122">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="9f18a-123">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="9f18a-123">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f18a-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f18a-124">Return value</span></span>

<span data-ttu-id="9f18a-125">Wenn der- [**Befehl**](swbemrefreshableitem.md) erfolgreich ausgeführt wurde, wird ein-Objekt mit einem-Enumerator zurückgegeben, das einen Enumerator für alle Instanzen der angegebenen Klasse enthält.</span><span class="sxs-lookup"><span data-stu-id="9f18a-125">If the call is successful, an [**SWbemRefreshableItem**](swbemrefreshableitem.md) object that contains an enumerator for all the instances for the specified class is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f18a-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f18a-126">Requirements</span></span>



| <span data-ttu-id="9f18a-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f18a-127">Requirement</span></span> | <span data-ttu-id="9f18a-128">Wert</span><span class="sxs-lookup"><span data-stu-id="9f18a-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f18a-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f18a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9f18a-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f18a-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9f18a-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f18a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9f18a-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f18a-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9f18a-133">Header</span><span class="sxs-lookup"><span data-stu-id="9f18a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f18a-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f18a-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9f18a-135">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9f18a-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="9f18a-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9f18a-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9f18a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="9f18a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f18a-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f18a-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9f18a-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="9f18a-139">CLSID</span></span><br/>                    | <span data-ttu-id="9f18a-140">CLSID- \_ Austauschprogramm</span><span class="sxs-lookup"><span data-stu-id="9f18a-140">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="9f18a-141">IID</span><span class="sxs-lookup"><span data-stu-id="9f18a-141">IID</span></span><br/>                      | <span data-ttu-id="9f18a-142">IID \_ iswbemfreshsher</span><span class="sxs-lookup"><span data-stu-id="9f18a-142">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="9f18a-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f18a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f18a-144">**Swap-Aktualisierungs Programm**</span><span class="sxs-lookup"><span data-stu-id="9f18a-144">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




