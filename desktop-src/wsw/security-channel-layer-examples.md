---
title: Beispiele für Sicherheits Kanal Ebenen
description: In den folgenden Beispielen wird die Sicherheit in der Kanal Ebene veranschaulicht.
ms.assetid: ac4f0275-4783-411d-98da-2c5a1a169dcc
keywords:
- Sicherheits Beispiele
- Sicherheits Beispiele, Setup
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1283339b1a4af624e118e3f6c76a07449f9274
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340224"
---
# <a name="security-channel-layer-examples"></a><span data-ttu-id="8ea25-107">Beispiele für Sicherheits Kanal Ebenen</span><span class="sxs-lookup"><span data-stu-id="8ea25-107">Security Channel Layer Examples</span></span>

<span data-ttu-id="8ea25-108">In den folgenden Beispielen wird die Sicherheit in der [Kanal Ebene](channel-layer-overview.md) veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="8ea25-108">The following examples illustrate security in the [Channel Layer](channel-layer-overview.md)</span></span>

<span data-ttu-id="8ea25-109">Windows-Transportsicherheit über TCP: Client: [requestreplytcpclientwithwindowstransportsecurityexample](requestreplytcpclientwithwindowstransportsecurityexample.md), Server: [requestreplytcpserverwithwindowstransportsecurityexample](requestreplytcpserverwithwindowstransportsecurityexample.md).</span><span class="sxs-lookup"><span data-stu-id="8ea25-109">Windows transport security over TCP: Client: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md), Server: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).</span></span>

<span data-ttu-id="8ea25-110">Windows-Transportsicherheit über Named Pipes: Client: [requestreplynamedpipesclientwithwindowstransportsecurityexample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), Server: [requestreplynamedpipesserverwithwindowstransportsecurityexample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).</span><span class="sxs-lookup"><span data-stu-id="8ea25-110">Windows transport security over named pipes: Client: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), Server: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).</span></span>

<span data-ttu-id="8ea25-111">SSL-Transportsicherheit: Client: [httpclientwithsslexample](httpclientwithsslexample.md), Server: [httpserverwithsslexample](httpserverwithsslexample.md).</span><span class="sxs-lookup"><span data-stu-id="8ea25-111">SSL transport security: Client: [HttpClientWithSslExample](httpclientwithsslexample.md), Server: [HttpServerWithSslExample](httpserverwithsslexample.md).</span></span>

<span data-ttu-id="8ea25-112">Benutzername über SSL-Sicherheit im gemischten Modus: Client: [httpclientwithusernameoversslexample](httpclientwithusernameoversslexample.md), Server: [httpserverwithusernameoversslexample](httpserverwithusernameoversslexample.md).</span><span class="sxs-lookup"><span data-stu-id="8ea25-112">Username over SSL mixed-mode security: Client: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md), Server: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md).</span></span>

<span data-ttu-id="8ea25-113">Benutzername über SSL-Sicherheit im gemischten Modus: Client: [httpclientwithkerberosoversslexample](httpclientwithkerberosoversslexample.md), Server: [httpserverwithkerberosoversslexample](httpserverwithkerberosoversslexample.md).</span><span class="sxs-lookup"><span data-stu-id="8ea25-113">Username over SSL mixed-mode security: Client: [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md), Server: [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md).</span></span>

<span data-ttu-id="8ea25-114">Benutzername über SSL-Sicherheit im gemischten Modus: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md).</span><span class="sxs-lookup"><span data-stu-id="8ea25-114">Username over SSL mixed-mode security: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md).</span></span> <span data-ttu-id="8ea25-115">Ausgestelltes Token über SSL-Sicherheit im gemischten Modus: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md).</span><span class="sxs-lookup"><span data-stu-id="8ea25-115">Issued token over SSL mixed-mode security: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md).</span></span> <span data-ttu-id="8ea25-116">X509-Zertifikat über SSL-Sicherheit im gemischten Modus: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).</span><span class="sxs-lookup"><span data-stu-id="8ea25-116">X509 certificate over SSL mixed-mode security: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).</span></span>

## <a name="one-time-setup-for-security-samples"></a><span data-ttu-id="8ea25-117">One-Time Setup für Sicherheits Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ea25-117">One-Time Setup for Security Samples</span></span>

<span data-ttu-id="8ea25-118">Zum Ausführen von wwsapi-Sicherheits Beispielen müssen Sie sowohl die Client-als auch die Server Zertifikate für SSL sowie ein lokales Benutzerkonto für die HTTP-Header Authentifizierung einrichten.</span><span class="sxs-lookup"><span data-stu-id="8ea25-118">To run WWSAPI security examples, you need to set up the client and server certificates for SSL, as well as a local user account for HTTP header authentication.</span></span> <span data-ttu-id="8ea25-119">Bevor Sie beginnen, benötigen Sie die folgenden Tools:</span><span class="sxs-lookup"><span data-stu-id="8ea25-119">Before you start, you need the following tools:</span></span>

