---
description: 'IEnumMedia::Next-Methode: Die Next-Methode ruft die nächste angegebene Anzahl von Elementen in der Enumerationssequenz ab.'
ms.assetid: 39c6d082-415f-4375-8cad-6d4c734d277f
title: IEnumMedia::Next-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711e9c844c46aab6ca90988d4e456e926716b201
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113438"
---
# <a name="ienummedianext-method"></a><span data-ttu-id="c301d-103">IEnumMedia::Next-Methode</span><span class="sxs-lookup"><span data-stu-id="c301d-103">IEnumMedia::Next method</span></span>

<span data-ttu-id="c301d-104">\[ Rendezvous IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c301d-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c301d-105">Die RTC-Client-API bietet ähnliche Funktionen.\]</span><span class="sxs-lookup"><span data-stu-id="c301d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c301d-106">Die **Next-Methode** ruft die nächste angegebene Anzahl von Elementen in der Enumerationssequenz ab.</span><span class="sxs-lookup"><span data-stu-id="c301d-106">The **Next** method gets the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="c301d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c301d-107">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG   celt,
  [out] ITMedia **pVal,
  [out] ULONG   *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="c301d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c301d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c301d-109">*celt* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c301d-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c301d-110">Anzahl der angeforderten Elemente.</span><span class="sxs-lookup"><span data-stu-id="c301d-110">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="c301d-111">*pVal* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c301d-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c301d-112">Zeiger auf die [**ITMedia-Schnittstelle.**](itmedia.md)</span><span class="sxs-lookup"><span data-stu-id="c301d-112">Pointer to the [**ITMedia**](itmedia.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="c301d-113">*pceltFetched* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c301d-113">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c301d-114">Zeiger auf die Anzahl der tatsächlich bereitgestellten Elemente.</span><span class="sxs-lookup"><span data-stu-id="c301d-114">Pointer to the number of elements actually supplied.</span></span> <span data-ttu-id="c301d-115">Kann NULL **sein,** *wenn celt* eins ist.</span><span class="sxs-lookup"><span data-stu-id="c301d-115">May be **NULL** if *celt* is one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c301d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c301d-116">Return value</span></span>

<span data-ttu-id="c301d-117">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c301d-117">This method can return one of these values.</span></span>



| <span data-ttu-id="c301d-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c301d-118">Value</span></span>                                                                                     | <span data-ttu-id="c301d-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c301d-119">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="c301d-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c301d-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="c301d-121">Die Methode hat *die Anzahl der* Elemente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c301d-121">Method returned *celt* number of elements.</span></span><br/>         |
| <dl> <span data-ttu-id="c301d-122"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="c301d-122"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="c301d-123">Die Anzahl der verbleibenden Elemente war kleiner *als celt.*</span><span class="sxs-lookup"><span data-stu-id="c301d-123">Number of elements remaining was less than *celt*.</span></span><br/> |
| <dl> <span data-ttu-id="c301d-124"><dt>**\_E-ZEIGER**</dt></span><span class="sxs-lookup"><span data-stu-id="c301d-124"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="c301d-125">Der *pVal-Parameter* ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="c301d-125">The *pVal* parameter is not a valid pointer.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="c301d-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c301d-126">Remarks</span></span>

<span data-ttu-id="c301d-127">TAPI ruft die **AddRef-Methode** auf der [**ITMedia-Schnittstelle**](itmedia.md) auf, die von **IEnumMedia::Next** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c301d-127">TAPI calls the **AddRef** method on the [**ITMedia**](itmedia.md) interface returned by **IEnumMedia::Next**.</span></span> <span data-ttu-id="c301d-128">Die Anwendung muss **Release** auf der **ITMedia-Schnittstelle** aufrufen, um zugeordnete Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="c301d-128">The application must call **Release** on the **ITMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="c301d-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c301d-129">Requirements</span></span>



| <span data-ttu-id="c301d-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c301d-130">Requirement</span></span> | <span data-ttu-id="c301d-131">Wert</span><span class="sxs-lookup"><span data-stu-id="c301d-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c301d-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="c301d-132">TAPI version</span></span><br/> | <span data-ttu-id="c301d-133">Erfordert TAPI 3.0 oder höher</span><span class="sxs-lookup"><span data-stu-id="c301d-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c301d-134">Header</span><span class="sxs-lookup"><span data-stu-id="c301d-134">Header</span></span><br/>       | <dl> <span data-ttu-id="c301d-135"><dt>Sdpblb.h</dt></span><span class="sxs-lookup"><span data-stu-id="c301d-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="c301d-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c301d-136">Library</span></span><br/>      | <dl> <span data-ttu-id="c301d-137"><dt>Uuid.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c301d-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c301d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c301d-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="c301d-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c301d-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c301d-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c301d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c301d-141">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="c301d-141">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




