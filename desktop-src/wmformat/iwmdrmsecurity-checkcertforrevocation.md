---
title: Iwmdrmsecurity checkcertforwiderruf-Methode (wmdrmsdk. h)
description: Die checkcertforwiderruf-Methode bestimmt, ob ein Zertifikat gesperrt wurde.
ms.assetid: 3efde398-f2ba-486e-b017-6787ca402e4c
keywords:
- Checkcertforwiderruf-Methode Windows Media-Format
- Checkcertforwiderruf-Methode Windows Media-Format, iwmdrmsecurity-Schnittstelle
- Iwmdrmsecurity-Schnittstelle Windows Media-Format, checkcertforwiderruf-Methode
topic_type:
- apiref
api_name:
- IWMDRMSecurity.CheckCertForRevocation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a2439085c6483720e84956ef9932f4f1ab95535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365958"
---
# <a name="iwmdrmsecuritycheckcertforrevocation-method"></a><span data-ttu-id="74eca-106">Iwmdrmsecurity:: checkcertforwiderruf-Methode</span><span class="sxs-lookup"><span data-stu-id="74eca-106">IWMDRMSecurity::CheckCertForRevocation method</span></span>

<span data-ttu-id="74eca-107">Die **checkcertforwiderruf** -Methode bestimmt, ob ein Zertifikat gesperrt wurde.</span><span class="sxs-lookup"><span data-stu-id="74eca-107">The **CheckCertForRevocation** method determines whether a certificate has been revoked.</span></span>

## <a name="syntax"></a><span data-ttu-id="74eca-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="74eca-108">Syntax</span></span>


```C++
HRESULT CheckCertForRevocation(
  [in]  REFGUID rguidRevocationList,
  [in]  BYTE    *pbCert,
  [in]  DWORD   cbCert,
  [out] BOOL    *fRevoked
);
```



## <a name="parameters"></a><span data-ttu-id="74eca-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="74eca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74eca-110">*rguidrevocationlist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74eca-110">*rguidRevocationList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74eca-111">GUID, die die zu verwendende Sperr Liste identifiziert.</span><span class="sxs-lookup"><span data-stu-id="74eca-111">GUID identifying the revocation list to use.</span></span> <span data-ttu-id="74eca-112">Legen Sie auf einen der Werte in der folgenden Tabelle fest.</span><span class="sxs-lookup"><span data-stu-id="74eca-112">Set to one of the values in the following table.</span></span>



| <span data-ttu-id="74eca-113">GUID-Konstante</span><span class="sxs-lookup"><span data-stu-id="74eca-113">GUID constant</span></span>                 | <span data-ttu-id="74eca-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74eca-114">Description</span></span>                                                                                |
|-------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="74eca-115">WMDRM- \_ revocationtype- \_ App</span><span class="sxs-lookup"><span data-stu-id="74eca-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="74eca-116">Gibt die Sperr Liste für das Anwendungs Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="74eca-116">Specifies the application certificate revocation list.</span></span>                                     |
| <span data-ttu-id="74eca-117">WMDRM- \_ revocationtype- \_ Gerät</span><span class="sxs-lookup"><span data-stu-id="74eca-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="74eca-118">Gibt die Zertifikat Sperr Liste für das Gerät an.</span><span class="sxs-lookup"><span data-stu-id="74eca-118">Specifies the device certificate revocation list.</span></span>                                          |
| <span data-ttu-id="74eca-119">WMDRM \_ revocationtype \_ Cardea</span><span class="sxs-lookup"><span data-stu-id="74eca-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="74eca-120">Gibt die Zertifikat Sperr Liste für Microsoft Windows Media DRM für Netzwerkgeräte an.</span><span class="sxs-lookup"><span data-stu-id="74eca-120">Specifies the Microsoft Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="74eca-121">*pbcert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74eca-121">*pbCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74eca-122">Puffer, der das zu überprüfen Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="74eca-122">Buffer containing the certificate to look up.</span></span>

</dd> <dt>

<span data-ttu-id="74eca-123">*cbcert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74eca-123">*cbCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74eca-124">Größe des Puffers *pbcert*(in Bytes).</span><span class="sxs-lookup"><span data-stu-id="74eca-124">Size of the buffer *pbCert*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="74eca-125">*frei.* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="74eca-125">*fRevoked* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74eca-126">Gibt bei Ausgabe an, ob das Zertifikat in der Sperr Liste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="74eca-126">On output, indicates whether the certificate is present in the revocation list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74eca-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74eca-127">Return value</span></span>

<span data-ttu-id="74eca-128">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="74eca-128">The method returns an **HRESULT**.</span></span> <span data-ttu-id="74eca-129">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="74eca-129">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="74eca-130">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="74eca-130">Return code</span></span>                                                                          | <span data-ttu-id="74eca-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74eca-131">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="74eca-132"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="74eca-132"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="74eca-133">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="74eca-133">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="74eca-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74eca-134">Requirements</span></span>



| <span data-ttu-id="74eca-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74eca-135">Requirement</span></span> | <span data-ttu-id="74eca-136">Wert</span><span class="sxs-lookup"><span data-stu-id="74eca-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74eca-137">Header</span><span class="sxs-lookup"><span data-stu-id="74eca-137">Header</span></span><br/>  | <dl> <span data-ttu-id="74eca-138"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="74eca-138"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="74eca-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="74eca-139">Library</span></span><br/> | <dl> <span data-ttu-id="74eca-140"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74eca-140"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74eca-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74eca-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74eca-142">**Iwmdrmsecurity-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="74eca-142">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





