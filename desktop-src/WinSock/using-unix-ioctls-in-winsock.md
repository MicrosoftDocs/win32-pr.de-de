---
description: Der von den meisten UNIX-Implementierungen bereitgestellte SIOCGIFCONF-Befehl wird in Form von WSAIoctl- und WSPIoctl-Funktionen mit dem Befehl SIO \_ GET \_ INTERFACE LIST \_ unterstützt. Dieser Befehl gibt die Liste der konfigurierten Schnittstellen und deren Parameter zurück.
ms.assetid: c5028dae-052a-444c-837c-cd8d6d901b6c
title: Verwenden UNIX Ioctls in Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da517adb6480a1bd20100a3d9a6d0896f544c1b541ce547a0f76e5c88aa24210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558862"
---
# <a name="using-unix-ioctls-in-winsock"></a>Verwenden UNIX Ioctls in Winsock

Der von den meisten UNIX-Implementierungen bereitgestellte **SIOCGIFCONF-Befehl** wird in Form von [**WSAIoctl-**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) und [**WSPIoctl-Funktionen**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) mit dem Befehl **SIO \_ GET INTERFACE \_ LIST \_ unterstützt.** Dieser Befehl gibt die Liste der konfigurierten Schnittstellen und deren Parameter zurück.

> [!Note]  
> Die Unterstützung dieses Befehls ist für Windows Sockets 2-kompatible TCP/IP-Dienstanbieter obligatorisch.

 

Der Parameter *lpvOutBuffer verweist* auf den Puffer, in dem [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) und [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) die Informationen zu Schnittstellen speichern. Die Anzahl der Schnittstellen (Anzahl der in *lpvOutBuffer* zurückgegebenen Strukturen) kann basierend auf der tatsächlichen Länge des Ausgabepuffers bestimmt werden, der in *lpcbBytesReturned zurückgegeben wird.*

 

 
