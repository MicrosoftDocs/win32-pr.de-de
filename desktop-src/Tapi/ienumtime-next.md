---
description: 'IEnumTime::Next-Methode: Die Next-Methode ruft die nächste angegebene Anzahl von Elementen in der Enumerationssequenz ab.'
ms.assetid: e8ca77b8-0322-43b4-9996-26f584cf878a
title: IEnumTime::Next-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1487136b0e3e41ba11a23ba92500d2aa0758df79
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118388"
---
# <a name="ienumtimenext-method"></a><span data-ttu-id="544bb-103">IEnumTime::Next-Methode</span><span class="sxs-lookup"><span data-stu-id="544bb-103">IEnumTime::Next method</span></span>

<span data-ttu-id="544bb-104">\[ Rendezvous IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="544bb-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="544bb-105">Die RTC-Client-API bietet ähnliche Funktionen.\]</span><span class="sxs-lookup"><span data-stu-id="544bb-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="544bb-106">Die **Next-Methode** ruft die nächste angegebene Anzahl von Elementen in der Enumerationssequenz ab.</span><span class="sxs-lookup"><span data-stu-id="544bb-106">The **Next** method gets the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="544bb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="544bb-107">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG  celt,
  [out] ITTime **pVal,
  [out] ULONG  *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="544bb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="544bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="544bb-109">*celt* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="544bb-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="544bb-110">Anzahl der angeforderten Elemente.</span><span class="sxs-lookup"><span data-stu-id="544bb-110">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="544bb-111">*pVal* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="544bb-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="544bb-112">Zeiger auf die [**ITTime-Schnittstelle.**](ittime.md)</span><span class="sxs-lookup"><span data-stu-id="544bb-112">Pointer to the [**ITTime**](ittime.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="544bb-113">*pceltFetched* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="544bb-113">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="544bb-114">Zeiger auf die Anzahl der tatsächlich bereitgestellten Elemente.</span><span class="sxs-lookup"><span data-stu-id="544bb-114">Pointer to the number of elements actually supplied.</span></span> <span data-ttu-id="544bb-115">Kann NULL **sein,** *wenn celt* gleich 1 ist.</span><span class="sxs-lookup"><span data-stu-id="544bb-115">May be **NULL** if *celt* is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="544bb-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="544bb-116">Return value</span></span>

<span data-ttu-id="544bb-117">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="544bb-117">This method can return one of these values.</span></span>



| <span data-ttu-id="544bb-118">Wert</span><span class="sxs-lookup"><span data-stu-id="544bb-118">Value</span></span>                                                                                     | <span data-ttu-id="544bb-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="544bb-119">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="544bb-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="544bb-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="544bb-121">Die Methode hat *die Anzahl der* Elemente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="544bb-121">Method returned *celt* number of elements.</span></span><br/>         |
| <dl> <span data-ttu-id="544bb-122"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="544bb-122"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="544bb-123">Die Anzahl der verbleibenden Elemente war kleiner *als celt.*</span><span class="sxs-lookup"><span data-stu-id="544bb-123">Number of elements remaining was less than *celt*.</span></span><br/> |
| <dl> <span data-ttu-id="544bb-124"><dt>**\_E-ZEIGER**</dt></span><span class="sxs-lookup"><span data-stu-id="544bb-124"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="544bb-125">Der *pVal-Parameter* ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="544bb-125">The *pVal* parameter is not a valid pointer.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="544bb-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="544bb-126">Remarks</span></span>

<span data-ttu-id="544bb-127">TAPI ruft die **AddRef-Methode** für die [**ITTime-Schnittstelle**](ittime.md) auf, die von **IEnumTime::Next** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="544bb-127">TAPI calls the **AddRef** method on the [**ITTime**](ittime.md) interface returned by **IEnumTime::Next**.</span></span> <span data-ttu-id="544bb-128">Die Anwendung muss **Release** auf der **ITTime-Schnittstelle** aufrufen, um zugeordnete Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="544bb-128">The application must call **Release** on the **ITTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="544bb-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="544bb-129">Requirements</span></span>



| <span data-ttu-id="544bb-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="544bb-130">Requirement</span></span> | <span data-ttu-id="544bb-131">Wert</span><span class="sxs-lookup"><span data-stu-id="544bb-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="544bb-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="544bb-132">TAPI version</span></span><br/> | <span data-ttu-id="544bb-133">Erfordert TAPI 3.0 oder höher</span><span class="sxs-lookup"><span data-stu-id="544bb-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="544bb-134">Header</span><span class="sxs-lookup"><span data-stu-id="544bb-134">Header</span></span><br/>       | <dl> <span data-ttu-id="544bb-135"><dt>Sdpblb.h</dt></span><span class="sxs-lookup"><span data-stu-id="544bb-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="544bb-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="544bb-136">Library</span></span><br/>      | <dl> <span data-ttu-id="544bb-137"><dt>Uuid.lib</dt></span><span class="sxs-lookup"><span data-stu-id="544bb-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="544bb-138">DLL</span><span class="sxs-lookup"><span data-stu-id="544bb-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="544bb-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="544bb-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="544bb-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="544bb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="544bb-141">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="544bb-141">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




