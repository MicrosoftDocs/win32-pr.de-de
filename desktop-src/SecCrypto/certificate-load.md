---
description: Importiert ein Zertifikat aus einer Datei.
ms.assetid: 62c3bf8e-2f52-4342-b3ee-744b032578bf
title: 'ICertificate2:: Load-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Load
- ICertificate2.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9193297ad7eacc1994e4bf3729a87054573b1574
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367436"
---
# <a name="icertificate2load-method"></a><span data-ttu-id="090f9-103">ICertificate2:: Load-Methode</span><span class="sxs-lookup"><span data-stu-id="090f9-103">ICertificate2::Load method</span></span>

<span data-ttu-id="090f9-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="090f9-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="090f9-105">Verwenden Sie stattdessen die [**X509Certificate2-Klasse**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="090f9-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="090f9-106">Die **Load** -Methode importiert ein Zertifikat aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="090f9-106">The **Load** method imports a certificate from a file.</span></span> <span data-ttu-id="090f9-107">Diese Methode wurde in CAPICOM 2,0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="090f9-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="090f9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="090f9-108">Syntax</span></span>


```VB
Certificate.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ], _
  [ ByVal KeyLocation ] _
)
```



## <a name="parameters"></a><span data-ttu-id="090f9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="090f9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="090f9-110">*Dateiname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="090f9-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="090f9-111">Eine Zeichenfolge, die den Pfad zu einer CER-oder PFX-Datei enthält, die die Zertifikatsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="090f9-111">A string that contains the path to a .cer or .pfx file that contains the certificate data.</span></span>

</dd> <dt>

<span data-ttu-id="090f9-112">*Kennwort* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="090f9-112">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="090f9-113">Eine Zeichenfolge, die das [*Klartext*](../secgloss/p-gly.md) -Kennwort für die Datei mit dem [*privaten Schlüssel*](../secgloss/p-gly.md) enthält.</span><span class="sxs-lookup"><span data-stu-id="090f9-113">A string that contains the [*plaintext*](../secgloss/p-gly.md) password to the [*private key*](../secgloss/p-gly.md) file.</span></span> <span data-ttu-id="090f9-114">Das Kennwort kann bis zu 32 Unicode-Zeichen enthalten, einschließlich eines abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="090f9-114">The password can contain up to 32 Unicode characters, including a terminating null character.</span></span> <span data-ttu-id="090f9-115">Informationen zum Schützen des Kennworts finden Sie unter Behandeln von Kenn [Wörtern](../secbp/handling-passwords.md).</span><span class="sxs-lookup"><span data-stu-id="090f9-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="090f9-116">*Keystorageflag* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="090f9-116">*KeyStorageFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="090f9-117">Ein Wert der [**CAPICOM- \_ \_ Schlüsselspeicherflag \_**](capicom-key-storage-flag.md) -Enumeration, die Schlüsselspeicherflags definiert.</span><span class="sxs-lookup"><span data-stu-id="090f9-117">A value of the [**CAPICOM\_KEY\_STORAGE\_FLAG**](capicom-key-storage-flag.md) enumeration that defines key storage flags.</span></span> <span data-ttu-id="090f9-118">Der Standardwert ist der Standardwert von CAPICOM \_ Key \_ Storage \_ .</span><span class="sxs-lookup"><span data-stu-id="090f9-118">The default is CAPICOM\_KEY\_STORAGE\_DEFAULT.</span></span> <span data-ttu-id="090f9-119">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="090f9-119">The following table shows the possible values.</span></span>



| <span data-ttu-id="090f9-120">Wert</span><span class="sxs-lookup"><span data-stu-id="090f9-120">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="090f9-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="090f9-121">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <span data-ttu-id="090f9-122"><dt>**Standardwert für CAPICOM- \_ Schlüssel \_ Speicher \_**</dt></span><span class="sxs-lookup"><span data-stu-id="090f9-122"><dt>**CAPICOM\_KEY\_STORAGE\_DEFAULT**</dt></span></span> </dl>                       | <span data-ttu-id="090f9-123">Standardschlüssel Speicher.</span><span class="sxs-lookup"><span data-stu-id="090f9-123">Default key storage.</span></span><br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <span data-ttu-id="090f9-124"><dt>**zu \_ \_ \_ exportier barer CAPICOM-Schlüsselspeicher**</dt></span><span class="sxs-lookup"><span data-stu-id="090f9-124"><dt>**CAPICOM\_KEY\_STORAGE\_EXPORTABLE**</dt></span></span> </dl>              | <span data-ttu-id="090f9-125">Der Schlüssel ist exportierbar.</span><span class="sxs-lookup"><span data-stu-id="090f9-125">The key is exportable.</span></span><br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <span data-ttu-id="090f9-126"><dt>**Benutzer geschützter CAPICOM- \_ Schlüssel \_ Speicher \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="090f9-126"><dt>**CAPICOM\_KEY\_STORAGE\_USER\_PROTECTED**</dt></span></span> </dl> | <span data-ttu-id="090f9-127">Der Schlüssel ist Benutzer geschützt.</span><span class="sxs-lookup"><span data-stu-id="090f9-127">The key is user protected.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="090f9-128">*Keylocation* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="090f9-128">*KeyLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="090f9-129">Ein Wert der [**CAPICOM- \_ \_ schlüssellocation**](capicom-key-location.md) -Enumeration, die Schlüssel Speicherort Typen definiert.</span><span class="sxs-lookup"><span data-stu-id="090f9-129">A value of the [**CAPICOM\_KEY\_LOCATION**](capicom-key-location.md) enumeration that defines key location types.</span></span> <span data-ttu-id="090f9-130">Der Standardwert ist der aktuelle CAPICOM- \_ \_ Benutzer \_ Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="090f9-130">The default value is CAPICOM\_CURRENT\_USER\_KEY.</span></span> <span data-ttu-id="090f9-131">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="090f9-131">The following table shows the possible values.</span></span>



| <span data-ttu-id="090f9-132">Wert</span><span class="sxs-lookup"><span data-stu-id="090f9-132">Value</span></span>                                                                                                                                                                                               | <span data-ttu-id="090f9-133">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="090f9-133">Meaning</span></span>                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="CAPICOM_CURRENT_USER_KEY"></span><span id="capicom_current_user_key"></span><dl> <span data-ttu-id="090f9-134"><dt>**Schlüssel für aktuellen CAPICOM- \_ \_ Benutzer \_**</dt></span><span class="sxs-lookup"><span data-stu-id="090f9-134"><dt>**CAPICOM\_CURRENT\_USER\_KEY**</dt></span></span> </dl>    | <span data-ttu-id="090f9-135">Der Schlüssel ist ein Benutzerschlüssel.</span><span class="sxs-lookup"><span data-stu-id="090f9-135">The key is a user key.</span></span><br/>    |
| <span id="CAPICOM_LOCAL_MACHINE_KEY"></span><span id="capicom_local_machine_key"></span><dl> <span data-ttu-id="090f9-136"><dt>**lokaler CAPICOM- \_ \_ Computer \_ Schlüssel**</dt></span><span class="sxs-lookup"><span data-stu-id="090f9-136"><dt>**CAPICOM\_LOCAL\_MACHINE\_KEY**</dt></span></span> </dl> | <span data-ttu-id="090f9-137">Der Schlüssel ist ein Computer Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="090f9-137">The key is a machine key.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="090f9-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="090f9-138">Return value</span></span>

<span data-ttu-id="090f9-139">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="090f9-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="090f9-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="090f9-140">Remarks</span></span>

<span data-ttu-id="090f9-141">Diese Methode löst CAPICOM \_ E \_ nicht \_ zulässig aus, wenn eine Skripterstellung aus einer webbasierten Anwendung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="090f9-141">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="090f9-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="090f9-142">Requirements</span></span>



| <span data-ttu-id="090f9-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="090f9-143">Requirement</span></span> | <span data-ttu-id="090f9-144">Wert</span><span class="sxs-lookup"><span data-stu-id="090f9-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="090f9-145">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="090f9-145">End of client support</span></span><br/> | <span data-ttu-id="090f9-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="090f9-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="090f9-147">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="090f9-147">End of server support</span></span><br/> | <span data-ttu-id="090f9-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="090f9-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="090f9-149">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="090f9-149">Redistributable</span></span><br/>       | <span data-ttu-id="090f9-150">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="090f9-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="090f9-151">DLL</span><span class="sxs-lookup"><span data-stu-id="090f9-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="090f9-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="090f9-152"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
