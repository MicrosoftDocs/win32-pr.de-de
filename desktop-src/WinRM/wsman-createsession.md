---
title: WSMAN. kreatesession-Methode (WSManDisp. h)
description: Erstellt ein Sitzungs Objekt, das dann für nachfolgende Netzwerk Vorgänge verwendet werden kann.
ms.assetid: 299d9a95-bd30-414c-996d-6633e8b7ce52
ms.tgt_platform: multiple
keywords:
- Windows-Remoteverwaltung der Methode "kreatesession"
- Die Methode "kreatesession" Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, Methode "kreatesession"
topic_type:
- apiref
api_name:
- WSMan.CreateSession
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 966fd1f43db7114d3a4c0cf4cddaa4428fcb41c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518143"
---
# <a name="wsmancreatesession-method"></a><span data-ttu-id="c0b68-106">WSMAN. kreatesession-Methode</span><span class="sxs-lookup"><span data-stu-id="c0b68-106">WSMan.CreateSession method</span></span>

<span data-ttu-id="c0b68-107">Erstellt ein [**Sitzungs**](session.md) Objekt, das dann für nachfolgende Netzwerk Vorgänge verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c0b68-107">Creates a [**Session**](session.md) object that can then be used for subsequent network operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0b68-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0b68-108">Syntax</span></span>


