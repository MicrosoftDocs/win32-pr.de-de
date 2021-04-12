---
title: Authentication-Service Konstanten (rpcdce. h)
description: Die Authentifizierungsdienst Konstanten stellen die Authentifizierungsdienste dar, die an verschiedene Lauf Zeitfunktionen übermittelt werden.
ms.assetid: ac95276f-230d-4993-92fe-1739d022c8b3
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_NONE
- RPC_C_AUTHN_DCE_PRIVATE
- RPC_C_AUTHN_DCE_PUBLIC
- RPC_C_AUTHN_DEC_PUBLIC
- RPC_C_AUTHN_GSS_NEGOTIATE
- RPC_C_AUTHN_WINNT
- RPC_C_AUTHN_GSS_SCHANNEL
- RPC_C_AUTHN_GSS_KERBEROS
- RPC_C_AUTHN_DPA
- RPC_C_AUTHN_MSN
- RPC_C_AUTHN_DIGEST
- RPC_C_AUTHN_NEGO_EXTENDER
- RPC_C_AUTHN_MQ
- RPC_C_AUTHN_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4ace510c1c26030542090eb1b00e76db803df6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518725"
---
# <a name="authentication-service-constants"></a><span data-ttu-id="01300-103">Authentication-Service Konstanten</span><span class="sxs-lookup"><span data-stu-id="01300-103">Authentication-Service Constants</span></span>

<span data-ttu-id="01300-104">Die Authentifizierungsdienst Konstanten stellen die Authentifizierungsdienste dar, die an verschiedene Lauf Zeitfunktionen übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="01300-104">The authentication service constants represent the authentication services passed to various run-time functions.</span></span>

<span data-ttu-id="01300-105">Die folgenden Konstanten sind gültige Werte für den *authnsvc* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="01300-105">The following constants are valid values for the *AuthnSvc* parameter.</span></span>



