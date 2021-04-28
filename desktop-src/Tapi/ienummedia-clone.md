---
description: 'IEnumMedia::Clone-Methode: Die Clone-Methode erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle enthält.'
ms.assetid: b48399f5-daaa-40e4-bd80-a918539d25c6
title: IEnumMedia::Clone-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f81542e1b0e3fc5bfb44e59827608396d7d906c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114548"
---
# <a name="ienummediaclone-method"></a><span data-ttu-id="8439f-103">IEnumMedia::Clone-Methode</span><span class="sxs-lookup"><span data-stu-id="8439f-103">IEnumMedia::Clone method</span></span>

<span data-ttu-id="8439f-104">\[ Rendezvous-IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8439f-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8439f-105">Die RTC-Client-API bietet ähnliche Funktionen.\]</span><span class="sxs-lookup"><span data-stu-id="8439f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8439f-106">Die **Clone-Methode** erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle enthält.</span><span class="sxs-lookup"><span data-stu-id="8439f-106">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="8439f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8439f-107">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumMedia **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="8439f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8439f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8439f-109">*ppEnum* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8439f-109">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8439f-110">Zeiger auf das neue [**IEnumMedia-Objekt.**](ienummedia.md)</span><span class="sxs-lookup"><span data-stu-id="8439f-110">Pointer to the new [**IEnumMedia**](ienummedia.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8439f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8439f-111">Return value</span></span>

<span data-ttu-id="8439f-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8439f-112">This method can return one of these values.</span></span>



| <span data-ttu-id="8439f-113">Wert</span><span class="sxs-lookup"><span data-stu-id="8439f-113">Value</span></span>                                                                                         | <span data-ttu-id="8439f-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8439f-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8439f-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8439f-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8439f-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8439f-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8439f-117"><dt>**E \_ POINTER**</dt></span><span class="sxs-lookup"><span data-stu-id="8439f-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8439f-118">Der *ppEnum-Parameter* ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="8439f-118">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="8439f-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8439f-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8439f-120">Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8439f-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="8439f-121"><dt>**E \_ UNEXPECTED**</dt></span><span class="sxs-lookup"><span data-stu-id="8439f-121"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="8439f-122">Fehler aus unbekannten Gründen.</span><span class="sxs-lookup"><span data-stu-id="8439f-122">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="8439f-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8439f-123">Remarks</span></span>

<span data-ttu-id="8439f-124">TAPI ruft die **AddRef-Methode** für die [**IEnumMedia-Schnittstelle**](ienummedia.md) auf, die von **IEnumMedia::Clone** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8439f-124">TAPI calls the **AddRef** method on the [**IEnumMedia**](ienummedia.md) interface returned by **IEnumMedia::Clone**.</span></span> <span data-ttu-id="8439f-125">Die Anwendung muss **Release** auf der **IEnumMedia-Schnittstelle** aufrufen, um zugeordnete Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="8439f-125">The application must call **Release** on the **IEnumMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="8439f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8439f-126">Requirements</span></span>



| <span data-ttu-id="8439f-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8439f-127">Requirement</span></span> | <span data-ttu-id="8439f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="8439f-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8439f-129">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="8439f-129">TAPI version</span></span><br/> | <span data-ttu-id="8439f-130">Erfordert TAPI 3.0 oder höher</span><span class="sxs-lookup"><span data-stu-id="8439f-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8439f-131">Header</span><span class="sxs-lookup"><span data-stu-id="8439f-131">Header</span></span><br/>       | <dl> <span data-ttu-id="8439f-132"><dt>Sdpblb.h</dt></span><span class="sxs-lookup"><span data-stu-id="8439f-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8439f-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8439f-133">Library</span></span><br/>      | <dl> <span data-ttu-id="8439f-134"><dt>Uuid.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8439f-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8439f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8439f-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="8439f-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8439f-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8439f-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8439f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8439f-138">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="8439f-138">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




