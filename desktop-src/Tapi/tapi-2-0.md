---
description: TAPI 2,0 bietet eine kleine Anzahl von Verbesserungen an der grundlegenden TAPI 1,4-Funktionalität.
ms.assetid: f3a319b4-5e82-4bf9-bd89-a027d58ad126
title: TAPI 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34a3503916c6ec90c3a90e648ac3622c271d810
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345428"
---
# <a name="tapi-20"></a>TAPI 2,0

TAPI 2,0 bietet eine kleine Anzahl von Verbesserungen an der grundlegenden TAPI 1,4-Funktionalität. Es gab jedoch einige wesentliche Änderungen an der Architektur, die die Stabilität erheblich verbessert haben. Die meisten Änderungen waren grundlegende Änderungen, die erforderlich waren, um TAPI in Windows NT 4,0 zu bringen und die Vorteile der Features zu nutzen (vollständige 32-Bit-Unterstützung, Dienste und Unicode). Allerdings waren diese Änderungen intern zu TAPI und hatten nur wenig Auswirkungen auf TAPI-Anwendungen.

Anwendungen, die TAPI 1,3 und 1,4 (16-Bit-Anwendungen über eine thunkingschicht) unterstützen, funktionieren gut für Windows Server 2003-Betriebssysteme, Windows XP, Windows 2000 und Windows NT. Die Auswirkungen auf Entwickler von Dienstanbietern waren jedoch von Bedeutung. Dienstanbieter für diese Betriebssysteme müssen vollständige 32-Bit-Unicode-DLLs sein, die im Kontext von tapisrv ausgeführt werden können, und nicht im Kontext der TAPI-Anwendung (wie alle früheren Win16 basierten TSPS). TSPS, die für TAPI 1,4 entworfen wurden, funktionieren unter Windows Server 2003-Betriebssystemen, Windows XP, Windows 2000 oder Windows NT nicht.

TAPI 2,0 bietet auch die wichtigen Features der Support Unterstützung für Callcenter und Quality of Service (QoS).

Die im Lieferumfang von Windows enthaltenen TAPI-System Binärdateien unterstützen TAPI-Versionen 1,3 und 1,4 für alle Anwendungen. Allerdings können von 16-Bit-Anwendungen TAPI 2,0 nicht verwendet werden, und Sie können keine 16-Bit-TAPI 2. x-TSP verwenden.

 

 



