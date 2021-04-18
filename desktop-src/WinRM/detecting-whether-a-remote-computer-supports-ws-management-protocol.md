---
title: Erkennen, ob ein Remote Computer WS-Management Protokoll unterstützt
description: Sie können die Methoden Session. identifioder iwsmansession. identifiverwenden, um zu bestimmen, ob der Remote Computer über einen Dienst verfügt, der das WS-Management Protokoll unterstützt.
ms.assetid: 4d11ac02-fa8b-45d7-bceb-a18f561bc928
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af82284b38b2a101c767766d44eb975ff7e1dadc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338994"
---
# <a name="detecting-whether-a-remote-computer-supports-ws-management-protocol"></a><span data-ttu-id="9728b-103">Erkennen, ob ein Remote Computer WS-Management Protokoll unterstützt</span><span class="sxs-lookup"><span data-stu-id="9728b-103">Detecting Whether a Remote Computer Supports WS-Management Protocol</span></span>

<span data-ttu-id="9728b-104">Sie können die Methoden [**Session. identifioder**](session-identify.md) [**iwsmansession. identifiverwenden**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) , um zu bestimmen, ob der Remote Computer über einen Dienst verfügt, der das WS-Management Protokoll unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9728b-104">You can use the [**Session.Identify**](session-identify.md) or [**IWSManSession.Identify**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) methods to determine if the remote computer has a service that supports the WS-Management protocol.</span></span>

<span data-ttu-id="9728b-105">Wenn ein WS-Management Protokolldienst auf dem Remote Computer konfiguriert ist und auf Anforderungen lauscht, kann der Dienst eine Erkennungs Anforderung mit dem folgenden XML-Code in der Kopfzeile erkennen.</span><span class="sxs-lookup"><span data-stu-id="9728b-105">If a WS-Management protocol service is configured on the remote computer and is listening for requests, the service can detect an Identify request by the following XML in the header.</span></span>


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



<span data-ttu-id="9728b-106">Der WS-Management Protokolldienst, der die Anforderung empfängt, gibt die Informationen, die in der folgenden Liste enthalten sind, im Nachrichtentext zurück:</span><span class="sxs-lookup"><span data-stu-id="9728b-106">The WS-Management protocol service that receives the request returns the information, contained in the following list, in the body of the message:</span></span>

-   <span data-ttu-id="9728b-107">Die WS-Management Protokollversion.</span><span class="sxs-lookup"><span data-stu-id="9728b-107">The WS-Management protocol version.</span></span> <span data-ttu-id="9728b-108">Beispiel: „https://schemas.dmtf.org/wbem/wsman/1/wsman“.</span><span class="sxs-lookup"><span data-stu-id="9728b-108">For example, "https://schemas.dmtf.org/wbem/wsman/1/wsman".</span></span>
-   <span data-ttu-id="9728b-109">Der Produkthersteller, z. b. "Microsoft Corporation".</span><span class="sxs-lookup"><span data-stu-id="9728b-109">The product vendor, for example, "Microsoft Corporation".</span></span>
-   <span data-ttu-id="9728b-110">Die Produktversion.</span><span class="sxs-lookup"><span data-stu-id="9728b-110">The product version.</span></span> <span data-ttu-id="9728b-111">Wenn die Anforderung mit **wsmanflagusenoauthentication** im *Flags* -Parameter gesendet wird, werden keine Produkt Versionsinformationen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9728b-111">If the request is sent with **WSManFlagUseNoAuthentication** in the *flags* parameter, then no product version information is returned.</span></span> <span data-ttu-id="9728b-112">Wenn die Anforderung entweder mit der Standard Authentifizierung oder mit einem anderen angegebenen Authentifizierungsmodus gesendet wird, können die Produkt Versionsinformationen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9728b-112">If the request is sent with either the default authentication in effect or with another authentication mode specified, then the product version information can be returned.</span></span>

<span data-ttu-id="9728b-113">Die Anforderung, zu ermitteln, ob der Remote Computer über einen konfigurierten und lauschenden WS-Management Protokolldienst am Anfang eines Skripts mit anderen Vorgängen ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9728b-113">The request to detect whether the remote computer has a configured and listening WS-Management protocol service can be performed at the beginning of a script with other operations.</span></span> <span data-ttu-id="9728b-114">Dadurch wird überprüft, ob der Bereitstellungs Zielcomputer auf Weitere WS-Management Protokoll Anforderungen reagieren kann.</span><span class="sxs-lookup"><span data-stu-id="9728b-114">This will verify that the target computer or computers can respond to further WS-Management protocol requests.</span></span> <span data-ttu-id="9728b-115">Die Überprüfung kann auch in einem separaten Skript durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9728b-115">The verification also can be done in a separate script.</span></span>

