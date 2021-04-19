---
description: Die Get-Methode ruft den Wert einer angegebenen audioeinstellungs Eigenschaft ab.
ms.assetid: 5ad9a4e8-c5b0-43e9-bf75-6460fd23501a
title: 'Itaudiosettings:: Get-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2773bf0f1a26978321ed0d02c3c30d8a96fef1c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361647"
---
# <a name="itaudiosettingsget-method"></a><span data-ttu-id="26b68-103">Itaudiosettings:: Get-Methode</span><span class="sxs-lookup"><span data-stu-id="26b68-103">ITAudioSettings::Get method</span></span>

<span data-ttu-id="26b68-104">\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="26b68-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="26b68-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="26b68-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="26b68-106">Die **Get** -Methode ruft den Wert einer angegebenen [**audioeinstellungs Eigenschaft**](audiosettingsproperty.md)ab.</span><span class="sxs-lookup"><span data-stu-id="26b68-106">The **Get** method retrieves the value of a given [**audio setting property**](audiosettingsproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="26b68-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="26b68-107">Syntax</span></span>


```C++
HRESULT get_Call(
  [out] ITCallInfo **ppCall
);
```



## <a name="parameters"></a><span data-ttu-id="26b68-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="26b68-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26b68-109">*Eigenschaft* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26b68-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26b68-110">Member der [**audiosettingsproperty**](audiosettingsproperty.md) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="26b68-110">Member of the [**AudioSettingsProperty**](audiosettingsproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="26b68-111">*plvalue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="26b68-111">*plValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26b68-112">Der Wert der input- *Eigenschaft*.</span><span class="sxs-lookup"><span data-stu-id="26b68-112">Value of the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="26b68-113">*plflags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="26b68-113">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26b68-114">Der Wert der [**tapicontrolflags**](tapicontrolflags.md) -Enumeration, die angibt, wie der- *Eigenschafts* Wert gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="26b68-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26b68-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26b68-115">Return value</span></span>

<span data-ttu-id="26b68-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="26b68-116">This method can return one of these values.</span></span>



| <span data-ttu-id="26b68-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="26b68-117">Return code</span></span>                                                                                   | <span data-ttu-id="26b68-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26b68-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="26b68-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="26b68-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="26b68-120">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="26b68-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="26b68-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="26b68-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="26b68-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="26b68-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="26b68-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26b68-123">Requirements</span></span>



| <span data-ttu-id="26b68-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26b68-124">Requirement</span></span> | <span data-ttu-id="26b68-125">Wert</span><span class="sxs-lookup"><span data-stu-id="26b68-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="26b68-126">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="26b68-126">TAPI version</span></span><br/> | <span data-ttu-id="26b68-127">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="26b68-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="26b68-128">Header</span><span class="sxs-lookup"><span data-stu-id="26b68-128">Header</span></span><br/>       | <dl> <span data-ttu-id="26b68-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="26b68-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="26b68-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="26b68-130">Library</span></span><br/>      | <dl> <span data-ttu-id="26b68-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26b68-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="26b68-132">DLL</span><span class="sxs-lookup"><span data-stu-id="26b68-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="26b68-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26b68-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26b68-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26b68-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26b68-135">**Itaudiosettings**</span><span class="sxs-lookup"><span data-stu-id="26b68-135">**ITAudioSettings**</span></span>](itaudiosettings.md)
</dt> <dt>

[<span data-ttu-id="26b68-136">**Tapicontrolflags**</span><span class="sxs-lookup"><span data-stu-id="26b68-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="26b68-137">**Audiosettingsproperty**</span><span class="sxs-lookup"><span data-stu-id="26b68-137">**AudioSettingsProperty**</span></span>](audiosettingsproperty.md)
</dt> </dl>

 

 




