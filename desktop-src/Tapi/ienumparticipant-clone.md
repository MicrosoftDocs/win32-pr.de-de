---
description: Die Clone-Methode erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält. Diese Methode ist in Visual Basic-und Skriptsprachen ausgeblendet.
ms.assetid: 551e0ddc-7ebf-4fc2-a155-0c9ee2f406d4
title: 'Ienumparticipants:: Clone-Methode (confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5b094f47738fd23f2762b7012a4e23c8b89da57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371339"
---
# <a name="ienumparticipantclone-method"></a><span data-ttu-id="2ad39-104">Ienumteilnehmer:: Clone-Methode</span><span class="sxs-lookup"><span data-stu-id="2ad39-104">IEnumParticipant::Clone method</span></span>

<span data-ttu-id="2ad39-105">\[**Clone** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2ad39-105">\[**Clone** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2ad39-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="2ad39-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2ad39-107">Die **Clone** -Methode erstellt einen weiteren Enumerator, der den gleichen Enumerationszustand wie der aktuelle Enumerator enthält.</span><span class="sxs-lookup"><span data-stu-id="2ad39-107">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span> <span data-ttu-id="2ad39-108">Diese Methode ist in Visual Basic-und Skriptsprachen ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="2ad39-108">This method is hidden from Visual Basic and scripting languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ad39-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ad39-109">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumParticipant **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="2ad39-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ad39-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ad39-111">*ppum* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2ad39-111">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ad39-112">Zeiger auf die neue [**ienumteilnehmer**](ienumparticipant.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2ad39-112">Pointer to new [**IEnumParticipant**](ienumparticipant.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ad39-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ad39-113">Return value</span></span>

<span data-ttu-id="2ad39-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2ad39-114">This method can return one of these values.</span></span>



| <span data-ttu-id="2ad39-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2ad39-115">Return code</span></span>                                                                                   | <span data-ttu-id="2ad39-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ad39-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="2ad39-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2ad39-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2ad39-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="2ad39-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2ad39-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="2ad39-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2ad39-120">Der *ppum* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="2ad39-120">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="2ad39-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="2ad39-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2ad39-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2ad39-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="2ad39-123"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="2ad39-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="2ad39-124">Aus unbekannten Gründen fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="2ad39-124">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="2ad39-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ad39-125">Remarks</span></span>

<span data-ttu-id="2ad39-126">TAPI Ruft die [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) -Methode für die [**ienumparticipants**](ienumparticipant.md) -Schnittstelle auf, die von **ienumteilnehmer:: Clone** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="2ad39-126">TAPI calls the [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method on the [**IEnumParticipant**](ienumparticipant.md) interface returned by **IEnumParticipant::Clone**.</span></span> <span data-ttu-id="2ad39-127">Die Anwendung muss Release auf der **ienumparticipants** -Schnittstelle aufzurufen, um Ihnen zugeordnete Ressourcen frei [**zugeben**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="2ad39-127">The application must call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the **IEnumParticipant** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ad39-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ad39-128">Requirements</span></span>



| <span data-ttu-id="2ad39-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ad39-129">Requirement</span></span> | <span data-ttu-id="2ad39-130">Wert</span><span class="sxs-lookup"><span data-stu-id="2ad39-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ad39-131">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="2ad39-131">TAPI version</span></span><br/> | <span data-ttu-id="2ad39-132">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="2ad39-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2ad39-133">Header</span><span class="sxs-lookup"><span data-stu-id="2ad39-133">Header</span></span><br/>       | <dl> <span data-ttu-id="2ad39-134"><dt>"Confpriv. h"</dt></span><span class="sxs-lookup"><span data-stu-id="2ad39-134"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="2ad39-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2ad39-135">Library</span></span><br/>      | <dl> <span data-ttu-id="2ad39-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ad39-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2ad39-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2ad39-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="2ad39-138"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ad39-138"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2ad39-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ad39-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ad39-140">**Ienumteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="2ad39-140">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="2ad39-141">**Itteilnehmer**</span><span class="sxs-lookup"><span data-stu-id="2ad39-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

