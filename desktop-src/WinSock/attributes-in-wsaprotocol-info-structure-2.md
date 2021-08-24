---
description: XP1 \_ UNTERSTÜTZT \_ DIE Attributparameter MULTIPOINT, XP1 \_ MULTIPOINT CONTROL PLANE und \_ \_ XP1 \_ MULTIPOINT DATA PLANE in der \_ \_ Winsock WSAPROTOCOL \_ INFO-Struktur.
ms.assetid: 62f5b8b0-a404-49d1-b163-026f79a46845
title: Attribute in WSAPROTOCOL_INFO-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb502c0f29f09604f80e5437774f2b481cef238aaf34f566e78886127dae1027
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898550"
---
# <a name="attributes-in-wsaprotocol_info-structure"></a>Attribute in der WSAPROTOCOL \_ INFO-Struktur

Zur Unterstützung der oben beschriebenen Taxonomie werden drei Attributparameter in der [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) verwendet, um die Schemas zu unterscheiden, die in den Steuerelement- bzw. Datenebenen verwendet werden:

-   XP1 \_ SUPPORT \_ MULTIPOINT mit dem Wert 1 gibt an, dass dieser Protokolleintrag die Multipointkommunikation unterstützt und dass die folgenden beiden Parameter sinnvoll sind.
-   XP1 \_ MULTIPOINT \_ CONTROL PLANE gibt \_ an, ob die Steuerungsebene root (Wert = 1) oder nicht gerootet (Wert = 0) ist.
-   XP1 \_ MULTIPOINT \_ DATA PLANE gibt \_ an, ob die Datenebene stammgerootet (Wert = 1) oder nicht gerootet (Wert = 0) ist.

Beachten Sie, dass zwei [**WSAPROTOCOL \_ INFO-Einträge**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) vorhanden wären, wenn ein Multipointprotokoll sowohl root- als auch nicht rooted-Datenebenen unterstützt , jeweils einen Eintrag.

Die Anwendung kann [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) verwenden, um zu ermitteln, ob die Multipointkommunikation für ein bestimmtes Protokoll unterstützt wird und, falls ja, wie sie in Bezug auf die Steuerungs- bzw. Datenebenen unterstützt wird.

 

 