<span data-ttu-id="9728b-116">**So erkennen Sie einen WS-Management Protokolldienst**</span><span class="sxs-lookup"><span data-stu-id="9728b-116">**To detect a WS-Management protocol service**</span></span>

1.  <span data-ttu-id="9728b-117">Erstellen Sie ein [**WSMAN**](wsman.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="9728b-117">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  <span data-ttu-id="9728b-118">Legen Sie fest, ob die Anforderung authentifiziert oder nicht authentifiziert gesendet werden soll, und legen Sie den *Flags* -Parameter entsprechend im [**WSMAN. kreatesession**](wsman-createsession.md)-aufrufen fest.</span><span class="sxs-lookup"><span data-stu-id="9728b-118">Determine whether the request should be sent authenticated or unauthenticated and set the *flags* parameter accordingly in the call to [**WSMan.CreateSession**](wsman-createsession.md).</span></span>

    ```VB
    set objSession = objWsman.CreateSession("Remote1", _
       objWsman.SessionFlagUseNoAuthentication)
    ```

    

3.  <span data-ttu-id="9728b-119">" [**Session. Identifi"**](session-identify.md)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="9728b-119">Call [**Session.Identify**](session-identify.md).</span></span>

    ```VB
    objSession.Identify
    ```

    

## <a name="examples"></a><span data-ttu-id="9728b-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9728b-120">Examples</span></span>

<span data-ttu-id="9728b-121">Das folgende VBScript-Codebeispiel sendet eine nicht authentifizierte Identifizierungs Anforderung an den Remote Computer mit dem Namen "remote1" in derselben Domäne.</span><span class="sxs-lookup"><span data-stu-id="9728b-121">The following VBScript code example sends an unauthenticated Identify request to the remote computer named "Remote1" in the same domain.</span></span>


```VB
set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession("Remote1", _
  objWsman.SessionFlagUseNoAuthentication)
WScript.Echo objSession.Identify
```



<span data-ttu-id="9728b-122">Die folgende Antwort zeigt den XML-Code, der vom Remote Computer zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="9728b-122">The following response shows the XML returned by the remote computer.</span></span> <span data-ttu-id="9728b-123">Die WS-Management-Protokollversion (" https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd ") und der Betriebssystemhersteller ("Microsoft Corporation") werden in der zurückgegebenen XML-Datei angegeben.</span><span class="sxs-lookup"><span data-stu-id="9728b-123">The WS-Management protocol version ("https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd") and the operating system vendor ("Microsoft Corporation") are specified in the returned XML.</span></span> <span data-ttu-id="9728b-124">Da die Nachricht nicht authentifiziert gesendet wird, wird die Produktversion nicht vom Windows-Remoteverwaltung-Dienst zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9728b-124">Because the message is sent unauthenticated, the product version is not returned by the Windows Remote Management service.</span></span>


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 0.0.0 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



<span data-ttu-id="9728b-125">Im folgenden VBScript-Codebeispiel wird eine authentifizierte Identifizierungs Anforderung an den Remote Computer gesendet.</span><span class="sxs-lookup"><span data-stu-id="9728b-125">The following VBScript code example sends an authenticated Identify request to the remote computer.</span></span>


```VB
set ObjWSMan = CreateObject("Wsman.Automation")
set objSession = WSMan.CreateSession("Remote1", _
  objWSMan.SessionFlagUseKerberos)
WScript.Echo objSession.Identify
```



<span data-ttu-id="9728b-126">Da die Anforderung mit der Authentifizierung gesendet wurde, werden die Versionsinformationen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9728b-126">Because the request was sent with authentication, the version information is returned.</span></span>


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 6.0.5384 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



## <a name="related-topics"></a><span data-ttu-id="9728b-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9728b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9728b-128">Informationen zu Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="9728b-128">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="9728b-129">Verwenden von Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="9728b-129">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="9728b-130">Windows-Remoteverwaltung Referenz</span><span class="sxs-lookup"><span data-stu-id="9728b-130">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 




