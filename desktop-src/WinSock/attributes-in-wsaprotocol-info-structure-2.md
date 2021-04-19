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
# <a name="attributes-in-wsaprotocol_info-structure"></a><span data-ttu-id="015eb-103">Attribute in der wsaprotocol- \_ Informationsstruktur</span><span class="sxs-lookup"><span data-stu-id="015eb-103">Attributes in WSAPROTOCOL\_INFO Structure</span></span>

<span data-ttu-id="015eb-104">Zur Unterstützung der oben beschriebenen Taxonomie werden drei Attribut Parameter in der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur verwendet, um die Schemas zu unterscheiden, die im Steuerelement bzw. in den Daten Ebenen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="015eb-104">In support of the taxonomy described above, three attribute parameters in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure are used to distinguish the schemes used in the control and data planes respectively:</span></span>

-   <span data-ttu-id="015eb-105">XP1 \_ Unterstützung \_ von Multipoint mit dem Wert 1 gibt an, dass dieser Protokolleintrag Multipoint-Kommunikation unterstützt und dass die folgenden beiden Parameter aussagekräftig sind.</span><span class="sxs-lookup"><span data-stu-id="015eb-105">XP1\_SUPPORT\_MULTIPOINT with a value of 1 indicates this protocol entry supports multipoint communications, and that the following two parameters are meaningful.</span></span>
-   <span data-ttu-id="015eb-106">\_Die Multipoint- \_ Steuerungsebene XP1 gibt an, \_ ob die Steuerungsebene einen Stamm (Wert = 1) oder einen nicht-Stamm (Wert = 0) hat.</span><span class="sxs-lookup"><span data-stu-id="015eb-106">XP1\_MULTIPOINT\_CONTROL\_PLANE indicates whether the control plane is rooted (value = 1) or nonrooted (value = 0).</span></span>
-   <span data-ttu-id="015eb-107">Die XP1- \_ Multipoint- \_ Daten \_ Ebene gibt an, ob die Datenebene (Wert = 1) oder nicht als Stamm (Wert = 0) verankert ist.</span><span class="sxs-lookup"><span data-stu-id="015eb-107">XP1\_MULTIPOINT\_DATA\_PLANE indicates whether the data plane is rooted (value = 1) or nonrooted (value = 0).</span></span>

<span data-ttu-id="015eb-108">Beachten Sie, dass zwei [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Einträge vorhanden sind, wenn ein Multipoint-Protokoll sowohl Stamm-als auch nicht-Stammdaten Ebenen unterstützt, jeweils einen Eintrag für jeden.</span><span class="sxs-lookup"><span data-stu-id="015eb-108">Note that two [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entries would be present if a multipoint protocol supported both rooted and nonrooted data planes, one entry for each.</span></span>

<span data-ttu-id="015eb-109">Die Anwendung kann [**wsaenumprotokolle**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) verwenden, um zu ermitteln, ob Multipoint-Kommunikationen für ein bestimmtes Protokoll unterstützt werden, und wenn dies der Fall ist, wie Sie in Bezug auf das Steuerelement bzw. die Daten Ebenen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="015eb-109">The application can use [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) to discover whether multipoint communications is supported for a given protocol and, if so, how it is supported with respect to the control and data planes, respectively.</span></span>

 

 
