---
description: Verwenden des \_ Befehls Codes für die Verwendung von SIO-Multicast \_ Bereich zum Angeben des Bereichs, in dem der Multicast auftreten soll.
ms.assetid: 3acec987-9cb4-446c-af6e-ea0e6a96e70c
title: SIO_MULTICAST_SCOPE ioctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d1fd6f2bea76d095ea88d66c0ac029fb9168ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364109"
---
# <a name="sio_multicast_scope-ioctl"></a>Bereich für die SIO- \_ Multicast- \_ ioctl

Wenn Multicasting verwendet wird, ist es in der Regel erforderlich, den Bereich anzugeben, in dem der Multicast auftreten soll. Der Gültigkeitsbereich ist so definiert, dass es sich um die Anzahl der weitergeleiteten Netzwerksegmente handelt. Der \_ \_ Befehls Code für die Verwendung von "sio Multicast Scope" für " [**wspioctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) " wird zur Steuerung verwendet. Ein Bereich von 0 (null) gibt an, dass die Multicast Übertragung nicht bei der Übertragung platziert würde, sondern über Sockets innerhalb des lokalen Hosts verteilt werden könnte. Ein Bereichs Wert von 1 (Standardwert) gibt an, dass die Übertragung in das Netzwerk übertragen wird, ohne Router zu überschreiten. Höhere Bereichs Werte bestimmen die Anzahl von Routern, die möglicherweise überschritten werden. Beachten Sie, dass dies dem Time-to-Live (TTL)-Parameter in IP-Multicasting entspricht.

 

 
