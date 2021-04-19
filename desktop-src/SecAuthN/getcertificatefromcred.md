---
description: Ruft das Zertifikat aus den Anmelde Informationen des Benutzers ab.
ms.assetid: 3C79D049-89DC-4AF5-8C0A-5B7EBBBD69D3
title: Getcertifipeefromkred-Funktion (lsaidprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificateFromCred
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: 1120e7859080657e2a04202e01a01464694a3450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345881"
---
# <a name="getcertificatefromcred-function"></a><span data-ttu-id="f625d-103">Getcertifipeefromkred-Funktion</span><span class="sxs-lookup"><span data-stu-id="f625d-103">GetCertificateFromCred function</span></span>

<span data-ttu-id="f625d-104">Ruft das Zertifikat aus den Anmelde Informationen des Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="f625d-104">Gets the certificate from the user credential.</span></span>

## <a name="syntax"></a><span data-ttu-id="f625d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f625d-105">Syntax</span></span>


```C++
NTSTATUS GetCertificateFromCred(
  _In_  PVOID  ProviderHandle,
  _In_  HANDLE ClientToken,
  _In_  PVOID  SuppliedCred,
  _In_  ULONG  SuppliedCredSize,
  _Out_ PVOID  *CertContext
);
```



## <a name="parameters"></a><span data-ttu-id="f625d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f625d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f625d-107">*ProviderHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f625d-107">*ProviderHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f625d-108">Handle des Identitäts Anbieters.</span><span class="sxs-lookup"><span data-stu-id="f625d-108">Identity provider handle.</span></span>

</dd> <dt>

<span data-ttu-id="f625d-109">*Clienttoken* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f625d-109">*ClientToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f625d-110">Das Token des Aufrufers, der das Zertifikat abruft.</span><span class="sxs-lookup"><span data-stu-id="f625d-110">Token of the caller who is retrieving the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="f625d-111">*Supplied-* \[ ID in\]</span><span class="sxs-lookup"><span data-stu-id="f625d-111">*SuppliedCred* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f625d-112">Ein Zeiger auf eine durch [**secpkg \_ angegebene \_**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) Anmelde Informationsstruktur, die die Anmelde Informationen einer Online-ID enthält, deren Zertifikat angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="f625d-112">A pointer to a [**SECPKG\_SUPPLIED\_CREDENTIAL**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) structure that contains the credential of an online ID whose certificate is requested.</span></span> <span data-ttu-id="f625d-113">Der Identitäts Anbieter muss die Eingabedaten So validieren, als ob Sie aus einer nicht vertrauenswürdigen Quelle stammen.</span><span class="sxs-lookup"><span data-stu-id="f625d-113">The identity provider must validate the input data as if it is coming from an untrusted source.</span></span>

</dd> <dt>

<span data-ttu-id="f625d-114">*Suppliedkredsize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f625d-114">*SuppliedCredSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f625d-115">Die Größe des *suppliedup-* Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="f625d-115">The size, in bytes, of the *SuppliedCred* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f625d-116">*Certcontext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f625d-116">*CertContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f625d-117">Wenn die Funktion erfolgreich ausgeführt wird, ist dieser Parameter ein Zeiger auf den zurückgegebenen ccert- \_ Kontext Zeiger.</span><span class="sxs-lookup"><span data-stu-id="f625d-117">If the function succeeds, this parameter is a pointer to the returned CCERT\_CONTEXT pointer.</span></span> <span data-ttu-id="f625d-118">Wenn Sie die Verwendung des Zertifikat Kontexts abgeschlossen haben, geben Sie ihn durch Aufrufen der [**certfreecertifipriecontext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) -Funktion frei.</span><span class="sxs-lookup"><span data-stu-id="f625d-118">When you have finished using the certificate context, release it by calling the [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f625d-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f625d-119">Return value</span></span>

<span data-ttu-id="f625d-120">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion Status \_ Erfolg zurück.</span><span class="sxs-lookup"><span data-stu-id="f625d-120">If the function succeeds, the function returns STATUS\_SUCCESS.</span></span>

<span data-ttu-id="f625d-121">Wenn die Funktion fehlschlägt, gibt die Funktion möglicherweise einen der folgenden NTSTATUS-Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="f625d-121">If the function fails, the function may return one of the following NTSTATUS error codes.</span></span>



| <span data-ttu-id="f625d-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f625d-122">Return value</span></span>                                                                                            | <span data-ttu-id="f625d-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f625d-123">Description</span></span>                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f625d-124"><dt>Status \_ \_ wird nicht unterstützt</dt></span><span class="sxs-lookup"><span data-stu-id="f625d-124"><dt>STATUS\_NOT\_SUPPORTED</dt></span></span> </dl>       | <span data-ttu-id="f625d-125">Der Identitäts Anbieter erkennt den Anmelde Informationstyp der angegebenen Anmelde Informationen nicht.</span><span class="sxs-lookup"><span data-stu-id="f625d-125">The identity provider does not recognize the credential type of the supplied credential.</span></span> <span data-ttu-id="f625d-126">Der nächste Identitäts Anbieter wird von LSA ausprobiert.</span><span class="sxs-lookup"><span data-stu-id="f625d-126">LSA will try the next identity provider.</span></span><br/>                                           |
| <dl> <span data-ttu-id="f625d-127"><dt>Fehler bei der Status \_ Anmeldung \_</dt></span><span class="sxs-lookup"><span data-stu-id="f625d-127"><dt>STATUS\_LOGON\_FAILURE</dt></span></span> </dl>       | <span data-ttu-id="f625d-128">Die Anmelde Informationen sind falsch.</span><span class="sxs-lookup"><span data-stu-id="f625d-128">The credential is incorrect.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="f625d-129"><dt>\_ungültiger \_ Parameter.</dt></span><span class="sxs-lookup"><span data-stu-id="f625d-129"><dt>STATUS\_INVALID\_PARAMETER</dt></span></span> </dl>   | <span data-ttu-id="f625d-130">Ein Parameter ist nicht gültig.</span><span class="sxs-lookup"><span data-stu-id="f625d-130">A parameter is not valid.</span></span> <span data-ttu-id="f625d-131">Die Anmelde Informationen haben möglicherweise ein falsches Format und nicht die definierte [**secpkg- \_ \_**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) Anmelde Informationsstruktur.</span><span class="sxs-lookup"><span data-stu-id="f625d-131">The credential may be in an incorrect format and not in the defined [**SECPKG\_SUPPLIED\_CREDENTIAL**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) structure.</span></span><br/> |
| <dl> <span data-ttu-id="f625d-132"><dt>Status \_ Netzwerk \_ nicht erreichbar</dt></span><span class="sxs-lookup"><span data-stu-id="f625d-132"><dt>STATUS\_NETWORK\_UNREACHABLE</dt></span></span> </dl> | <span data-ttu-id="f625d-133">Der Identitäts Anbieter kann keine Verbindung mit der Cloud hergestellt werden, um das Zertifikat zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f625d-133">The identity provider cannot contact the cloud to obtain the certificate.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="f625d-134"><dt>Status \_ Kennwort \_ abgelaufen</dt></span><span class="sxs-lookup"><span data-stu-id="f625d-134"><dt>STATUS\_PASSWORD\_EXPIRED</dt></span></span> </dl>    | <span data-ttu-id="f625d-135">Das Konto Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="f625d-135">The account password has expired.</span></span><br/>                                                                                                                                           |
| <dl> <span data-ttu-id="f625d-136"><dt>Status \_ Konto \_ gesperrt \_</dt></span><span class="sxs-lookup"><span data-stu-id="f625d-136"><dt>STATUS\_ACCOUNT\_LOCKED\_OUT</dt></span></span> </dl> | <span data-ttu-id="f625d-137">Das Konto wurde gesperrt.</span><span class="sxs-lookup"><span data-stu-id="f625d-137">The account has been locked out.</span></span> <br/>                                                                                                                                           |
| <dl> <span data-ttu-id="f625d-138"><dt>Andere</dt></span><span class="sxs-lookup"><span data-stu-id="f625d-138"><dt>Others</dt></span></span> </dl>                       | <span data-ttu-id="f625d-139">Andere Anbieterspezifische Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="f625d-139">Other provider-specific error codes.</span></span> <br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="f625d-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f625d-140">Remarks</span></span>

<span data-ttu-id="f625d-141">Bevor Sie das Zertifikat aus der Cloud abrufen, sollte der Identitäts Anbieter überprüfen, ob für diesen Benutzer ein gültiges Zertifikat im Zertifikat Speicher des Benutzers vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f625d-141">Before fetching the certificate from the cloud, the identity provider should check that there is a valid certificate for this user in the user's "MY" certificate store.</span></span> <span data-ttu-id="f625d-142">Wenn ein gültiges Zertifikat vorhanden ist, sollte der Anbieter dieses Zertifikat zurückgeben, um unnötigen Netzwerkverkehr zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="f625d-142">If a valid certificate exists, the provider should return this certificate to avoid unnecessary network traffic.</span></span>

<span data-ttu-id="f625d-143">Der Identitäts Anbieter kann das Zertifikat auch lokal zwischenspeichern, solange es vor dem aktuellen Benutzer geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="f625d-143">The identity provider can also cache the certificate locally as long as it is protected from the current user.</span></span>

## <a name="requirements"></a><span data-ttu-id="f625d-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f625d-144">Requirements</span></span>



| <span data-ttu-id="f625d-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f625d-145">Requirement</span></span> | <span data-ttu-id="f625d-146">Wert</span><span class="sxs-lookup"><span data-stu-id="f625d-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f625d-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f625d-147">Minimum supported client</span></span><br/> | <span data-ttu-id="f625d-148">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f625d-148">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f625d-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f625d-149">Minimum supported server</span></span><br/> | <span data-ttu-id="f625d-150">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f625d-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f625d-151">Header</span><span class="sxs-lookup"><span data-stu-id="f625d-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="f625d-152"><dt>Lsaidprov. h</dt></span><span class="sxs-lookup"><span data-stu-id="f625d-152"><dt>Lsaidprov.h</dt></span></span> </dl> |



 

