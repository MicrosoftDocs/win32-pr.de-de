---
description: Die Clone-Methode erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.
ms.assetid: b48399f5-daaa-40e4-bd80-a918539d25c6
title: 'Ienummedia:: Clone-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c29671819db202643506cbdf90a1550abb305718
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371340"
---
# <a name="ienummediaclone-method"></a><span data-ttu-id="d1ecb-103">Ienummedia:: Clone-Methode</span><span class="sxs-lookup"><span data-stu-id="d1ecb-103">IEnumMedia::Clone method</span></span>

<span data-ttu-id="d1ecb-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d1ecb-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="d1ecb-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d1ecb-106">Die **Clone** -Methode erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-106">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1ecb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1ecb-107">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumMedia **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="d1ecb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1ecb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1ecb-109">*ppum* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d1ecb-109">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1ecb-110">Zeiger auf das neue [**ienummedia**](ienummedia.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-110">Pointer to the new [**IEnumMedia**](ienummedia.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1ecb-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1ecb-111">Return value</span></span>

<span data-ttu-id="d1ecb-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-112">This method can return one of these values.</span></span>



| <span data-ttu-id="d1ecb-113">Wert</span><span class="sxs-lookup"><span data-stu-id="d1ecb-113">Value</span></span>                                                                                         | <span data-ttu-id="d1ecb-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d1ecb-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="d1ecb-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d1ecb-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d1ecb-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d1ecb-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="d1ecb-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d1ecb-118">Der *ppum* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-118">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="d1ecb-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="d1ecb-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d1ecb-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="d1ecb-121"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="d1ecb-121"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="d1ecb-122">Aus unbekannten Gründen fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-122">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="d1ecb-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1ecb-123">Remarks</span></span>

<span data-ttu-id="d1ecb-124">TAPI Ruft die **adressf** -Methode für die [**ienummedia**](ienummedia.md) -Schnittstelle auf, die von **ienummedia:: Clone** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-124">TAPI calls the **AddRef** method on the [**IEnumMedia**](ienummedia.md) interface returned by **IEnumMedia::Clone**.</span></span> <span data-ttu-id="d1ecb-125">Die Anwendung muss Release auf der **ienummedia** -Schnittstelle aufzurufen, um Ressourcen frei **zugeben** , die ihr zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d1ecb-125">The application must call **Release** on the **IEnumMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1ecb-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1ecb-126">Requirements</span></span>



| <span data-ttu-id="d1ecb-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1ecb-127">Requirement</span></span> | <span data-ttu-id="d1ecb-128">Wert</span><span class="sxs-lookup"><span data-stu-id="d1ecb-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1ecb-129">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="d1ecb-129">TAPI version</span></span><br/> | <span data-ttu-id="d1ecb-130">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="d1ecb-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d1ecb-131">Header</span><span class="sxs-lookup"><span data-stu-id="d1ecb-131">Header</span></span><br/>       | <dl> <span data-ttu-id="d1ecb-132"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1ecb-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1ecb-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d1ecb-133">Library</span></span><br/>      | <dl> <span data-ttu-id="d1ecb-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1ecb-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d1ecb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d1ecb-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="d1ecb-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1ecb-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1ecb-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1ecb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1ecb-138">**Ienummedia**</span><span class="sxs-lookup"><span data-stu-id="d1ecb-138">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




