---
description: Ruft ein Handle für bereits vorhandene Anmelde Informationen eines Sicherheits Prinzipals ab, der Kerberos verwendet.
ms.assetid: 2612bbe9-856b-4a81-bffb-6c761035883d
title: AcquireCredentialsHandle (Kerberos)-Funktion (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 05a4dd885712e89b812896684f73d60df610e41d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373230"
---
# <a name="acquirecredentialshandle-kerberos-function"></a><span data-ttu-id="64f1b-103">AcquireCredentialsHandle (Kerberos)-Funktion</span><span class="sxs-lookup"><span data-stu-id="64f1b-103">AcquireCredentialsHandle (Kerberos) function</span></span>

<span data-ttu-id="64f1b-104">Die Funktion **AcquireCredentialsHandle (Kerberos)** Ruft ein Handle für bereits vorhandene Anmelde Informationen eines [*Sicherheits Prinzipals*](../secgloss/s-gly.md)ab.</span><span class="sxs-lookup"><span data-stu-id="64f1b-104">The **AcquireCredentialsHandle (Kerberos)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="64f1b-105">Dieses Handle ist für die Funktionen [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) und [**akzeptsecuritycontext (Kerberos)**](acceptsecuritycontext--kerberos.md) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="64f1b-105">This handle is required by the [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) and [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) functions.</span></span> <span data-ttu-id="64f1b-106">Hierbei kann es sich um bereits vorhandene *Anmelde* Informationen handeln, die über eine System Anmeldung eingerichtet werden, die hier nicht beschrieben wird, oder der Aufrufer kann Alternative Anmelde Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="64f1b-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="64f1b-107">Dabei handelt es sich nicht um eine "beim Netzwerk anmelden", und es ist nicht beabsichtigt, Anmelde Informationen zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="64f1b-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="64f1b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="64f1b-108">Syntax</span></span>


```C++
SECURITY_STATUS SEC_Entry AcquireCredentialsHandle(
  _In_  SEC_CHAR       *pszPrincipal,
  _In_  SEC_CHAR       *pszPackage,
  _In_  ULONG          fCredentialUse,
  _In_  PLUID          pvLogonID,
  _In_  PVOID          pAuthData,
  _In_  SEC_GET_KEY_FN pGetKeyFn,
  _In_  PVOID          pvGetKeyArgument,
  _Out_ PCredHandle    phCredential,
  _Out_ PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a><span data-ttu-id="64f1b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="64f1b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64f1b-110">*pszprincipal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64f1b-110">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64f1b-111">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Prinzipals angibt, auf dessen Anmelde Informationen das Handle verweist.</span><span class="sxs-lookup"><span data-stu-id="64f1b-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

> [!Note]  
> <span data-ttu-id="64f1b-112">Wenn der Prozess, der das Handle anfordert, keinen Zugriff auf die Anmelde Informationen hat, gibt die Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="64f1b-112">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="64f1b-113">Eine NULL-Zeichenfolge gibt an, dass der Prozess ein Handle für die Anmelde Informationen des Benutzers erfordert, in dessen [*Sicherheitskontext*](../secgloss/s-gly.md) er ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="64f1b-113">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="64f1b-114">*pszpackage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64f1b-114">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64f1b-115">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des [*Sicherheitspakets*](../secgloss/s-gly.md) angibt, mit dem diese Anmelde Informationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64f1b-115">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="64f1b-116">Dies ist ein [*Sicherheitspaket*](../secgloss/s-gly.md) Name, der im **Name** -Member einer [**secpkginfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) -Struktur zurückgegeben wird, die von der [**enumeratesecuritypackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="64f1b-116">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="64f1b-117">Nachdem ein Kontext eingerichtet wurde, kann [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) aufgerufen werden, wobei *ulattribute* auf secpkg \_ attr Package Info festgelegt ist, \_ \_ um Informationen zum verwendeten [*Sicherheitspaket*](../secgloss/s-gly.md) zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="64f1b-117">After a context is established, [**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

</dd> <dt>

<span data-ttu-id="64f1b-118">*"f"* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64f1b-118">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64f1b-119">Ein Flag, das angibt, wie diese Anmelde Informationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64f1b-119">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="64f1b-120">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="64f1b-120">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="64f1b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="64f1b-121">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="64f1b-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="64f1b-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_BOTH"></span><span id="secpkg_cred_both"></span><dl> <span data-ttu-id="64f1b-123"><dt>**"secpkg" \_ -Funktion \_**</dt></span><span class="sxs-lookup"><span data-stu-id="64f1b-123"><dt>**SECPKG\_CRED\_BOTH**</dt></span></span> </dl>             | <span data-ttu-id="64f1b-124">Überprüfen Sie eingehende Anmelde Informationen, oder verwenden Sie lokale Anmelde Informationen, um ein Ausgeh Endes Token vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="64f1b-124">Validate an incoming credential or use a local credential to prepare an outgoing token.</span></span> <span data-ttu-id="64f1b-125">Dieses Flag aktiviert beide anderen Flags.</span><span class="sxs-lookup"><span data-stu-id="64f1b-125">This flag enables both other flags.</span></span><br/>                                                                                                                                                                                                                                                                                                                              |
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="64f1b-126"><dt>**secpkg-in \_ \_ eingehender Richtung**</dt></span><span class="sxs-lookup"><span data-stu-id="64f1b-126"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>    | <span data-ttu-id="64f1b-127">Überprüfen Sie die Anmelde Informationen eines eingehenden Servers.</span><span class="sxs-lookup"><span data-stu-id="64f1b-127">Validate an incoming server credential.</span></span> <span data-ttu-id="64f1b-128">Eingehende Anmelde Informationen können mithilfe einer authentifizier enden Zertifizierungsstelle überprüft werden, wenn [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) oder [**Accept-SecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="64f1b-128">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) or [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) is called.</span></span> <span data-ttu-id="64f1b-129">Wenn eine solche Autorität nicht verfügbar ist, schlägt die Funktion fehl und gibt SEK \_ \_ . E keine \_ authentifizier Ende Zertifizierungs \_ Stelle zurück.</span><span class="sxs-lookup"><span data-stu-id="64f1b-129">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="64f1b-130">Die Validierung ist Paket spezifisch.</span><span class="sxs-lookup"><span data-stu-id="64f1b-130">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="64f1b-131"><dt>**Outbound für secpkg-Datenverkehr \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="64f1b-131"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl> | <span data-ttu-id="64f1b-132">Ermöglicht die Vorbereitung eines ausgehenden Tokens durch lokale Client Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="64f1b-132">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="64f1b-133">*pvlogonid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64f1b-133">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64f1b-134">Ein Zeiger auf einen [*lokal eindeutigen Bezeichner*](../secgloss/l-gly.md) (LUID), der den Benutzer identifiziert.</span><span class="sxs-lookup"><span data-stu-id="64f1b-134">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="64f1b-135">Dieser Parameter wird für Dateisystem Prozesse, z. b. netzwerkredirectors, bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="64f1b-135">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="64f1b-136">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="64f1b-136">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="64f1b-137">*pauthdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64f1b-137">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64f1b-138">Ein Zeiger auf Paket spezifische Daten.</span><span class="sxs-lookup"><span data-stu-id="64f1b-138">A pointer to package-specific data.</span></span> <span data-ttu-id="64f1b-139">Dieser Parameter kann **null** sein, was darauf hinweist, dass die Standard Anmelde Informationen für das [*Sicherheitspaket*](../secgloss/s-gly.md) verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="64f1b-139">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="64f1b-140">Um die angegebenen Anmelde Informationen zu verwenden, übergeben Sie eine [**sec- \_ Winnt-Authentifizierungs \_ \_ Identitäts**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) Struktur, die diese Anmelde Informationen enthält, in diesem Parameter.</span><span class="sxs-lookup"><span data-stu-id="64f1b-140">To use supplied credentials, pass a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that includes those credentials in this parameter.</span></span> <span data-ttu-id="64f1b-141">Die RPC-Laufzeit übergibt alle in [**rpcbindingsetauthinfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo)bereitgestellten.</span><span class="sxs-lookup"><span data-stu-id="64f1b-141">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

</dd> <dt>

<span data-ttu-id="64f1b-142">*pgetkeyfn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64f1b-142">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64f1b-143">Dieser Parameter wird nicht verwendet und sollte auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64f1b-143">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="64f1b-144">*pvgetkeyargument* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64f1b-144">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64f1b-145">Dieser Parameter wird nicht verwendet und sollte auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="64f1b-145">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="64f1b-146">*phcredential* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="64f1b-146">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64f1b-147">Ein Zeiger auf eine " [kredhandle](sspi-handles.md) "-Struktur, die das Handle für die Anmelde Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="64f1b-147">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="64f1b-148">*ptsexpiry* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="64f1b-148">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64f1b-149">Ein Zeiger auf eine [**Zeitstempel**](timestamp.md) Struktur, die die Uhrzeit empfängt, zu der die zurückgegebenen Anmelde Informationen ablaufen.</span><span class="sxs-lookup"><span data-stu-id="64f1b-149">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="64f1b-150">Der in dieser **Zeitstempel** Struktur zurückgegebene Wert hängt von der [*eingeschränkten Delegierung*](../secgloss/s-gly.md)ab.</span><span class="sxs-lookup"><span data-stu-id="64f1b-150">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="64f1b-151">Das [*Sicherheitspaket*](../secgloss/s-gly.md) muss diesen Wert in der Ortszeit zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="64f1b-151">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64f1b-152">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64f1b-152">Return value</span></span>

<span data-ttu-id="64f1b-153">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion sec \_ E \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="64f1b-153">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="64f1b-154">Wenn die Funktion fehlschlägt, wird einer der folgenden Fehlercodes zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="64f1b-154">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="64f1b-155">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="64f1b-155">Return code</span></span>                                                                                                 | <span data-ttu-id="64f1b-156">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64f1b-156">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="64f1b-157"><dt>**SEK \_ b \_ nicht genügend Arbeits \_ Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="64f1b-157"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="64f1b-158">Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="64f1b-158">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="64f1b-159"><dt>**Sek. \_ E ( \_ interner \_ Fehler)**</dt></span><span class="sxs-lookup"><span data-stu-id="64f1b-159"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="64f1b-160">Es ist ein Fehler aufgetreten, der keinem SSPI-Fehlercode zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="64f1b-160">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="64f1b-161"><dt>**s \_ E \_ keine \_ Anmelde Informationen**</dt></span><span class="sxs-lookup"><span data-stu-id="64f1b-161"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="64f1b-162">In der [*eingeschränkten Delegierung*](../secgloss/s-gly.md)sind keine Anmelde Informationen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="64f1b-162">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="64f1b-163"><dt>**Sek. \_ E \_ nicht \_ Besitzer**</dt></span><span class="sxs-lookup"><span data-stu-id="64f1b-163"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="64f1b-164">Der Aufrufer der Funktion verfügt nicht über die erforderlichen Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="64f1b-164">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="64f1b-165"><dt>**Sek. \_ E \_ secpkg \_ nicht \_ gefunden**</dt></span><span class="sxs-lookup"><span data-stu-id="64f1b-165"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="64f1b-166">Das angeforderte [*Sicherheitspaket*](../secgloss/s-gly.md) ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="64f1b-166">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="64f1b-167"><dt>**SEK \_ . \_ unbekannte \_ Anmelde Informationen**</dt></span><span class="sxs-lookup"><span data-stu-id="64f1b-167"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="64f1b-168">Die für das Paket angegebenen Anmelde Informationen wurden nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="64f1b-168">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="64f1b-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64f1b-169">Remarks</span></span>

<span data-ttu-id="64f1b-170">Die Funktion **AcquireCredentialsHandle (Kerberos)** gibt ein Handle für die Anmelde Informationen eines Prinzipals (z. b. einen Benutzer oder Client) zurück, der von einer bestimmten [*eingeschränkten Delegierung*](../secgloss/s-gly.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="64f1b-170">The **AcquireCredentialsHandle (Kerberos)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="64f1b-171">Dies kann das Handle für bereits vorhandene Anmelde Informationen sein, oder die Funktion kann einen neuen Satz von Anmelde Informationen erstellen und zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="64f1b-171">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="64f1b-172">Dieses Handle kann in nachfolgenden Aufrufen der Funktionen " [**Accept tsecuritycontext" (Kerberos)**](acceptsecuritycontext--kerberos.md) und " [**InitializeSecurityContext" (Kerberos)**](initializesecuritycontext--kerberos.md) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64f1b-172">This handle can be used in subsequent calls to the [**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md) and [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md) functions.</span></span>

<span data-ttu-id="64f1b-173">Im Allgemeinen gestattet **AcquireCredentialsHandle (Kerberos)** einem Prozess nicht das Abrufen eines Handles für die Anmelde Informationen anderer Benutzer, die am gleichen Computer angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="64f1b-173">In general, **AcquireCredentialsHandle (Kerberos)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="64f1b-174">Allerdings hat ein Aufrufer mit der Berechtigung "SE \_ TCB \_ Name" die Option, den [*Anmelde Bezeichner*](../secgloss/l-gly.md) (LUID) eines beliebigen vorhandenen Anmelde Sitzungs Tokens anzugeben, um ein Handle für die Anmelde Informationen dieser Sitzung zu erhalten. [](../secgloss/s-gly.md)</span><span class="sxs-lookup"><span data-stu-id="64f1b-174">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="64f1b-175">Diese wird in der Regel von Kernelmodusmodulen verwendet, die im Auftrag eines angemeldeten Benutzers agieren müssen.</span><span class="sxs-lookup"><span data-stu-id="64f1b-175">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="64f1b-176">Ein Paket kann die Funktion in *pgetkeyfn* aufrufen, die vom RPC-Lauf Zeit Transport bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="64f1b-176">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="64f1b-177">Wenn der Transport die Rückruffunktion zum Abrufen von Anmelde Informationen nicht unterstützt, muss dieser Parameter **null** sein.</span><span class="sxs-lookup"><span data-stu-id="64f1b-177">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="64f1b-178">Bei kernelmodusaufrufern müssen die folgenden Unterschiede beachtet werden:</span><span class="sxs-lookup"><span data-stu-id="64f1b-178">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="64f1b-179">Die beiden Zeichen folgen Parameter müssen [*Unicode*](../secgloss/u-gly.md) -Zeichen folgen sein.</span><span class="sxs-lookup"><span data-stu-id="64f1b-179">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="64f1b-180">Die Puffer Werte müssen im virtuellen Arbeitsspeicher des Prozesses zugeordnet werden, nicht aus dem Pool.</span><span class="sxs-lookup"><span data-stu-id="64f1b-180">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="64f1b-181">Wenn Sie die zurückgegebenen Anmelde Informationen nicht mehr verwenden, geben Sie den von den Anmelde Informationen genutzten Arbeitsspeicher frei, indem Sie die [**freecredentialshandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="64f1b-181">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="64f1b-182">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64f1b-182">Requirements</span></span>



| <span data-ttu-id="64f1b-183">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64f1b-183">Requirement</span></span> | <span data-ttu-id="64f1b-184">Wert</span><span class="sxs-lookup"><span data-stu-id="64f1b-184">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64f1b-185">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="64f1b-185">Minimum supported client</span></span><br/> | <span data-ttu-id="64f1b-186">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64f1b-186">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="64f1b-187">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="64f1b-187">Minimum supported server</span></span><br/> | <span data-ttu-id="64f1b-188">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="64f1b-188">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="64f1b-189">Header</span><span class="sxs-lookup"><span data-stu-id="64f1b-189">Header</span></span><br/>                   | <dl> <span data-ttu-id="64f1b-190"><dt>SSPI. h (Include Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="64f1b-190"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="64f1b-191">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="64f1b-191">Library</span></span><br/>                  | <dl> <span data-ttu-id="64f1b-192"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64f1b-192"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="64f1b-193">DLL</span><span class="sxs-lookup"><span data-stu-id="64f1b-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64f1b-194"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64f1b-194"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="64f1b-195">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="64f1b-195">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="64f1b-196">**Acquirecredentialshandlew** (Unicode) und **AcquireCredentialsHandleA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="64f1b-196">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="64f1b-197">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64f1b-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64f1b-198">SSPI-Funktionen</span><span class="sxs-lookup"><span data-stu-id="64f1b-198">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="64f1b-199">**Akzeptsecuritycontext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="64f1b-199">**AcceptSecurityContext (Kerberos)**</span></span>](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="64f1b-200">**InitializeSecurityContext (Kerberos)**</span><span class="sxs-lookup"><span data-stu-id="64f1b-200">**InitializeSecurityContext (Kerberos)**</span></span>](initializesecuritycontext--kerberos.md)
</dt> <dt>

[<span data-ttu-id="64f1b-201">**Freecredentialshandle**</span><span class="sxs-lookup"><span data-stu-id="64f1b-201">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
