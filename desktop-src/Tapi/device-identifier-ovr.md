---
description: Eine Geräte-ID ist ein Anwendungs unabhängiger Bezeichner für ein bestimmtes Kommunikationsgerät.
ms.assetid: c7ca72a6-97fa-441f-92ce-a4c77a53765c
title: Gerätebezeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aeb9c88820ecfe26d3ecd971489d709a34af10f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529078"
---
# <a name="device-identifier"></a>Gerätebezeichner

Eine *Geräte-ID* ist ein Anwendungs unabhängiger Bezeichner für ein bestimmtes Kommunikationsgerät. Dies ist in der Regel nur erforderlich, wenn eine TAPI-Anwendung einen Teil der Verarbeitung an eine Kommunikationssitzung an die Funktionen einer anderen API übergeben muss. TAPI 2,2-Anwendungen können z. b. möglicherweise nicht direkt auf einen Medienstrom zugreifen und können die Wave-API verwenden.

**TAPI 2. x:** Siehe [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid).

**TAPI 3. x:** Siehe [**itaddresscapability:: get \_ addresscapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) (*addresscap* festgelegt auf den **AC \_ PERMANENTDEVICEID** Member of [**Address \_ Capability**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)).

 

 
