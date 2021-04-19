---
description: Mit der Put \_ sessionversion-Methode wird die Sitzungs Version festgelegt.
ms.assetid: 8984d608-0fad-4979-9c58-ac2fb7926796
title: Itsdp::p ut_SessionVersion-Methode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a096117f894a2ff33f127c683b84ba50e88308e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373989"
---
# <a name="itsdpput_sessionversion-method"></a><span data-ttu-id="4c607-103">Itsdp::p UT \_ sessionversion-Methode</span><span class="sxs-lookup"><span data-stu-id="4c607-103">ITSdp::put\_SessionVersion method</span></span>

<span data-ttu-id="4c607-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4c607-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4c607-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="4c607-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4c607-106">Mit der **Put \_ sessionversion** -Methode wird die Sitzungs Version festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4c607-106">The **put\_SessionVersion** method sets the session version.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c607-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c607-107">Syntax</span></span>


```C++
HRESULT put_SessionVersion(
  [in] DOUBLE SessionVersion
);
```



## <a name="parameters"></a><span data-ttu-id="4c607-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c607-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c607-109">*Sessionversion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c607-109">*SessionVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c607-110">Der Sitzungs Versions Wert.</span><span class="sxs-lookup"><span data-stu-id="4c607-110">Session version value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c607-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4c607-111">Return value</span></span>

<span data-ttu-id="4c607-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4c607-112">This method can return one of these values.</span></span>



| <span data-ttu-id="4c607-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4c607-113">Return code</span></span>                                                                                   | <span data-ttu-id="4c607-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c607-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="4c607-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4c607-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4c607-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="4c607-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="4c607-117"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="4c607-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4c607-118">Der *sessionversion* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="4c607-118">The *SessionVersion* parameter is not valid.</span></span><br/>         |
| <dl> <span data-ttu-id="4c607-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="4c607-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4c607-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4c607-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="4c607-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="4c607-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="4c607-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="4c607-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="4c607-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="4c607-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="4c607-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="4c607-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="4c607-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4c607-125">Remarks</span></span>

<span data-ttu-id="4c607-126">Der Rückgabewert dieser Methode kann **ulong** lauten, Visual Basic den **ulong** -Typ jedoch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c607-126">The return value of this method could be **ULONG**, but Visual Basic doesn't support the **ULONG** type.</span></span> <span data-ttu-id="4c607-127">Ein **Double** ist der nächste kleinste Typ, der den gesamten erforderlichen Wertebereich umfasst.</span><span class="sxs-lookup"><span data-stu-id="4c607-127">A **DOUBLE** is the next smallest type that encompasses the entire range of values required.</span></span>

<span data-ttu-id="4c607-128">Diese Funktion kann Daten in unverschlüsselter Form über das Netzwerk senden. aus diesem Grund kann ein Benutzer, der sich im Netzwerk befindet, möglicherweise die Daten lesen.</span><span class="sxs-lookup"><span data-stu-id="4c607-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="4c607-129">Das Sicherheitsrisiko, dass Daten im Klartext gesendet werden, sollte vor der Verwendung dieser Methode berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="4c607-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c607-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4c607-130">Requirements</span></span>



| <span data-ttu-id="4c607-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4c607-131">Requirement</span></span> | <span data-ttu-id="4c607-132">Wert</span><span class="sxs-lookup"><span data-stu-id="4c607-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c607-133">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="4c607-133">TAPI version</span></span><br/> | <span data-ttu-id="4c607-134">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="4c607-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4c607-135">Header</span><span class="sxs-lookup"><span data-stu-id="4c607-135">Header</span></span><br/>       | <dl> <span data-ttu-id="4c607-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c607-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="4c607-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4c607-137">Library</span></span><br/>      | <dl> <span data-ttu-id="4c607-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c607-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4c607-139">DLL</span><span class="sxs-lookup"><span data-stu-id="4c607-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="4c607-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c607-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c607-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c607-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c607-142">**Itsdp**</span><span class="sxs-lookup"><span data-stu-id="4c607-142">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="4c607-143">**Itsdp:: get \_ sessionversion**</span><span class="sxs-lookup"><span data-stu-id="4c607-143">**ITSdp::get\_SessionVersion**</span></span>](itsdp-get-sessionversion.md)
</dt> </dl>

 

 




