---
description: 'IEnumTime::Clone-Methode: Die Clone-Methode erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle enthält.'
ms.assetid: 0e9973de-d179-4a2d-a9bd-6d5f2523da52
title: IEnumTime::Clone-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 406dac1fad611ee5d3cb6c8b6ef32dfdb62cc963
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090738"
---
# <a name="ienumtimeclone-method"></a><span data-ttu-id="4bb72-103">IEnumTime::Clone-Methode</span><span class="sxs-lookup"><span data-stu-id="4bb72-103">IEnumTime::Clone method</span></span>

<span data-ttu-id="4bb72-104">\[ Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4bb72-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4bb72-105">Die RTC-Client-API bietet ähnliche Funktionen.\]</span><span class="sxs-lookup"><span data-stu-id="4bb72-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4bb72-106">Die **Clone-Methode** erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle enthält.</span><span class="sxs-lookup"><span data-stu-id="4bb72-106">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bb72-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bb72-107">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumTime **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="4bb72-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bb72-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bb72-109">*ppEnum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4bb72-109">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bb72-110">Zeiger auf das neue [**IEnumTime-Objekt.**](ienumtime.md)</span><span class="sxs-lookup"><span data-stu-id="4bb72-110">Pointer to the new [**IEnumTime**](ienumtime.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bb72-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4bb72-111">Return value</span></span>

<span data-ttu-id="4bb72-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4bb72-112">This method can return one of these values.</span></span>



| <span data-ttu-id="4bb72-113">Wert</span><span class="sxs-lookup"><span data-stu-id="4bb72-113">Value</span></span>                                                                                         | <span data-ttu-id="4bb72-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="4bb72-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="4bb72-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4bb72-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4bb72-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="4bb72-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="4bb72-117"><dt>**E \_ POINTER**</dt></span><span class="sxs-lookup"><span data-stu-id="4bb72-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4bb72-118">Der *ppEnum-Parameter* ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="4bb72-118">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="4bb72-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4bb72-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4bb72-120">Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4bb72-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="4bb72-121"><dt>**E \_ UNEXPECTED**</dt></span><span class="sxs-lookup"><span data-stu-id="4bb72-121"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="4bb72-122">Fehler aus unbekannten Gründen.</span><span class="sxs-lookup"><span data-stu-id="4bb72-122">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="4bb72-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4bb72-123">Remarks</span></span>

<span data-ttu-id="4bb72-124">TAPI ruft die **AddRef-Methode** für die [**IEnumTime-Schnittstelle**](ienumtime.md) auf, die von **IEnumTime::Clone** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4bb72-124">TAPI calls the **AddRef** method on the [**IEnumTime**](ienumtime.md) interface returned by **IEnumTime::Clone**.</span></span> <span data-ttu-id="4bb72-125">Die Anwendung muss **Release** auf der **IEnumTime-Schnittstelle** aufrufen, um zugeordnete Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="4bb72-125">The application must call **Release** on the **IEnumTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bb72-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4bb72-126">Requirements</span></span>



| <span data-ttu-id="4bb72-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4bb72-127">Requirement</span></span> | <span data-ttu-id="4bb72-128">Wert</span><span class="sxs-lookup"><span data-stu-id="4bb72-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4bb72-129">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="4bb72-129">TAPI version</span></span><br/> | <span data-ttu-id="4bb72-130">Erfordert TAPI 3.0 oder höher</span><span class="sxs-lookup"><span data-stu-id="4bb72-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4bb72-131">Header</span><span class="sxs-lookup"><span data-stu-id="4bb72-131">Header</span></span><br/>       | <dl> <span data-ttu-id="4bb72-132"><dt>Sdpblb.h</dt></span><span class="sxs-lookup"><span data-stu-id="4bb72-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="4bb72-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4bb72-133">Library</span></span><br/>      | <dl> <span data-ttu-id="4bb72-134"><dt>Uuid.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bb72-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4bb72-135">DLL</span><span class="sxs-lookup"><span data-stu-id="4bb72-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="4bb72-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bb72-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bb72-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4bb72-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bb72-138">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="4bb72-138">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




