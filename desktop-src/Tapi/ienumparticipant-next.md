---
description: Die Next-Methode ruft die nächste angegebene Anzahl von Elementen in der enumerationssequenz ab. Diese Methode ist in Visual Basic-und Skriptsprachen ausgeblendet.
ms.assetid: bd94f592-ac6f-48b7-8190-352a5e18f224
title: 'Ienumteilnehmer:: Next-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89586370d01aaac54f05242e0eb3c53eb938c47b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364471"
---
# <a name="ienumparticipantnext-method"></a><span data-ttu-id="fb621-104">Ienumteilnehmer:: Next-Methode</span><span class="sxs-lookup"><span data-stu-id="fb621-104">IEnumParticipant::Next method</span></span>

<span data-ttu-id="fb621-105">\[**Als nächstes** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fb621-105">\[**Next** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fb621-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="fb621-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fb621-107">Die **Next** -Methode ruft die nächste angegebene Anzahl von Elementen in der enumerationssequenz ab.</span><span class="sxs-lookup"><span data-stu-id="fb621-107">The **Next** method gets the next specified number of elements in the enumeration sequence.</span></span> <span data-ttu-id="fb621-108">Diese Methode ist in Visual Basic-und Skriptsprachen ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="fb621-108">This method is hidden from Visual Basic and scripting languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb621-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb621-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG         celt,
  [out] ITParticipant **ppElements,
  [out] ULONG         *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="fb621-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb621-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb621-111">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb621-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb621-112">Anzahl der angeforderten Elemente.</span><span class="sxs-lookup"><span data-stu-id="fb621-112">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="fb621-113">*ppelements* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fb621-113">*ppElements* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb621-114">Zeiger auf [**itagenthandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) -Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="fb621-114">Pointer to [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="fb621-115">*pceltfetch* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fb621-115">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb621-116">Ein Zeiger auf die Anzahl der tatsächlich bereitgestellten Elemente.</span><span class="sxs-lookup"><span data-stu-id="fb621-116">Pointer to number of elements actually supplied.</span></span> <span data-ttu-id="fb621-117">Kann **null** sein, wenn es sich um einen *celt* handelt.</span><span class="sxs-lookup"><span data-stu-id="fb621-117">May be **NULL** if *celt* is one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb621-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb621-118">Return value</span></span>

<span data-ttu-id="fb621-119">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="fb621-119">This method can return one of these values.</span></span>



| <span data-ttu-id="fb621-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="fb621-120">Return code</span></span>                                                                                   | <span data-ttu-id="fb621-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb621-121">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="fb621-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fb621-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fb621-123">Von der Methode wurde *die Anzahl der* Elemente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fb621-123">Method returned *celt* number of elements.</span></span><br/>           |
| <dl> <span data-ttu-id="fb621-124"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="fb621-124"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="fb621-125">Die Anzahl der verbleibenden Elemente war kleiner als *celt*.</span><span class="sxs-lookup"><span data-stu-id="fb621-125">Number of elements remaining was less than *celt*.</span></span><br/>   |
| <dl> <span data-ttu-id="fb621-126"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="fb621-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="fb621-127">Der *ppelements* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="fb621-127">The *ppElements* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="fb621-128"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="fb621-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fb621-129">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="fb621-129">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fb621-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb621-130">Remarks</span></span>

<span data-ttu-id="fb621-131">TAPI Ruft die [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) -Methode für die [**itagenthandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) -Schnittstelle auf, die von **ienumteilnehmer:: Next** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="fb621-131">TAPI calls the [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method on the [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) interface returned by **IEnumParticipant::Next**.</span></span> <span data-ttu-id="fb621-132">Die Anwendung muss Release auf der **itagenthandler** -Schnittstelle aufzurufen, um Ressourcen frei [**zugeben**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) , die ihr zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fb621-132">The application must call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the **ITAgentHandler** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb621-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb621-133">Requirements</span></span>



| <span data-ttu-id="fb621-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb621-134">Requirement</span></span> | <span data-ttu-id="fb621-135">Wert</span><span class="sxs-lookup"><span data-stu-id="fb621-135">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fb621-136">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="fb621-136">TAPI version</span></span><br/> | <span data-ttu-id="fb621-137">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="fb621-137">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="fb621-138">Header</span><span class="sxs-lookup"><span data-stu-id="fb621-138">Header</span></span><br/>       | <dl> <span data-ttu-id="fb621-139"><dt>"Confpriv. h"</dt></span><span class="sxs-lookup"><span data-stu-id="fb621-139"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="fb621-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fb621-140">Library</span></span><br/>      | <dl> <span data-ttu-id="fb621-141"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb621-141"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="fb621-142">DLL</span><span class="sxs-lookup"><span data-stu-id="fb621-142">DLL</span></span><br/>          | <dl> <span data-ttu-id="fb621-143"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb621-143"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="fb621-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb621-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb621-145">**Ienumteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="fb621-145">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="fb621-146">**Itteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="fb621-146">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