| <span data-ttu-id="01300-106">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="01300-106">Constant/value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="01300-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01300-107">Description</span></span>                                                                                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_NONE"></span><span id="rpc_c_authn_none"></span><dl> <span data-ttu-id="01300-108"><dt>**RPC \_ C \_ authn \_ None**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="01300-108"><dt>**RPC\_C\_AUTHN\_NONE**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="01300-109">Keine Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="01300-109">No authentication.</span></span><br/>                                                                                                                                                        |
| <span id="RPC_C_AUTHN_DCE_PRIVATE"></span><span id="rpc_c_authn_dce_private"></span><dl> <span data-ttu-id="01300-110"><dt>**RPC \_ C \_ authn \_ DCE \_ private**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="01300-110"><dt>**RPC\_C\_AUTHN\_DCE\_PRIVATE**</dt> <dt>1</dt></span></span> </dl>        | <span data-ttu-id="01300-111">Verwenden Sie die Authentifizierung für den privaten Schlüssel der verteilten Computerumgebung (DCE).</span><span class="sxs-lookup"><span data-stu-id="01300-111">Use Distributed Computing Environment (DCE) private key authentication.</span></span><br/>                                                                                                   |
| <span id="RPC_C_AUTHN_DCE_PUBLIC"></span><span id="rpc_c_authn_dce_public"></span><dl> <span data-ttu-id="01300-112"><dt>**RPC \_ C \_ authn \_ DCE \_ Public**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="01300-112"><dt>**RPC\_C\_AUTHN\_DCE\_PUBLIC**</dt> <dt>2</dt></span></span> </dl>           | <span data-ttu-id="01300-113">Authentifizierung mit öffentlichem Schlüssel für DCE (für zukünftige Verwendung reserviert).</span><span class="sxs-lookup"><span data-stu-id="01300-113">DCE public key authentication (reserved for future use).</span></span><br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_DEC_PUBLIC"></span><span id="rpc_c_authn_dec_public"></span><dl> <span data-ttu-id="01300-114"><dt>**RPC \_ C \_ authn \_ , \_ Public**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="01300-114"><dt>**RPC\_C\_AUTHN\_DEC\_PUBLIC**</dt> <dt>4</dt></span></span> </dl>           | <span data-ttu-id="01300-115">Authentifizierung mit öffentlichem Schlüssel (für zukünftige Verwendung reserviert)</span><span class="sxs-lookup"><span data-stu-id="01300-115">DEC public key authentication (reserved for future use).</span></span><br/>                                                                                                                  |
| <span id="RPC_C_AUTHN_GSS_NEGOTIATE"></span><span id="rpc_c_authn_gss_negotiate"></span><dl> <span data-ttu-id="01300-116"><dt>**RPC \_ C \_ authn- \_ GSS- \_ Aushandlung**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="01300-116"><dt>**RPC\_C\_AUTHN\_GSS\_NEGOTIATE**</dt> <dt>9</dt></span></span> </dl>  | <span data-ttu-id="01300-117">Verwenden Sie den [Microsoft Aushandlungs-SSP](/windows/desktop/SecAuthN/microsoft-negotiate).</span><span class="sxs-lookup"><span data-stu-id="01300-117">Use the [Microsoft Negotiate SSP](/windows/desktop/SecAuthN/microsoft-negotiate).</span></span> <span data-ttu-id="01300-118">Dieser SSP verhandelt zwischen der Verwendung der NTLM-und Kerberos-Protokoll Sicherheits Unterstützungs Anbieter (SSP).</span><span class="sxs-lookup"><span data-stu-id="01300-118">This SSP negotiates between the use of the NTLM and Kerberos protocol Security Support Providers (SSP).</span></span><br/>  |
| <span id="RPC_C_AUTHN_WINNT"></span><span id="rpc_c_authn_winnt"></span><dl> <span data-ttu-id="01300-119"><dt>**RPC \_ C \_ authn \_ Winnt**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="01300-119"><dt>**RPC\_C\_AUTHN\_WINNT**</dt> <dt>10</dt></span></span> </dl>                          | <span data-ttu-id="01300-120">Verwenden Sie den [SSP von Microsoft NT LAN Manager (NTLM)](/windows/desktop/SecAuthN/microsoft-ntlm).</span><span class="sxs-lookup"><span data-stu-id="01300-120">Use the [Microsoft NT LAN Manager (NTLM) SSP](/windows/desktop/SecAuthN/microsoft-ntlm).</span></span><br/>                                                                                                   |
| <span id="RPC_C_AUTHN_GSS_SCHANNEL"></span><span id="rpc_c_authn_gss_schannel"></span><dl> <span data-ttu-id="01300-121"><dt>**RPC \_ C \_ authn \_ GSS \_ SChannel**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="01300-121"><dt>**RPC\_C\_AUTHN\_GSS\_SCHANNEL**</dt> <dt>14</dt></span></span> </dl>    | <span data-ttu-id="01300-122">Verwenden Sie den [Schannel SSP](/windows/desktop/SecAuthN/secure-channel).</span><span class="sxs-lookup"><span data-stu-id="01300-122">Use the [Schannel SSP](/windows/desktop/SecAuthN/secure-channel).</span></span> <span data-ttu-id="01300-123">Dieser SSP unterstützt SSL (Secure Socket Layer), private Kommunikationstechnologie (PCT) und TLS (Transport Level Security).</span><span class="sxs-lookup"><span data-stu-id="01300-123">This SSP supports Secure Socket Layer (SSL), private communication technology (PCT), and transport level security (TLS).</span></span><br/> |
| <span id="RPC_C_AUTHN_GSS_KERBEROS"></span><span id="rpc_c_authn_gss_kerberos"></span><dl> <span data-ttu-id="01300-124"><dt>**RPC \_ C \_ authn \_ GSS \_ Kerberos**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="01300-124"><dt>**RPC\_C\_AUTHN\_GSS\_KERBEROS**</dt> <dt>16</dt></span></span> </dl>    | <span data-ttu-id="01300-125">Verwenden Sie den [Kerberos-SSP von Microsoft](/windows/desktop/SecAuthN/microsoft-kerberos).</span><span class="sxs-lookup"><span data-stu-id="01300-125">Use the [Microsoft Kerberos SSP](/windows/desktop/SecAuthN/microsoft-kerberos).</span></span><br/>                                                                                                            |
| <span id="RPC_C_AUTHN_DPA"></span><span id="rpc_c_authn_dpa"></span><dl> <span data-ttu-id="01300-126"><dt>**RPC \_ C \_ authn \_ DPA**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="01300-126"><dt>**RPC\_C\_AUTHN\_DPA**</dt> <dt>17</dt></span></span> </dl>                                | <span data-ttu-id="01300-127">Verwenden Sie die Authentifizierung verteilter Kenn Wörter (dpa).</span><span class="sxs-lookup"><span data-stu-id="01300-127">Use Distributed Password Authentication (DPA).</span></span><br/>                                                                                                                            |
| <span id="RPC_C_AUTHN_MSN"></span><span id="rpc_c_authn_msn"></span><dl> <span data-ttu-id="01300-128"><dt>**RPC \_ C \_ authn \_ MSN**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="01300-128"><dt>**RPC\_C\_AUTHN\_MSN**</dt> <dt>18</dt></span></span> </dl>                                | <span data-ttu-id="01300-129">Der Authentifizierungsprotokoll-SSP, der für das Microsoft-Netzwerk (MSN) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="01300-129">Authentication protocol SSP used for the Microsoft Network (MSN).</span></span><br/>                                                                                                         |
| <span id="RPC_C_AUTHN_DIGEST"></span><span id="rpc_c_authn_digest"></span><dl> <span data-ttu-id="01300-130"><dt>**RPC \_ C- \_ authn \_ Digest**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="01300-130"><dt>**RPC\_C\_AUTHN\_DIGEST**</dt> <dt>21</dt></span></span> </dl>                       | <span data-ttu-id="01300-131">Windows XP oder höher: Verwenden des [Microsoft Digest SSP](/windows/desktop/SecAuthN/microsoft-digest-ssp)</span><span class="sxs-lookup"><span data-stu-id="01300-131">Windows XP or later: Use the [Microsoft Digest SSP](/windows/desktop/SecAuthN/microsoft-digest-ssp)</span></span><br/>                                                                                        |
| <span id="RPC_C_AUTHN_NEGO_EXTENDER"></span><span id="rpc_c_authn_nego_extender"></span><dl> <span data-ttu-id="01300-132"><dt>**RPC \_ C \_ authn- \_ \_ Extender-Extender**</dt> <dt>30</dt></span><span class="sxs-lookup"><span data-stu-id="01300-132"><dt>**RPC\_C\_AUTHN\_NEGO\_EXTENDER**</dt> <dt>30</dt></span></span> </dl> | <span data-ttu-id="01300-133">Windows 7 oder höher: reserviert.</span><span class="sxs-lookup"><span data-stu-id="01300-133">Windows 7 or later: Reserved.</span></span> <span data-ttu-id="01300-134">Nicht verwenden</span><span class="sxs-lookup"><span data-stu-id="01300-134">Do not use</span></span><br/>                                                                                                                                  |
| <span id="RPC_C_AUTHN_MQ"></span><span id="rpc_c_authn_mq"></span><dl> <span data-ttu-id="01300-135"><dt>**RPC \_ C \_ authn \_ MQ**</dt> <dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="01300-135"><dt>**RPC\_C\_AUTHN\_MQ**</dt> <dt>100</dt></span></span> </dl>                                  | <span data-ttu-id="01300-136">Dieser SSP bietet einen SSPI-kompatiblen Wrapper für das Protokoll der Microsoft Message Queue (MSMQ)-Transport Ebene.</span><span class="sxs-lookup"><span data-stu-id="01300-136">This SSP provides an SSPI-compatible wrapper for the Microsoft Message Queue (MSMQ) transport-level protocol.</span></span><br/>                                                             |
| <span id="RPC_C_AUTHN_DEFAULT"></span><span id="rpc_c_authn_default"></span><dl> <span data-ttu-id="01300-137"><dt>**RPC \_ C \_ authn \_ Standard**</dt> <dt>0xFFFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="01300-137"><dt>**RPC\_C\_AUTHN\_DEFAULT**</dt> <dt>0xffffffff</dt></span></span> </dl>            | <span data-ttu-id="01300-138">Verwenden Sie den Standard Authentifizierungsdienst.</span><span class="sxs-lookup"><span data-stu-id="01300-138">Use the default authentication service.</span></span><br/>                                                                                                                                   |



