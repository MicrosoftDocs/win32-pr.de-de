---
description: Ein Thread kann jederzeit WSAIsBlocking aufrufen, um zu bestimmen, ob derzeit ein blockierender Aufruf ausgeführt wird.
ms.assetid: 6213ded4-feab-404f-86a0-3db9a0a42769
title: Abbrechen von blockierenden Vorgängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5064948fe7c1c1262acb9f4f8ef25a3ad3e721e77a188f313541595ef75f9ce9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030690"
---
# <a name="canceling-blocking-operations"></a>Abbrechen von blockierenden Vorgängen

Ein Thread kann jederzeit [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) aufrufen, um zu bestimmen, ob derzeit ein blockierender Aufruf ausgeführt wird. (Diese Funktion wird innerhalb der Windows Sockets 1.1-Kompatibilitätss shims implementiert und verfügt daher über keine SPI-Entsprechung.) Dies ist natürlich nur möglich, wenn der Dienstanbieter eine Pseudoblockierung und keine echte Blockierung verwendet. Bei Bedarf kann [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) jederzeit aufgerufen werden, um jeden aktuellen Pseudoblockierungsvorgang abzubrechen.

 

 
