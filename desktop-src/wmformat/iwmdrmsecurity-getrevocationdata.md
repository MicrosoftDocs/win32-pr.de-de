---
title: Iwmdrmsecurity getrevocationdata-Methode (wmdrmsdk. h)
description: Die getrevocationdata-Methode ruft eine Zertifikat Sperr Liste aus dem lokalen Speicher ab.
ms.assetid: 218f4f3a-02bc-4b1d-9320-e35ed8cc3b11
keywords:
- Getrevocationdata-Methode, Windows Media-Format
- Getrevocationdata-Methode, Windows Media-Format, iwmdrmsecurity-Schnittstelle
- Iwmdrmsecurity-Schnittstelle Windows Media-Format, getrevocationdata-Methode
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38e9e0b428a3922f84141ef855d8468b79b3bb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357977"
---
# <a name="iwmdrmsecuritygetrevocationdata-method"></a><span data-ttu-id="1920e-106">Iwmdrmsecurity:: getrevocationdata-Methode</span><span class="sxs-lookup"><span data-stu-id="1920e-106">IWMDRMSecurity::GetRevocationData method</span></span>

<span data-ttu-id="1920e-107">Die **getrevocationdata** -Methode ruft eine Zertifikat Sperr Liste aus dem lokalen Speicher ab.</span><span class="sxs-lookup"><span data-stu-id="1920e-107">The **GetRevocationData** method retrieves a certificate revocation list from the local store.</span></span>

## <a name="syntax"></a><span data-ttu-id="1920e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1920e-108">Syntax</span></span>


```C++
HRESULT GetRevocationData(
  [in]      REFGUID f_guidRevocationType,
  [out]     BYTE    *f_pbCRL,
  [in, out] DWORD   *f_pcbCRL
);
```



## <a name="parameters"></a><span data-ttu-id="1920e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1920e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1920e-110">*f \_ guidrevocationtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1920e-110">*f\_guidRevocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1920e-111">GUID, die den Typ der abzurufenden Sperr Liste identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1920e-111">GUID identifying the type of revocation list to retrieve.</span></span> <span data-ttu-id="1920e-112">Verwenden Sie eine der-Konstanten in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1920e-112">Use one of the constants in the following table.</span></span>



| <span data-ttu-id="1920e-113">GUID-Konstante</span><span class="sxs-lookup"><span data-stu-id="1920e-113">GUID constant</span></span>                 | <span data-ttu-id="1920e-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1920e-114">Description</span></span>                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1920e-115">WMDRM- \_ revocationtype- \_ App</span><span class="sxs-lookup"><span data-stu-id="1920e-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="1920e-116">Gibt die Sperr Liste für das Anwendungs Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="1920e-116">Specifies the application certificate revocation list.</span></span>                           |
| <span data-ttu-id="1920e-117">WMDRM- \_ revocationtype- \_ Gerät</span><span class="sxs-lookup"><span data-stu-id="1920e-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="1920e-118">Gibt die Zertifikat Sperr Liste für das Gerät an.</span><span class="sxs-lookup"><span data-stu-id="1920e-118">Specifies the device certificate revocation list.</span></span>                                |
| <span data-ttu-id="1920e-119">WMDRM \_ revocationtype \_ Cardea</span><span class="sxs-lookup"><span data-stu-id="1920e-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="1920e-120">Gibt die Zertifikat Sperr Liste für Windows Media DRM für Netzwerkgeräte an.</span><span class="sxs-lookup"><span data-stu-id="1920e-120">Specifies the Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="1920e-121">*f \_ pbcrl* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1920e-121">*f\_pbCRL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1920e-122">Puffer, der die Sperr Liste empfängt.</span><span class="sxs-lookup"><span data-stu-id="1920e-122">Buffer that receives the revocation list.</span></span> <span data-ttu-id="1920e-123">Auf **null** festgelegt, um die erforderliche Puffergröße zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1920e-123">Set to **NULL** to get the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="1920e-124">*f \_ pcbcrl* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1920e-124">*f\_pcbCRL* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1920e-125">Größe des Puffers in Byte.</span><span class="sxs-lookup"><span data-stu-id="1920e-125">Size of the buffer in bytes.</span></span> <span data-ttu-id="1920e-126">Wenn *f \_ pbcrl* **null** ist, wird dieser Wert auf die erforderliche Puffergröße bei der Ausgabe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1920e-126">If *f\_pbCRL* is **NULL**, this value is set to the required buffer size on output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1920e-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1920e-127">Return value</span></span>

<span data-ttu-id="1920e-128">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="1920e-128">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1920e-129">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1920e-129">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1920e-130">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1920e-130">Return code</span></span>                                                                          | <span data-ttu-id="1920e-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1920e-131">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1920e-132"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1920e-132"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1920e-133">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1920e-133">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1920e-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1920e-134">Requirements</span></span>



| <span data-ttu-id="1920e-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1920e-135">Requirement</span></span> | <span data-ttu-id="1920e-136">Wert</span><span class="sxs-lookup"><span data-stu-id="1920e-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1920e-137">Header</span><span class="sxs-lookup"><span data-stu-id="1920e-137">Header</span></span><br/>  | <dl> <span data-ttu-id="1920e-138"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="1920e-138"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="1920e-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1920e-139">Library</span></span><br/> | <dl> <span data-ttu-id="1920e-140"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1920e-140"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1920e-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1920e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1920e-142">**Automatisierte Sperrung und Erneuerung von Komponenten**</span><span class="sxs-lookup"><span data-stu-id="1920e-142">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="1920e-143">**Getrevocationdataversion**</span><span class="sxs-lookup"><span data-stu-id="1920e-143">**GetRevocationDataVersion**</span></span>](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[<span data-ttu-id="1920e-144">**Iwmdrmsecurity-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="1920e-144">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> <dt>

[<span data-ttu-id="1920e-145">**"Abtrevocationdata"**</span><span class="sxs-lookup"><span data-stu-id="1920e-145">**SetRevocationData**</span></span>](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





