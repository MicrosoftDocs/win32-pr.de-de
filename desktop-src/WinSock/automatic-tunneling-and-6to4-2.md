---
description: Automatische Tunnelung mit IPv4-kompatiblen Adressen und IPv6-zu-IPv4-Verbindungen arbeiten über eine Route für ein Präfix, das mit Schnittstelle 2 verknüpft ist \# . Die 32 Bits nach dem Präfix werden extrahiert und als IPv4-Zieladresse für das gekapselte Paket verwendet.
ms.assetid: 92261a1b-2b7f-4a76-b98a-2631dc303618
title: Automatisches IPv6-Tunnelung und IPv6-zu-IPv4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede1179902a7ec3276058e078d56e069603e54a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348183"
---
# <a name="ipv6-automatic-tunneling-and-6to4"></a>Automatisches IPv6-Tunnelung und IPv6-zu-IPv4

Automatische Tunnelung mit IPv4-kompatiblen Adressen und IPv6-zu-IPv4-Verbindungen arbeiten über eine Route für ein Präfix, das mit Schnittstelle 2 verknüpft ist \# . Die 32 Bits nach dem Präfix werden extrahiert und als IPv4-Zieladresse für das gekapselte Paket verwendet.

Bei der automatischen Tunnelung wird das Präfix::/96 verwendet, das standardmäßig aktiviert ist. Sie kann deaktiviert werden, indem Sie die Route für::/96 entfernen.

IPv6-zu-IPv4 verwendet das Präfix 2002::/16, das nicht standardmäßig aktiviert ist.

 

 