```VB
WSMan.CreateSession( _
  [ ByVal connection ], _
  [ ByVal flags ], _
  [ ByVal connectionOptions ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c0b68-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0b68-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0b68-110">*Verbindung* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c0b68-110">*connection* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c0b68-111">Das Protokoll und der Dienst, mit denen eine Verbindung hergestellt werden soll, einschließlich IPv4 oder IPv6.</span><span class="sxs-lookup"><span data-stu-id="c0b68-111">The protocol and service to connect to, including either IPv4 or IPv6.</span></span> <span data-ttu-id="c0b68-112">Das Format der Verbindungsinformationen lautet wie folgt: <*Transport* >< *Adress* >< *Suffix*>.</span><span class="sxs-lookup"><span data-stu-id="c0b68-112">The format of the connection information is as follows: <*Transport*><*Address*><*Suffix*>.</span></span> <span data-ttu-id="c0b68-113">Beispiele finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="c0b68-113">For examples, see Remarks.</span></span> <span data-ttu-id="c0b68-114">Wenn keine Verbindungsinformationen bereitgestellt werden, wird der lokale Computer verwendet.</span><span class="sxs-lookup"><span data-stu-id="c0b68-114">If no connection information is provided, the local computer is used.</span></span>

</dd> <dt>

<span data-ttu-id="c0b68-115">*Flags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c0b68-115">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c0b68-116">Die Sitzungsflags, die die Authentifizierungsmethode angeben, z. b. [*Aushandlung der Authentifizierung*](windows-remote-management-glossary.md) oder [*Digestauthentifizierung*](windows-remote-management-glossary.md)zum Herstellen einer Verbindung mit einem Remote Computer.</span><span class="sxs-lookup"><span data-stu-id="c0b68-116">The session flags that specify the authentication method, such as [*Negotiate authentication*](windows-remote-management-glossary.md) or [*Digest authentication*](windows-remote-management-glossary.md), for connecting to a remote computer.</span></span> <span data-ttu-id="c0b68-117">Diese Flags geben auch andere Sitzungs Verbindungsinformationen an, z. b. Codierung oder Verschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="c0b68-117">These flags also specify other session connection information, such as encoding or encryption.</span></span> <span data-ttu-id="c0b68-118">Dieser Parameter muss mindestens eines der Flags in **\_ \_ wsmansessionflags** für eine Remote Verbindung enthalten.</span><span class="sxs-lookup"><span data-stu-id="c0b68-118">This parameter must contain one or more of the flags in **\_\_WSManSessionFlags** for a remote connection.</span></span> <span data-ttu-id="c0b68-119">Weitere Informationen finden Sie unter [Sitzungs Konstanten](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c0b68-119">For more information, see [Session Constants](session-constants.md).</span></span> <span data-ttu-id="c0b68-120">Für eine Verbindung mit WinRM auf dem lokalen Computer sind keine Flag-Einstellungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c0b68-120">No flag settings are required for a connection to WinRM on the local computer.</span></span> <span data-ttu-id="c0b68-121">Der Standardwert ist " **wsmanflagusenegotiate**".</span><span class="sxs-lookup"><span data-stu-id="c0b68-121">The default is **WSManFlagUseNegotiate**.</span></span>

<span data-ttu-id="c0b68-122">Weitere Informationen finden Sie unter [Authentifizierung für Remote Verbindungen](authentication-for-remote-connections.md) und *ConnectionOptions* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="c0b68-122">For more information, see [Authentication for Remote Connections](authentication-for-remote-connections.md) and the *connectionOptions* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c0b68-123">*ConnectionOptions* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c0b68-123">*connectionOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c0b68-124">Ein Zeiger auf ein [**ConnectionOptions**](connectionoptions.md) -Objekt, das einen Benutzernamen und ein Kennwort enthält.</span><span class="sxs-lookup"><span data-stu-id="c0b68-124">A pointer to a [**ConnectionOptions**](connectionoptions.md) object that contains a user name and password.</span></span> <span data-ttu-id="c0b68-125">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="c0b68-125">The default is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0b68-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0b68-126">Return value</span></span>

<span data-ttu-id="c0b68-127">Ein [**Sitzungs**](session.md) Objekt, das dann zum Ausführen von lokalen oder Remote-WinRM-Vorgängen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c0b68-127">A [**Session**](session.md) object that can then be used to perform local or remote WinRM operations.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0b68-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0b68-128">Remarks</span></span>

<span data-ttu-id="c0b68-129">Die Methode " **kreatesession** " initialisiert das [**Sitzungs**](session.md) Objekt, indem Parameter, wie z. b. Flags, Anmelde Informationen und eine Verbindungs Zeichenfolge für den *Verbindungs* Parameter, gesammelt werden.</span><span class="sxs-lookup"><span data-stu-id="c0b68-129">The **CreateSession** method initializes the [**Session**](session.md) object by gathering parameters, such as flags, credentials, and a connection string for the *connection* parameter.</span></span> <span data-ttu-id="c0b68-130">" **Anatesession** " stellt keine Verbindung mit dem lokalen Computer oder dem Remote Computer her.</span><span class="sxs-lookup"><span data-stu-id="c0b68-130">**CreateSession** does not actually connect to the local or remote computer.</span></span> <span data-ttu-id="c0b68-131">Wenn die Verbindung nicht hergestellt werden kann, tritt beim ersten **Sitzungs** Vorgang (z. b. [**Get**](session-get.md) oder [**Enumerate**](session-enumerate.md)) nach dem Aufrufen von " **anatesession**" ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="c0b68-131">If the connection cannot be established, a failure occurs on the first **Session** operation, such as a [**Get**](session-get.md) or [**Enumerate**](session-enumerate.md), after the call to **CreateSession**.</span></span> <span data-ttu-id="c0b68-132">Dieses Verhalten unterscheidet sich von einer [*WMI*](windows-remote-management-glossary.md) -Verbindung mit einem [*Namespace*](windows-remote-management-glossary.md) auf einem Remote Computer.</span><span class="sxs-lookup"><span data-stu-id="c0b68-132">This behavior differs from a [*WMI*](windows-remote-management-glossary.md) connection to a [*namespace*](windows-remote-management-glossary.md) on a remote computer.</span></span> <span data-ttu-id="c0b68-133">Weitere Informationen finden Sie unter [Windows-Remoteverwaltung und WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="c0b68-133">For more information, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="c0b68-134">Das folgende VBScript-Codebeispiel wird verwendet, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c0b68-134">The following VBScript code example is used to call this method.</span></span>


```VB
Set session = _
    wsman.CreateSession("<Transport><Address><Suffix>")
