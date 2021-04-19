---
description: Die filesignatureinfo-Methode des Installer-Objekts nimmt den Pfad zu einer Datei an und gibt ein SafeArray von Bytes zurück, die den Hash oder das codierte Zertifikat darstellen.
ms.assetid: ab34bc46-8a8f-4b48-a1d1-d824ff36a9cc
title: Installer. filesignatureinfo-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSignatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5dbb758118b7612aaef3f7cca744674bca1c768d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355891"
---
# <a name="installerfilesignatureinfo-method"></a><span data-ttu-id="0b4f1-103">Installer. filesignatureinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="0b4f1-103">Installer.FileSignatureInfo method</span></span>

<span data-ttu-id="0b4f1-104">Die **filesignatureinfo** -Methode des [**Installer**](installer-object.md) -Objekts nimmt den Pfad zu einer Datei an und gibt ein SafeArray von Bytes zurück, die den Hash oder das codierte Zertifikat darstellen.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-104">The **FileSignatureInfo** method of the [**Installer**](installer-object.md) object takes the path to a file and returns a SAFEARRAY of bytes that represent the hash or the encoded certificate.</span></span> <span data-ttu-id="0b4f1-105">Die Werte können dann verwendet werden, um die Tabellen [msidigitalsignature](msidigitalsignature-table.md), [MsiPatchCertificate](msipatchcertificate-table.md)und [msidigitalcertificate](msidigitalcertificate-table.md) aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-105">The values can then be used to populate the [MsiDigitalSignature](msidigitalsignature-table.md), [MsiPatchCertificate](msipatchcertificate-table.md), and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables.</span></span>

