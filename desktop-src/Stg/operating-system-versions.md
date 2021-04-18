---
title: Betriebs System Versionen
description: Dieser DWORD-Datentyp sollte den Betriebs Systemtyp im hohen Bestell Wort und die Versionsnummer des Betriebssystems im nieder wertigen Wort enthalten. Mögliche Werte für das Betriebssystem sind in der folgenden Tabelle aufgeführt.
ms.assetid: 318e277b-a797-45a5-87c5-25b91fdf278d
keywords:
- Strukturierte Speicherung von Betriebs System Versionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5de916d354a721834b9a10651c36d3bf389e28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338070"
---
# <a name="operating-system-versions"></a>Betriebs System Versionen

Dieser **DWORD** -Datentyp sollte den Betriebs Systemtyp im hohen Bestell Wort und die Versionsnummer des Betriebssystems im nieder wertigen Wort enthalten. Mögliche Werte für das Betriebssystem sind in der folgenden Tabelle aufgeführt.



| Betriebssystem       | Wert  |
|------------------------|--------|
| 32-Bit-Windows (Win32) | 0x0002 |
| Macintosh              | 0x0001 |
| 16-Bit-Windows (Win16) | 0x0000 |



 

Bei Microsoft Windows-Betriebssystemen ist die Betriebssystemversion das von der Funktion " [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion) " zurückgegebene Wort mit niedriger Reihenfolge. Im folgenden Beispielcode wird für Microsoft Windows die Version des Ursprungs Betriebssystems ordnungsgemäß festgelegt.

``` syntax
#ifdef WIN32 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 2 ) ; 
#else 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 0 ) ; 
#endif
```

 

 