```



<span data-ttu-id="c0b68-135">In den folgenden Beispielen werden die unterschiedlichen Formate zum Angeben von Verbindungsinformationen im *Verbindungs* Parameter veranschaulicht (beim Erstellen einer HTTPS-Sitzung muss das Feld <*Adresse*> mit dem Namen des Server Computer Zertifikats identisch sein, andernfalls tritt ein Fehler auf):</span><span class="sxs-lookup"><span data-stu-id="c0b68-135">The following examples show the different formats used to specify connection information in the *connection* parameter (when creating an HTTPS session, the <*Address*> field must match the server computer certificate name, otherwise a failure occurs):</span></span>

-   <span data-ttu-id="c0b68-136">"https://service"</span><span class="sxs-lookup"><span data-stu-id="c0b68-136">"https://service"</span></span>

    <span data-ttu-id="c0b68-137">Verwendet HTTPS zum Herstellen der Verbindung mit dem Standardweb Dienst-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="c0b68-137">Uses HTTPS to connect to the default web service location.</span></span>

-   <span data-ttu-id="c0b68-138">"https://service.corp.com/websvcs/wsman"</span><span class="sxs-lookup"><span data-stu-id="c0b68-138">"https://service.corp.com/websvcs/wsman"</span></span>

    <span data-ttu-id="c0b68-139">Verwendet HTTPS zum Herstellen der Verbindung mit dem spezifischen Webdienst Speicherort.</span><span class="sxs-lookup"><span data-stu-id="c0b68-139">Uses HTTPS to connect to the specific web service location.</span></span>

-   <span data-ttu-id="c0b68-140">"https:// \[ E3D7:0000:0000:0000:51F 4:9bc8: c0a8:6420 \] "</span><span class="sxs-lookup"><span data-stu-id="c0b68-140">"https://\[E3D7:0000:0000:0000:51F4:9BC8:C0A8:6420\]"</span></span>

    <span data-ttu-id="c0b68-141">Verwendet HTTPS und IPv6 mit dem Standardport.</span><span class="sxs-lookup"><span data-stu-id="c0b68-141">Uses HTTPS and IPv6 with the default port.</span></span>

-   <span data-ttu-id="c0b68-142">"https:// \[ E3D7:0000:0000:0000:51F 4:9bc8: c0a8:6420 \] : 9999/WSMAN"</span><span class="sxs-lookup"><span data-stu-id="c0b68-142">"https://\[E3D7:0000:0000:0000:51F4:9BC8:C0A8:6420\]:9999/wsman"</span></span>

    <span data-ttu-id="c0b68-143">Verwendet HTTPS und IPv6 mit dem angegebenen Port.</span><span class="sxs-lookup"><span data-stu-id="c0b68-143">Uses HTTPS and IPv6 with the given port.</span></span>

## <a name="examples"></a><span data-ttu-id="c0b68-144">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0b68-144">Examples</span></span>

<span data-ttu-id="c0b68-145">Im folgenden VBScript-Codebeispiel wird eine Sitzung auf dem lokalen Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="c0b68-145">The following VBScript code example creates a session on the local computer.</span></span>


```VB
 Set NewSession = Wsman.CreateSession   
   
