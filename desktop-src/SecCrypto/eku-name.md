---
description: Legt einen Enumerationswert fest, der den CAPICOM-Namen der EKU angibt, oder ruft ihn ab. Dies ist die Standard Eigenschaft.
ms.assetid: afce5553-ef18-4a7f-b1c8-fbe00d3277e0
title: 'Ieku:: Name-Eigenschaft'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.Name
- IEKU.get_Name
- IEKU.put_Name
- EKU.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e0e28a8816d7e4c4f44e3cd1ec0dc479372d66d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373908"
---
# <a name="iekuname-property"></a><span data-ttu-id="b7622-104">Ieku:: Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b7622-104">IEKU::Name property</span></span>

<span data-ttu-id="b7622-105">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b7622-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b7622-106">Verwenden Sie stattdessen die [**X509EnhancedKeyUsageExtension-Klasse**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) im [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) -Namespace.\]</span><span class="sxs-lookup"><span data-stu-id="b7622-106">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="b7622-107">Die **Name** -Eigenschaft legt einen Enumerationswert fest, der den CAPICOM-Namen der EKU angibt, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="b7622-107">The **Name** property sets or retrieves an enumeration value that specifies the CAPICOM name of the EKU.</span></span> <span data-ttu-id="b7622-108">Dies ist die Standard Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b7622-108">This is the default property.</span></span>

<span data-ttu-id="b7622-109">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b7622-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7622-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7622-110">Syntax</span></span>


```VB
EKU.Name As CAPICOM_EKU
```



## <a name="property-value"></a><span data-ttu-id="b7622-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b7622-111">Property value</span></span>

