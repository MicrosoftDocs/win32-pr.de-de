---
description: Ein unformatierte Socket ist ein Typ von Socket, der den Zugriff auf den zugrunde liegenden Transportanbieter ermöglicht. Die Verwendung von rohsockets beim Portieren von Anwendungen auf Winsock wird aus verschiedenen Gründen nicht empfohlen.
ms.assetid: b78c75b7-255c-4e85-9a88-0efb3b5f0e51
title: Rohdaten Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209c884e85327a7a8c1d21292d9342a0c032747a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131024"
---
# <a name="raw-sockets"></a><span data-ttu-id="7a083-104">Rohdaten Sockets</span><span class="sxs-lookup"><span data-stu-id="7a083-104">Raw Sockets</span></span>

<span data-ttu-id="7a083-105">Ein unformatierte Socket ist ein Typ von Socket, der den Zugriff auf den zugrunde liegenden Transportanbieter ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="7a083-105">A raw socket is a type of socket that allows access to the underlying transport provider.</span></span> <span data-ttu-id="7a083-106">Die Verwendung von rohsockets beim Portieren von Anwendungen auf Winsock wird aus verschiedenen Gründen nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="7a083-106">The use of raw sockets when porting applications to Winsock is not recommended for several reasons.</span></span>

<span data-ttu-id="7a083-107">Die Windows Sockets-Spezifikation gibt nicht an, dass ein Winsock-Dienstanbieter Rohdaten Sockets unterstützt, d. h. Sockets vom Typ " **Sock \_ RAW**".</span><span class="sxs-lookup"><span data-stu-id="7a083-107">The Windows Sockets specification does not mandate that a Winsock service provider support raw sockets, that is, sockets of type **SOCK\_RAW**.</span></span> <span data-ttu-id="7a083-108">Dienstanbieter werden jedoch empfohlen, RAW Socket-Unterstützung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7a083-108">However, service providers are encouraged to supply raw socket support.</span></span> <span data-ttu-id="7a083-109">Eine Windows Sockets-kompatible Anwendung, die unformatierte Sockets verwenden möchte, sollte versuchen, den Socket mit dem [**socketbefehl**](/windows/desktop/api/Winsock2/nf-winsock2-socket) zu öffnen, und wenn Sie fehlschlägt, versuchen Sie, einen anderen Sockettyp zu verwenden, oder geben Sie den Fehler des Benutzers an.</span><span class="sxs-lookup"><span data-stu-id="7a083-109">A Windows Sockets-compliant application that wishes to use raw sockets should attempt to open the socket with the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) call, and if it fails either attempt to use another socket type or indicate the failure to the user.</span></span>

<span data-ttu-id="7a083-110">Unter Windows 7, Windows Server 2008 R2, Windows Vista und Windows XP mit Service Pack 2 (SP2) wurde die Möglichkeit zum Senden von Datenverkehr über Unformatierte Sockets auf verschiedene Weise eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="7a083-110">On Windows 7, Windows Server 2008 R2, Windows Vista, and Windows XP with Service Pack 2 (SP2), the ability to send traffic over raw sockets has been restricted in several ways.</span></span> <span data-ttu-id="7a083-111">Weitere Informationen finden Sie unter [TCP/IP-rohsockets](tcp-ip-raw-sockets-2.md).</span><span class="sxs-lookup"><span data-stu-id="7a083-111">For more information, see [TCP/IP Raw Sockets](tcp-ip-raw-sockets-2.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a083-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7a083-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a083-113">Portieren von Socketanwendungen auf Winsock</span><span class="sxs-lookup"><span data-stu-id="7a083-113">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="7a083-114">**Glühbirne**</span><span class="sxs-lookup"><span data-stu-id="7a083-114">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[<span data-ttu-id="7a083-115">TCP/IP-Rohdaten Sockets</span><span class="sxs-lookup"><span data-stu-id="7a083-115">TCP/IP Raw Sockets</span></span>](tcp-ip-raw-sockets-2.md)
</dt> <dt>

[<span data-ttu-id="7a083-116">Überlegungen zur Winsock-Programmierung</span><span class="sxs-lookup"><span data-stu-id="7a083-116">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



