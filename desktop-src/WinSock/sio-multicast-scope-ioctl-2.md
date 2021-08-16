---
description: Verwenden sie den SIO \_ MULTICAST \_ SCOPE-Befehlscode, um den Bereich anzugeben, für den der Multicast ausgeführt werden soll.
ms.assetid: 3acec987-9cb4-446c-af6e-ea0e6a96e70c
title: SIO_MULTICAST_SCOPE Ioctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1be65ee600b680805177a44125c03e65e49364ae9008d306349da8f60f9d9de8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559688"
---
# <a name="sio_multicast_scope-ioctl"></a>SIO \_ MULTICAST \_ SCOPE Ioctl

Wenn Multicasting verwendet wird, ist es in der Regel erforderlich, den Bereich anzugeben, über den der Multicast erfolgen soll. Hier wird der Bereich definiert, um die Anzahl der zu abgedeckten Routennetzwerksegmente zu sein. Der SIO \_ MULTICAST \_ SCOPE-Befehlscode für [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) wird verwendet, um dies zu steuern. Ein Bereich von 0 (null) gibt an, dass die Multicastübertragung nicht auf dem Kabel platziert wird, sondern über Sockets innerhalb des lokalen Hosts verteilt werden kann. Ein Bereichswert von 1 (Standard) gibt an, dass die Übertragung an das Netzwerk übertragen wird, aber keine Router überquert. Höhere Bereichswerte bestimmen die Anzahl der Router, die überschritten werden können. Beachten Sie, dass dies dem TTL-Parameter (Time-to-Live) beim IP-Multicasting entspricht.

 

 
