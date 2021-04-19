---
description: Beispiel für Multicast Programmierung
ms.assetid: 87a6d3bb-3827-4a84-ba2d-c7bd2dd73eb2
title: Beispiel für Multicast Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cde6b8ab9ac0dd6b4fc16ae36bec4a4e939466b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348389"
---
# <a name="multicast-programming-sample"></a>Beispiel für Multicast Programmierung

Der folgende Beispielcode veranschaulicht, wie Multicast Funktionen mithilfe von Socketoptionen in eine Windows Sockets-Anwendung eingeschlossen werden.


```C++
#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <mswsock.h>

#define u_int32 UINT32  // Unix uses u_int32

// Need to link with Ws2_32.lib
#pragma comment (lib, "Ws2_32.lib")


int                  /* OUT: whatever setsockopt() returns */
join_source_group(int sd, u_int32 grpaddr, 
   u_int32 srcaddr, u_int32 iaddr)
{
   struct ip_mreq_source imr; 
   
   imr.imr_multiaddr.s_addr  = grpaddr;
   imr.imr_sourceaddr.s_addr = srcaddr;
   imr.imr_interface.s_addr  = iaddr;
   return setsockopt(sd, IPPROTO_IP, IP_ADD_SOURCE_MEMBERSHIP, (char *) &imr, sizeof(imr));  
}

int
leave_source_group(int sd, u_int32 grpaddr, 
   u_int32 srcaddr, u_int32 iaddr)
{
   struct ip_mreq_source imr;

   imr.imr_multiaddr.s_addr  = grpaddr;
   imr.imr_sourceaddr.s_addr = srcaddr;
   imr.imr_interface.s_addr  = iaddr;
   return setsockopt(sd, IPPROTO_IP, IP_DROP_SOURCE_MEMBERSHIP, (char *) &imr, sizeof(imr));
}
```



 

 



