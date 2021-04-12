---
title: Authentifizierungs Konstanten (WSManDisp. h)
description: Geben Sie die Authentifizierungsmethode an und wie Sie Zertifikat Server für den HTTPS-Transport von Anforderungen verarbeiten.
ms.assetid: adfefbc9-c386-48db-a0c2-145aa4f91bfa
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagCredUsernamePassword
- WSManFlagSkipCACheck
- WSManFlagSkipCNCheck
- WSManFlagUseNoAuthentication
- WSManFlagUseDigest
- WSManFlagUseNegotiate
- WSManFlagUseBasic
- WSManFlagUseKerberos
- WSManFlagNoEncryption
- WSManFlagUseClientCertificate
- WSManFlagUseCredSsp
- WSManFlagSkipRevocationCheck
- WSManFlagAllowNegotiateImplicitCredentials
- WSManFlagUseSsl
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce45d1474cf6c925149c05ae348231333c3356e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518773"
---
# <a name="authentication-constants"></a><span data-ttu-id="09253-103">Authentifizierungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="09253-103">Authentication Constants</span></span>

<span data-ttu-id="09253-104">Authentifizierungs Konstanten sind Konstanten in der **\_ \_ wsmansessionflags** -Enumeration, die die Authentifizierungsmethode angeben und angeben, wie Zertifikat Server für den HTTPS-Transport von Anforderungen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="09253-104">Authentication constants are constants in the **\_\_WSManSessionFlags** enumeration that specify the authentication method and how to handle certificate servers for HTTPS transport of requests.</span></span>

<span data-ttu-id="09253-105">Mindestens eine der in der folgenden Liste aufgeführten Konstanten ist im *Flags* -Parameter in Aufrufen von [**WSMAN. kreatesession**](wsman-createsession.md) oder in [**iwsman:: anatesession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) -aufrufen erforderlich, die eine Verbindung mit einem Remote Computer herstellen.</span><span class="sxs-lookup"><span data-stu-id="09253-105">One or more of the constants listed in the following list are required in the *flags* parameter in calls to [**WSMan.CreateSession**](wsman-createsession.md) or in [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) calls that connect to a remote computer.</span></span>

<dl> <dt>

<span data-ttu-id="09253-106"><span id="WSManFlagCredUsernamePassword"></span><span id="wsmanflagcredusernamepassword"></span><span id="WSMANFLAGCREDUSERNAMEPASSWORD"></span>**Wsmanflagkredusernamepassword**</span><span class="sxs-lookup"><span data-stu-id="09253-106"><span id="WSManFlagCredUsernamePassword"></span><span id="wsmanflagcredusernamepassword"></span><span id="WSMANFLAGCREDUSERNAMEPASSWORD"></span>**WSManFlagCredUsernamePassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09253-107">4096 (0x1000)</span><span class="sxs-lookup"><span data-stu-id="09253-107">4096 (0x1000)</span></span>
</dt> <dt>



