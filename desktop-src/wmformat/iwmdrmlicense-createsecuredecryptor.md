---
title: Iwmdrmlicense | atesecuredecryptor-Methode (wmdrmsdk. h)
description: Die Methode "kreatesecuredecryptor" erstellt ein sicheres Entschlüsselungs-Objekt. Der sichere entschlüsselungstyp unterscheidet sich vom normalen entschlüsselungstyp darin, dass er den Inhalt entschlüsselt und dann gemäß den in den Parametern dieser Methode angegebenen Einstellungen erneut verschlüsselt.
ms.assetid: f3fe8d47-ec7b-4ba5-b5ae-6262cb455ffc
keywords:
- "\"Kreatesecuredecryptor\"-Methode Windows Media-Format"
- Kreatesecuredecryptor-Methode Windows Media-Format, iwmdrmlicense-Schnittstelle
- Iwmdrmlicense-Schnittstelle Windows Media-Format, Methode "kreatesecuredecryptor"
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateSecureDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ededb4c985e345c1e40563d02c87bfe447b8960f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358210"
---
# <a name="iwmdrmlicensecreatesecuredecryptor-method"></a><span data-ttu-id="836d9-107">Iwmdrmlicense:: kreatesecuredecryptor-Methode</span><span class="sxs-lookup"><span data-stu-id="836d9-107">IWMDRMLicense::CreateSecureDecryptor method</span></span>

<span data-ttu-id="836d9-108">Die Methode " **kreatesecuredecryptor** " erstellt ein sicheres Entschlüsselungs-Objekt.</span><span class="sxs-lookup"><span data-stu-id="836d9-108">The **CreateSecureDecryptor** method creates a secure decryptor object.</span></span> <span data-ttu-id="836d9-109">Der sichere entschlüsselungstyp unterscheidet sich vom normalen entschlüsselungstyp darin, dass er den Inhalt entschlüsselt und dann gemäß den in den Parametern dieser Methode angegebenen Einstellungen erneut verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="836d9-109">The secure decryptor differs from the normal decryptor in that it decrypts the content and then re-encrypts it according to the settings specified in the parameters of this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="836d9-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="836d9-110">Syntax</span></span>


