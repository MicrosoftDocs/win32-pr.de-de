---
title: Authentifizierung (Windows Media-Format 11 SDK)
description: Authentifizierung
ms.assetid: 9c181615-e864-4588-846f-d04d73824f5f
keywords:
- SDK für Windows Media-Format, Authentifizierung
- Windows Media-Format-SDK, Netzwerk Authentifizierung
- Advanced Systems Format (ASF), Authentifizierung
- ASF (Advanced Systems Format), Authentifizierung
- Advanced Systems Format (ASF), Netzwerk Authentifizierung
- ASF (Advanced Systems Format), Netzwerk Authentifizierung
- authentication
- Netzwerk Authentifizierung, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf815881ac7beb354fffbfdb9b5475d040e9e83
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106338516"
---
# <a name="authentication-windows-media-format-11-sdk"></a><span data-ttu-id="c9fd8-111">Authentifizierung (Windows Media-Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="c9fd8-111">Authentication (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="c9fd8-112">Das Reader-Objekt kann Probleme mit der Netzwerk Authentifizierung behandeln, einschließlich Digestauthentifizierung und NTLM-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-112">The reader object can handle network authentication challenges, including digest authentication and NTLM authentication.</span></span> <span data-ttu-id="c9fd8-113">In einigen Fällen muss die Anwendung die Anmelde Informationen des Benutzers über eine Rückruf Schnittstelle bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="c9fd8-113">In some cases the application must provide the user's credentials through a callback interface:</span></span>

-   <span data-ttu-id="c9fd8-114">Digestauthentifizierung: die Anwendung muss die **iwmkredentialcallback** -Schnittstelle implementieren, wie weiter unten in diesem Thema beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-114">Digest authentication: The application must implement the **IWMCredentialCallback** interface, as described later in this topic.</span></span>
-   <span data-ttu-id="c9fd8-115">NTLM-Authentifizierung: der Reader antwortet automatisch mit den Anmelde Informationen des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-115">NTLM authentication: The reader automatically responds with the user's logon credentials.</span></span> <span data-ttu-id="c9fd8-116">Wenn der aktuelle Benutzer für die Anmeldung am Server autorisiert ist, muss die Anwendung nichts Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-116">If the current user is authorized to log on to the server, the application does not have to do anything.</span></span> <span data-ttu-id="c9fd8-117">Wenn der Benutzer keine Autorisierung hat, muss die Anwendung die **iwmkredentialcallback** -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-117">If the user does not have authorization, the application must implement the **IWMCredentialCallback** interface.</span></span>

    > [!Note]  
    > <span data-ttu-id="c9fd8-118">Windows Media Services Version 4,1 unterstützt die NTLM-Authentifizierung nicht über einen Proxy Server.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-118">Windows Media Services version 4.1 does not support NTLM authentication through a proxy server.</span></span> <span data-ttu-id="c9fd8-119">Die NTLM-Authentifizierung erfordert mehrere Client/Server-Austausch Vorgänge auf derselben Verbindung, und Version 4,1 behält keine permanente Verbindung mit dem Proxy bei.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-119">NTLM authentication requires several client-server exchanges on the same connection, and version 4.1 does not keep a persistent connection with the proxy.</span></span> <span data-ttu-id="c9fd8-120">Die Windows Media Services 9-Reihe in Microsoft Windows Server 2003 unterstützt die NTLM-Authentifizierung über einen Proxy Server, solange der Proxy Keep-Alive-Verbindungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-120">Windows Media Services 9 Series in Microsoft Windows Server 2003 supports NTLM authentication through a proxy server, as long as the proxy supports keep-alive connections.</span></span>

     

