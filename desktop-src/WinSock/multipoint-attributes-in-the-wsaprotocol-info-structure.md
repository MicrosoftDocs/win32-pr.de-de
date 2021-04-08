---
title: Multipoint-Attribute in WSAPROTOCOL_INFO
description: Zu den Multipoint-Attributen in der wsaprotocol- \_ Informationsstruktur gehören XP1 \_ -Unterstützung für \_ Multipoint-, XP1 \_ Multipoint \_ \_ -Steuerungsebene und XP1- \_ Multipoint- \_ Daten \_ Ebene.
ms.assetid: f1bd5aa1-e705-4eaf-9436-fed0ea03f113
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baedcd07f53db462eb090217b53d93a1a4aa8c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751440"
---
# <a name="multipoint-attributes-in-wsaprotocol_info"></a><span data-ttu-id="50c3e-103">Multipoint-Attribute in WSAPROTOCOL_INFO</span><span class="sxs-lookup"><span data-stu-id="50c3e-103">Multipoint attributes in WSAPROTOCOL_INFO</span></span>

<span data-ttu-id="50c3e-104">Drei Attribut Parameter sind in der [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Struktur definiert, um die unterschiedlichen Schemas zu unterscheiden, die im Steuerelement bzw. in den Daten Ebenen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="50c3e-104">Three attribute parameters are defined in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure in order to distinguish the different schemes used in the control and data planes, respectively:</span></span>

-   <span data-ttu-id="50c3e-105">XP1 \_ Unterstützung \_ von Multipoint mit dem Wert 1 gibt an, dass dieser Protokolleintrag Multipoint-Kommunikation unterstützt und dass die folgenden beiden Parameter aussagekräftig sind.</span><span class="sxs-lookup"><span data-stu-id="50c3e-105">XP1\_SUPPORT\_MULTIPOINT with a value of 1 indicates this protocol entry supports multipoint communications, and that the following two parameters are meaningful.</span></span>
-   <span data-ttu-id="50c3e-106">\_Die Multipoint- \_ Steuerungsebene XP1 gibt an, \_ ob die Steuerungsebene einen Stamm (Wert = 1) oder einen nicht-Stamm (Wert = 0) hat.</span><span class="sxs-lookup"><span data-stu-id="50c3e-106">XP1\_MULTIPOINT\_CONTROL\_PLANE indicates whether the control plane is rooted (value = 1) or nonrooted (value = 0).</span></span>
-   <span data-ttu-id="50c3e-107">Die XP1- \_ Multipoint- \_ Daten \_ Ebene gibt an, ob die Datenebene (Wert = 1) oder nicht als Stamm (Wert = 0) verankert ist.</span><span class="sxs-lookup"><span data-stu-id="50c3e-107">XP1\_MULTIPOINT\_DATA\_PLANE indicates whether the data plane is rooted (value = 1) or nonrooted (value = 0).</span></span>

<span data-ttu-id="50c3e-108">Wenn ein Multipoint-Protokoll sowohl Stamm-als auch nicht-Stammdaten Ebenen unterstützt, sind zwei [**wsaprotocol- \_ Informations**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Einträge vorhanden.</span><span class="sxs-lookup"><span data-stu-id="50c3e-108">Two [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entries would be present if a multipoint protocol supported both rooted and nonrooted data planes, one entry for each.</span></span>

 

 
