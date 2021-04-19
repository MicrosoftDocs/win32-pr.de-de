---
description: Importiert Zertifikate aus einer Datei in den Speicher.
ms.assetid: 884326b4-77ca-43d4-bda9-127d823ce9bc
title: Store. Load-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 32261a6fd8c5cf4382832d8286d63ce5d44fb542
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355053"
---
# <a name="storeload-method"></a><span data-ttu-id="90e4b-103">Store. Load-Methode</span><span class="sxs-lookup"><span data-stu-id="90e4b-103">Store.Load method</span></span>

<span data-ttu-id="90e4b-104">\[Die **Load** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="90e4b-104">\[The **Load** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="90e4b-105">Verwenden Sie stattdessen die [**X509Store-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="90e4b-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="90e4b-106">Die **Load** -Methode importiert Zertifikate aus einer Datei in den Speicher.</span><span class="sxs-lookup"><span data-stu-id="90e4b-106">The **Load** method imports certificates from a file into the store.</span></span>

## <a name="syntax"></a><span data-ttu-id="90e4b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="90e4b-107">Syntax</span></span>


```VB
Store.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ] _
)
```



## <a name="parameters"></a><span data-ttu-id="90e4b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="90e4b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90e4b-109">*Dateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90e4b-109">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90e4b-110">Die Zeichenfolge, die den Pfad zu einer CER-, SST-,. SPC-,. p7s-oder PFX-Datei oder einer beliebigen mit Authenticode signierten Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="90e4b-110">The string that contains the path to a .cer, .sst, .spc, .p7s, or .pfx file, or any Authenticode signed file.</span></span>

</dd> <dt>

<span data-ttu-id="90e4b-111">*Kennwort* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="90e4b-111">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="90e4b-112">Die Zeichenfolge, die das Klartext-Kennwort für die Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="90e4b-112">The string that contains the plaintext password to the file.</span></span> <span data-ttu-id="90e4b-113">Bis zu 32 Unicode-Zeichen, einschließlich eines abschließenden NULL-Zeichens, können für das Kennwort verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="90e4b-113">Up to 32 Unicode characters, including a terminating null character, can be used for the password.</span></span> <span data-ttu-id="90e4b-114">Informationen zum Schützen des Kennworts finden Sie unter Behandeln von Kenn [Wörtern](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="90e4b-114">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="90e4b-115">*Keystorageflag* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="90e4b-115">*KeyStorageFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="90e4b-116">Ein Wert der [**CAPICOM- \_ \_ Schlüsselspeicherflag \_**](capicom-key-storage-flag.md) -Enumeration, die Schlüsselspeicherflags definiert.</span><span class="sxs-lookup"><span data-stu-id="90e4b-116">A value of the [**CAPICOM\_KEY\_STORAGE\_FLAG**](capicom-key-storage-flag.md) enumeration that defines key storage flags.</span></span> <span data-ttu-id="90e4b-117">Der Standardwert ist der Standardwert von CAPICOM \_ Key \_ Storage \_ .</span><span class="sxs-lookup"><span data-stu-id="90e4b-117">The default is CAPICOM\_KEY\_STORAGE\_DEFAULT.</span></span> <span data-ttu-id="90e4b-118">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="90e4b-118">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="90e4b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="90e4b-119">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="90e4b-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="90e4b-120">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <span data-ttu-id="90e4b-121"><dt>**Standardwert für CAPICOM- \_ Schlüssel \_ Speicher \_**</dt></span><span class="sxs-lookup"><span data-stu-id="90e4b-121"><dt>**CAPICOM\_KEY\_STORAGE\_DEFAULT**</dt></span></span> </dl>                       | <span data-ttu-id="90e4b-122">Standardschlüssel Speicher.</span><span class="sxs-lookup"><span data-stu-id="90e4b-122">Default key storage.</span></span><br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <span data-ttu-id="90e4b-123"><dt>**zu \_ \_ \_ exportier barer CAPICOM-Schlüsselspeicher**</dt></span><span class="sxs-lookup"><span data-stu-id="90e4b-123"><dt>**CAPICOM\_KEY\_STORAGE\_EXPORTABLE**</dt></span></span> </dl>              | <span data-ttu-id="90e4b-124">Der Schlüssel ist exportierbar.</span><span class="sxs-lookup"><span data-stu-id="90e4b-124">The key is exportable.</span></span><br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <span data-ttu-id="90e4b-125"><dt>**Benutzer geschützter CAPICOM- \_ Schlüssel \_ Speicher \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="90e4b-125"><dt>**CAPICOM\_KEY\_STORAGE\_USER\_PROTECTED**</dt></span></span> </dl> | <span data-ttu-id="90e4b-126">Der Schlüssel ist Benutzer geschützt.</span><span class="sxs-lookup"><span data-stu-id="90e4b-126">The key is user protected.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90e4b-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90e4b-127">Return value</span></span>

<span data-ttu-id="90e4b-128">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="90e4b-128">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="90e4b-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90e4b-129">Remarks</span></span>

<span data-ttu-id="90e4b-130">Wenn die **Load** -Methode für einen Speicher Speicher aufgerufen wird, werden alle erstellten Schlüssel Container gelöscht, wenn der Speicher Speicher gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="90e4b-130">If the **Load** method is called on a memory store, any key containers that are created will be deleted when the memory store is deleted.</span></span> <span data-ttu-id="90e4b-131">Wenn z. b. eine PFX-Datei in einen Speicher Speicher geladen und später einem Systemspeicher (z. b. dem eigenen Speicher) aus dem Speicher Speicher hinzugefügt wird, enthält das Zertifikat im My Store keinen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="90e4b-131">For example, if a .pfx file is loaded into a memory store and later added to a system store (such as the My store) from the memory store, the certificate in the My store will not contain a key.</span></span> <span data-ttu-id="90e4b-132">In diesem Fall muss die PFX-Datei direkt in den My-Speicher geladen werden.</span><span class="sxs-lookup"><span data-stu-id="90e4b-132">In this case, the .pfx file should be loaded directly into the My store.</span></span>

<span data-ttu-id="90e4b-133">Diese Methode löst CAPICOM \_ E \_ nicht \_ zulässig aus, wenn eine Skripterstellung aus einer webbasierten Anwendung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="90e4b-133">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

<span data-ttu-id="90e4b-134">Wenn das Kennwort die Datei mit dem privaten Schlüssel nicht entschlüsseln kann, sollte der Standard- [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP) abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="90e4b-134">If the password fails to decrypt the private key file, then the default [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) should be queried.</span></span> <span data-ttu-id="90e4b-135">Wenn der Standard-CSP der Kryptografieanbieter von Microsoft ist und der Entschlüsselungsvorgang fehlschlägt, sollte der Entschlüsselungsvorgang erneut mit dem Microsoft-starken Kryptografieanbieter oder Microsoft Enhanced Cryptographic Provider ausgeführt werden, je nachdem, welcher Wert verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="90e4b-135">If the default CSP is the Microsoft Base Cryptographic Provider and the decrypt operation fails, then the decrypt operation should be tried again with the Microsoft Strong Cryptographic Provider or Microsoft Enhanced Cryptographic Provider, whichever is available.</span></span>

<span data-ttu-id="90e4b-136">Wenn das Zertifikat, das in den Speicher geladen wird, dasselbe ist, das bereits vorhanden ist, löscht die **Load** -Methode das vorhandene Zertifikat aus dem Speicher und fügt dann das neue Zertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="90e4b-136">If the certificate being loaded into the store is the same as one that is already there, the **Load** method will delete the existing certificate from the store and then add the new certificate.</span></span> <span data-ttu-id="90e4b-137">Das neue Zertifikat erbt die Eigenschaften des vorhandenen Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="90e4b-137">The new certificate will inherit properties from the existing certificate.</span></span> <span data-ttu-id="90e4b-138">Der vorhandene Container für den privaten Schlüssel wird durch den neuen Container für private Schlüssel ersetzt.</span><span class="sxs-lookup"><span data-stu-id="90e4b-138">The existing private key container is replaced by the new private key container.</span></span>

## <a name="requirements"></a><span data-ttu-id="90e4b-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90e4b-139">Requirements</span></span>



| <span data-ttu-id="90e4b-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90e4b-140">Requirement</span></span> | <span data-ttu-id="90e4b-141">Wert</span><span class="sxs-lookup"><span data-stu-id="90e4b-141">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90e4b-142">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="90e4b-142">Redistributable</span></span><br/> | <span data-ttu-id="90e4b-143">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="90e4b-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="90e4b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="90e4b-144">DLL</span></span><br/>             | <dl> <span data-ttu-id="90e4b-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90e4b-145"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90e4b-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90e4b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90e4b-147">**Speicher**</span><span class="sxs-lookup"><span data-stu-id="90e4b-147">**Store**</span></span>](store.md)
</dt> </dl>

 

 
