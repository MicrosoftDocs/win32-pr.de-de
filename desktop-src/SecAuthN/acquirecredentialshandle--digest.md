---
description: Ruft ein Handle für bereits vorhandene Anmelde Informationen eines Sicherheits Prinzipals ab, der Digest verwendet.
ms.assetid: 79f49240-e394-4584-8db7-ef721672ba6b
title: AcquireCredentialsHandle (Digest)-Funktion (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 1474eef8ad5f5a30fe7d930431185a8ff70f7dfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217463"
---
# <a name="acquirecredentialshandle-digest-function"></a><span data-ttu-id="553cc-103">AcquireCredentialsHandle (Digest)-Funktion</span><span class="sxs-lookup"><span data-stu-id="553cc-103">AcquireCredentialsHandle (Digest) function</span></span>

<span data-ttu-id="553cc-104">Die **AcquireCredentialsHandle (Digest)** -Funktion Ruft ein Handle für bereits vorhandene Anmelde Informationen eines [*Sicherheits Prinzipals*](../secgloss/s-gly.md)ab.</span><span class="sxs-lookup"><span data-stu-id="553cc-104">The **AcquireCredentialsHandle (Digest)** function acquires a handle to preexisting credentials of a [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="553cc-105">Dieses Handle ist für die Funktionen " [**Accept tsecuritycontext (Digest)**](acceptsecuritycontext--digest.md) " und " [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) " erforderlich.</span><span class="sxs-lookup"><span data-stu-id="553cc-105">This handle is required by the [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) and [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) functions.</span></span> <span data-ttu-id="553cc-106">Hierbei kann es sich um bereits vorhandene *Anmelde* Informationen handeln, die über eine System Anmeldung eingerichtet werden, die hier nicht beschrieben wird, oder der Aufrufer kann Alternative Anmelde Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="553cc-106">These can be either preexisting *credentials*, which are established through a system logon that is not described here, or the caller can provide alternative credentials.</span></span>

> [!Note]  
> <span data-ttu-id="553cc-107">Dabei handelt es sich nicht um eine "beim Netzwerk anmelden", und es ist nicht beabsichtigt, Anmelde Informationen zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="553cc-107">This is not a "log on to the network" and does not imply gathering of credentials.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="553cc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="553cc-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="553cc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="553cc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="553cc-110">*pszprincipal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="553cc-110">*pszPrincipal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="553cc-111">Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Namen des Prinzipals angibt, auf dessen Anmelde Informationen das Handle verweist.</span><span class="sxs-lookup"><span data-stu-id="553cc-111">A pointer to a null-terminated string that specifies the name of the principal whose credentials the handle will reference.</span></span>

<span data-ttu-id="553cc-112">Wenn Sie den Digest-SSP verwenden, ist dieser Parameter optional.</span><span class="sxs-lookup"><span data-stu-id="553cc-112">When using the Digest SSP, this parameter is optional.</span></span>

> [!Note]  
> <span data-ttu-id="553cc-113">Wenn der Prozess, der das Handle anfordert, keinen Zugriff auf die Anmelde Informationen hat, gibt die Funktion einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="553cc-113">If the process that requests the handle does not have access to the credentials, the function returns an error.</span></span> <span data-ttu-id="553cc-114">Eine NULL-Zeichenfolge gibt an, dass der Prozess ein Handle für die Anmelde Informationen des Benutzers erfordert, in dessen [*Sicherheitskontext*](../secgloss/s-gly.md) er ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="553cc-114">A null string indicates that the process requires a handle to the credentials of the user under whose [*security context*](../secgloss/s-gly.md) it is executing.</span></span>

 

</dd> <dt>

<span data-ttu-id="553cc-115">*pszpackage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="553cc-115">*pszPackage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="553cc-116">Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Namen des [*Sicherheitspakets*](../secgloss/s-gly.md) angibt, mit dem diese Anmelde Informationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="553cc-116">A pointer to a null-terminated string that specifies the name of the [*security package*](../secgloss/s-gly.md) with which these credentials will be used.</span></span> <span data-ttu-id="553cc-117">Dies ist ein [*Sicherheitspaket*](../secgloss/s-gly.md) Name, der im **Name** -Member einer [**secpkginfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) -Struktur zurückgegeben wird, die von der [**enumeratesecuritypackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="553cc-117">This is a [*security package*](../secgloss/s-gly.md) name returned in the **Name** member of a [**SecPkgInfo**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) structure returned by the [**EnumerateSecurityPackages**](/windows/win32/api/sspi/ns-sspi-secpkginfoa) function.</span></span> <span data-ttu-id="553cc-118">Nachdem ein Kontext eingerichtet wurde, kann [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) aufgerufen werden, wobei *ulattribute* auf secpkg \_ attr Package Info festgelegt wird, \_ \_ um Informationen zum verwendeten [*Sicherheitspaket*](../secgloss/s-gly.md) zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="553cc-118">After a context is established, [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) can be called with *ulAttribute* set to SECPKG\_ATTR\_PACKAGE\_INFO to return information on the [*security package*](../secgloss/s-gly.md) in use.</span></span>

<span data-ttu-id="553cc-119">Wenn Sie den Digest-SSP verwenden, legen Sie diesen Parameter auf wdigest \_ SP \_ Name fest.</span><span class="sxs-lookup"><span data-stu-id="553cc-119">When using the Digest SSP, set this parameter to WDIGEST\_SP\_NAME.</span></span>

</dd> <dt>

<span data-ttu-id="553cc-120">*"f"* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="553cc-120">*fCredentialUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="553cc-121">Ein Flag, das angibt, wie diese Anmelde Informationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="553cc-121">A flag that indicates how these credentials will be used.</span></span> <span data-ttu-id="553cc-122">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="553cc-122">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="553cc-123">Wert</span><span class="sxs-lookup"><span data-stu-id="553cc-123">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="553cc-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="553cc-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SECPKG_CRED_INBOUND"></span><span id="secpkg_cred_inbound"></span><dl> <span data-ttu-id="553cc-125"><dt>**secpkg-in \_ \_ eingehender Richtung**</dt></span><span class="sxs-lookup"><span data-stu-id="553cc-125"><dt>**SECPKG\_CRED\_INBOUND**</dt></span></span> </dl>    | <span data-ttu-id="553cc-126">Überprüfen Sie die Anmelde Informationen eines eingehenden Servers.</span><span class="sxs-lookup"><span data-stu-id="553cc-126">Validate an incoming server credential.</span></span> <span data-ttu-id="553cc-127">Eingehende Anmelde Informationen können mithilfe einer authentifizier enden Zertifizierungsstelle überprüft werden, wenn [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) oder [**Accept tsecuritycontext (Digest)**](acceptsecuritycontext--digest.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="553cc-127">Inbound credentials might be validated by using an authenticating authority when [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) or [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) is called.</span></span> <span data-ttu-id="553cc-128">Wenn eine solche Autorität nicht verfügbar ist, schlägt die Funktion fehl und gibt SEK \_ \_ . E keine \_ authentifizier Ende Zertifizierungs \_ Stelle zurück.</span><span class="sxs-lookup"><span data-stu-id="553cc-128">If such an authority is not available, the function will fail and return SEC\_E\_NO\_AUTHENTICATING\_AUTHORITY.</span></span> <span data-ttu-id="553cc-129">Die Validierung ist Paket spezifisch.</span><span class="sxs-lookup"><span data-stu-id="553cc-129">Validation is package specific.</span></span><br/> |
| <span id="SECPKG_CRED_OUTBOUND"></span><span id="secpkg_cred_outbound"></span><dl> <span data-ttu-id="553cc-130"><dt>**Outbound für secpkg-Datenverkehr \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="553cc-130"><dt>**SECPKG\_CRED\_OUTBOUND**</dt></span></span> </dl> | <span data-ttu-id="553cc-131">Ermöglicht die Vorbereitung eines ausgehenden Tokens durch lokale Client Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="553cc-131">Allow a local client credential to prepare an outgoing token.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="553cc-132">*pvlogonid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="553cc-132">*pvLogonID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="553cc-133">Ein Zeiger auf einen [*lokal eindeutigen Bezeichner*](../secgloss/l-gly.md) (LUID), der den Benutzer identifiziert.</span><span class="sxs-lookup"><span data-stu-id="553cc-133">A pointer to a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) that identifies the user.</span></span> <span data-ttu-id="553cc-134">Dieser Parameter wird für Dateisystem Prozesse, z. b. netzwerkredirectors, bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="553cc-134">This parameter is provided for file-system processes such as network redirectors.</span></span> <span data-ttu-id="553cc-135">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="553cc-135">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="553cc-136">*pauthdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="553cc-136">*pAuthData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="553cc-137">Ein Zeiger auf Paket spezifische Daten.</span><span class="sxs-lookup"><span data-stu-id="553cc-137">A pointer to package-specific data.</span></span> <span data-ttu-id="553cc-138">Dieser Parameter kann **null** sein, was darauf hinweist, dass die Standard Anmelde Informationen für das [*Sicherheitspaket*](../secgloss/s-gly.md) verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="553cc-138">This parameter can be **NULL**, which indicates that the default credentials for that [*security package*](../secgloss/s-gly.md) must be used.</span></span> <span data-ttu-id="553cc-139">Um die angegebenen Anmelde Informationen zu verwenden, übergeben Sie eine [**sec- \_ Winnt-Authentifizierungs \_ \_ Identitäts**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) Struktur, die diese Anmelde Informationen enthält, in diesem Parameter.</span><span class="sxs-lookup"><span data-stu-id="553cc-139">To use supplied credentials, pass a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that includes those credentials in this parameter.</span></span> <span data-ttu-id="553cc-140">Die RPC-Laufzeit übergibt alle in [**rpcbindingsetauthinfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo)bereitgestellten.</span><span class="sxs-lookup"><span data-stu-id="553cc-140">The RPC run time passes whatever was provided in [**RpcBindingSetAuthInfo**](/windows/win32/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfo).</span></span>

<span data-ttu-id="553cc-141">Bei Verwendung des Digest-SSP ist dieser Parameter ein Zeiger auf eine [**sec- \_ Winnt-Authentifizierungs \_ \_ Identitäts**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) Struktur, die Authentifizierungsinformationen enthält, die zum Suchen der Anmelde Informationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="553cc-141">When using the Digest SSP, this parameter is a pointer to a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure that contains authentication information to use to locate the credentials.</span></span>

</dd> <dt>

<span data-ttu-id="553cc-142">*pgetkeyfn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="553cc-142">*pGetKeyFn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="553cc-143">Dieser Parameter wird nicht verwendet und sollte auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="553cc-143">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="553cc-144">*pvgetkeyargument* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="553cc-144">*pvGetKeyArgument* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="553cc-145">Dieser Parameter wird nicht verwendet und sollte auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="553cc-145">This parameter is not used and should be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="553cc-146">*phcredential* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="553cc-146">*phCredential* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="553cc-147">Ein Zeiger auf eine " [kredhandle](sspi-handles.md) "-Struktur, die das Handle für die Anmelde Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="553cc-147">A pointer to a [CredHandle](sspi-handles.md) structure to receive the credential handle.</span></span>

</dd> <dt>

<span data-ttu-id="553cc-148">*ptsexpiry* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="553cc-148">*ptsExpiry* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="553cc-149">Ein Zeiger auf eine [**Zeitstempel**](timestamp.md) Struktur, die die Uhrzeit empfängt, zu der die zurückgegebenen Anmelde Informationen ablaufen.</span><span class="sxs-lookup"><span data-stu-id="553cc-149">A pointer to a [**TimeStamp**](timestamp.md) structure that receives the time at which the returned credentials expire.</span></span> <span data-ttu-id="553cc-150">Der in dieser **Zeitstempel** Struktur zurückgegebene Wert hängt von der [*eingeschränkten Delegierung*](../secgloss/s-gly.md)ab.</span><span class="sxs-lookup"><span data-stu-id="553cc-150">The value returned in this **TimeStamp** structure depends on the [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="553cc-151">Das [*Sicherheitspaket*](../secgloss/s-gly.md) muss diesen Wert in der Ortszeit zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="553cc-151">The [*security package*](../secgloss/s-gly.md) must return this value in local time.</span></span>

<span data-ttu-id="553cc-152">Dieser Parameter ist auf eine Konstante maximale Zeit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="553cc-152">This parameter is set to a constant maximum time.</span></span> <span data-ttu-id="553cc-153">Es gibt keine Ablaufzeit für Digest- [*Sicherheitskontext*](../secgloss/s-gly.md)-oder-Anmelde Informationen oder bei Verwendung des Digest-SSP.</span><span class="sxs-lookup"><span data-stu-id="553cc-153">There is no expiration time for Digest [*security context*](../secgloss/s-gly.md)s or credentials or when using the Digest SSP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="553cc-154">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="553cc-154">Return value</span></span>

<span data-ttu-id="553cc-155">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion sec \_ E \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="553cc-155">If the function succeeds, the function returns SEC\_E\_OK.</span></span>

<span data-ttu-id="553cc-156">Wenn die Funktion fehlschlägt, wird einer der folgenden Fehlercodes zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="553cc-156">If the function fails, it returns one of the following error codes.</span></span>



| <span data-ttu-id="553cc-157">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="553cc-157">Return code</span></span>                                                                                                 | <span data-ttu-id="553cc-158">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="553cc-158">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="553cc-159"><dt>**SEK \_ b \_ nicht genügend Arbeits \_ Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="553cc-159"><dt>**SEC\_E\_INSUFFICIENT\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="553cc-160">Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="553cc-160">There is not enough memory available to complete the requested action.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="553cc-161"><dt>**Sek. \_ E ( \_ interner \_ Fehler)**</dt></span><span class="sxs-lookup"><span data-stu-id="553cc-161"><dt>**SEC\_E\_INTERNAL\_ERROR**</dt></span></span> </dl>      | <span data-ttu-id="553cc-162">Es ist ein Fehler aufgetreten, der keinem SSPI-Fehlercode zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="553cc-162">An error occurred that did not map to an SSPI error code.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="553cc-163"><dt>**s \_ E \_ keine \_ Anmelde Informationen**</dt></span><span class="sxs-lookup"><span data-stu-id="553cc-163"><dt>**SEC\_E\_NO\_CREDENTIALS**</dt></span></span> </dl>      | <span data-ttu-id="553cc-164">In der [*eingeschränkten Delegierung*](../secgloss/s-gly.md)sind keine Anmelde Informationen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="553cc-164">No credentials are available in the [*constrained delegation*](../secgloss/s-gly.md).</span></span><br/> |
| <dl> <span data-ttu-id="553cc-165"><dt>**Sek. \_ E \_ nicht \_ Besitzer**</dt></span><span class="sxs-lookup"><span data-stu-id="553cc-165"><dt>**SEC\_E\_NOT\_OWNER**</dt></span></span> </dl>           | <span data-ttu-id="553cc-166">Der Aufrufer der Funktion verfügt nicht über die erforderlichen Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="553cc-166">The caller of the function does not have the necessary credentials.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="553cc-167"><dt>**Sek. \_ E \_ secpkg \_ nicht \_ gefunden**</dt></span><span class="sxs-lookup"><span data-stu-id="553cc-167"><dt>**SEC\_E\_SECPKG\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="553cc-168">Das angeforderte [*Sicherheitspaket*](../secgloss/s-gly.md) ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="553cc-168">The requested [*security package*](../secgloss/s-gly.md) does not exist.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="553cc-169"><dt>**SEK \_ . \_ unbekannte \_ Anmelde Informationen**</dt></span><span class="sxs-lookup"><span data-stu-id="553cc-169"><dt>**SEC\_E\_UNKNOWN\_CREDENTIALS**</dt></span></span> </dl> | <span data-ttu-id="553cc-170">Die für das Paket angegebenen Anmelde Informationen wurden nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="553cc-170">The credentials supplied to the package were not recognized.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="553cc-171">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="553cc-171">Remarks</span></span>

<span data-ttu-id="553cc-172">Die **AcquireCredentialsHandle (Digest)** -Funktion gibt ein Handle für die Anmelde Informationen eines Prinzipals (z. b. einen Benutzer oder Client) zurück, der von einer bestimmten [*eingeschränkten Delegierung*](../secgloss/s-gly.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="553cc-172">The **AcquireCredentialsHandle (Digest)** function returns a handle to the credentials of a principal, such as a user or client, as used by a specific [*constrained delegation*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="553cc-173">Dies kann das Handle für bereits vorhandene Anmelde Informationen sein, oder die Funktion kann einen neuen Satz von Anmelde Informationen erstellen und zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="553cc-173">This can be the handle to preexisting credentials, or the function can create a new set of credentials and return it.</span></span> <span data-ttu-id="553cc-174">Dieses Handle kann in nachfolgenden Aufrufen der Funktionen [**akzeptsecuritycontext (Digest)**](acceptsecuritycontext--digest.md) und [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="553cc-174">This handle can be used in subsequent calls to the [**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md) and [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md) functions.</span></span>

<span data-ttu-id="553cc-175">Im Allgemeinen gestattet **AcquireCredentialsHandle (Digest)** einem Prozess nicht das Abrufen eines Handles für die Anmelde Informationen anderer Benutzer, die am gleichen Computer angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="553cc-175">In general, **AcquireCredentialsHandle (Digest)** does not allow a process to obtain a handle to the credentials of other users logged on to the same computer.</span></span> <span data-ttu-id="553cc-176">Allerdings hat ein Aufrufer mit der Berechtigung "SE \_ TCB \_ Name" die Option, den [*Anmelde Bezeichner*](../secgloss/l-gly.md) (LUID) eines beliebigen vorhandenen Anmelde Sitzungs Tokens anzugeben, um ein Handle für die Anmelde Informationen dieser Sitzung zu erhalten. [](../secgloss/s-gly.md)</span><span class="sxs-lookup"><span data-stu-id="553cc-176">However, a caller with SE\_TCB\_NAME [*privilege*](../secgloss/s-gly.md) has the option of specifying the [*logon identifier*](../secgloss/l-gly.md) (LUID) of any existing logon session token to get a handle to that session's credentials.</span></span> <span data-ttu-id="553cc-177">Diese wird in der Regel von Kernelmodusmodulen verwendet, die im Auftrag eines angemeldeten Benutzers agieren müssen.</span><span class="sxs-lookup"><span data-stu-id="553cc-177">Typically, this is used by kernel-mode modules that must act on behalf of a logged-on user.</span></span>

<span data-ttu-id="553cc-178">Ein Paket kann die Funktion in *pgetkeyfn* aufrufen, die vom RPC-Lauf Zeit Transport bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="553cc-178">A package might call the function in *pGetKeyFn* provided by the RPC run-time transport.</span></span> <span data-ttu-id="553cc-179">Wenn der Transport die Rückruffunktion zum Abrufen von Anmelde Informationen nicht unterstützt, muss dieser Parameter **null** sein.</span><span class="sxs-lookup"><span data-stu-id="553cc-179">If the transport does not support the notion of callback to retrieve credentials, this parameter must be **NULL**.</span></span>

<span data-ttu-id="553cc-180">Bei kernelmodusaufrufern müssen die folgenden Unterschiede beachtet werden:</span><span class="sxs-lookup"><span data-stu-id="553cc-180">For kernel mode callers, the following differences must be noted:</span></span>

-   <span data-ttu-id="553cc-181">Die beiden Zeichen folgen Parameter müssen [*Unicode*](../secgloss/u-gly.md) -Zeichen folgen sein.</span><span class="sxs-lookup"><span data-stu-id="553cc-181">The two string parameters must be [*Unicode*](../secgloss/u-gly.md) strings.</span></span>
-   <span data-ttu-id="553cc-182">Die Puffer Werte müssen im virtuellen Arbeitsspeicher des Prozesses zugeordnet werden, nicht aus dem Pool.</span><span class="sxs-lookup"><span data-stu-id="553cc-182">The buffer values must be allocated in process virtual memory, not from the pool.</span></span>

<span data-ttu-id="553cc-183">Wenn Sie die zurückgegebenen Anmelde Informationen nicht mehr verwenden, geben Sie den von den Anmelde Informationen genutzten Arbeitsspeicher frei, indem Sie die [**freecredentialshandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="553cc-183">When you have finished using the returned credentials, free the memory used by the credentials by calling the [**FreeCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-freecredentialshandle) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="553cc-184">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="553cc-184">Requirements</span></span>



| <span data-ttu-id="553cc-185">Anforderung</span><span class="sxs-lookup"><span data-stu-id="553cc-185">Requirement</span></span> | <span data-ttu-id="553cc-186">Wert</span><span class="sxs-lookup"><span data-stu-id="553cc-186">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="553cc-187">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="553cc-187">Minimum supported client</span></span><br/> | <span data-ttu-id="553cc-188">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="553cc-188">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="553cc-189">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="553cc-189">Minimum supported server</span></span><br/> | <span data-ttu-id="553cc-190">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="553cc-190">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="553cc-191">Header</span><span class="sxs-lookup"><span data-stu-id="553cc-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="553cc-192"><dt>SSPI. h (Include Security. h)</dt></span><span class="sxs-lookup"><span data-stu-id="553cc-192"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |
| <span data-ttu-id="553cc-193">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="553cc-193">Library</span></span><br/>                  | <dl> <span data-ttu-id="553cc-194"><dt>Secur32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="553cc-194"><dt>Secur32.lib</dt></span></span> </dl>                 |
| <span data-ttu-id="553cc-195">DLL</span><span class="sxs-lookup"><span data-stu-id="553cc-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="553cc-196"><dt>Secur32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="553cc-196"><dt>Secur32.dll</dt></span></span> </dl>                 |
| <span data-ttu-id="553cc-197">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="553cc-197">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="553cc-198">**Acquirecredentialshandlew** (Unicode) und **AcquireCredentialsHandleA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="553cc-198">**AcquireCredentialsHandleW** (Unicode) and **AcquireCredentialsHandleA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="553cc-199">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="553cc-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="553cc-200">SSPI-Funktionen</span><span class="sxs-lookup"><span data-stu-id="553cc-200">SSPI Functions</span></span>](authentication-functions.md#sspi-functions)
</dt> <dt>

[<span data-ttu-id="553cc-201">**Akzeptsecuritycontext (Digest)**</span><span class="sxs-lookup"><span data-stu-id="553cc-201">**AcceptSecurityContext (Digest)**</span></span>](acceptsecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="553cc-202">**InitializeSecurityContext (Digest)**</span><span class="sxs-lookup"><span data-stu-id="553cc-202">**InitializeSecurityContext (Digest)**</span></span>](initializesecuritycontext--digest.md)
</dt> <dt>

[<span data-ttu-id="553cc-203">**Freecredentialshandle**</span><span class="sxs-lookup"><span data-stu-id="553cc-203">**FreeCredentialsHandle**</span></span>](/windows/win32/api/sspi/nf-sspi-freecredentialshandle)
</dt> </dl>

 

 
