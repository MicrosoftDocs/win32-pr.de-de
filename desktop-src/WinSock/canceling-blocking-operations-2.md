---
description: Ein Thread kann jederzeit wsaisblockierung aufzurufen, um zu bestimmen, ob zurzeit ein Blockierungs Aufruf ausgeführt wird.
ms.assetid: 6213ded4-feab-404f-86a0-3db9a0a42769
title: Abbrechen von blockierenden Vorgängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 502870b8935dc97c1d6c3714808d1c6532780f7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349002"
---
# <a name="canceling-blocking-operations"></a>Abbrechen von blockierenden Vorgängen

Ein Thread kann jederzeit [wsaisblockierung](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) aufzurufen, um zu bestimmen, ob zurzeit ein Blockierungs Aufruf ausgeführt wird. (Diese Funktion ist innerhalb der Windows Sockets 1,1-Kompatibilitäts-Shims implementiert und hat daher kein SPI-Pendant.) Dies ist offensichtlich nur möglich, wenn eine Pseudo Blockierung statt einer echten Blockierung vom Dienstanbieter eingesetzt wird. Bei Bedarf kann [**wspcancelblockingcalljederzeit**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) aufgerufen werden, um alle aktuellen Pseudo Blockierungs Vorgänge abzubrechen.

 

 
