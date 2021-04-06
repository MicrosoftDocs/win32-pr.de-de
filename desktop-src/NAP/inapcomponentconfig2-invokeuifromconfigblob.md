---
title: INapComponentConfig2 invokeuifromconfigblob-Methode (napcommon. h)
description: Wird von System Integritätsprüfungen (SHVs) nach Bedarf implementiert, um die Konfiguration eines Remote Computers oder eines lokalen Computers in den Arbeitsspeicher zu laden und eine Benutzeroberfläche anzuzeigen, die die Bearbeitung der Konfigurationsdaten ermöglicht.
ms.assetid: 9c012690-6751-4a47-8683-74abac610c77
keywords:
- Invokeuifromconfigblob-Methode NAP
- Invokeuifromconfigblob-Methode NAP, INapComponentConfig2-Schnittstelle
- INapComponentConfig2 Interface NAP, invokeuifromconfigblob-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIFromConfigBlob
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54cc1efaf7da3434e1aff10d57c2e175481a3d2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858777"
---
# <a name="inapcomponentconfig2invokeuifromconfigblob-method"></a><span data-ttu-id="d5f9d-106">INapComponentConfig2:: invokeuifromconfigblob-Methode</span><span class="sxs-lookup"><span data-stu-id="d5f9d-106">INapComponentConfig2::InvokeUIFromConfigBlob method</span></span>

> [!Note]  
> <span data-ttu-id="d5f9d-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d5f9d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d5f9d-108">Die **invokeuifromconfigblob** -Methode wird nach Bedarf von System Integritätsprüfungen (SHVs) implementiert, um die Konfiguration eines Remote Computers oder eines lokalen Computers in den Arbeitsspeicher zu laden und eine Benutzeroberfläche anzuzeigen, die die Bearbeitung der Konfigurationsdaten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="d5f9d-108">The **InvokeUIFromConfigBlob** method is implemented by system health validators (SHVs) as needed to load the configuration of a remote or local machine in memory and display a UI that allows manipulation of the configuration data.</span></span> <span data-ttu-id="d5f9d-109">Die Konfigurationskomponente muss die Verwendung von [**inapcomponentconfig**](inapcomponentconfig.md) über DCOM unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d5f9d-109">The configuration component must support the usage of [**INapComponentConfig**](inapcomponentconfig.md) through DCOM.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5f9d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5f9d-110">Syntax</span></span>


```C++
HRESULT InvokeUIFromConfigBlob(
  [in, unique] HWND   hwndParent,
  [in]         UINT16 inbCount,
  [in]         BYTE   *inData,
  [out]        UINT16 *outbCount,
  [out]        BYTE   **outdata,
  [out]        BOOL   *fConfigChanged
);
```



## <a name="parameters"></a><span data-ttu-id="d5f9d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5f9d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5f9d-112">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5f9d-112">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5f9d-113">Ein Handle für das übergeordnete Fenster oder Besitzer Fenster.</span><span class="sxs-lookup"><span data-stu-id="d5f9d-113">A handle to the parent or owner window.</span></span> <span data-ttu-id="d5f9d-114">Ein gültiges Fenster Handle muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d5f9d-114">A valid window handle must be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="d5f9d-115">*inbcount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5f9d-115">*inbCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5f9d-116">Die Größe von *InData* in Byte.</span><span class="sxs-lookup"><span data-stu-id="d5f9d-116">The size, in bytes, of *inData*.</span></span>

</dd> <dt>

<span data-ttu-id="d5f9d-117">*InData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5f9d-117">*inData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5f9d-118">Ein Zeiger auf einen Puffer, in dem die anfänglichen Konfigurationsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="d5f9d-118">A pointer to a buffer that stores the initial configuration data.</span></span> <span data-ttu-id="d5f9d-119">Diese Daten werden vom Remote-oder lokalen Computer exportiert.</span><span class="sxs-lookup"><span data-stu-id="d5f9d-119">This data is exported from the remote or local machine.</span></span>

</dd> <dt>

<span data-ttu-id="d5f9d-120">*outbcount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d5f9d-120">*outbCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5f9d-121">Die Größe (in Bytes) der *OutData*.</span><span class="sxs-lookup"><span data-stu-id="d5f9d-121">The size, in bytes, of *outdata*.</span></span>

</dd> <dt>

<span data-ttu-id="d5f9d-122">*OutData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d5f9d-122">*outdata* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5f9d-123">Ein Zeiger auf einen Puffer, in dem Konfigurationsdaten gespeichert werden, die von der SHV-Konfigurations Benutzeroberfläche geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="d5f9d-123">A pointer to a buffer that stores configuration data changed by the SHV configuration user interface.</span></span> <span data-ttu-id="d5f9d-124">Diese Daten werden vom Remote-oder lokalen Computer importiert.</span><span class="sxs-lookup"><span data-stu-id="d5f9d-124">This data is imported by the remote or local machine.</span></span>

</dd> <dt>

<span data-ttu-id="d5f9d-125">nicht *geändert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d5f9d-125">*fConfigChanged* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5f9d-126">Ein Zeiger auf einen **booleschen** Wert, der auf **true** festgelegt ist, wenn die Konfiguration während des UI-Vorgangs geändert wurde, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="d5f9d-126">A pointer to a **BOOL** that is set to **TRUE** if the configuration was changed during the UI operation and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5f9d-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5f9d-127">Return value</span></span>

<span data-ttu-id="d5f9d-128">Gibt \_ bei Erfolg S OK oder einen der standardmäßigen Windows-Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="d5f9d-128">Returns S\_OK if successful, or one of the standard Windows error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5f9d-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5f9d-129">Remarks</span></span>

<span data-ttu-id="d5f9d-130">Bei Verwendung für einen lokalen Computer kann diese Funktion für die SHV-Konfiguration pro Richtlinie verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5f9d-130">If used for a local machine, this function can be used for per policy SHV configuration.</span></span> <span data-ttu-id="d5f9d-131">Es bietet eine Möglichkeit, eine SHV-Benutzeroberfläche aufzurufen und eine vorhandene SHV-Konfiguration zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="d5f9d-131">It provides a way to invoke an SHV UI and edit an existing SHV configuration.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5f9d-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5f9d-132">Requirements</span></span>



| <span data-ttu-id="d5f9d-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5f9d-133">Requirement</span></span> | <span data-ttu-id="d5f9d-134">Wert</span><span class="sxs-lookup"><span data-stu-id="d5f9d-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f9d-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5f9d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d5f9d-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d5f9d-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="d5f9d-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5f9d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d5f9d-138">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5f9d-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d5f9d-139">Header</span><span class="sxs-lookup"><span data-stu-id="d5f9d-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5f9d-140"><dt>Napcommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5f9d-140"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="d5f9d-141">IDL</span><span class="sxs-lookup"><span data-stu-id="d5f9d-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d5f9d-142"><dt>Napcommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d5f9d-142"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5f9d-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5f9d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5f9d-144">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="d5f9d-144">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> </dl>

 

 





