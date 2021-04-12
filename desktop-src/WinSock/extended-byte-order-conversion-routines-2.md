---
description: Windows Sockets 2 geht nicht davon aus, dass die Netzwerk-Byte Reihenfolge für alle Protokolle identisch ist.
ms.assetid: 517c21b5-4b56-49f8-88ae-103fdfce6441
title: Erweiterte Byte-Order Konvertierungs Routinen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9addb2b1527546b8a7d13eb90581a333f87c6f0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526183"
---
# <a name="extended-byte-order-conversion-routines"></a><span data-ttu-id="dd0a2-103">Erweiterte Byte-Order Konvertierungs Routinen</span><span class="sxs-lookup"><span data-stu-id="dd0a2-103">Extended Byte-Order Conversion Routines</span></span>

<span data-ttu-id="dd0a2-104">Windows Sockets 2 geht nicht davon aus, dass die Netzwerk-Byte Reihenfolge für alle Protokolle identisch ist.</span><span class="sxs-lookup"><span data-stu-id="dd0a2-104">Windows Sockets 2 does not assume that the network byte order for all protocols is the same.</span></span> <span data-ttu-id="dd0a2-105">Eine Reihe von Konvertierungs Routinen wird zum Konvertieren von 16-Bit-und 32-Bit-Mengen in und aus der Netzwerk-Byte Reihenfolge bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="dd0a2-105">A set of conversion routines is supplied for converting 16-bit and 32-bit quantities to and from network byte order.</span></span> <span data-ttu-id="dd0a2-106">Diese Routinen akzeptieren als Eingabeparameter das Sockethandle, dem eine [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="dd0a2-106">These routines take as an input parameter the socket handle that has a [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure associated with it.</span></span> <span data-ttu-id="dd0a2-107">Der **networkbyteorder** -Member der **wsaprotocol- \_ Informations** Struktur gibt die gewünschte netzwerkbyte Reihenfolge an (zurzeit Big-Endian oder Little-Endian).</span><span class="sxs-lookup"><span data-stu-id="dd0a2-107">The **NetworkByteOrder** member of the **WSAPROTOCOL\_INFO** structure specifies the desired network byte order (currently either big-endian or little-endian).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd0a2-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dd0a2-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd0a2-109">**htonl**</span><span class="sxs-lookup"><span data-stu-id="dd0a2-109">**htonl**</span></span>](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[<span data-ttu-id="dd0a2-110">**htonnen**</span><span class="sxs-lookup"><span data-stu-id="dd0a2-110">**htons**</span></span>](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[<span data-ttu-id="dd0a2-111">**nzu HLS**</span><span class="sxs-lookup"><span data-stu-id="dd0a2-111">**ntohl**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[<span data-ttu-id="dd0a2-112">**NUM**</span><span class="sxs-lookup"><span data-stu-id="dd0a2-112">**ntohs**</span></span>](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[<span data-ttu-id="dd0a2-113">Portieren von Socketanwendungen auf Winsock</span><span class="sxs-lookup"><span data-stu-id="dd0a2-113">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="dd0a2-114">Überlegungen zur Winsock-Programmierung</span><span class="sxs-lookup"><span data-stu-id="dd0a2-114">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="dd0a2-115">**Wsahtonl**</span><span class="sxs-lookup"><span data-stu-id="dd0a2-115">**WSAHtonl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[<span data-ttu-id="dd0a2-116">**Wsahtonnen**</span><span class="sxs-lookup"><span data-stu-id="dd0a2-116">**WSAHtons**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[<span data-ttu-id="dd0a2-117">**Wsanum**</span><span class="sxs-lookup"><span data-stu-id="dd0a2-117">**WSANtohl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[<span data-ttu-id="dd0a2-118">**Wsanum**</span><span class="sxs-lookup"><span data-stu-id="dd0a2-118">**WSANtohs**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> <dt>

[<span data-ttu-id="dd0a2-119">**wsaprotocol- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="dd0a2-119">**WSAPROTOCOL\_INFO**</span></span>](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)
</dt> </dl>

 

 
