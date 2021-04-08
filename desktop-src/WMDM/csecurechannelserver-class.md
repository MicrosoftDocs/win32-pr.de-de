---
title: Csecurechannelserver-Klasse
description: Csecurechannelserver-Klasse
ms.assetid: e6e1463a-5a26-4b83-85e0-a639d384a199
keywords:
- Windows Media Device Manager, csecurechannelserver-Klasse
- Device Manager, csecurechannelserver-Klasse
- Dienstanbieter, csecurechannelserver-Klasse
- Programmier Referenz, csecurechannelserver-Klasse
- Referenz für Windows Media Device Manager, csecurechannelserver-Klasse
- Csecurechannelserver-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99efdd4d4fa245000d27b5874439375d968591e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727880"
---
# <a name="csecurechannelserver-class"></a><span data-ttu-id="b81b2-109">Csecurechannelserver-Klasse</span><span class="sxs-lookup"><span data-stu-id="b81b2-109">CSecureChannelServer Class</span></span>

<span data-ttu-id="b81b2-110">Die **csecurechannelserver** -Klasse ist eine Hilfsklasse (keine Schnittstelle), die einem Dienstanbieter oder einem sicheren Inhaltsanbieter ermöglicht, eine Anwendung mithilfe der [**icomponentauthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) -Schnittstelle zu authentifizieren, Daten zu verschlüsseln und zu entschlüsseln und Mac-Signaturen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b81b2-110">The **CSecureChannelServer** class is a helper class (not an interface) that enables a service provider or secure content provider to authenticate an application using the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface, to encrypt and decrypt data, and to create MAC signatures.</span></span> <span data-ttu-id="b81b2-111">Der Authentifizierungsprozess erfordert, dass die Anwendung ein **csecurechannelclient** -Objekt erstellt und dass der Dienstanbieter ein **csecurechannelserver** -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="b81b2-111">The authentication process requires that the application create a **CSecureChannelClient** object and that the service provider create a **CSecureChannelServer** object.</span></span> <span data-ttu-id="b81b2-112">Die **csecurechannelclient** -Klasse und die **csecurechannelserver** -Klasse werden in der statischen Link Bibliothek "mssachlp. lib" deklariert.</span><span class="sxs-lookup"><span data-stu-id="b81b2-112">The **CSecureChannelClient** and **CSecureChannelServer** classes are declared in the static link library, Mssachlp.lib.</span></span> <span data-ttu-id="b81b2-113">Alle Methoden der Schnittstellen von Windows Media Device Manager, Service Provider und Secure Content Provider können WMDM \_ E \_ notcertified zurückgeben, um anzugeben, dass der Aufrufer nicht erfolgreich authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="b81b2-113">All methods of Windows Media Device Manager, service provider, and secure content provider interfaces can return WMDM\_E\_NOTCERTIFIED to indicate that the caller has not authenticated successfully.</span></span>

<span data-ttu-id="b81b2-114">Die **csecurechannelserver** -Klasse stellt die folgenden Methoden zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="b81b2-114">The **CSecureChannelServer** class exposes the following methods.</span></span>



