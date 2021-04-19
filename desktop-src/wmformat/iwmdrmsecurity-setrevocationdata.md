---
title: Iwmdrmsecurity-Methode "* trevocationdata" (wmdrmsdk. h)
description: Die setrevocationdata-Methode legt eine Zertifikat Sperr Liste im lokalen Speicher fest.
ms.assetid: 7e1c6d50-7a22-41b7-b29f-b1e5809a2097
keywords:
- "\"Strevocationdata\"-Methode, Windows Media-Format"
- "\"Ttrevocationdata\"-Methode, Windows Media-Format, iwmdrmsecurity-Schnittstelle"
- Iwmdrmsecurity-Schnittstelle Windows Media-Format, Methode "Methode"
topic_type:
- apiref
api_name:
- IWMDRMSecurity.SetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e3ece5a9285420261add123a61d0b7123896e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369978"
---
# <a name="iwmdrmsecuritysetrevocationdata-method"></a><span data-ttu-id="a186a-106">Iwmdrmsecurity:: abtrevocationdata-Methode</span><span class="sxs-lookup"><span data-stu-id="a186a-106">IWMDRMSecurity::SetRevocationData method</span></span>

<span data-ttu-id="a186a-107">Die **setrevocationdata** -Methode legt eine Zertifikat Sperr Liste im lokalen Speicher fest.</span><span class="sxs-lookup"><span data-stu-id="a186a-107">The **SetRevocationData** method sets a certificate revocation list in the local store.</span></span>

## <a name="syntax"></a><span data-ttu-id="a186a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a186a-108">Syntax</span></span>


```C++
HRESULT SetRevocationData(
  [in] REFGUID f_guidRevocationType,
  [in] BYTE    *f_pbCRL,
  [in] DWORD   f_cbCRL
);
```



## <a name="parameters"></a><span data-ttu-id="a186a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a186a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a186a-110">*f \_ guidrevocationtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a186a-110">*f\_guidRevocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a186a-111">GUID, die den Typ der Sperr Liste angibt.</span><span class="sxs-lookup"><span data-stu-id="a186a-111">GUID specifying the type of revocation list.</span></span> <span data-ttu-id="a186a-112">Legen Sie auf eine der Konstanten in der folgenden Tabelle fest.</span><span class="sxs-lookup"><span data-stu-id="a186a-112">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="a186a-113">GUID-Konstante</span><span class="sxs-lookup"><span data-stu-id="a186a-113">GUID constant</span></span>                 | <span data-ttu-id="a186a-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a186a-114">Description</span></span>                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a186a-115">WMDRM- \_ revocationtype- \_ App</span><span class="sxs-lookup"><span data-stu-id="a186a-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="a186a-116">Gibt die Sperr Liste für das Anwendungs Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="a186a-116">Specifies the application certificate revocation list.</span></span>                           |
| <span data-ttu-id="a186a-117">WMDRM- \_ revocationtype- \_ Gerät</span><span class="sxs-lookup"><span data-stu-id="a186a-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="a186a-118">Gibt die Zertifikat Sperr Liste für das Gerät an.</span><span class="sxs-lookup"><span data-stu-id="a186a-118">Specifies the device certificate revocation list.</span></span>                                |
| <span data-ttu-id="a186a-119">WMDRM \_ revocationtype \_ Cardea</span><span class="sxs-lookup"><span data-stu-id="a186a-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="a186a-120">Gibt die Zertifikat Sperr Liste für Windows Media DRM für Netzwerkgeräte an.</span><span class="sxs-lookup"><span data-stu-id="a186a-120">Specifies the Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="a186a-121">*f \_ pbcrl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a186a-121">*f\_pbCRL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a186a-122">Puffer, der die Zertifikat Sperr Liste enthält.</span><span class="sxs-lookup"><span data-stu-id="a186a-122">Buffer containing the certificate revocation list.</span></span>

</dd> <dt>

<span data-ttu-id="a186a-123">*f \_ cbcrl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a186a-123">*f\_cbCRL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a186a-124">Größe des Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a186a-124">Size of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a186a-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a186a-125">Return value</span></span>

<span data-ttu-id="a186a-126">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="a186a-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a186a-127">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a186a-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a186a-128">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a186a-128">Return code</span></span>                                                                          | <span data-ttu-id="a186a-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a186a-129">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a186a-130"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a186a-130"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a186a-131">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a186a-131">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a186a-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a186a-132">Requirements</span></span>



| <span data-ttu-id="a186a-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a186a-133">Requirement</span></span> | <span data-ttu-id="a186a-134">Wert</span><span class="sxs-lookup"><span data-stu-id="a186a-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a186a-135">Header</span><span class="sxs-lookup"><span data-stu-id="a186a-135">Header</span></span><br/>  | <dl> <span data-ttu-id="a186a-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="a186a-136"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="a186a-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a186a-137">Library</span></span><br/> | <dl> <span data-ttu-id="a186a-138"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a186a-138"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a186a-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a186a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a186a-140">**Getrevocationdata**</span><span class="sxs-lookup"><span data-stu-id="a186a-140">**GetRevocationData**</span></span>](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[<span data-ttu-id="a186a-141">**Getrevocationdataversion**</span><span class="sxs-lookup"><span data-stu-id="a186a-141">**GetRevocationDataVersion**</span></span>](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[<span data-ttu-id="a186a-142">**Iwmdrmsecurity-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a186a-142">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