```



<span data-ttu-id="c0b68-146">Im folgenden VBScript-Codebeispiel wird eine Sitzung auf einem Remote Computer erstellt, der durch eine IP-Adresse identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="c0b68-146">The following VBScript code example creates a session on a remote computer that is identified by an IP address.</span></span> <span data-ttu-id="c0b68-147">Das Skript stellt einen Benutzernamen und ein Kennwort für ein Konto bereit.</span><span class="sxs-lookup"><span data-stu-id="c0b68-147">The script supplies a user name and password for an account.</span></span> <span data-ttu-id="c0b68-148">Die Flags **wsmanflagkredusernamepassword** und **wsmanflagusebasic** werden kombiniert, um anzugeben, dass es sich bei dem Konto um ein lokales Konto auf dem Remote Computer handelt.</span><span class="sxs-lookup"><span data-stu-id="c0b68-148">The flags **WSManFlagCredUserNamePassword** and **WSManFlagUseBasic** are combined to indicate that the account is a local account on the remote computer.</span></span> <span data-ttu-id="c0b68-149">Wenn die Erstellung der Sitzung fehlschlägt, wird das Skript beendet.</span><span class="sxs-lookup"><span data-stu-id="c0b68-149">If the creation of the session fails, the script terminates.</span></span> <span data-ttu-id="c0b68-150">Das Skript verwendet die Methoden, die die Konstante zurückgeben, z. b. [**WSMAN. sessionflagusebasic**](wsman-sessionflagusebasic.md).</span><span class="sxs-lookup"><span data-stu-id="c0b68-150">The script uses the methods that return the constant, such as [**WSMan.SessionFlagUseBasic**](wsman-sessionflagusebasic.md).</span></span>

<span data-ttu-id="c0b68-151">Beachten Sie beim Ausführen dieses Skripts, dass Sie die Standard Konfigurationseinstellungen für Client und Server so konfigurieren müssen, dass unverschlüsselter Datenverkehr und die Standard Authentifizierung zulässig sind ("'" auf **true** und "Basic" auf " **true\*\*\*\*" festgelegt** ist).</span><span class="sxs-lookup"><span data-stu-id="c0b68-151">To run this script, be aware that you must configure the default configuration settings for both client and server to allow unencrypted traffic and Basic authentication (**AllowUnencrypted** set to **True** and Basic set to **True**).</span></span> <span data-ttu-id="c0b68-152">Weitere Informationen finden Sie unter [Installation und Konfiguration für Windows-Remoteverwaltung](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="c0b68-152">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>


```VB
iFlags = WSMan.SessionFlagUseBasic Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



<span data-ttu-id="c0b68-153">Im folgenden VBScript-Codebeispiel handelt es sich bei dem Konto um ein Domänen Konto, und Aushandlungs Authentifizierung wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="c0b68-153">In the following VBScript code example, the account is a domain account and Negotiate authentication is used.</span></span> <span data-ttu-id="c0b68-154">Bei der Aushandlung der Authentifizierung müssen Sie den Benutzernamen als `computername\username` oder angeben `ipaddress\username` .</span><span class="sxs-lookup"><span data-stu-id="c0b68-154">With Negotiate authentication, you must specify the user name as `computername\username` or `ipaddress\username`.</span></span>


```VB
iFlags = WSMan.SessionFlagUseNegotiate Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyComputer\MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



## <a name="requirements"></a><span data-ttu-id="c0b68-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0b68-155">Requirements</span></span>



| <span data-ttu-id="c0b68-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0b68-156">Requirement</span></span> | <span data-ttu-id="c0b68-157">Wert</span><span class="sxs-lookup"><span data-stu-id="c0b68-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0b68-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0b68-158">Minimum supported client</span></span><br/> | <span data-ttu-id="c0b68-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0b68-159">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="c0b68-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0b68-160">Minimum supported server</span></span><br/> | <span data-ttu-id="c0b68-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0b68-161">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c0b68-162">Header</span><span class="sxs-lookup"><span data-stu-id="c0b68-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0b68-163"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0b68-163"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0b68-164">IDL</span><span class="sxs-lookup"><span data-stu-id="c0b68-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c0b68-165"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c0b68-165"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="c0b68-166">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c0b68-166">Library</span></span><br/>                  | <dl> <span data-ttu-id="c0b68-167"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c0b68-167"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c0b68-168">DLL</span><span class="sxs-lookup"><span data-stu-id="c0b68-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0b68-169"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0b68-169"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c0b68-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0b68-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0b68-171">**WSMAN**</span><span class="sxs-lookup"><span data-stu-id="c0b68-171">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="c0b68-172">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="c0b68-172">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> <dt>

[<span data-ttu-id="c0b68-173">**Sitzung**</span><span class="sxs-lookup"><span data-stu-id="c0b68-173">**Session**</span></span>](session.md)
</dt> <dt>

[<span data-ttu-id="c0b68-174">Authentifizierung für Remote Verbindungen</span><span class="sxs-lookup"><span data-stu-id="c0b68-174">Authentication for Remote Connections</span></span>](authentication-for-remote-connections.md)
</dt> <dt>

[<span data-ttu-id="c0b68-175">Installation und Konfiguration für Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="c0b68-175">Installation and Configuration for Windows Remote Management</span></span>](installation-and-configuration-for-windows-remote-management.md)
</dt> </dl>

 

 