<span data-ttu-id="b7622-112">Ein Wert der [**CAPICOM \_ EKU**](capicom-eku.md) -Enumeration, der den CAPICOM-Namen der EKU angibt.</span><span class="sxs-lookup"><span data-stu-id="b7622-112">A value of the [**CAPICOM\_EKU**](capicom-eku.md) enumeration that specifies the CAPICOM name of the EKU.</span></span> <span data-ttu-id="b7622-113">In der folgenden Tabelle sind die möglichen Werte aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7622-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="b7622-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b7622-114">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="b7622-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b7622-115">Meaning</span></span>                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_EKU_OTHER"></span><span id="capicom_eku_other"></span><dl> <span data-ttu-id="b7622-116"><dt>**Weitere CAPICOM- \_ EKU \_ other**</dt></span><span class="sxs-lookup"><span data-stu-id="b7622-116"><dt>**CAPICOM\_EKU\_OTHER**</dt></span></span> </dl>                                                      | <span data-ttu-id="b7622-117">Das Zertifikat verfügt über in der lokalen Richtlinie definierte Verwendung.</span><span class="sxs-lookup"><span data-stu-id="b7622-117">Certificate has uses defined in local policy.</span></span> <span data-ttu-id="b7622-118">Diese wird verwendet, wenn die erforderliche EKU nicht vordefiniert ist und der OID-Wert von der Anwendung festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="b7622-118">This is used if the EKU needed is not predefined and the OID value must be set by the application.</span></span><br/> |
| <span id="CAPICOM_EKU_SERVER_AUTH"></span><span id="capicom_eku_server_auth"></span><dl> <span data-ttu-id="b7622-119"><dt>**CAPICOM- \_ EKU- \_ Server Authentifizierung \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b7622-119"><dt>**CAPICOM\_EKU\_SERVER\_AUTH**</dt></span></span> </dl>                                   | <span data-ttu-id="b7622-120">Das Zertifikat kann zum Authentifizieren eines Servers verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7622-120">Certificate can be used to authenticate a server.</span></span><br/>                                                                                                |
| <span id="CAPICOM_EKU_CLIENT_AUTH"></span><span id="capicom_eku_client_auth"></span><dl> <span data-ttu-id="b7622-121"><dt>**CAPICOM- \_ EKU- \_ Client Authentifizierung \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b7622-121"><dt>**CAPICOM\_EKU\_CLIENT\_AUTH**</dt></span></span> </dl>                                   | <span data-ttu-id="b7622-122">Das Zertifikat kann zum Authentifizieren eines Clients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7622-122">Certificate can be used to authenticate a client.</span></span><br/>                                                                                                |
| <span id="CAPICOM_EKU_CODE_SIGNING"></span><span id="capicom_eku_code_signing"></span><dl> <span data-ttu-id="b7622-123"><dt>**CAPICOM- \_ EKU- \_ Code \_ Signatur**</dt></span><span class="sxs-lookup"><span data-stu-id="b7622-123"><dt>**CAPICOM\_EKU\_CODE\_SIGNING**</dt></span></span> </dl>                                | <span data-ttu-id="b7622-124">Das Zertifikat kann verwendet werden, um eine digitale Signatur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b7622-124">Certificate can be used to create a digital signature.</span></span><br/>                                                                                           |
| <span id="CAPICOM_EKU_EMAIL_PROTECTION"></span><span id="capicom_eku_email_protection"></span><dl> <span data-ttu-id="b7622-125"><dt>**CAPICOM \_ EKU \_ -e-Mail- \_ Schutz**</dt></span><span class="sxs-lookup"><span data-stu-id="b7622-125"><dt>**CAPICOM\_EKU\_EMAIL\_PROTECTION**</dt></span></span> </dl>                    | <span data-ttu-id="b7622-126">Zertifikat kann für den e-Mail-Schutz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7622-126">Certificate can be used for email protection.</span></span><br/>                                                                                                    |
| <span id="CAPICOM_EKU_SMARTCARD_LOGON"></span><span id="capicom_eku_smartcard_logon"></span><dl> <span data-ttu-id="b7622-127"><dt>**CAPICOM \_ EKU \_ Smartcard- \_ Anmeldung**</dt></span><span class="sxs-lookup"><span data-stu-id="b7622-127"><dt>**CAPICOM\_EKU\_SMARTCARD\_LOGON**</dt></span></span> </dl>                       | <span data-ttu-id="b7622-128">Das Zertifikat kann für die Smartcard-Anmeldung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7622-128">Certificate can be used for smart card logon.</span></span> <span data-ttu-id="b7622-129">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="b7622-129">Introduced in CAPICOM 2.0.</span></span><br/>                                                                         |
| <span id="CAPICOM_EKU_ENCRYPTING_FILE_SYSTEM"></span><span id="capicom_eku_encrypting_file_system"></span><dl> <span data-ttu-id="b7622-130"><dt>**CAPICOM- \_ EKU- \_ verschlüsselndes \_ Datei \_ System**</dt></span><span class="sxs-lookup"><span data-stu-id="b7622-130"><dt>**CAPICOM\_EKU\_ENCRYPTING\_FILE\_SYSTEM**</dt></span></span> </dl> | <span data-ttu-id="b7622-131">Das Zertifikat kann für EFS verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7622-131">Certificate can be used for EFS.</span></span> <span data-ttu-id="b7622-132">Eingeführt in CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="b7622-132">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="b7622-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7622-133">Remarks</span></span>

<span data-ttu-id="b7622-134">Wenn der Wert dieser Eigenschaft direkt oder indirekt zurückgesetzt wird, wird der gesamte [*Status*](../secgloss/s-gly.md) des Objekts zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="b7622-134">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7622-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7622-135">Requirements</span></span>



| <span data-ttu-id="b7622-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7622-136">Requirement</span></span> | <span data-ttu-id="b7622-137">Wert</span><span class="sxs-lookup"><span data-stu-id="b7622-137">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7622-138">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b7622-138">End of client support</span></span><br/> | <span data-ttu-id="b7622-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7622-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b7622-140">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="b7622-140">End of server support</span></span><br/> | <span data-ttu-id="b7622-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7622-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b7622-142">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="b7622-142">Redistributable</span></span><br/>       | <span data-ttu-id="b7622-143">CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP</span><span class="sxs-lookup"><span data-stu-id="b7622-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b7622-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b7622-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b7622-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7622-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
