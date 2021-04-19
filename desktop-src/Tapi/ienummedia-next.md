---
description: Die Next-Methode ruft die nächste angegebene Anzahl von Elementen in der enumerationssequenz ab.
ms.assetid: 39c6d082-415f-4375-8cad-6d4c734d277f
title: 'Ienummedia:: Next-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f04b92220d8fe93058533427ff8cc7bcc7ad7a02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365814"
---
# <a name="ienummedianext-method"></a><span data-ttu-id="b5692-103">Ienummedia:: Next-Methode</span><span class="sxs-lookup"><span data-stu-id="b5692-103">IEnumMedia::Next method</span></span>

<span data-ttu-id="b5692-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b5692-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b5692-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="b5692-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b5692-106">Die **Next** -Methode ruft die nächste angegebene Anzahl von Elementen in der enumerationssequenz ab.</span><span class="sxs-lookup"><span data-stu-id="b5692-106">The **Next** method gets the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5692-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5692-107">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG   celt,
  [out] ITMedia **pVal,
  [out] ULONG   *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="b5692-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5692-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5692-109">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5692-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5692-110">Anzahl der angeforderten Elemente.</span><span class="sxs-lookup"><span data-stu-id="b5692-110">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="b5692-111">*PVal* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b5692-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5692-112">Zeiger auf die [**ITmedia**](itmedia.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b5692-112">Pointer to the [**ITMedia**](itmedia.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="b5692-113">*pceltfetch* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b5692-113">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5692-114">Ein Zeiger auf die Anzahl der tatsächlich bereitgestellten Elemente.</span><span class="sxs-lookup"><span data-stu-id="b5692-114">Pointer to the number of elements actually supplied.</span></span> <span data-ttu-id="b5692-115">Kann **null** sein, wenn es sich um einen *celt* handelt.</span><span class="sxs-lookup"><span data-stu-id="b5692-115">May be **NULL** if *celt* is one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5692-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5692-116">Return value</span></span>

<span data-ttu-id="b5692-117">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b5692-117">This method can return one of these values.</span></span>



| <span data-ttu-id="b5692-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b5692-118">Value</span></span>                                                                                     | <span data-ttu-id="b5692-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b5692-119">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="b5692-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b5692-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="b5692-121">Von der Methode wurde *die Anzahl der* Elemente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b5692-121">Method returned *celt* number of elements.</span></span><br/>         |
| <dl> <span data-ttu-id="b5692-122"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="b5692-122"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="b5692-123">Die Anzahl der verbleibenden Elemente war kleiner als *celt*.</span><span class="sxs-lookup"><span data-stu-id="b5692-123">Number of elements remaining was less than *celt*.</span></span><br/> |
| <dl> <span data-ttu-id="b5692-124"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="b5692-124"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="b5692-125">Der *PVal* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="b5692-125">The *pVal* parameter is not a valid pointer.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="b5692-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5692-126">Remarks</span></span>

<span data-ttu-id="b5692-127">TAPI Ruft die **adressf** -Methode auf der [**ITmedia**](itmedia.md) -Schnittstelle auf, die von **ienummedia:: Next** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="b5692-127">TAPI calls the **AddRef** method on the [**ITMedia**](itmedia.md) interface returned by **IEnumMedia::Next**.</span></span> <span data-ttu-id="b5692-128">Die Anwendung muss Release auf der **ITmedia** -Schnittstelle aufzurufen, um Ressourcen frei **zugeben** , die ihr zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b5692-128">The application must call **Release** on the **ITMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5692-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5692-129">Requirements</span></span>



| <span data-ttu-id="b5692-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5692-130">Requirement</span></span> | <span data-ttu-id="b5692-131">Wert</span><span class="sxs-lookup"><span data-stu-id="b5692-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5692-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="b5692-132">TAPI version</span></span><br/> | <span data-ttu-id="b5692-133">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="b5692-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b5692-134">Header</span><span class="sxs-lookup"><span data-stu-id="b5692-134">Header</span></span><br/>       | <dl> <span data-ttu-id="b5692-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5692-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5692-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b5692-136">Library</span></span><br/>      | <dl> <span data-ttu-id="b5692-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5692-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b5692-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b5692-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="b5692-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5692-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5692-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5692-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5692-141">**Ienummedia**</span><span class="sxs-lookup"><span data-stu-id="b5692-141">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