```C++
HRESULT CreateSecureDecryptor(
  [in]      BYTE          *pbCertificate,
  [in]      DWORD         cbCertificate,
  [in]      DWORD         dwCertificateType,
  [in]      DWORD         dwFlags,
  [out]     BYTE          *pbInitializationVector,
  [in, out] DWORD         *pcbInitializationVector,
  [out]     IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a><span data-ttu-id="836d9-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="836d9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="836d9-112">*pbcertificate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="836d9-112">*pbCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="836d9-113">Zertifikat der aufrufenden Anwendung.</span><span class="sxs-lookup"><span data-stu-id="836d9-113">Certificate of the calling application.</span></span>

</dd> <dt>

<span data-ttu-id="836d9-114">*cbcertificate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="836d9-114">*cbCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="836d9-115">Größe des Zertifikats in Bytes.</span><span class="sxs-lookup"><span data-stu-id="836d9-115">Size of the certificate in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="836d9-116">*dwcertifialisietype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="836d9-116">*dwCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="836d9-117">Der Typ des Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="836d9-117">The type of the certificate.</span></span> <span data-ttu-id="836d9-118">Legen Sie auf WMDRM \_ Certificate \_ Type \_ XML fest.</span><span class="sxs-lookup"><span data-stu-id="836d9-118">Set to WMDRM\_CERTIFICATE\_TYPE\_XML.</span></span>

</dd> <dt>

<span data-ttu-id="836d9-119">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="836d9-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="836d9-120">Der Typ des Sitzungs Schutzes, der für die erneute Codierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="836d9-120">The type of session protection to use for re-encoding.</span></span> <span data-ttu-id="836d9-121">Muss auf eine der Konstanten in der folgenden Tabelle festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="836d9-121">Must be set to one of the constants in the following table:</span></span>



| <span data-ttu-id="836d9-122">Konstante</span><span class="sxs-lookup"><span data-stu-id="836d9-122">Constant</span></span>                     | <span data-ttu-id="836d9-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="836d9-123">Description</span></span>                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="836d9-124">WMDRM \_ - \_ Schutztyp \_ RC4</span><span class="sxs-lookup"><span data-stu-id="836d9-124">WMDRM\_PROTECTION\_TYPE\_RC4</span></span> | <span data-ttu-id="836d9-125">Verwendet die RC4-Verschlüsselung für die Sitzungs Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="836d9-125">Uses RC4 encryption for session encryption.</span></span> <span data-ttu-id="836d9-126">Dies ist der einzige unterstützte Sitzungs Schutz für diese Version.</span><span class="sxs-lookup"><span data-stu-id="836d9-126">This is the only supported session protection for this version.</span></span> |



 

</dd> <dt>

<span data-ttu-id="836d9-127">*pbinitializationvector* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="836d9-127">*pbInitializationVector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="836d9-128">Empfängt den Initialisierungs Vektor.</span><span class="sxs-lookup"><span data-stu-id="836d9-128">Receives the initialization vector.</span></span> <span data-ttu-id="836d9-129">Der Initialisierungs Vektor ist RSA mit dem OAEP-Auffüll Schema verschlüsselt, wobei der öffentliche RSA-Schlüssel im Zertifikat gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="836d9-129">The initialization vector is RSA encrypted using the OAEP padding scheme with the RSA public key found in the certificate.</span></span> <span data-ttu-id="836d9-130">Legen Sie diesen Wert auf **null** fest, um die erforderliche Puffergröße in *pcbinitializationvector* zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="836d9-130">Set to **NULL** to receive the required buffer size in *pcbInitializationVector*.</span></span>

</dd> <dt>

<span data-ttu-id="836d9-131">*pcbinitializationvector* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="836d9-131">*pcbInitializationVector* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="836d9-132">Bei Eingabe die Größe des Puffers, der als *pbinitializationvector* übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="836d9-132">On input, the size of the buffer passed as *pbInitializationVector*.</span></span> <span data-ttu-id="836d9-133">Bei Ausgabe die Größe des verwendeten Teils des Puffers.</span><span class="sxs-lookup"><span data-stu-id="836d9-133">On output, the size of the used portion of the buffer.</span></span> <span data-ttu-id="836d9-134">Wenn Sie **null** für *pbinitializationvector* übergeben, wird dieser Wert auf die erforderliche Puffergröße bei der Ausgabe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="836d9-134">If you pass **NULL** for *pbInitializationVector*, this value is set to the required buffer size on output.</span></span>

</dd> <dt>

<span data-ttu-id="836d9-135">*ppdecryptor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="836d9-135">*ppDecryptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="836d9-136">Empfängt einen Zeiger auf die [**iwmdrmentschlüsseln**](iwmdrmdecrypt.md) -Schnittstelle des neu erstellten Objekts.</span><span class="sxs-lookup"><span data-stu-id="836d9-136">Receives a pointer to the [**IWMDRMDecrypt**](iwmdrmdecrypt.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="836d9-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="836d9-137">Return value</span></span>

<span data-ttu-id="836d9-138">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="836d9-138">The method returns an **HRESULT**.</span></span> <span data-ttu-id="836d9-139">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="836d9-139">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="836d9-140">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="836d9-140">Return code</span></span>                                                                          | <span data-ttu-id="836d9-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="836d9-141">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="836d9-142"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="836d9-142"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="836d9-143">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="836d9-143">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="836d9-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="836d9-144">Remarks</span></span>

<span data-ttu-id="836d9-145">Keine.</span><span class="sxs-lookup"><span data-stu-id="836d9-145">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="836d9-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="836d9-146">Requirements</span></span>



| <span data-ttu-id="836d9-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="836d9-147">Requirement</span></span> | <span data-ttu-id="836d9-148">Wert</span><span class="sxs-lookup"><span data-stu-id="836d9-148">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="836d9-149">Header</span><span class="sxs-lookup"><span data-stu-id="836d9-149">Header</span></span><br/> | <dl> <span data-ttu-id="836d9-150"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="836d9-150"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="836d9-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="836d9-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="836d9-152">**Iwmdrmlicense-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="836d9-152">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





