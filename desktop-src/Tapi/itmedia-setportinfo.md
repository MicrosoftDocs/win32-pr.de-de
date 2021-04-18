---
description: Die setportinfo-Methode legt den Wert für den 16-Bit-Port für den ersten Port und die Anzahl der für eine Sitzung benötigten Ports fest.
ms.assetid: 4726b39b-cd10-4630-8f38-8671db4f432b
title: 'ITmedia:: setportinfo-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c605c1768316871f6c3c9ec10f991f21c1643794
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352132"
---
# <a name="itmediasetportinfo-method"></a><span data-ttu-id="103d4-103">ITmedia:: setportinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="103d4-103">ITMedia::SetPortInfo method</span></span>

<span data-ttu-id="103d4-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="103d4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="103d4-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="103d4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="103d4-106">Die **setportinfo** -Methode legt den Wert für den 16-Bit-Port für den ersten Port und die Anzahl der für eine Sitzung benötigten Ports fest.</span><span class="sxs-lookup"><span data-stu-id="103d4-106">The **SetPortInfo** method sets the 16-bit port value for the first port and the number of ports needed for a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="103d4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="103d4-107">Syntax</span></span>


```C++
HRESULT SetPortInfo(
  [in] LONG StartPort,
  [in] LONG NumPorts
);
```



## <a name="parameters"></a><span data-ttu-id="103d4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="103d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="103d4-109">*Startport* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="103d4-109">*StartPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="103d4-110">Startport.</span><span class="sxs-lookup"><span data-stu-id="103d4-110">Starting port.</span></span> <span data-ttu-id="103d4-111">Hierbei kann es sich um einen Wert im Bereich 0-65535 handeln.</span><span class="sxs-lookup"><span data-stu-id="103d4-111">This can be a value in the range 0-65535.</span></span>

</dd> <dt>

<span data-ttu-id="103d4-112">*Numports* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="103d4-112">*NumPorts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="103d4-113">Anzahl von Ports.</span><span class="sxs-lookup"><span data-stu-id="103d4-113">Number of ports.</span></span> <span data-ttu-id="103d4-114">Hierbei kann es sich um einen Wert im Bereich 0-65535 handeln.</span><span class="sxs-lookup"><span data-stu-id="103d4-114">This can be a value in the range 0-65535.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="103d4-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="103d4-115">Return value</span></span>

<span data-ttu-id="103d4-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="103d4-116">This method can return one of these values.</span></span>



| <span data-ttu-id="103d4-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="103d4-117">Return code</span></span>                                                                                   | <span data-ttu-id="103d4-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="103d4-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="103d4-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="103d4-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="103d4-120">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="103d4-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="103d4-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="103d4-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="103d4-122">Der *startport-Parameter oder der numports* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="103d4-122">The *StartPort or NumPorts* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="103d4-123"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="103d4-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="103d4-124">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="103d4-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="103d4-125"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="103d4-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="103d4-126">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="103d4-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="103d4-127"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="103d4-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="103d4-128">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="103d4-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="103d4-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="103d4-129">Remarks</span></span>

<span data-ttu-id="103d4-130">Diese Funktion kann Daten in unverschlüsselter Form über das Netzwerk senden. aus diesem Grund kann ein Benutzer, der sich im Netzwerk befindet, möglicherweise die Daten lesen.</span><span class="sxs-lookup"><span data-stu-id="103d4-130">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="103d4-131">Das Sicherheitsrisiko, dass Daten im Klartext gesendet werden, sollte vor der Verwendung dieser Methode berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="103d4-131">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="103d4-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="103d4-132">Requirements</span></span>



| <span data-ttu-id="103d4-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="103d4-133">Requirement</span></span> | <span data-ttu-id="103d4-134">Wert</span><span class="sxs-lookup"><span data-stu-id="103d4-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="103d4-135">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="103d4-135">TAPI version</span></span><br/> | <span data-ttu-id="103d4-136">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="103d4-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="103d4-137">Header</span><span class="sxs-lookup"><span data-stu-id="103d4-137">Header</span></span><br/>       | <dl> <span data-ttu-id="103d4-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="103d4-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="103d4-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="103d4-139">Library</span></span><br/>      | <dl> <span data-ttu-id="103d4-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="103d4-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="103d4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="103d4-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="103d4-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="103d4-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="103d4-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="103d4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="103d4-144">**ITmedia**</span><span class="sxs-lookup"><span data-stu-id="103d4-144">**ITMedia**</span></span>](itmedia.md)
</dt> </dl>

 

 




