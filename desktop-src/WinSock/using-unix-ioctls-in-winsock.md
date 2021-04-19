---
description: Der von den meisten UNIX-Implementierungen bereitgestellte Befehl "siocgifconf" wird in Form von WSAIoctl-und wspioctl-Funktionen mit dem Befehl "sio \_ Get Interface List" unterstützt \_ \_ . Mit diesem Befehl wird die Liste der konfigurierten Schnittstellen und deren Parameter zurückgegeben.
ms.assetid: c5028dae-052a-444c-837c-cd8d6d901b6c
title: Verwenden von UNIX IOCTLs in Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b52c311ea8c5f67dc374503f00c3ca16c5d053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362280"
---
# <a name="using-unix-ioctls-in-winsock"></a>Verwenden von UNIX IOCTLs in Winsock

Der von den meisten UNIX-Implementierungen bereitgestellte Befehl " **siocgifconf** " wird in Form von [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -und [**wspioctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) -Funktionen mit dem Befehl " **SIO \_ get \_ Interface \_ List**" unterstützt. Mit diesem Befehl wird die Liste der konfigurierten Schnittstellen und deren Parameter zurückgegeben.

> [!Note]  
> Die Unterstützung dieses Befehls ist für Windows Sockets 2-kompatible TCP/IP-Dienstanbieter obligatorisch.

 

Der *lpvoutbuffer* -Parameter verweist auf den Puffer, in dem [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) und [**wspioctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) die Informationen über Schnittstellen speichern. Die Anzahl der Schnittstellen (Anzahl der in *lpvoutbuffer* zurückgegebenen Strukturen) kann basierend auf der tatsächlichen Länge des Ausgabepuffers bestimmt werden, der in *lpcbbyteszurück* gegeben wurde.

 

 
