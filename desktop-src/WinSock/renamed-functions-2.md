---
description: In zwei Fällen war es erforderlich, Funktionen umzubenennen, die in Berkeley Sockets verwendet werden, um Konflikte mit anderen Microsoft Windows-API-Funktionen zu vermeiden.
ms.assetid: b53b1622-cba4-47e3-a371-b3186de6d61b
title: Umbenannte Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8fd2af33bdeb74dd7a4c83fe535bae2a020530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863815"
---
# <a name="renamed-functions"></a><span data-ttu-id="19071-103">Umbenannte Funktionen</span><span class="sxs-lookup"><span data-stu-id="19071-103">Renamed Functions</span></span>

<span data-ttu-id="19071-104">In zwei Fällen war es erforderlich, Funktionen umzubenennen, die in Berkeley Sockets verwendet werden, um Konflikte mit anderen Microsoft Windows-API-Funktionen zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="19071-104">In two cases it was necessary to rename functions that are used in Berkeley Sockets in order to avoid clashes with other Microsoft Windows API functions.</span></span>

## <a name="close-and-closesocket"></a><span data-ttu-id="19071-105">Schließen und closesocket</span><span class="sxs-lookup"><span data-stu-id="19071-105">Close and Closesocket</span></span>

<span data-ttu-id="19071-106">Sockets werden von Standarddatei Deskriptoren in Berkeley Sockets dargestellt, sodass die **Close** -Funktion verwendet werden kann, um Sockets und normale Dateien zu schließen.</span><span class="sxs-lookup"><span data-stu-id="19071-106">Sockets are represented by standard file descriptors in Berkeley Sockets, so the **close** function can be used to close sockets as well as regular files.</span></span> <span data-ttu-id="19071-107">Obwohl nichts in Windows Sockets verhindert, dass eine Implementierung reguläre Datei Handles verwendet, um Sockets zu identifizieren, ist dies nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="19071-107">While nothing in Windows Sockets prevents an implementation from using regular file handles to identify sockets, nothing requires it either.</span></span> <span data-ttu-id="19071-108">Unter Windows müssen Sockets mithilfe der [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) -Routine geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="19071-108">On Windows, sockets must be closed by using the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) routine.</span></span> <span data-ttu-id="19071-109">Unter Windows ist die Verwendung der **Close** -Funktion zum Schließen eines Sockets falsch, und die Auswirkungen, die dies bewirkt, sind durch diese Spezifikation nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="19071-109">ON Windows, using the **close** function to close a socket is incorrect and the effects of doing so are undefined by this specification.</span></span>

## <a name="ioctl-and-ioctlsocketwsaioctl"></a><span data-ttu-id="19071-110">Ioctl und ioctlsocket/WSAIoctl</span><span class="sxs-lookup"><span data-stu-id="19071-110">Ioctl and Ioctlsocket/WSAIoctl</span></span>

<span data-ttu-id="19071-111">Verschiedene C-sprach Laufzeitsysteme verwenden IOCTLs für Zwecke, die nicht mit Windows Sockets verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="19071-111">Various C language run-time systems use the IOCTLs for purposes unrelated to Windows Sockets.</span></span> <span data-ttu-id="19071-112">Folglich wurden die [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) -Funktion und die [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -Funktion definiert, um Socketfunktionen zu verarbeiten, die von **ioctl** und **fcntl** in der Berkeley-Software Verteilung durchgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="19071-112">As a consequence, the [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) function and the [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function were defined to handle socket functions that were performed by **IOCTL** and **fcntl** in the Berkeley Software Distribution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19071-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="19071-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19071-114">**closesocket**</span><span class="sxs-lookup"><span data-stu-id="19071-114">**closesocket**</span></span>](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[<span data-ttu-id="19071-115">**ioctlsocket**</span><span class="sxs-lookup"><span data-stu-id="19071-115">**ioctlsocket**</span></span>](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)
</dt> <dt>

[<span data-ttu-id="19071-116">Portieren von Socketanwendungen auf Winsock</span><span class="sxs-lookup"><span data-stu-id="19071-116">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="19071-117">Überlegungen zur Winsock-Programmierung</span><span class="sxs-lookup"><span data-stu-id="19071-117">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="19071-118">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="19071-118">**WSAIoctl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)
</dt> </dl>

 

 



