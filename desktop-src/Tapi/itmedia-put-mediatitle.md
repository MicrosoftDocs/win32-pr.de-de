---
description: Mit der Put \_ mediatitle-Methode wird ein Text Titel für die Medien festgelegt, die von der Anwendung zur Informations-oder Anzeige Zwecken verwendet werden können. Dies muss eine ASCII-konvertierbare Zeichenfolge sein, wenn der Zeichensatz ASCII ist. Andernfalls kann es sich um eine beliebige BSTR-Zeichenfolge handeln.
ms.assetid: bbab033b-bd37-4ef6-9e84-1d0b17ecbd4e
title: ITmedia::p ut_MediaTitle-Methode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d1abee91b08555f79437e5e26710761429e4f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368345"
---
# <a name="itmediaput_mediatitle-method"></a><span data-ttu-id="ecc8b-105">ITmedia::p UT \_ mediatitle-Methode</span><span class="sxs-lookup"><span data-stu-id="ecc8b-105">ITMedia::put\_MediaTitle method</span></span>

<span data-ttu-id="ecc8b-106">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ecc8b-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ecc8b-107">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="ecc8b-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ecc8b-108">Mit der **Put \_ mediatitle** -Methode wird ein Text Titel für die Medien festgelegt, die von der Anwendung zur Informations-oder Anzeige Zwecken verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ecc8b-108">The **put\_MediaTitle** method sets a textual title for the media that the application can use for informational or display purposes.</span></span> <span data-ttu-id="ecc8b-109">Dies muss eine ASCII-konvertierbare Zeichenfolge sein, wenn der Zeichensatz ASCII ist.</span><span class="sxs-lookup"><span data-stu-id="ecc8b-109">This must be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="ecc8b-110">Andernfalls kann es sich um eine beliebige **BSTR** -Zeichenfolge handeln.</span><span class="sxs-lookup"><span data-stu-id="ecc8b-110">Otherwise, it can be any **BSTR** string.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecc8b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecc8b-111">Syntax</span></span>


```C++
HRESULT put_MediaTitle(
  [in] BSTR pMediaTitle
);
```



## <a name="parameters"></a><span data-ttu-id="ecc8b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ecc8b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecc8b-113">*pmediatitle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecc8b-113">*pMediaTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecc8b-114">Zeiger auf einen **BSTR** -Wert, der den Titel des Mediums enthält.</span><span class="sxs-lookup"><span data-stu-id="ecc8b-114">Pointer to a **BSTR** containing the title of the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecc8b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ecc8b-115">Return value</span></span>

<span data-ttu-id="ecc8b-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ecc8b-116">This method can return one of these values.</span></span>



| <span data-ttu-id="ecc8b-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ecc8b-117">Return code</span></span>                                                                                   | <span data-ttu-id="ecc8b-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ecc8b-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="ecc8b-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ecc8b-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ecc8b-120">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ecc8b-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ecc8b-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="ecc8b-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ecc8b-122">Der *pmediatitle* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="ecc8b-122">The *pMediaTitle* parameter is not a valid pointer.</span></span><br/>  |
| <dl> <span data-ttu-id="ecc8b-123"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="ecc8b-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ecc8b-124">Der *pmediatitle* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ecc8b-124">The *pMediaTitle* parameter is not valid.</span></span><br/>            |
| <dl> <span data-ttu-id="ecc8b-125"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="ecc8b-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ecc8b-126">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ecc8b-126">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="ecc8b-127"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="ecc8b-127"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="ecc8b-128">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="ecc8b-128">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="ecc8b-129"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="ecc8b-129"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="ecc8b-130">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="ecc8b-130">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="ecc8b-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ecc8b-131">Remarks</span></span>

<span data-ttu-id="ecc8b-132">Die Anwendung muss " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Speicher für den *pmediatitle* -Parameter zuzuweisen, und " [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) " verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="ecc8b-132">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pMediaTitle* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="ecc8b-133">Diese Funktion kann Daten in unverschlüsselter Form über das Netzwerk senden. aus diesem Grund kann ein Benutzer, der sich im Netzwerk befindet, möglicherweise die Daten lesen.</span><span class="sxs-lookup"><span data-stu-id="ecc8b-133">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="ecc8b-134">Das Sicherheitsrisiko, dass Daten im Klartext gesendet werden, sollte vor der Verwendung dieser Methode berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="ecc8b-134">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecc8b-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ecc8b-135">Requirements</span></span>



| <span data-ttu-id="ecc8b-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ecc8b-136">Requirement</span></span> | <span data-ttu-id="ecc8b-137">Wert</span><span class="sxs-lookup"><span data-stu-id="ecc8b-137">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ecc8b-138">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="ecc8b-138">TAPI version</span></span><br/> | <span data-ttu-id="ecc8b-139">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="ecc8b-139">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ecc8b-140">Header</span><span class="sxs-lookup"><span data-stu-id="ecc8b-140">Header</span></span><br/>       | <dl> <span data-ttu-id="ecc8b-141"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecc8b-141"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ecc8b-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ecc8b-142">Library</span></span><br/>      | <dl> <span data-ttu-id="ecc8b-143"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ecc8b-143"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ecc8b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="ecc8b-144">DLL</span></span><br/>          | <dl> <span data-ttu-id="ecc8b-145"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecc8b-145"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecc8b-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ecc8b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecc8b-147">**ITmedia**</span><span class="sxs-lookup"><span data-stu-id="ecc8b-147">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="ecc8b-148">**ITmedia:: get \_ mediatitle**</span><span class="sxs-lookup"><span data-stu-id="ecc8b-148">**ITMedia::get\_MediaTitle**</span></span>](itmedia-get-mediatitle.md)
</dt> </dl>

 

