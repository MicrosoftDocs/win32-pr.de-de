---
description: TAPI 2.0 bietet eine kleine Anzahl von Verbesserungen an der grundlegenden TAPI 1.4-Funktionalität.
ms.assetid: f3a319b4-5e82-4bf9-bd89-a027d58ad126
title: TAPI 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 926def5cf2348396b9197a83e17b35d9a91d4dee617e00abe4c02d0428f2884e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118861246"
---
# <a name="tapi-20"></a>TAPI 2.0

TAPI 2.0 bietet eine kleine Anzahl von Verbesserungen an der grundlegenden TAPI 1.4-Funktionalität. Es gab jedoch einige wichtige Änderungen an der Architektur, die die Stabilität erheblich verbessert haben. Die meisten Änderungen waren grundlegende Änderungen, die erforderlich waren, um TAPI in Windows NT 4.0 zu bringen und die Features (vollständige 32-Bit-Unterstützung, Dienste und Unicode) zu nutzen. Diese Änderungen waren jedoch intern für TAPI und hatten nur geringe Auswirkungen auf TAPI-Anwendungen.

Anwendungen, die TAPI 1.3 und 1.4 (16-Bit-Anwendungen über eine 16-Bit-Schicht) unterstützen, funktionieren gut auf Windows Server 2003-Betriebssystemen, Windows XP, Windows 2000 und Windows NT. Die Auswirkungen auf Dienstanbieterentwickler waren jedoch erheblich. Dienstanbieter für diese Betriebssysteme müssen vollständig 32-Bit-Unicode-DLLs sein, die im Kontext von TAPISRV und nicht im Kontext der TAPI-Anwendung ausgeführt werden können (wie alle früheren Win16-basierten TSPs). TSPs, die für TAPI 1.4 entwickelt wurden, funktionieren nicht unter Windows Server 2003-Betriebssystemen, Windows XP, Windows 2000 oder Windows NT.

TAPI 2.0 fügt auch die wichtigen Features der Callcenterunterstützung und Quality of Service -Unterstützung (QOS) hinzu.

Die TAPI-Systembinärdateien, die mit Windows geliefert werden, unterstützen tapi-Versionen 1.3 und 1.4 für alle Anwendungen. 16-Bit-Anwendungen können jedoch TAPI 2.0 nicht verwenden, und Sie können keinen 16-Bit-TAPI 2.x-TSP verwenden.

 

 



