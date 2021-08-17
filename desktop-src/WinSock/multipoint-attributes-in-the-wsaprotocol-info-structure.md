---
title: Multipointattribute in WSAPROTOCOL_INFO
description: Zu den Multipointattributen in der WSAPROTOCOL \_ INFO-Struktur gehören XP1 \_ SUPPORT \_ MULTIPOINT, XP1 \_ MULTIPOINT \_ CONTROL PLANE und \_ XP1 \_ MULTIPOINT DATA \_ \_ PLANE.
ms.assetid: f1bd5aa1-e705-4eaf-9436-fed0ea03f113
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1275b6da00258be10b071bc9b2399abaf5dd608583f3d81a0fdb16af493824ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741104"
---
# <a name="multipoint-attributes-in-wsaprotocol_info"></a>Multipointattribute in WSAPROTOCOL_INFO

In der [**WSAPROTOCOL \_ INFO-Struktur**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) werden drei Attributparameter definiert, um die verschiedenen Schemas zu unterscheiden, die in der Steuerungs- bzw. Datenebene verwendet werden:

-   XP1 \_ SUPPORT \_ MULTIPOINT mit dem Wert 1 gibt an, dass dieser Protokolleintrag die Multipointkommunikation unterstützt und dass die folgenden beiden Parameter sinnvoll sind.
-   XP1 \_ MULTIPOINT \_ CONTROL PLANE gibt \_ an, ob die Steuerungsebene root (Wert = 1) oder nicht gerootet (Wert = 0) ist.
-   XP1 \_ MULTIPOINT \_ DATA PLANE gibt \_ an, ob die Datenebene stammgerootet (Wert = 1) oder nicht gerootet (Wert = 0) ist.

Zwei [**WSAPROTOCOL \_ INFO-Einträge**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) würden vorhanden sein, wenn ein Multipointprotokoll sowohl root- als auch nicht rooted-Datenebenen unterstützt, jeweils einen Eintrag.

 

 