-   <span data-ttu-id="8ea25-120">MakeCert.exe (verfügbar im Windows 7 SDK.)</span><span class="sxs-lookup"><span data-stu-id="8ea25-120">MakeCert.exe (Available in the Windows 7 SDK.)</span></span>
-   <span data-ttu-id="8ea25-121">CertUtil.exe oder CertMgr.exe (CertUtil.exe ist in den Windows sdert ab Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8ea25-121">CertUtil.exe or CertMgr.exe (CertUtil.exe is available in the Windows SDKs starting with Windows Server 2003.</span></span> <span data-ttu-id="8ea25-122">CertMgr.exe ist im Windows 7 SDK verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8ea25-122">CertMgr.exe is available in the Windows 7 SDK.</span></span> <span data-ttu-id="8ea25-123">Sie benötigen nur eines dieser Tools.)</span><span class="sxs-lookup"><span data-stu-id="8ea25-123">You only need one of these tools.)</span></span>
-   <span data-ttu-id="8ea25-124">HttpCfg.exe: (Dies ist nur erforderlich, wenn Sie Windows 2003 oder Windows XP verwenden.</span><span class="sxs-lookup"><span data-stu-id="8ea25-124">HttpCfg.exe: (You need this only if you are using Windows 2003 or Windows XP.</span></span> <span data-ttu-id="8ea25-125">Dieses Tool ist in den Windows XP SP2-Support Tools verfügbar und enthält auch die Windows Server 2003 Resource Kit-Tools-CD.)</span><span class="sxs-lookup"><span data-stu-id="8ea25-125">This tool is available in Windows XP SP2 Support Tools and also comes with the Windows Server 2003 Resource Kit Tools CD.)</span></span>

<span data-ttu-id="8ea25-126">Wenn Sie die wwsapi-Beispiele erhalten, indem Sie das Windows 7 SDK installieren, finden Sie die MakeCert.exe und CertMgr.exe unter% Program Files% \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ bin.</span><span class="sxs-lookup"><span data-stu-id="8ea25-126">If you get the WWSAPI examples by installing the Windows 7 SDK, you can find the MakeCert.exe and CertMgr.exe under %ProgramFiles%\\Microsoft SDKs\\Windows\\v7.0\\bin.</span></span>

<span data-ttu-id="8ea25-127">Führen Sie die folgende fünfstufige Einrichtung von der Eingabeaufforderung aus (erweitert, wenn Sie Windows Vista und höher verwenden):</span><span class="sxs-lookup"><span data-stu-id="8ea25-127">Perform the following five-step setup from the command prompt (elevated if you are using Windows Vista and above):</span></span>

1.  <span data-ttu-id="8ea25-128">Generieren eines selbst signierten Zertifikats als Zertifizierungsstelle (Certificate Authority, ca) oder Aussteller: **MakeCert.exe-SS root-SR LocalMachine-n "CN = Fake-Test-ca"-CY Authority-r-SK "cakeycontainer"**</span><span class="sxs-lookup"><span data-stu-id="8ea25-128">Generate a self-signed certificate to be the certificate authority (CA) or issuer: **MakeCert.exe -ss Root -sr LocalMachine -n "CN=Fake-Test-CA" -cy authority -r -sk "CAKeyContainer"**</span></span>
2.  <span data-ttu-id="8ea25-129">Generieren Sie ein Serverzertifikat mit dem vorherigen Zertifikat als Aussteller: **MakeCert.exe-SS My-SR LocalMachine-n "CN = localhost"-Sky Exchange-is root-IR LocalMachine-in Fake-Test-ca-SK "serverkeycontainer"**</span><span class="sxs-lookup"><span data-stu-id="8ea25-129">Generate a server certificate using the previous certificate as the issuer: **MakeCert.exe -ss My -sr LocalMachine -n "CN=localhost" -sky exchange -is Root -ir LocalMachine -in Fake-Test-CA -sk "ServerKeyContainer"**</span></span>
3.  <span data-ttu-id="8ea25-130">Suchen Sie den Fingerabdruck (ein SHA-1-Hash mit 40 Zeichen) des Serverzertifikats, indem Sie einen der folgenden Befehle ausführen und nach dem Zertifikat mit dem Namen "localhost" mit dem Aussteller "Fake-Test-ca" suchen:</span><span class="sxs-lookup"><span data-stu-id="8ea25-130">Find the thumbprint (a 40-character SHA-1 hash) of the server certificate by running either of the following commands and search for the certificate named localhost with issuer Fake-Test-CA:</span></span>
    -   <span data-ttu-id="8ea25-131">**"Localhost"CertUtil.exe speichern**</span><span class="sxs-lookup"><span data-stu-id="8ea25-131">**CertUtil.exe -store My localhost**</span></span>
    -   <span data-ttu-id="8ea25-132">**CertMgr.exe-s-r LocalMachine My**</span><span class="sxs-lookup"><span data-stu-id="8ea25-132">**CertMgr.exe -s -r LocalMachine My**</span></span>
