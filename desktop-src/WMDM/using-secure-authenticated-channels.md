---
title: Verwenden sicherer authentifizierter Kanäle
description: Verwenden sicherer authentifizierter Kanäle
ms.assetid: ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7
keywords:
- Windows Media-Device Manager, Authentifizierung
- Device Manager, Authentifizierung
- Desktop Anwendungen, Authentifizierung
- Dienstanbieter, Authentifizierung
- Programmier Handbuch, Authentifizierung
- authentication
- Windows Media Device Manager, sichere Kommunikation
- Device Manager, sichere Kommunikation
- Desktop Anwendungen, sichere Kommunikation
- Dienstanbieter, sichere Kommunikation
- Programmier Handbuch, sichere Kommunikation
- sichere Kommunikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f88c271cecc2e9252a3f7af0540beef3dc57d2b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036591"
---
# <a name="using-secure-authenticated-channels"></a><span data-ttu-id="cc29c-115">Verwenden sicherer authentifizierter Kanäle</span><span class="sxs-lookup"><span data-stu-id="cc29c-115">Using Secure Authenticated Channels</span></span>

<span data-ttu-id="cc29c-116">Windows Media Device Manager ermöglicht die Authentifizierung und die sichere Kommunikation zwischen Komponenten durch Bereitstellung von zwei Hilfsklassen, [csecurechannelclient](csecurechannelclient-class.md) (für Anwendungen) und [csecurechannelserver](csecurechannelserver-class.md) (für Dienstanbieter) und einer Schnittstelle, [**icomponentauthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (für beides).</span><span class="sxs-lookup"><span data-stu-id="cc29c-116">Windows Media Device Manager enables authentication and secure communication between components by providing two helper classes, [CSecureChannelClient](csecurechannelclient-class.md) (for applications) and [CSecureChannelServer](csecurechannelserver-class.md) (for service providers), and one interface, [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (for both).</span></span> <span data-ttu-id="cc29c-117">Zusammen bilden diese eine API für die Verwendung von Secure authentifiziert Channels (SAC).</span><span class="sxs-lookup"><span data-stu-id="cc29c-117">Together these make up an API for the use of secure authenticated channels (SAC).</span></span> <span data-ttu-id="cc29c-118">SAC verarbeitet die folgenden drei Aufgaben für Dienstanbieter oder Anwendungen, die Windows Media Device Manager verwenden:</span><span class="sxs-lookup"><span data-stu-id="cc29c-118">SAC handles the following three tasks for service providers or applications using Windows Media Device Manager:</span></span>

-   [<span data-ttu-id="cc29c-119">Komponenten Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="cc29c-119">Component Authentication</span></span>](component-authentication.md)
-   [<span data-ttu-id="cc29c-120">Verschlüsselung und Entschlüsselung</span><span class="sxs-lookup"><span data-stu-id="cc29c-120">Encryption and Decryption</span></span>](encryption-and-decryption.md)
-   [<span data-ttu-id="cc29c-121">Nachrichten Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="cc29c-121">Message Authentication</span></span>](message-authentication.md)

<span data-ttu-id="cc29c-122">Eine Anwendung oder ein Dienstanbieter muss die Komponenten Authentifizierung, Verschlüsselung und Entschlüsselung verarbeiten. die Nachrichten Authentifizierung ist optional.</span><span class="sxs-lookup"><span data-stu-id="cc29c-122">An application or service provider must handle component authentication, encryption, and decryption; message authentication is optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc29c-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cc29c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc29c-124">**Allgemeine Aufgaben für Anwendungen und Dienstanbieter**</span><span class="sxs-lookup"><span data-stu-id="cc29c-124">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




