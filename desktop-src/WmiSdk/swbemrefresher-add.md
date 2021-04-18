---
description: Die Methode "taubemaktualisierer. Add" fügt der Auflistung im "Swap-Aktualisierer"-Objekt ein neues ""-Objekt "-Objekt" aus. Das taubemfreshableitem-Objekt wird in die Auflistung im Objekt "Swap-Aktualisierungs Programm" versetzt.
ms.assetid: 92d11a18-1eed-4958-b74a-2f9de4907dd0
ms.tgt_platform: multiple
title: Taubemaktusher. Add-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Add
- ISWbemRefresher.Add
- ISWbemRefresher.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ebe9da221314252b2b143bf674cd7bb7177329b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106351199"
---
# <a name="swbemrefresheradd-method"></a><span data-ttu-id="d513d-103">Methode ' Swap. Add '</span><span class="sxs-lookup"><span data-stu-id="d513d-103">SWbemRefresher.Add method</span></span>

<span data-ttu-id="d513d-104">Die Methode " **taubemaktualisierer. Add** " fügt der Auflistung im " [**Swap**](swbemrefresher.md) -Aktualisierer" [**-Objekt ein neues "**](swbemrefreshableitem.md) "-Objekt "-Objekt" aus.</span><span class="sxs-lookup"><span data-stu-id="d513d-104">The **SWbemRefresher.Add** method adds a new [**SWbemRefreshableItem**](swbemrefreshableitem.md) object to the collection in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="d513d-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d513d-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d513d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d513d-106">Syntax</span></span>


```VB
objRefreshItem = .Add( _
  ByVal objWbemService, _
  ByVal strInstancePath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d513d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d513d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d513d-108">*objwbemservice*</span><span class="sxs-lookup"><span data-stu-id="d513d-108">*objWbemService*</span></span> 
</dt> <dd>

<span data-ttu-id="d513d-109">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d513d-109">Required.</span></span> <span data-ttu-id="d513d-110">Ein-Objekt, [**das eine Verbindung**](swbemservices.md) mit dem Namespace darstellt, in dem sich das dem Aktualisierungs Programm hinzugefügte Objekt befindet.</span><span class="sxs-lookup"><span data-stu-id="d513d-110">An [**SWbemServices**](swbemservices.md) object that represents a connection to the namespace in which the object that is being added to the refresher resides.</span></span>

</dd> <dt>

<span data-ttu-id="d513d-111">*"straumpcepath"*</span><span class="sxs-lookup"><span data-stu-id="d513d-111">*strInstancePath*</span></span> 
</dt> <dd>

<span data-ttu-id="d513d-112">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d513d-112">Required.</span></span> <span data-ttu-id="d513d-113">Eine Zeichenfolge, die den relativen Pfad des-Objekts im-Namespace enthält.</span><span class="sxs-lookup"><span data-stu-id="d513d-113">String that contains the relative path of the object in the namespace.</span></span> <span data-ttu-id="d513d-114">Der Pfad muss eine-Instanz enthalten.</span><span class="sxs-lookup"><span data-stu-id="d513d-114">The path must contain an instance.</span></span> <span data-ttu-id="d513d-115">Die [**Index**](swbemrefreshableitem-index.md) -Eigenschaft des zurückgegebenen " [**taubemfreshableitem**](swbemrefreshableitem.md) "-Objekts stellt den Index des-Objekts in der Aktualisierungs-Auflistung dar.</span><span class="sxs-lookup"><span data-stu-id="d513d-115">The [**Index**](swbemrefreshableitem-index.md) property of the returned [**SWbemRefreshableItem**](swbemrefreshableitem.md) represents the index of the object in the refresher collection.</span></span>

</dd> <dt>

<span data-ttu-id="d513d-116">*IFlags* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="d513d-116">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d513d-117">Eine Zeichenfolge, die den Objekt Pfad des Objekts enthält, für das die Methode ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d513d-117">String that contains the object path of the object for which the method is executed.</span></span>

</dd> <dt>

<span data-ttu-id="d513d-118">*objwbemnamedvalueset* \[ optionale\]</span><span class="sxs-lookup"><span data-stu-id="d513d-118">*objWbemNamedvalueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d513d-119">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="d513d-119">Typically, this is undefined.</span></span> <span data-ttu-id="d513d-120">Andernfalls handelt es sich hierbei um ein Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d513d-120">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="d513d-121">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="d513d-121">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d513d-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d513d-122">Return value</span></span>

<span data-ttu-id="d513d-123">Wenn der Aufruf erfolgreich ist, wird ein Objekt vom Typ " [**taubemerfrischendes ableitem**](swbemrefreshableitem.md) " zurückgegeben, das ein einzelnes Aktualisier bares Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="d513d-123">If the call is successful, an [**SWbemRefreshableItem**](swbemrefreshableitem.md) object that contains a single refreshable object is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="d513d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d513d-124">Requirements</span></span>



| <span data-ttu-id="d513d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d513d-125">Requirement</span></span> | <span data-ttu-id="d513d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="d513d-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d513d-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d513d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d513d-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d513d-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d513d-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d513d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d513d-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d513d-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d513d-131">Header</span><span class="sxs-lookup"><span data-stu-id="d513d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d513d-132"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d513d-132"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d513d-133">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="d513d-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="d513d-134"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d513d-134"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d513d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d513d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d513d-136"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d513d-136"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d513d-137">CLSID</span><span class="sxs-lookup"><span data-stu-id="d513d-137">CLSID</span></span><br/>                    | <span data-ttu-id="d513d-138">CLSID- \_ Austauschprogramm</span><span class="sxs-lookup"><span data-stu-id="d513d-138">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="d513d-139">IID</span><span class="sxs-lookup"><span data-stu-id="d513d-139">IID</span></span><br/>                      | <span data-ttu-id="d513d-140">IID \_ iswbemfreshsher</span><span class="sxs-lookup"><span data-stu-id="d513d-140">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="d513d-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d513d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d513d-142">**Swap-Aktualisierungs Programm**</span><span class="sxs-lookup"><span data-stu-id="d513d-142">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




