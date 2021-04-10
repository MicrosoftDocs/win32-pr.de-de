---
description: Im folgenden finden Sie eine Anleitung zum Sichern der Windows Sockets-Programmierung.
ms.assetid: 70210e86-ead6-4b0c-ae47-66b2ef0a8d11
title: Sichere Winsock-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70d7a0710a4446486835ec14435fa7d7ba1458c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755073"
---
# <a name="secure-winsock-programming"></a><span data-ttu-id="341a5-103">Sichere Winsock-Programmierung</span><span class="sxs-lookup"><span data-stu-id="341a5-103">Secure Winsock Programming</span></span>

<span data-ttu-id="341a5-104">Im folgenden finden Sie eine Anleitung zum Sichern der Windows Sockets-Programmierung.</span><span class="sxs-lookup"><span data-stu-id="341a5-104">The following is a guide to secure Windows Sockets programming.</span></span> <span data-ttu-id="341a5-105">Es wurde entwickelt, um ein Verständnis der Winsock-Sicherheit und der Optionen zu bieten, die für den Entwickler der sicheren Netzwerk Anwendung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="341a5-105">It is designed to provide an understanding of Winsock security and the options available to the secure network application developer.</span></span>

-   [<span data-ttu-id="341a5-106">Verwenden von " \_ reuseaddr" und " \_ exclusiveaddruse"</span><span class="sxs-lookup"><span data-stu-id="341a5-106">Using SO\_REUSEADDR and SO\_EXCLUSIVEADDRUSE</span></span>](using-so-reuseaddr-and-so-exclusiveaddruse.md)
-   [<span data-ttu-id="341a5-107">Winsock Secure Socket Extensions</span><span class="sxs-lookup"><span data-stu-id="341a5-107">Winsock Secure Socket Extensions</span></span>](winsock-secure-socket-extensions.md)

<span data-ttu-id="341a5-108">Die Kommunikation mit Sockets kann auch mithilfe der SSL/TLS-Standards mithilfe des sicheren Kanals, auch als SChannel-Technologie bezeichnet, verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="341a5-108">Communications using sockets can also be encrypted using the SSL/TLS standards using Secure Channel, also known as Schannel technology.</span></span> <span data-ttu-id="341a5-109">SChannel ist eine Security Support Provider (SSP), die eine Reihe von Sicherheitsprotokollen enthält, die Identitäts Authentifizierung und eine sichere private Kommunikation durch Verschlüsselung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="341a5-109">Schannel is a security support provider (SSP) that contains a set of security protocols that provide identity authentication and secure, private communication through encryption.</span></span> <span data-ttu-id="341a5-110">SChannel wird hauptsächlich für Internet Anwendungen verwendet, die eine HTTP-Kommunikation (Secure Hypertext Transfer Protocol) erfordern.</span><span class="sxs-lookup"><span data-stu-id="341a5-110">Schannel is primarily used for Internet applications that require secure Hypertext Transfer Protocol (HTTP) communications.</span></span> <span data-ttu-id="341a5-111">Weitere Informationen finden Sie unter [sicherer Kanal](../secauthn/secure-channel.md).</span><span class="sxs-lookup"><span data-stu-id="341a5-111">For more information, please see [Secure Channel](../secauthn/secure-channel.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="341a5-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="341a5-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="341a5-113">Secure Channel</span><span class="sxs-lookup"><span data-stu-id="341a5-113">Secure Channel</span></span>](../secauthn/secure-channel.md)
</dt> </dl>

 

 
