---
description: Stellt eine Verbindung mit dem Namespace auf dem Computer her, der im Parameter "strinserver" angegeben ist.
ms.assetid: 31364c68-b031-4cf0-851f-b4e302f077e0
ms.tgt_platform: multiple
title: Methode "Swap. ConnectServer" (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 31c2e6de8cf1504543727cad056a3616a51182d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369835"
---
# <a name="swbemlocatorconnectserver-method"></a><span data-ttu-id="a0ff7-103">Methode "Swap. ConnectServer"</span><span class="sxs-lookup"><span data-stu-id="a0ff7-103">SWbemLocator.ConnectServer method</span></span>

<span data-ttu-id="a0ff7-104">Die **ConnectServer** -Methode des Objekts " [**Swap-Locator**](swbemlocator.md) " stellt eine Verbindung mit dem Namespace auf dem Computer her, der im Parameter " *strinserver* " angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-104">The **ConnectServer** method of the [**SWbemLocator**](swbemlocator.md) object connects to the namespace on the computer that is specified in the *strServer* parameter.</span></span> <span data-ttu-id="a0ff7-105">Der Zielcomputer kann entweder lokal oder Remote sein, aber es muss WMI installiert sein.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-105">The target computer can be either local or remote, but it must have WMI installed.</span></span> <span data-ttu-id="a0ff7-106">Beispiele und einen Vergleich mit dem monikertyp Verbindung finden Sie unter [Erstellen eines WMI-Skripts](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="a0ff7-106">For examples and a comparison with the moniker type of connection, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span>

<span data-ttu-id="a0ff7-107">Ab Windows Vista kann der **Austausch von "taubemlocator. ConnectServer** " mit Computern, auf denen IPv6 ausgeführt wird, über eine IPv6-Adresse *im Parameter "* Parameter" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-107">Starting with Windows Vista, **SWbemLocator.ConnectServer** can connect with computers running IPv6 using an IPv6 address in the *strServer* parameter.</span></span> <span data-ttu-id="a0ff7-108">Weitere Informationen finden Sie [unter IPv6-und IPv4-Unterstützung in WMI](ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="a0ff7-108">For more information, see [IPv6 and IPv4 Support in WMI](ipv6-and-ipv4-support-in-wmi.md).</span></span>

<span data-ttu-id="a0ff7-109">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a0ff7-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a0ff7-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0ff7-110">Syntax</span></span>


```VB
objwbemServices = .ConnectServer( _
  [ ByVal strServer ], _
  [ ByVal strNamespace ], _
  [ ByVal strUser ], _
  [ ByVal strPassword ], _
  [ ByVal strLocale ], _
  [ ByVal strAuthority ], _
  [ ByVal iSecurityFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a0ff7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0ff7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0ff7-112">- *Server* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="a0ff7-112">*strServer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ff7-113">Der Name des Computers, mit dem Sie eine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-113">Computer name to which you are connecting.</span></span> <span data-ttu-id="a0ff7-114">Wenn sich der Remote Computer in einer anderen Domäne als das Benutzerkonto befindet, unter dem Sie sich anmelden, verwenden Sie den voll qualifizierten Computernamen.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-114">If the remote computer is in a different domain than the user account under which you log in, then use the fully qualified computer name.</span></span> <span data-ttu-id="a0ff7-115">Wenn Sie diesen Parameter nicht angeben, wird als Standardwert der lokale Computer verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-115">If you do not provide this parameter, the call defaults to the local computer.</span></span>

<span data-ttu-id="a0ff7-116">Ein Beispiel: `server1.network.fabrikam`</span><span class="sxs-lookup"><span data-stu-id="a0ff7-116">Example: `server1.network.fabrikam`</span></span>

<span data-ttu-id="a0ff7-117">Sie können auch eine IP-Adresse in diesem Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-117">You also can use an IP address in this parameter.</span></span> <span data-ttu-id="a0ff7-118">Wenn die IP-Adresse im IPv6-Format vorliegt, muss auf dem Bereitstellungs Zielcomputer IPv6 ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-118">If the IP address is in IPv6 format, the target computer must be running IPv6.</span></span> <span data-ttu-id="a0ff7-119">Eine Adresse in IPv4 sieht wie folgt aus. `123.123.123.123`</span><span class="sxs-lookup"><span data-stu-id="a0ff7-119">An address in IPv4 looks like `123.123.123.123`</span></span>

<span data-ttu-id="a0ff7-120">Eine IP-Adresse im IPv6-Format sieht wie folgt aus `2010:836B:4179::836B:4179`</span><span class="sxs-lookup"><span data-stu-id="a0ff7-120">An IP address in IPv6 format looks like `2010:836B:4179::836B:4179`</span></span>

<span data-ttu-id="a0ff7-121">Weitere Informationen zu DNS und IPv4 finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="a0ff7-121">For more information on DNS and IPv4, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="a0ff7-122">" *strinnamespace* \[ " in, optional\]</span><span class="sxs-lookup"><span data-stu-id="a0ff7-122">*strNamespace* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ff7-123">Eine Zeichenfolge, die den Namespace angibt, an dem Sie sich anmelden.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-123">String that specifies the namespace to which you log on.</span></span> <span data-ttu-id="a0ff7-124">Wenn Sie sich beispielsweise beim Stamm- \\ Standard Namespace anmelden möchten, verwenden Sie root \\ default.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-124">For example, to log on to the root\\default namespace, use root\\default.</span></span> <span data-ttu-id="a0ff7-125">Wenn Sie diesen Parameter nicht angeben, wird standardmäßig der Namespace verwendet, der als Standard Namespace für die Skripterstellung konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-125">If you do not specify this parameter, it defaults to the namespace that is configured as the default namespace for scripting.</span></span> <span data-ttu-id="a0ff7-126">Weitere Informationen finden Sie unter [Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="a0ff7-126">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

<span data-ttu-id="a0ff7-127">Beispiel: "root \\ CIMV2"</span><span class="sxs-lookup"><span data-stu-id="a0ff7-127">Example: "root\\CIMV2"</span></span>

</dd> <dt>

<span data-ttu-id="a0ff7-128">*strUser* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="a0ff7-128">*strUser* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ff7-129">Der zum Herstellen der Verbindung zu verwendende Benutzername.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-129">User name to use to connect.</span></span> <span data-ttu-id="a0ff7-130">Die Zeichenfolge kann entweder einen Benutzernamen oder einen Domänen \\ Benutzernamen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-130">The string can be in the form of either a user name or a Domain\\Username.</span></span> <span data-ttu-id="a0ff7-131">Lassen Sie diesen Parameter leer, um den aktuellen Sicherheitskontext zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-131">Leave this parameter blank to use the current security context.</span></span> <span data-ttu-id="a0ff7-132">Der *strUser* -Parameter sollte nur mit Verbindungen mit Remote-WMI-Servern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-132">The *strUser* parameter should only be used with connections to remote WMI servers.</span></span> <span data-ttu-id="a0ff7-133">Wenn Sie den *strUser* für eine lokale WMI-Verbindung angeben möchten, schlägt der Verbindungsversuch fehl.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-133">If you attempt to specify *strUser* for a local WMI connection, the connection attempt fails.</span></span> <span data-ttu-id="a0ff7-134">Wenn die Kerberos-Authentifizierung verwendet wird, können der Benutzername und das Kennwort, die in " *strUser* " und " *stranpassword* " angegeben sind, nicht in einem Netzwerk abgefangen werden.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-134">If Kerberos authentication is in use, then the username and password that is specified in *strUser* and *strPassword* cannot be intercepted on a network.</span></span> <span data-ttu-id="a0ff7-135">Sie können das UPN-Format verwenden, um den *strUser* anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-135">You can use the UPN format to specify the *strUser*.</span></span>

<span data-ttu-id="a0ff7-136">Beispiel: "Domainname \\ username"</span><span class="sxs-lookup"><span data-stu-id="a0ff7-136">Example: "DomainName\\UserName"</span></span>

> [!Note]  
> <span data-ttu-id="a0ff7-137">Wenn eine Domäne in " *stranauthority*" angegeben ist, darf die Domäne hier nicht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-137">If a domain is specified in *strAuthority*, then the domain must not be specified here.</span></span> <span data-ttu-id="a0ff7-138">Wenn Sie die Domäne in beiden Parametern angeben, führt dies zu einem ungültigen Parameter Fehler.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-138">Specifying the domain in both parameters results in an Invalid Parameter error.</span></span>

 

</dd> <dt>

<span data-ttu-id="a0ff7-139">*"Straume"* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="a0ff7-139">*strPassword* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ff7-140">Eine Zeichenfolge, die das Kennwort angibt, das beim Verbindungsversuch verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-140">String that specifies the password to use when attempting to connect.</span></span> <span data-ttu-id="a0ff7-141">Lassen Sie den-Parameter leer, um den aktuellen Sicherheitskontext zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-141">Leave the parameter blank to use the current security context.</span></span> <span data-ttu-id="a0ff7-142">Der Parameter " *straupassword* " sollte nur mit Verbindungen mit Remote-WMI-Servern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-142">The *strPassword* parameter should only be used with connections to remote WMI servers.</span></span> <span data-ttu-id="a0ff7-143">Wenn *Sie angeben,* dass für eine lokale WMI-Verbindung "für eine lokale WMI"-Verbindung festgelegt werden soll</span><span class="sxs-lookup"><span data-stu-id="a0ff7-143">If you attempt to specify *strPassword* for a local WMI connection, the connection attempt fails.</span></span> <span data-ttu-id="a0ff7-144">Wenn die Kerberos-Authentifizierung verwendet wird, können der Benutzername und das Kennwort, die in " *strUser* " und " *stranpassword* " angegeben sind, im Netzwerk nicht abgefangen werden.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-144">If Kerberos authentication is in use then the username and password that is specified in *strUser* and *strPassword* cannot be intercepted on the network.</span></span>

</dd> <dt>

<span data-ttu-id="a0ff7-145">*"Straume"* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="a0ff7-145">*strLocale* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ff7-146">Eine Zeichenfolge, die den Lokalisierungs Code angibt.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-146">String that specifies the localization code.</span></span> <span data-ttu-id="a0ff7-147">Wenn Sie das aktuelle Gebiets Schema verwenden möchten, lassen Sie es leer.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-147">If you want to use the current locale, leave it blank.</span></span> <span data-ttu-id="a0ff7-148">Wenn nicht leer, muss dieser Parameter eine Zeichenfolge sein, die das gewünschte Gebiets Schema angibt, in das Informationen abgerufen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-148">If not blank, this parameter must be a string that indicates the desired locale where information must be retrieved.</span></span> <span data-ttu-id="a0ff7-149">Für Microsoft-Gebiets Schema Bezeichner ist das Format der Zeichenfolge "MS \_ xxxx", wobei xxxx eine Zeichenfolge im Hexadezimal Format ist, die die LCID angibt.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-149">For Microsoft locale identifiers, the format of the string is "MS\_xxxx", where xxxx is a string in the hexadecimal form that indicates the LCID.</span></span> <span data-ttu-id="a0ff7-150">Beispielsweise würde American English als "MS \_ 409" angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-150">For example, American English would appear as "MS\_409".</span></span>

</dd> <dt>

<span data-ttu-id="a0ff7-151">- *Autorität* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="a0ff7-151">*strAuthority* \[in, optional\]</span></span>
</dt> <dd>

<dt>

<span data-ttu-id="a0ff7-152">""</span><span class="sxs-lookup"><span data-stu-id="a0ff7-152">""</span></span>
</dt> <dd>

<span data-ttu-id="a0ff7-153">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-153">This parameter is optional.</span></span> <span data-ttu-id="a0ff7-154">Wenn Sie jedoch angegeben ist, kann nur Kerberos oder ntlmdomain verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-154">However, if it is specified, only Kerberos or NTLMDomain can be used.</span></span>

</dd> <dt>

<span data-ttu-id="a0ff7-155">Kerberos</span><span class="sxs-lookup"><span data-stu-id="a0ff7-155">Kerberos:</span></span>
</dt> <dd>

<span data-ttu-id="a0ff7-156">Wenn der Parameter " *strauauthority* " mit der Zeichenfolge "Kerberos:" beginnt, wird die Kerberos-Authentifizierung verwendet, und dieser Parameter sollte einen Kerberos-Prinzipal Namen enthalten.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-156">If the *strAuthority* parameter begins with the string "Kerberos:", then Kerberos authentication is used and this parameter should contain a Kerberos principal name.</span></span> <span data-ttu-id="a0ff7-157">Der Kerberos-Prinzipal Name wird als Kerberos:*Domäne* angegeben, z `Kerberos:fabrikam` . b. Wenn `fabrikam` der Server ist, zu dem eine Verbindung hergestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-157">The Kerberos principal name is specified as Kerberos:*domain*, such as `Kerberos:fabrikam` where `fabrikam` is the server to which you are attempting to connect.</span></span>

<span data-ttu-id="a0ff7-158">Beispiel: "Kerberos: Domäne"</span><span class="sxs-lookup"><span data-stu-id="a0ff7-158">Example: "Kerberos:DOMAIN"</span></span>

</dd> <dt>

<span data-ttu-id="a0ff7-159">Quot ntlmdomain</span><span class="sxs-lookup"><span data-stu-id="a0ff7-159">NTLMDomain:</span></span>
</dt> <dd>

<span data-ttu-id="a0ff7-160">Um die NTLM-Authentifizierung (NT LAN Manager) verwenden zu können, müssen Sie diese als ntlmdomain:*Domain* angeben, z `NTLMDomain:fabrikam` . b `fabrikam` . wobei der Name der Domäne ist.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-160">To use NT Lan Manager (NTLM) authentication, you must specify it as NTLMDomain:*domain*, such as `NTLMDomain:fabrikam` where `fabrikam` is the name of the domain.</span></span>

<span data-ttu-id="a0ff7-161">Beispiel: "ntlmdomain: Domain"</span><span class="sxs-lookup"><span data-stu-id="a0ff7-161">Example: "NTLMDomain:DOMAIN"</span></span>

</dd> </dl>

<span data-ttu-id="a0ff7-162">Wenn Sie diesen Parameter leer lassen, verhandelt das Betriebssystem mit com, um zu bestimmen, ob die NTLM-oder Kerberos-Authentifizierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-162">If you leave this parameter blank, the operating system negotiates with COM to determine whether NTLM or Kerberos authentication is used.</span></span> <span data-ttu-id="a0ff7-163">Dieser Parameter sollte nur für Verbindungen mit Remote-WMI-Servern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-163">This parameter should only be used with connections to remote WMI servers.</span></span> <span data-ttu-id="a0ff7-164">Wenn Sie versuchen, die Autorität für eine lokale WMI-Verbindung festzulegen, schlägt der Verbindungsversuch fehl.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-164">If you attempt to set the authority for a local WMI connection, the connection attempt fails.</span></span>

> [!Note]  
> <span data-ttu-id="a0ff7-165">Wenn die Domäne in " *strUser*" angegeben ist, was der bevorzugte Speicherort ist, darf Sie hier nicht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-165">If the domain is specified in *strUser*, which is the preferred location, then it must not be specified here.</span></span> <span data-ttu-id="a0ff7-166">Wenn Sie die Domäne in beiden Parametern angeben, führt dies zu einem ungültigen Parameter Fehler.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-166">Specifying the domain in both parameters results in an Invalid Parameter error.</span></span>

 

</dd> <dt>

<span data-ttu-id="a0ff7-167">*isecurityflags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="a0ff7-167">*iSecurityFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ff7-168">Wird verwendet, um Flagwerte an **ConnectServer** zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-168">Used to pass flag values to **ConnectServer**.</span></span>

<dt>

<span data-ttu-id="a0ff7-169">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="a0ff7-169">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="a0ff7-170">Der Wert 0 für diesen Parameter bewirkt, dass der Connector **ConnectServer** erst nach dem Herstellen der Verbindung mit dem Server zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-170">A value of 0 for this parameter causes the call to **ConnectServer** to return only after the connection to the server is established.</span></span> <span data-ttu-id="a0ff7-171">Dies könnte dazu führen, dass das Programm nicht mehr unbegrenzt reagiert, wenn die Verbindung nicht hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-171">This could cause your program to stop responding indefinitely if the connection cannot be established.</span></span>

</dd> <dt>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>

<span data-ttu-id="a0ff7-172"><span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>wbemconnectflagusemaxwait \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="a0ff7-172"><span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>\*\*\*\*wbemConnectFlagUseMaxWait\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="a0ff7-173">Der **ConnectServer** -Rückruf wird garantiert in maximal 2 Minuten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-173">The **ConnectServer** call is guaranteed to return in 2 minutes or less.</span></span> <span data-ttu-id="a0ff7-174">Verwenden Sie dieses Flag, um zu verhindern, dass das Programm unbegrenzt reagiert, wenn die Verbindung nicht hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-174">Use this flag to prevent your program from ceasing to respond indefinitely if the connection cannot be established.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a0ff7-175">*objwbemnamedvalueset* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="a0ff7-175">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0ff7-176">Dies ist in der Regel nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-176">Typically, this is undefined.</span></span> <span data-ttu-id="a0ff7-177">Andernfalls handelt es sich hierbei um ein-Objekt vom [**typswap namedvalueset**](swbemnamedvalueset.md) , dessen Elemente die Kontextinformationen darstellen, die von dem Anbieter verwendet werden können, der die Anforderung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-177">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="a0ff7-178">Ein Anbieter, der solche Informationen unterstützt oder erfordert, muss die erkannten Wertnamen, den Datentyp des Werts, zulässige Werte und die Semantik dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-178">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0ff7-179">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0ff7-179">Return value</span></span>

<span data-ttu-id="a0ff7-180">Bei erfolgreicher Ausführung gibt WMI ein-Objekt zurück, [**das an den**](swbemservices.md) Namespace gebunden ist, der auf dem in " *strinserver*" angegebenen Computer in " *strinnamespace* " angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-180">If successful, WMI returns an [**SWbemServices**](swbemservices.md) object that is bound to the namespace that is specified in *strNamespace* on the computer that is specified in *strServer*.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a0ff7-181">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a0ff7-181">Error codes</span></span>

<span data-ttu-id="a0ff7-182">Nach dem Abschluss der **ConnectServer** -Methode kann das [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-182">After the completion of the **ConnectServer** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="a0ff7-183">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="a0ff7-183">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="a0ff7-184">Der aktuelle oder der angegebene Benutzername und das Kennwort waren ungültig oder zum Herstellen der Verbindung autorisiert.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-184">The current or specified user name and password were not valid or authorized to make the connection.</span></span>

</dd> <dt>

<span data-ttu-id="a0ff7-185">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="a0ff7-185">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="a0ff7-186">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-186">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="a0ff7-187">**wbemErrInvalidNamespace** -2147749902 (0x8004100e)</span><span class="sxs-lookup"><span data-stu-id="a0ff7-187">**wbemErrInvalidNamespace** - 2147749902 (0x8004100E)</span></span>
</dt> <dd>

<span data-ttu-id="a0ff7-188">Der angegebene Namespace war auf dem Server nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-188">The specified namespace did not exist on the server.</span></span>

</dd> <dt>

<span data-ttu-id="a0ff7-189">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="a0ff7-189">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="a0ff7-190">Es wurde ein ungültiger Parameter angegeben, oder der Namespace konnte nicht analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-190">An invalid parameter was specified, or the namespace could not be parsed.</span></span>

</dd> <dt>

<span data-ttu-id="a0ff7-191">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="a0ff7-191">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="a0ff7-192">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-192">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="a0ff7-193">**wbemErrTransportFailure** -2147749909</span><span class="sxs-lookup"><span data-stu-id="a0ff7-193">**wbemErrTransportFailure** - 2147749909</span></span>
</dt> <dd>

<span data-ttu-id="a0ff7-194">Netzwerkfehler. der normale Betrieb wird verhindert.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-194">A networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a0ff7-195">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0ff7-195">Remarks</span></span>

<span data-ttu-id="a0ff7-196">Die **ConnectServer** -Methode wird häufig verwendet, wenn eine Verbindung mit einem Konto mit einem anderen Benutzernamen und Kenn Wort Anmelde Informationen auf einem Remote Computer hergestellt wird, da Sie kein anderes Kennwort in einer [Monikerzeichenfolge](constructing-a-moniker-string.md) angeben können.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-196">The **ConnectServer** method is often used when connecting to an account with a different username and password credentials on a remote computer because you cannot specify a different password in a [moniker](constructing-a-moniker-string.md) string.</span></span> <span data-ttu-id="a0ff7-197">Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="a0ff7-197">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="a0ff7-198">Das Verwenden einer IPv4-Adresse für die Verbindung mit einem Remote Server kann zu unerwartetem Verhalten führen.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-198">Using an IPv4 address to connect to a remote server may result in unexpected behavior.</span></span> <span data-ttu-id="a0ff7-199">Die wahrscheinlichste Ursache ist ein veralteter DNS-Eintrag in Ihrer Umgebung.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-199">The likely cause is stale DNS entries in your environment.</span></span> <span data-ttu-id="a0ff7-200">In diesen Fällen wird der veraltete PTR-Eintrag für den Computer mit unvorhersehbaren Ergebnissen verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-200">In these circumstances, the stale PTR entry for the machine will be used, with unpredictable results.</span></span> <span data-ttu-id="a0ff7-201">Um dieses Verhalten zu vermeiden, können Sie vor dem Aufrufen von ConnectServer einen Punkt (".") an die IP-Adresse anfügen.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-201">To avoid this behavior, you can append a period (".") to the IP address before calling ConnectServer.</span></span> <span data-ttu-id="a0ff7-202">Dies bewirkt, dass bei der Reverse-DNS-Suche ein Fehler auftritt, der **Verbindungs Server** jedoch möglicherweise auf dem richtigen Computer erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-202">This causes the reverse DNS lookup to fail, but may allow the **ConnectServer** call to succeed on the correct machine.</span></span>

## <a name="examples"></a><span data-ttu-id="a0ff7-203">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0ff7-203">Examples</span></span>

<span data-ttu-id="a0ff7-204">Im folgenden VBScript-Codebeispiel wird beschrieben, wie Sie eine Verbindung mit einem Remote Computer herstellen, um [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) -Daten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-204">The following VBScript code example describes how to connect to a remote computer to obtain [**Win32\_IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) data.</span></span> <span data-ttu-id="a0ff7-205">Der in " *straudomain* " angegebene Domänen Name wird in "Erstelle" *verwendet.*</span><span class="sxs-lookup"><span data-stu-id="a0ff7-205">The domain name that is specified in *strDomain* is used in *strAuthority*.</span></span>


```VB
Const intMin = 3600
strComputer = "RemoteComputer" 
strDomain = "DomainName"  
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
Wscript.Echo

Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator") 
Set objWMIService = objSWbemLocator.ConnectServer(strComputer, _ 
                                                  "root\CIMV2", _ 
                                                  strUser, _ 
                                                  strPassword, _ 
                                                  "MS_409", _ 
                                                  "NTLMDomain:" + strDomain) 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_IP4RouteTable",,48) 
For Each objItem in colItems
    WScript.Echo "Age in Minutes: " & int(objItem.Age/intMin) & VBNewLine _
               & "Description:    " & objItem.Description & VBNewLine _
               & "Destination:    " & objItem.Destination & VBNewLine _
               & "InterfaceIndex: " & objItem.InterfaceIndex & VBNewLine _
               & "Mask:           " & objItem.Mask & VBNewLine _
               & "Metric1:        " & objItem.Metric1 & VBNewLine _
               & "Metric2:        " & objItem.Metric2 & VBNewLine _
               & "Metric3:        " & objItem.Metric3 & VBNewLine _
               & "Metric4:        " & objItem.Metric4 & VBNewLine _
               & "Metric5:        " & objItem.Metric5 & VBNewLine _
               & "Name:           " & objItem.Name & VBNewLine _
               & "NextHop:        " & objItem.NextHop & VBNewLine _
               & "Protocol:       " & objItem.Protocol & VBNewLine _
               & "Type: " & objItem.Type
    WScript.Echo
   </example>
Next
```



<span data-ttu-id="a0ff7-206">Der folgende PowerShell-Code Ausschnitt greift auf einen Remote Server zu und listet die verfügbaren WMI-Klassen auf.</span><span class="sxs-lookup"><span data-stu-id="a0ff7-206">The following PowerShell snippet access a remote server and lists the available WMI classes.</span></span>


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a><span data-ttu-id="a0ff7-207">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0ff7-207">Requirements</span></span>



| <span data-ttu-id="a0ff7-208">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0ff7-208">Requirement</span></span> | <span data-ttu-id="a0ff7-209">Wert</span><span class="sxs-lookup"><span data-stu-id="a0ff7-209">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ff7-210">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a0ff7-210">Minimum supported client</span></span><br/> | <span data-ttu-id="a0ff7-211">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0ff7-211">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a0ff7-212">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a0ff7-212">Minimum supported server</span></span><br/> | <span data-ttu-id="a0ff7-213">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0ff7-213">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a0ff7-214">Header</span><span class="sxs-lookup"><span data-stu-id="a0ff7-214">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0ff7-215"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0ff7-215"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a0ff7-216">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a0ff7-216">Type library</span></span><br/>             | <dl> <span data-ttu-id="a0ff7-217"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a0ff7-217"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a0ff7-218">DLL</span><span class="sxs-lookup"><span data-stu-id="a0ff7-218">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0ff7-219"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0ff7-219"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a0ff7-220">CLSID</span><span class="sxs-lookup"><span data-stu-id="a0ff7-220">CLSID</span></span><br/>                    | <span data-ttu-id="a0ff7-221">CLSID- \_ Austausch</span><span class="sxs-lookup"><span data-stu-id="a0ff7-221">CLSID\_SWbemLocator</span></span><br/>                                                          |
| <span data-ttu-id="a0ff7-222">IID</span><span class="sxs-lookup"><span data-stu-id="a0ff7-222">IID</span></span><br/>                      | <span data-ttu-id="a0ff7-223">IID \_ iswbemlocator</span><span class="sxs-lookup"><span data-stu-id="a0ff7-223">IID\_ISWbemLocator</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="a0ff7-224">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0ff7-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0ff7-225">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="a0ff7-225">**SWbemLocator**</span></span>](swbemlocator.md)
</dt> <dt>

[<span data-ttu-id="a0ff7-226">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="a0ff7-226">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="a0ff7-227">Herstellen einer Verbindung mit WMI auf einem Remote Computer</span><span class="sxs-lookup"><span data-stu-id="a0ff7-227">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="a0ff7-228">Erstellen eines WMI-Skripts</span><span class="sxs-lookup"><span data-stu-id="a0ff7-228">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
</dt> </dl>

 