<span data-ttu-id="09253-108">Verwenden Sie den Benutzernamen und das Kennwort als Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="09253-108">Use the user name and password as the credentials.</span></span> <span data-ttu-id="09253-109">Legen Sie dieses Flag fest, wenn Sie ein [**ConnectionOptions**](connectionoptions.md) -Objekt erstellen und [**Benutzername**](connectionoptions-username.md) und [**Kennwort**](connectionoptions-password.md)angeben.</span><span class="sxs-lookup"><span data-stu-id="09253-109">Set this flag when you create a [**ConnectionOptions**](connectionoptions.md) object and supply [**Username**](connectionoptions-username.md) and [**Password**](connectionoptions-password.md).</span></span> <span data-ttu-id="09253-110">Bei den Anmelde Informationen kann es sich um ein Domänen Konto oder ein Konto auf dem lokalen Computer handeln.</span><span class="sxs-lookup"><span data-stu-id="09253-110">The credentials can be a domain account or an account on the local computer.</span></span> <span data-ttu-id="09253-111">Standardmäßig muss das Konto ein Mitglied der lokalen Gruppe "Administratoren" auf dem lokalen Computer oder dem Remote Computer sein.</span><span class="sxs-lookup"><span data-stu-id="09253-111">By default, the account must be a member of the local Administrators group on the local or remote computer.</span></span> <span data-ttu-id="09253-112">Der WinRM-Dienst kann jedoch so konfiguriert werden, dass er anderen Benutzern gestattet wird.</span><span class="sxs-lookup"><span data-stu-id="09253-112">However, the WinRM service can be configured to allow other users.</span></span> <span data-ttu-id="09253-113">Weitere Informationen finden Sie unter [Installation und Konfiguration für Windows-Remoteverwaltung](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="09253-113">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span> <span data-ttu-id="09253-114">Sie können dieses Flag festlegen, wenn Sie Anmelde Informationen für die Aushandlungs Authentifizierung (auch bekannt als [*integrierte Windows-Authentifizierung*](windows-remote-management-glossary.md)) oder für die Standard [*Authentifizierung*](windows-remote-management-glossary.md)angeben.</span><span class="sxs-lookup"><span data-stu-id="09253-114">You can set this flag when you specify credentials for Negotiate authentication (also known as [*Windows Integrated Authentication*](windows-remote-management-glossary.md)) or for [*Basic authentication*](windows-remote-management-glossary.md).</span></span>

<span data-ttu-id="09253-115">Die zugeordnete Skript Methode lautet " [**WSMAN. sessionflagkredusernamepassword**](wsman-sessionflagcredusernamepassword.md)", und die C++-Methode ist " [**iwsmanex. sessionflagkredusernamepassword**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword)".</span><span class="sxs-lookup"><span data-stu-id="09253-115">The associated scripting method is [**WSMan.SessionFlagCredUsernamePassword**](wsman-sessionflagcredusernamepassword.md), and the C++ method is [**IWSManEx.SessionFlagCredUsernamePassword**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="09253-116"><span id="WSManFlagSkipCACheck"></span><span id="wsmanflagskipcacheck"></span><span id="WSMANFLAGSKIPCACHECK"></span>**Wsmanflagskipcacheck**</span><span class="sxs-lookup"><span data-stu-id="09253-116"><span id="WSManFlagSkipCACheck"></span><span id="wsmanflagskipcacheck"></span><span id="WSMANFLAGSKIPCACHECK"></span>**WSManFlagSkipCACheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09253-117">8192 (0x2000)</span><span class="sxs-lookup"><span data-stu-id="09253-117">8192 (0x2000)</span></span>
</dt> <dt>



<span data-ttu-id="09253-118">Beim Herstellen einer Verbindung über HTTPS überprüft der Client nicht, ob das Serverzertifikat von einer vertrauenswürdigen Zertifizierungsstelle (Certification Authority, ca) signiert wurde.</span><span class="sxs-lookup"><span data-stu-id="09253-118">When connecting over HTTPS, the client does not validate that the server certificate is signed by a trusted certification authority (CA).</span></span> <span data-ttu-id="09253-119">Verwenden Sie diesen Wert nur, wenn der Remote Computer auf andere Weise vertrauenswürdig ist, z. b. wenn der Remote Computer Teil eines physisch sicheren und isolierten Netzwerks ist oder wenn der Remote Computer in der WinRM-Konfiguration als vertrauenswürdiger Host aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="09253-119">Use this value only when the remote computer is trusted by other means, for example, if the remote computer is part of a network that is physically secure and isolated or the remote computer is listed as a trusted host in the WinRM configuration.</span></span>

<span data-ttu-id="09253-120">Die zugeordnete Skript Methode lautet [**WSMAN. sessionflagskipcacheck**](wsman-sessionflagskipcacheck.md), und die C++-Methode ist [**iwsmanex. sessionflagskipcacheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck).</span><span class="sxs-lookup"><span data-stu-id="09253-120">The associated scripting method is [**WSMan.SessionFlagSkipCACheck**](wsman-sessionflagskipcacheck.md), and the C++ method is [**IWSManEx.SessionFlagSkipCACheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="09253-121"><span id="WSManFlagSkipCNCheck"></span><span id="wsmanflagskipcncheck"></span><span id="WSMANFLAGSKIPCNCHECK"></span>**Wsmanflagskipcncheck**</span><span class="sxs-lookup"><span data-stu-id="09253-121"><span id="WSManFlagSkipCNCheck"></span><span id="wsmanflagskipcncheck"></span><span id="WSMANFLAGSKIPCNCHECK"></span>**WSManFlagSkipCNCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09253-122">16384 (0x4000)</span><span class="sxs-lookup"><span data-stu-id="09253-122">16384 (0x4000)</span></span>
</dt> <dt>



<span data-ttu-id="09253-123">Wenn eine Verbindung über HTTPS hergestellt wird, überprüft der Client nicht, ob der allgemeine Name (Common Name, CN) im Serverzertifikat mit dem Computernamen in der Verbindungs Zeichenfolge übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="09253-123">When connecting over HTTPS, the client will not validate that the common name (CN) in the server certificate matches the computer name in the connection string.</span></span> <span data-ttu-id="09253-124">Nur verwenden, wenn der Remote Computer auf andere Weise vertrauenswürdig ist, z. b. wenn der Remote Computer Teil eines physisch sicheren und isolierten Netzwerks ist oder wenn der Remote Computer in der WinRM-Konfiguration als vertrauenswürdiger Host aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="09253-124">Use only when the remote computer is trusted by other means, for example, if the remote computer is part of a network that is physically secure and isolated or the remote computer is listed as a trusted host in the WinRM configuration.</span></span>

<span data-ttu-id="09253-125">Die zugeordnete Skript Methode lautet " [**WSMAN. sessionflagskipcncheck**](wsman-sessionflagskipcncheck.md)", und die C++-Methode ist " [**iwsmanex. sessionflagskipcncheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck)".</span><span class="sxs-lookup"><span data-stu-id="09253-125">The associated scripting method is [**WSMan.SessionFlagSkipCNCheck**](wsman-sessionflagskipcncheck.md), and the C++ method is [**IWSManEx.SessionFlagSkipCNCheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="09253-126"><span id="WSManFlagUseNoAuthentication"></span><span id="wsmanflagusenoauthentication"></span><span id="WSMANFLAGUSENOAUTHENTICATION"></span>**Wsmanflagusenoauthentication**</span><span class="sxs-lookup"><span data-stu-id="09253-126"><span id="WSManFlagUseNoAuthentication"></span><span id="wsmanflagusenoauthentication"></span><span id="WSMANFLAGUSENOAUTHENTICATION"></span>**WSManFlagUseNoAuthentication**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09253-127">32768 (0X8000)</span><span class="sxs-lookup"><span data-stu-id="09253-127">32768 (0x8000)</span></span>
</dt> <dt>



<span data-ttu-id="09253-128">Verwenden Sie keine Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="09253-128">Use no authentication.</span></span> <span data-ttu-id="09253-129">Geben Sie diese Konstante beim Testen einer Verbindung mit einem Remote Computer an, um zu bestimmen, ob ein Dienst, der das WS-Management Protokoll implementiert, für das Lauschen auf Datenanforderungen konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="09253-129">Specify this constant when testing a connection to a remote computer to determine if a service that implements the WS-Management protocol is configured to listen for data requests.</span></span> <span data-ttu-id="09253-130">" **Wsmanflagusenoauthentication** " kann nicht mit einer anderen [**Sitzungs**](session.md) Konstante kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="09253-130">**WSManFlagUseNoAuthentication** cannot be combined with any other [**Session**](session.md) constant.</span></span> <span data-ttu-id="09253-131">Die zugeordnete Skript Methode lautet [**WSMAN. sessionflagusenoauthentication**](wsman-sessionflagusenoauthentication.md), und die C++-Methode ist [**wsmanex. sessionflagusenoauthentication**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication).</span><span class="sxs-lookup"><span data-stu-id="09253-131">The associated scripting method is [**WSMan.SessionFlagUseNoAuthentication**](wsman-sessionflagusenoauthentication.md), and the C++ method is [**WSManEx.SessionFlagUseNoAuthentication**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="09253-132"><span id="WSManFlagUseDigest"></span><span id="wsmanflagusedigest"></span><span id="WSMANFLAGUSEDIGEST"></span>**Wsmanflagusedigest**</span><span class="sxs-lookup"><span data-stu-id="09253-132"><span id="WSManFlagUseDigest"></span><span id="wsmanflagusedigest"></span><span id="WSMANFLAGUSEDIGEST"></span>**WSManFlagUseDigest**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09253-133">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="09253-133">65536 (0x10000)</span></span>
</dt> <dt>



<span data-ttu-id="09253-134">Verwenden Sie die Digestauthentifizierung.</span><span class="sxs-lookup"><span data-stu-id="09253-134">Use Digest authentication.</span></span> <span data-ttu-id="09253-135">Nur der Clientcomputer kann eine Anforderung der Digestauthentifizierung initiieren.</span><span class="sxs-lookup"><span data-stu-id="09253-135">Only the client computer can initiate a Digest authentication request.</span></span> <span data-ttu-id="09253-136">Der Client sendet eine Anforderung an den Server, um eine Tokenzeichenfolge vom Server zu authentifizieren und zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="09253-136">The client sends a request to the server to authenticate and receives a token string from the server.</span></span> <span data-ttu-id="09253-137">Der Client sendet dann die Ressourcen Anforderung, einschließlich des Benutzernamens und eines kryptografischen Hashs des Kennworts, in Kombination mit der Tokenzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="09253-137">The client then sends the resource request, including the user name and a cryptographic hash of the password combined with the token string.</span></span> <span data-ttu-id="09253-138">Die Digest-Authentifizierung wird für http und HTTPS unterstützt.</span><span class="sxs-lookup"><span data-stu-id="09253-138">Digest authentication is supported for HTTP and HTTPS.</span></span> <span data-ttu-id="09253-139">WinRM-Client Skripts und-Anwendungen können die Digestauthentifizierung angeben, jedoch nicht den-Dienst.</span><span class="sxs-lookup"><span data-stu-id="09253-139">WinRM client scripts and applications can specify Digest authentication, but not the service.</span></span>

<span data-ttu-id="09253-140">Die zugeordnete Skript Methode ist [**WSMAN. sessionflagusedigest**](wsman-sessionflagusedigest.md), und die C++-Methode ist [**iwsmanex. sessionflagusedigest**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest).</span><span class="sxs-lookup"><span data-stu-id="09253-140">The associated scripting method is [**WSMan.SessionFlagUseDigest**](wsman-sessionflagusedigest.md), and the C++ method is [**IWSManEx.SessionFlagUseDigest**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="09253-141"><span id="WSManFlagUseNegotiate"></span><span id="wsmanflagusenegotiate"></span><span id="WSMANFLAGUSENEGOTIATE"></span>**Wsmanflagusenegotiate**</span><span class="sxs-lookup"><span data-stu-id="09253-141"><span id="WSManFlagUseNegotiate"></span><span id="wsmanflagusenegotiate"></span><span id="WSMANFLAGUSENEGOTIATE"></span>**WSManFlagUseNegotiate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09253-142">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="09253-142">131072 (0x20000)</span></span>
</dt> <dt>



<span data-ttu-id="09253-143">Verwenden Sie die Aushandlungs Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="09253-143">Use Negotiate authentication.</span></span> <span data-ttu-id="09253-144">Der Client sendet eine Anforderung an den Server, um sich zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="09253-144">The client sends a request to the server to authenticate.</span></span> <span data-ttu-id="09253-145">Der Server bestimmt, ob Kerberos oder NTLM verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="09253-145">The server determines whether to use Kerberos or NTLM.</span></span> <span data-ttu-id="09253-146">Kerberos wird zum Authentifizieren eines Domänen Kontos ausgewählt, und NTLM ist für lokale Computer Konten ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="09253-146">Kerberos is selected to authenticate a domain account and NTLM is selected for local computer accounts.</span></span> <span data-ttu-id="09253-147">Der Benutzername muss im Format Domäne \\ Benutzername für einen Domänen Benutzer oder \\ Servername Benutzername für einen lokalen Benutzer auf einem Server Computer angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="09253-147">The user name should be specified in the form domain\\username for a domain user or servername\\username for a local user on a server computer.</span></span>

<span data-ttu-id="09253-148">Die [Benutzerkontensteuerung (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) wirkt sich auf den Zugriff auf den WinRM-Dienst aus.</span><span class="sxs-lookup"><span data-stu-id="09253-148">[User Account Control (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) affects access to the WinRM service.</span></span> <span data-ttu-id="09253-149">Wenn die Aushandlungs Authentifizierung in einer Arbeitsgruppe oder Domäne verwendet wird, kann nur das integrierte Administrator Konto auf den Dienst zugreifen.</span><span class="sxs-lookup"><span data-stu-id="09253-149">When Negotiate authentication is used in a workgroup or domain, only the built-in Administrator account can access the service.</span></span> <span data-ttu-id="09253-150">Damit alle Konten in der Gruppe "Administratoren" auf den Dienst zugreifen können, legen Sie den folgenden Registrierungsschlüssel auf 1 fest: **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Policies \\ System \\ LocalAccountTokenFilterPolicy**.</span><span class="sxs-lookup"><span data-stu-id="09253-150">To allow all accounts in the Administrators group to access the service, set the following registry key to 1: **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Policies\\system\\LocalAccountTokenFilterPolicy**.</span></span>

<span data-ttu-id="09253-151">Die zugeordnete Skript Methode ist [**WSMAN. sessionflagusenegotiate**](wsman-sessionflagusenegotiate.md), und die C++-Methode ist [**iwsmanex. sessionflagusenegotiate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate).</span><span class="sxs-lookup"><span data-stu-id="09253-151">The associated scripting method is [**WSMan.SessionFlagUseNegotiate**](wsman-sessionflagusenegotiate.md), and the C++ method is [**IWSManEx.SessionFlagUseNegotiate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="09253-152"><span id="WSManFlagUseBasic"></span><span id="wsmanflagusebasic"></span><span id="WSMANFLAGUSEBASIC"></span>**Wsmanflagusebasic**</span><span class="sxs-lookup"><span data-stu-id="09253-152"><span id="WSManFlagUseBasic"></span><span id="wsmanflagusebasic"></span><span id="WSMANFLAGUSEBASIC"></span>**WSManFlagUseBasic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09253-153">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="09253-153">262144 (0x40000)</span></span>
</dt> <dt>



<span data-ttu-id="09253-154">Verwenden Sie die Standard Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="09253-154">Use Basic authentication.</span></span> <span data-ttu-id="09253-155">Der Client stellt Anmelde Informationen in Form eines Benutzernamens und eines Kennworts dar, die direkt in der Anforderungs Nachricht übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="09253-155">The client presents credentials in the form of a user name and password, directly transmitted in the request message.</span></span> <span data-ttu-id="09253-156">Sie können nur Anmelde Informationen angeben, die ein lokales Administrator Konto auf dem Remote Computer identifizieren.</span><span class="sxs-lookup"><span data-stu-id="09253-156">You can specify only credentials that identify a local administrator account on the remote computer.</span></span>

<span data-ttu-id="09253-157">Die zugeordnete Skript Methode lautet " [**WSMAN. sessionflagusebasic**](wsman-sessionflagusebasic.md)", und die C++-Methode ist " [**iwsmanex. sessionflagusebasic**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic)".</span><span class="sxs-lookup"><span data-stu-id="09253-157">The associated scripting method is [**WSMan.SessionFlagUseBasic**](wsman-sessionflagusebasic.md), and the C++ method is [**IWSManEx.SessionFlagUseBasic**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="09253-158"><span id="WSManFlagUseKerberos"></span><span id="wsmanflagusekerberos"></span><span id="WSMANFLAGUSEKERBEROS"></span>**Wsmanflagusekerberos**</span><span class="sxs-lookup"><span data-stu-id="09253-158"><span id="WSManFlagUseKerberos"></span><span id="wsmanflagusekerberos"></span><span id="WSMANFLAGUSEKERBEROS"></span>**WSManFlagUseKerberos**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09253-159">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="09253-159">524288 (0x80000)</span></span>
</dt> <dt>



<span data-ttu-id="09253-160">Verwenden Sie Kerberos-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="09253-160">Use Kerberos authentication.</span></span> <span data-ttu-id="09253-161">Der Client und der Server authentifizieren sich gegenseitig mithilfe von Kerberos-Tickets.</span><span class="sxs-lookup"><span data-stu-id="09253-161">The client and server mutually authenticate using Kerberos tickets.</span></span>

<span data-ttu-id="09253-162">Die zugeordnete Skript Methode lautet [**WSMAN. sessionflagusekerberos**](wsman-sessionflagusekerberos.md), und die C++-Methode ist [**iwsmanex. WSMAN. sessionflagusekerberos**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos).</span><span class="sxs-lookup"><span data-stu-id="09253-162">The associated scripting method is [**WSMan.SessionFlagUseKerberos**](wsman-sessionflagusekerberos.md), and the C++ method is [**IWSManEx.WSMan.SessionFlagUseKerberos**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="09253-163"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**Wsmanflagnoencryption**</span><span class="sxs-lookup"><span data-stu-id="09253-163"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09253-164">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="09253-164">1048576 (0x100000)</span></span>
</dt> <dt>



<span data-ttu-id="09253-165">Verwenden Sie keine Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="09253-165">Use no encryption.</span></span> <span data-ttu-id="09253-166">Unverschlüsselter Datenverkehr ist standardmäßig nicht zulässig und muss sowohl auf dem Client als auch auf dem Server aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="09253-166">Unencrypted traffic is not allowed by default and must be enabled on both the client and server.</span></span>

<span data-ttu-id="09253-167">Die zugeordnete Skript Methode lautet " [**WSMAN. sessionflagnoencryption**](wsman-sessionflagnoencryption.md)", und die C++-Methode ist " [**iwsmanex. sessionflagnoencryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption)".</span><span class="sxs-lookup"><span data-stu-id="09253-167">The associated scripting method is [**WSMan.SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md), and the C++ method is [**IWSManEx.SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="09253-168"><span id="WSManFlagUseClientCertificate"></span><span id="wsmanflaguseclientcertificate"></span><span id="WSMANFLAGUSECLIENTCERTIFICATE"></span>**Wsmanflaguseclientcertificate**</span><span class="sxs-lookup"><span data-stu-id="09253-168"><span id="WSManFlagUseClientCertificate"></span><span id="wsmanflaguseclientcertificate"></span><span id="WSMANFLAGUSECLIENTCERTIFICATE"></span>**WSManFlagUseClientCertificate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09253-169">2097152 (0x200.000)</span><span class="sxs-lookup"><span data-stu-id="09253-169">2097152 (0x200000)</span></span>
</dt> <dt>



<span data-ttu-id="09253-170">Verwenden Sie die Zertifikat basierte Client Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="09253-170">Use client certificate-based authentication.</span></span>

<span data-ttu-id="09253-171">Die zugehörige Skript Methode lautet [**WSMAN. sessionflaguseclientcertificate**](wsman-sessionflaguseclientcert.md), und die C++-Methode ist [**IWSManEx2. sessionflaguseclientcertificate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex2-sessionflaguseclientcertificate).</span><span class="sxs-lookup"><span data-stu-id="09253-171">The associated scripting method is [**WSMan.SessionFlagUseClientCertificate**](wsman-sessionflaguseclientcert.md), and the C++ method is [**IWSManEx2.SessionFlagUseClientCertificate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex2-sessionflaguseclientcertificate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="09253-172"><span id="WSManFlagUseCredSsp"></span><span id="wsmanflagusecredssp"></span><span id="WSMANFLAGUSECREDSSP"></span>**Wsmanflagusecredssp**</span><span class="sxs-lookup"><span data-stu-id="09253-172"><span id="WSManFlagUseCredSsp"></span><span id="wsmanflagusecredssp"></span><span id="WSMANFLAGUSECREDSSP"></span>**WSManFlagUseCredSsp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09253-173">16777216 (0x1000000)</span><span class="sxs-lookup"><span data-stu-id="09253-173">16777216 (0x1000000)</span></span>
</dt> <dt>



<span data-ttu-id="09253-174">Verwenden Sie die Authentifizierung der Credential Security Support Provider (kredssp).</span><span class="sxs-lookup"><span data-stu-id="09253-174">Use Credential Security Support Provider (CredSSP) authentication.</span></span>

<span data-ttu-id="09253-175">Die zugeordnete Skript Methode ist [**WSMAN. sessionflagusecredssp**](wsman-sessionflagusecredssp.md), und die C++-Methode ist [**IWSManEx3. sessionflagusecredssp**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex3-sessionflagusecredssp).</span><span class="sxs-lookup"><span data-stu-id="09253-175">The associated scripting method is [**WSMan.SessionFlagUseCredSsp**](wsman-sessionflagusecredssp.md), and the C++ method is [**IWSManEx3.SessionFlagUseCredSsp**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex3-sessionflagusecredssp).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="09253-176"><span id="WSManFlagSkipRevocationCheck"></span><span id="wsmanflagskiprevocationcheck"></span><span id="WSMANFLAGSKIPREVOCATIONCHECK"></span>**Wsmanflagskiprevocationcheck**</span><span class="sxs-lookup"><span data-stu-id="09253-176"><span id="WSManFlagSkipRevocationCheck"></span><span id="wsmanflagskiprevocationcheck"></span><span id="WSMANFLAGSKIPREVOCATIONCHECK"></span>**WSManFlagSkipRevocationCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09253-177">0x2000000</span><span class="sxs-lookup"><span data-stu-id="09253-177">0x2000000</span></span>
</dt> <dt>



<span data-ttu-id="09253-178">Überprüfen Sie während der Authentifizierung nicht, ob die Zertifikat Sperre besteht.</span><span class="sxs-lookup"><span data-stu-id="09253-178">Do not check for certificate revocation during authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="09253-179"><span id="WSManFlagAllowNegotiateImplicitCredentials"></span><span id="wsmanflagallownegotiateimplicitcredentials"></span><span id="WSMANFLAGALLOWNEGOTIATEIMPLICITCREDENTIALS"></span>**Wsmanflagallowaushandateimplicitanmelde Informationen**</span><span class="sxs-lookup"><span data-stu-id="09253-179"><span id="WSManFlagAllowNegotiateImplicitCredentials"></span><span id="wsmanflagallownegotiateimplicitcredentials"></span><span id="WSMANFLAGALLOWNEGOTIATEIMPLICITCREDENTIALS"></span>**WSManFlagAllowNegotiateImplicitCredentials**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09253-180">0x4000000</span><span class="sxs-lookup"><span data-stu-id="09253-180">0x4000000</span></span>
</dt> <dt>



<span data-ttu-id="09253-181">Implizite Anmelde Informationen zulassen.</span><span class="sxs-lookup"><span data-stu-id="09253-181">Allow implicit credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="09253-182"><span id="WSManFlagUseSsl"></span><span id="wsmanflagusessl"></span><span id="WSMANFLAGUSESSL"></span>**Wsmanflagus Essl**</span><span class="sxs-lookup"><span data-stu-id="09253-182"><span id="WSManFlagUseSsl"></span><span id="wsmanflagusessl"></span><span id="WSMANFLAGUSESSL"></span>**WSManFlagUseSsl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09253-183">0x8000000</span><span class="sxs-lookup"><span data-stu-id="09253-183">0x8000000</span></span>
</dt> <dt>



<span data-ttu-id="09253-184">Verwenden Sie Secure Socket Layer, aktiviert HTTPS.</span><span class="sxs-lookup"><span data-stu-id="09253-184">Use Secure Socket Layer, enables HTTPS.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09253-185">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09253-185">Requirements</span></span>



| <span data-ttu-id="09253-186">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09253-186">Requirement</span></span> | <span data-ttu-id="09253-187">Wert</span><span class="sxs-lookup"><span data-stu-id="09253-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="09253-188">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="09253-188">Minimum supported client</span></span><br/> | <span data-ttu-id="09253-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="09253-189">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="09253-190">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="09253-190">Minimum supported server</span></span><br/> | <span data-ttu-id="09253-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09253-191">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="09253-192">Header</span><span class="sxs-lookup"><span data-stu-id="09253-192">Header</span></span><br/>                   | <dl> <span data-ttu-id="09253-193"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="09253-193"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="09253-194">IDL</span><span class="sxs-lookup"><span data-stu-id="09253-194">IDL</span></span><br/>                      | <dl> <span data-ttu-id="09253-195"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="09253-195"><dt>WSManDisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09253-196">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09253-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09253-197">Sitzungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="09253-197">Session Constants</span></span>](session-constants.md)
</dt> </dl>

 

 





