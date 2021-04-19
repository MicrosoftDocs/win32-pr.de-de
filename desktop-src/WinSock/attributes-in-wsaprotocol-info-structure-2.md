---
description: XP1 \_ unterstützen die Multipoint \_ -, XP1 \_ Multipoint \_ \_ -Steuerungsebene und XP1 \_ Multipoint- \_ \_ Attribut Parameter für die Datenebene in der Struktur der Winsock-wsaprotocol- \_ Informationen.
ms.assetid: 62f5b8b0-a404-49d1-b163-026f79a46845
title: Attribute in WSAPROTOCOL_INFO Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39ea2905da3228860d4fe22f5a0f0d954ce0624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356762"
---
# <a name="attributes-in-wsaprotocol_info-structure"></a>Attribute in der wsaprotocol- \_ Informationsstruktur

Zur Unterstützung der oben beschriebenen Taxonomie werden drei Attribut Parameter in der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur verwendet, um die Schemas zu unterscheiden, die im Steuerelement bzw. in den Daten Ebenen verwendet werden:

-   XP1 \_ Unterstützung \_ von Multipoint mit dem Wert 1 gibt an, dass dieser Protokolleintrag Multipoint-Kommunikation unterstützt und dass die folgenden beiden Parameter aussagekräftig sind.
-   \_Die Multipoint- \_ Steuerungsebene XP1 gibt an, \_ ob die Steuerungsebene einen Stamm (Wert = 1) oder einen nicht-Stamm (Wert = 0) hat.
-   Die XP1- \_ Multipoint- \_ Daten \_ Ebene gibt an, ob die Datenebene (Wert = 1) oder nicht als Stamm (Wert = 0) verankert ist.

Beachten Sie, dass zwei [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Einträge vorhanden sind, wenn ein Multipoint-Protokoll sowohl Stamm-als auch nicht-Stammdaten Ebenen unterstützt, jeweils einen Eintrag für jeden.

Die Anwendung kann [**wsaenumprotokolle**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) verwenden, um zu ermitteln, ob Multipoint-Kommunikationen für ein bestimmtes Protokoll unterstützt werden, und wenn dies der Fall ist, wie Sie in Bezug auf das Steuerelement bzw. die Daten Ebenen unterstützt werden.

 

 
