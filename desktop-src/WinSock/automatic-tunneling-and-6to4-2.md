---
description: Automatisches Tunneln mit IPv4-kompatiblen Adressen und 6 zu 4 durcharbeiten beide eine Route für ein Präfix, das über eine Verbindung mit Schnittstelle \# 2 steht. Die 32 Bits nach dem Präfix werden extrahiert und als IPv4-Zieladresse für das gekapselte Paket verwendet.
ms.assetid: 92261a1b-2b7f-4a76-b98a-2631dc303618
title: Automatisches Tunneln von IPv6 und 6 zu 4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4170d937e331d38337c21b777ae232a39fcb304f8550a1d1ed994ef55101bb0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758490"
---
# <a name="ipv6-automatic-tunneling-and-6to4"></a>Automatisches Tunneln von IPv6 und 6 zu 4

Automatisches Tunneln mit IPv4-kompatiblen Adressen und 6 zu 4 durcharbeiten beide eine Route für ein Präfix, das über eine Verbindung mit Schnittstelle \# 2 steht. Die 32 Bits nach dem Präfix werden extrahiert und als IPv4-Zieladresse für das gekapselte Paket verwendet.

Automatisches Tunneln verwendet das Präfix ::/96, das standardmäßig aktiviert ist. Sie kann durch Entfernen der Route für ::/96 deaktiviert werden.

6to4 verwendet das Präfix 2002::/16, das standardmäßig nicht aktiviert ist.

 

 