| <span data-ttu-id="b81b2-115">Methode</span><span class="sxs-lookup"><span data-stu-id="b81b2-115">Method</span></span>                                                            | <span data-ttu-id="b81b2-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b81b2-116">Description</span></span>                                                                                 |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b81b2-117">[**Decryptparam**](/previous-versions/bb231598(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b81b2-117">[**DecryptParam**](/previous-versions/bb231598(v=vs.85))</span></span>         | <span data-ttu-id="b81b2-118">Entschlüsselt die Daten, die in einem Parameter enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b81b2-118">Decrypts the data contained in a parameter.</span></span>                                                 |
| <span data-ttu-id="b81b2-119">[**Verschlüsseltparam**](/previous-versions/ms868509(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b81b2-119">[**EncryptParam**](/previous-versions/ms868509(v=msdn.10))</span></span>         | <span data-ttu-id="b81b2-120">Verschlüsselt die Daten, die in einem Parameter enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b81b2-120">Encrypts the data contained in a parameter.</span></span>                                                 |
| <span data-ttu-id="b81b2-121">[**fisauthenticated**](/previous-versions/bb231600(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b81b2-121">[**fIsAuthenticated**](/previous-versions/bb231600(v=vs.85))</span></span> | <span data-ttu-id="b81b2-122">Mit dieser Option wird überprüft, ob ein sicherer Authentifizierungs Kanal erfolgreich eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="b81b2-122">Verifies that a secure authentication channel has been successfully established.</span></span>            |
| <span data-ttu-id="b81b2-123">[**Getappsec**](/previous-versions/bb231601(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b81b2-123">[**GetAppSec**](/previous-versions/bb231601(v=vs.85))</span></span>               | <span data-ttu-id="b81b2-124">Ruft die Anwendungs Sicherheitsgrade der lokalen Komponenten und Remote Komponenten ab.</span><span class="sxs-lookup"><span data-stu-id="b81b2-124">Retrieves the application security levels of the local and remote components.</span></span>               |
| <span data-ttu-id="b81b2-125">[**Getessionkey**](/previous-versions/bb231602(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b81b2-125">[**GetSessionKey**](/previous-versions/bb231602(v=vs.85))</span></span>       | <span data-ttu-id="b81b2-126">Ruft den aktuellen Sitzungsschlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="b81b2-126">Retrieves the current session key.</span></span>                                                          |
| <span data-ttu-id="b81b2-127">[**Macfinal**](/previous-versions/ms868513(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b81b2-127">[**MACFinal**](/previous-versions/ms868513(v=msdn.10))</span></span>                 | <span data-ttu-id="b81b2-128">Gibt den Mac-Kanal (Message Authentication Code) frei und Ruft einen abschließenden Mac-Wert ab.</span><span class="sxs-lookup"><span data-stu-id="b81b2-128">Releases the message authentication code (MAC) channel and retrieves a final MAC value.</span></span>     |
| <span data-ttu-id="b81b2-129">[**Macinit**](/previous-versions/ms868514(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b81b2-129">[**MACInit**](/previous-versions/ms868514(v=msdn.10))</span></span>                   | <span data-ttu-id="b81b2-130">Ruft einen Mac-Kanal (Message Authentication Code) ab.</span><span class="sxs-lookup"><span data-stu-id="b81b2-130">Acquires a message authentication code (MAC) channel.</span></span>                                       |
| <span data-ttu-id="b81b2-131">[**Macupdate**](/previous-versions/ms868515(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b81b2-131">[**MACUpdate**](/previous-versions/ms868515(v=msdn.10))</span></span>               | <span data-ttu-id="b81b2-132">Aktualisiert den Mac-Wert (Message Authentication Code) mit einem Parameterwert.</span><span class="sxs-lookup"><span data-stu-id="b81b2-132">Updates the message authentication code (MAC) value with a parameter value.</span></span>                 |
| <span data-ttu-id="b81b2-133">[**Sacauth**](/previous-versions/ms868516(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b81b2-133">[**SACAuth**](/previous-versions/ms868516(v=msdn.10))</span></span>                   | <span data-ttu-id="b81b2-134">Legt einen sicheren authentifizierten Kanal zwischen Komponenten fest.</span><span class="sxs-lookup"><span data-stu-id="b81b2-134">Establishes a secure authenticated channel between components.</span></span>                              |
| <span data-ttu-id="b81b2-135">[**Sacgetprotokolle**](/previous-versions/ms868517(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b81b2-135">[**SACGetProtocols**](/previous-versions/ms868517(v=msdn.10))</span></span>   | <span data-ttu-id="b81b2-136">Meldet die Protokolle, die von einer Komponente unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b81b2-136">Reports the protocols supported by a component.</span></span>                                             |
| <span data-ttu-id="b81b2-137">[**SetCertificate**](/previous-versions/ms868518(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b81b2-137">[**SetCertificate**](/previous-versions/ms868518(v=msdn.10))</span></span>     | <span data-ttu-id="b81b2-138">Gibt das Zertifikat und den privaten Schlüssel des SAC-Servers (Secure authentifiziert Channel) an.</span><span class="sxs-lookup"><span data-stu-id="b81b2-138">Specifies the certificate and private key of the secure authenticated channel (SAC) server.</span></span> |
| <span data-ttu-id="b81b2-139">[**"-Essionkey"**](/previous-versions/ms868519(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b81b2-139">[**SetSessionKey**](/previous-versions/ms868519(v=msdn.10))</span></span>       | <span data-ttu-id="b81b2-140">Legt den Sitzungsschlüssel fest, der für die Kommunikation mit einer anderen Komponente verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b81b2-140">Sets the session key that is used to communicate with another component.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="b81b2-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b81b2-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b81b2-142">**Csecurechannelclient-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b81b2-142">**CSecureChannelClient Class**</span></span>](csecurechannelclient-class.md)
</dt> <dt>

[<span data-ttu-id="b81b2-143">**Icomponentauthenticate-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b81b2-143">**IComponentAuthenticate Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[<span data-ttu-id="b81b2-144">**Schnittstellen für Dienstanbieter**</span><span class="sxs-lookup"><span data-stu-id="b81b2-144">**Interfaces for Service Providers**</span></span>](interfaces-for-service-providers.md)
</dt> <dt>

[<span data-ttu-id="b81b2-145">**Verwenden sicherer authentifizierter Kanäle**</span><span class="sxs-lookup"><span data-stu-id="b81b2-145">**Using Secure Authenticated Channels**</span></span>](using-secure-authenticated-channels.md)
</dt> </dl>

 

 