<span data-ttu-id="0b4f1-106">Weitere Informationen finden Sie unter dem [**SAFEARRAY-Datentyp**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span><span class="sxs-lookup"><span data-stu-id="0b4f1-106">For more information, see the [**SAFEARRAY Data Type**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span>

## <a name="syntax"></a><span data-ttu-id="0b4f1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b4f1-107">Syntax</span></span>


```JScript
Installer.FileSignatureInfo(
  FilePath,
  Options,
  Format
)
```



## <a name="parameters"></a><span data-ttu-id="0b4f1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b4f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b4f1-109">*FilePath*</span><span class="sxs-lookup"><span data-stu-id="0b4f1-109">*FilePath*</span></span> 
</dt> <dd>

<span data-ttu-id="0b4f1-110">Vollständiger Pfad zu einer Datei, die digital signiert ist.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-110">Full path to a file that is digitally signed.</span></span>

<span data-ttu-id="0b4f1-111">Beim Auffüllen der Tabellen [msidigitalsignature](msidigitalsignature-table.md) und [msidigitalcertificate](msidigitalcertificate-table.md) verweist *FilePath* auf eine Digital signierte CAB-Datei.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-111">When populating the [MsiDigitalSignature](msidigitalsignature-table.md) and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables, *FilePath* points to a digitally signed cabinet.</span></span> <span data-ttu-id="0b4f1-112">Beim Auffüllen der [MsiPatchCertificate](msipatchcertificate-table.md) -und msidigitalcertificate-Tabellen zeigt *FilePath* auf einen digital signierten Patch.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-112">When populating the [MsiPatchCertificate](msipatchcertificate-table.md) and MsiDigitalCertificate tables, *FilePath* points to a digitally signed patch.</span></span>

</dd> <dt>

<span data-ttu-id="0b4f1-113">*Optionen*</span><span class="sxs-lookup"><span data-stu-id="0b4f1-113">*Options*</span></span> 
</dt> <dd>

<span data-ttu-id="0b4f1-114">Spezielle fehlerfallflags.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-114">Special error case flags.</span></span>



| <span data-ttu-id="0b4f1-115">Flag</span><span class="sxs-lookup"><span data-stu-id="0b4f1-115">Flag</span></span>                                                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="0b4f1-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0b4f1-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiSignatureOptionInvalidHashFatal"></span><span id="msisignatureoptioninvalidhashfatal"></span><span id="MSISIGNATUREOPTIONINVALIDHASHFATAL"></span><dl> <span data-ttu-id="0b4f1-117"><dt>**msisignatureoptioninvalidhashfatal**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0b4f1-117"><dt>**msiSignatureOptionInvalidHashFatal**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="0b4f1-118">Wenn die *Optionen* auf msisignatureoptioninvalidhashfatal festgelegt sind, gibt **filesignatureinfo** immer einen schwerwiegenden Fehler für einen ungültigen Hash zurück.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-118">With *Options* set to msiSignatureOptionInvalidHashFatal, **FileSignatureInfo** always returns a fatal error for an invalid hash.</span></span> <br/> <span data-ttu-id="0b4f1-119">Wenn die *Optionen* nicht auf msisignatureoptioninvalidhashfatal festgelegt sind und *Format* auf msiSignatureInfoCertificate festgelegt ist, gibt **filesignatureinfo** keinen Fehler für einen ungültigen Hash zurück.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-119">If *Options* is not set to msiSignatureOptionInvalidHashFatal and *Format* is set to msiSignatureInfoCertificate, **FileSignatureInfo** does not return an error for an invalid hash.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0b4f1-120">*Format*</span><span class="sxs-lookup"><span data-stu-id="0b4f1-120">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="0b4f1-121">Die angeforderten Signatur Informationen.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-121">The requested signature information.</span></span>



| <span data-ttu-id="0b4f1-122">Flag</span><span class="sxs-lookup"><span data-stu-id="0b4f1-122">Flag</span></span>                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="0b4f1-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0b4f1-123">Meaning</span></span>                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="msiSignatureInfoCertificate"></span><span id="msisignatureinfocertificate"></span><span id="MSISIGNATUREINFOCERTIFICATE"></span><dl> <span data-ttu-id="0b4f1-124"><dt>**msiSignatureInfoCertificate**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0b4f1-124"><dt>**msiSignatureInfoCertificate**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="0b4f1-125">Gibt ein SafeArray von Bytes zurück, die das codierte Zertifikat darstellen.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-125">Returns a SAFEARRAY of bytes that represent the encoded certificate.</span></span><br/> |
| <span id="msiSignatureInfoHash"></span><span id="msisignatureinfohash"></span><span id="MSISIGNATUREINFOHASH"></span><dl> <span data-ttu-id="0b4f1-126"><dt>**msisignatureinfohash**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0b4f1-126"><dt>**msiSignatureInfoHash**</dt> <dt>1</dt></span></span> </dl>                             | <span data-ttu-id="0b4f1-127">Gibt ein SafeArray von Bytes zurück, die den Hash darstellen.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-127">Returns a SAFEARRAY of bytes that represent the hash.</span></span><br/>                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b4f1-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0b4f1-128">Return value</span></span>

<span data-ttu-id="0b4f1-129">Bei erfolgreicher Ausführung gibt die Methode ein [SAFEARRAY](/windows/win32/api/oaidl/ns-oaidl-safearray) von Bytes zurück, das entweder den Hash oder das codierte Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-129">If successful, the method returns a [SAFEARRAY](/windows/win32/api/oaidl/ns-oaidl-safearray) of bytes that contain either the hash or encoded certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b4f1-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b4f1-130">Remarks</span></span>

<span data-ttu-id="0b4f1-131">Um eine vollständig verifizierte signierte Installation mithilfe von Automation zu erstellen, verwenden Sie die **filesignatureinfo** -Methode, um die Tabellen [msidigitalcertificate](msidigitalcertificate-table.md), [MsiPatchCertificate](msipatchcertificate-table.md)und [msidigitalsignature](msidigitalsignature-table.md) aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-131">To author a fully verified signed installation by using automation, use the **FileSignatureInfo** method to populate the [MsiDigitalCertificate](msidigitalcertificate-table.md), [MsiPatchCertificate](msipatchcertificate-table.md), and [MsiDigitalSignature](msidigitalsignature-table.md) tables.</span></span> <span data-ttu-id="0b4f1-132">Weitere Informationen finden Sie unter [Erstellen einer vollständig verifizierten signierten Installation mithilfe von Automation](authoring-a-fully-verified-signed-installation-using-automation.md).</span><span class="sxs-lookup"><span data-stu-id="0b4f1-132">For more information, see [Authoring a Fully Verified Signed Installation Using Automation](authoring-a-fully-verified-signed-installation-using-automation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b4f1-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b4f1-133">Requirements</span></span>



| <span data-ttu-id="0b4f1-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b4f1-134">Requirement</span></span> | <span data-ttu-id="0b4f1-135">Wert</span><span class="sxs-lookup"><span data-stu-id="0b4f1-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b4f1-136">Version</span><span class="sxs-lookup"><span data-stu-id="0b4f1-136">Version</span></span><br/> | <span data-ttu-id="0b4f1-137">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-137">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0b4f1-138">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0b4f1-138">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0b4f1-139">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="0b4f1-139">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0b4f1-140">DLL</span><span class="sxs-lookup"><span data-stu-id="0b4f1-140">DLL</span></span><br/>     | <dl> <span data-ttu-id="0b4f1-141"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b4f1-141"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0b4f1-142">IID</span><span class="sxs-lookup"><span data-stu-id="0b4f1-142">IID</span></span><br/>     | <span data-ttu-id="0b4f1-143">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0b4f1-143">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="0b4f1-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b4f1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b4f1-145">Erstellen einer vollständig überprüften signierten Installation mithilfe von Automation</span><span class="sxs-lookup"><span data-stu-id="0b4f1-145">Authoring a Fully Verified Signed Installation Using Automation</span></span>](authoring-a-fully-verified-signed-installation-using-automation.md)
</dt> <dt>

[<span data-ttu-id="0b4f1-146">Digitale Signaturen und Windows Installer</span><span class="sxs-lookup"><span data-stu-id="0b4f1-146">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> <dt>

[<span data-ttu-id="0b4f1-147">**Msigetfilesignatureinformation**</span><span class="sxs-lookup"><span data-stu-id="0b4f1-147">**MsiGetFileSignatureInformation**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> </dl>

 

 