4.  <span data-ttu-id="8ea25-133">Registrieren Sie den Fingerabdruck des Serverzertifikats? s ohne Leerzeichen HTTP.SYS:</span><span class="sxs-lookup"><span data-stu-id="8ea25-133">Register the server certificate?s thumbprint with no spaces with HTTP.SYS:</span></span>
    -   <span data-ttu-id="8ea25-134">Unter Windows Vista und höher (die "AppID"-Option ist eine beliebige GUID): **Netsh.exe http Add sslcert IPPort = 0.0.0.0:8443 AppID = {00112233-4455-6677-8899-aabbccddeeff}** CertHash =<40charakterithumbprint></span><span class="sxs-lookup"><span data-stu-id="8ea25-134">On Windows Vista and above (the "appid" option is an arbitrary GUID): **Netsh.exe http add sslcert ipport=0.0.0.0:8443 appid={00112233-4455-6677-8899-AABBCCDDEEFF}** certhash=<40CharacterThumbprint></span></span>
    -   <span data-ttu-id="8ea25-135">Unter Windows XP oder 2003: **HttpCfg.exe Set SSL-i 0.0.0.0:8443-h <40charakterithumbprint>**</span><span class="sxs-lookup"><span data-stu-id="8ea25-135">On Windows XP or 2003: **HttpCfg.exe set ssl -i 0.0.0.0:8443 -h <40CharacterThumbprint>**</span></span>
5.  <span data-ttu-id="8ea25-136">Erstellen Sie einen lokalen Benutzer: **net user "testuserforbasicauth" "TstPWD@ \* 4bsic"/Add**</span><span class="sxs-lookup"><span data-stu-id="8ea25-136">Create a local user: **Net user "TestUserForBasicAuth" "TstPWD@\*4Bsic" /add**</span></span>

<span data-ttu-id="8ea25-137">Führen Sie die folgenden Befehle aus, um die Zertifikate, die SSL-Zertifikat Bindung und das Benutzerkonto, die in den vorherigen Schritten erstellt wurden, zu bereinigen.</span><span class="sxs-lookup"><span data-stu-id="8ea25-137">To clean up the certificates, SSL certificate binding and the user account created in the previous steps, run the following commands.</span></span> <span data-ttu-id="8ea25-138">Hinweis Wenn mehrere Zertifikate mit demselben Namen vorhanden sind, müssen CertMgr.exe vor dem Löschen die Eingabe benötigen.</span><span class="sxs-lookup"><span data-stu-id="8ea25-138">Note if there are multiple certificates of the same name, CertMgr.exe will need your input before deleting them.</span></span>

-   <span data-ttu-id="8ea25-139">**CertMgr.exe-del-c-n Fake-Test-ca-s-r LocalMachine root**</span><span class="sxs-lookup"><span data-stu-id="8ea25-139">**CertMgr.exe -del -c -n Fake-Test-CA -s -r LocalMachine Root**</span></span>
-   <span data-ttu-id="8ea25-140">**CertMgr.exe-del-c-n localhost-s-r LocalMachine My**</span><span class="sxs-lookup"><span data-stu-id="8ea25-140">**CertMgr.exe -del -c -n localhost -s -r LocalMachine My**</span></span>
-   <span data-ttu-id="8ea25-141">**Netsh.exe HTTP DELETE sslcert IPPort = 0.0.0.0:8443 (oder HttpCfg.exe DELETE SSL-i 0.0.0.0:8443)**</span><span class="sxs-lookup"><span data-stu-id="8ea25-141">**Netsh.exe http delete sslcert ipport=0.0.0.0:8443 (or HttpCfg.exe delete ssl -i 0.0.0.0:8443)**</span></span>
-   <span data-ttu-id="8ea25-142">**NET User "testuserforbasicauth"/Delete**</span><span class="sxs-lookup"><span data-stu-id="8ea25-142">**Net user "TestUserForBasicAuth" /delete**</span></span>

<span data-ttu-id="8ea25-143">Stellen Sie sicher, dass nur ein Stamm Zertifikat mit dem Namen "Fake-Test-ca" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8ea25-143">Make sure there is only one root certificate named Fake-Test-CA.</span></span> <span data-ttu-id="8ea25-144">Wenn Sie sich nicht sicher sind, können Sie versuchen, diese Zertifikate mithilfe der oben aufgeführten Bereinigungs Befehle zu bereinigen (und Fehler ignorieren), bevor Sie die fünfstufige Einrichtung starten.</span><span class="sxs-lookup"><span data-stu-id="8ea25-144">If you are unsure, it?s always safe to try to clean up these certificates using the cleanup commands above (and ignore errors) before starting the five-step setup.</span></span>

 

 