## <a name="remarks"></a><span data-ttu-id="01300-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01300-139">Remarks</span></span>

<span data-ttu-id="01300-140">Geben \_ Sie RPC C \_ authn \_ None an, um die Authentifizierung für Remote Prozedur Aufrufe, die über ein Bindungs handle erfolgen, zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="01300-140">Specify RPC\_C\_AUTHN\_NONE to turn off authentication for remote procedure calls made over a binding handle.</span></span> <span data-ttu-id="01300-141">Wenn Sie RPC \_ c \_ authn \_ default angeben, wird von der RPC-Lauf Zeit Bibliothek der RPC- \_ c- \_ authn- \_ Winnt-Authentifizierungsdienst für Remote Prozedur Aufrufe verwendet, die mithilfe des Bindungs Handles ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="01300-141">When you specify RPC\_C\_AUTHN\_DEFAULT, the RPC run-time library uses the RPC\_C\_AUTHN\_WINNT authentication service for remote procedure calls made using the binding handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="01300-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01300-142">Requirements</span></span>



| <span data-ttu-id="01300-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01300-143">Requirement</span></span> | <span data-ttu-id="01300-144">Wert</span><span class="sxs-lookup"><span data-stu-id="01300-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="01300-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="01300-145">Minimum supported client</span></span><br/> | <span data-ttu-id="01300-146">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="01300-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="01300-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="01300-147">Minimum supported server</span></span><br/> | <span data-ttu-id="01300-148">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="01300-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="01300-149">Header</span><span class="sxs-lookup"><span data-stu-id="01300-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="01300-150"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="01300-150"><dt>Rpcdce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01300-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01300-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01300-152">**Rpcbindinginqauthinfo**</span><span class="sxs-lookup"><span data-stu-id="01300-152">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="01300-153">**Rpcbindingsetauthinfo**</span><span class="sxs-lookup"><span data-stu-id="01300-153">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[<span data-ttu-id="01300-154">**Rpcbindinginqauthclient**</span><span class="sxs-lookup"><span data-stu-id="01300-154">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[<span data-ttu-id="01300-155">**Rpcbindinginqauthcliumtex**</span><span class="sxs-lookup"><span data-stu-id="01300-155">**RpcBindingInqAuthClientEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[<span data-ttu-id="01300-156">**Rpcbindingsetauthinfoex**</span><span class="sxs-lookup"><span data-stu-id="01300-156">**RpcBindingSetAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[<span data-ttu-id="01300-157">**Rpcbindinginqauthinfoex**</span><span class="sxs-lookup"><span data-stu-id="01300-157">**RpcBindingInqAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