<span data-ttu-id="c9fd8-121">Wie bereits erwähnt, muss die Anwendung in einigen Fällen die Anmelde Informationen des Benutzers bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-121">As noted, in some cases the application must provide the user's credentials.</span></span> <span data-ttu-id="c9fd8-122">Dies erfolgt über die **iwmkredentialcallback** -Schnittstelle, die über eine einzige Methode ( **acquirecredenseins**) verfügt.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-122">This occurs through the **IWMCredentialCallback** interface, which has a single method, **AcquireCredentials**.</span></span> <span data-ttu-id="c9fd8-123">Implementieren Sie diese Schnittstelle in der Anwendung, um die Authentifizierung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-123">To support authentication, implement this interface in your application.</span></span> <span data-ttu-id="c9fd8-124">Das Reader-Objekt fragt diese Schnittstelle ab, indem **QueryInterface** für den [**iwmreadercallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) -Zeiger aufgerufen wird, der von der Anwendung in der [**iwmreader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) -Methode empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-124">The reader object queries for this interface by calling **QueryInterface** on the [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) pointer that it received from the application in the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method.</span></span> <span data-ttu-id="c9fd8-125">Wenn das Reader-Objekt die Anmelde Informationen des Benutzers erhalten muss, ruft es die **acquirecreden-** Methode der Anwendung auf.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-125">If the reader object needs to get the user's credentials, it calls the application's **AcquireCredentials** method.</span></span>

<span data-ttu-id="c9fd8-126">Wenn die Anmelde Informationen ohne Verschlüsselung über das Netzwerk gesendet werden, legt der Reader das Flag zum Löschen von WMT-Anmelde Informationen \_ \_ \_ im *pdwflags* -Parameter fest.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-126">If the credentials will be sent over the network without encryption, the reader sets the WMT\_CREDENTIAL\_CLEAR\_TEXT flag in the *pdwFlags* parameter.</span></span> <span data-ttu-id="c9fd8-127">Dadurch erhält die Anwendung die Möglichkeit, den Benutzer zu warnen, dass Ihre Anmelde Informationen als nur-Text gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-127">This gives the application an opportunity to warn the user that his or her credentials will be sent in plain text.</span></span>

<span data-ttu-id="c9fd8-128">Andernfalls werden die Anmelde Informationen automatisch vom Reader-Objekt verschlüsselt, bevor Sie über das Netzwerk gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-128">Otherwise, the reader object automatically encrypts the credentials before sending them over the network.</span></span> <span data-ttu-id="c9fd8-129">Die Anwendung kann Sie als Klartext an das Reader-Objekt zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-129">The application can return them to the reader object in plain text.</span></span> <span data-ttu-id="c9fd8-130">Wenn das Reader-Objekt das Flag zum Verschlüsseln der WMT-Anmelde Informationen festlegt \_ \_ , bedeutet dies, dass der Reader das erhalten verschlüsselter Anmelde Informationen aus der Anwendung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-130">In addition, if the reader object sets the WMT\_CREDENTIAL\_ENCRYPT flag, it means the reader supports getting encrypted credentials from the application.</span></span> <span data-ttu-id="c9fd8-131">In diesem Fall kann die Anwendung die Anmelde Informationen entweder im nur-Text-Modus zurückgeben oder Sie selbst mithilfe der **CryptProtectData** -Funktion verschlüsseln, die in der Platform SDK-Dokumentation beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-131">In that case, the application can either return the credentials in plain text, or else encrypt them itself using the **CryptProtectData** function, which is described in the Platform SDK documentation.</span></span> <span data-ttu-id="c9fd8-132">Wenn die Anwendung die Anmelde Informationen verschlüsselt, muss Sie das Flag für die WMT-Anmelde Informationen \_ \_ Verschlüsselung im *pdwflags* -Parameter festlegen, bevor die Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-132">If the application encrypts the credentials, it must set the WMT\_CREDENTIAL\_ENCRYPT flag in the *pdwFlags* parameter before the method returns.</span></span>

<span data-ttu-id="c9fd8-133">Im Allgemeinen ist es nicht notwendig, die Daten zu verschlüsseln, da das Reader-Objekt die Daten bei Bedarf verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-133">Generally, it is not necessary to encrypt the data, because the reader object encrypts the data if necessary.</span></span> <span data-ttu-id="c9fd8-134">Die Verschlüsselung kann jedoch nützlich sein, wenn die Anwendung den Benutzernamen und das Kennwort im Arbeitsspeicher beibehält, da Sie verhindert, dass ein Angreifer ein Speicher Abbild des Prozesses überprüft.</span><span class="sxs-lookup"><span data-stu-id="c9fd8-134">However, encryption might be useful if the application keeps the user name and password in memory, because it prevents an attacker from inspecting a memory dump of the process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9fd8-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c9fd8-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9fd8-136">**Iwmkredentialcallback-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c9fd8-136">**IWMCredentialCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> <dt>

[<span data-ttu-id="c9fd8-137">**Iwmreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c9fd8-137">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> </dl>

 

 




