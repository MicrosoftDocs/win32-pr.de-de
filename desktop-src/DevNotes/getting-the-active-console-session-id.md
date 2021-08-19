---
description: Die folgende Definition von "Skinl.h" ist die statische Speicheradresse der sitzungs-ID der aktiven Terminaldienstekonsole. Diese aktive Konsolensitzungs-ID ist in Versionen des Microsoft Windows Betriebssystems vor Windows XP nicht definiert.
ms.assetid: f3022ab8-60ea-490b-a87d-cc1afc99d26f
title: Abrufen der Sitzungs-ID der aktiven Konsole
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f7b23669240f0cd109a48f454ee6f6329f6839221a1677e81b75712430cb42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002300"
---
# <a name="getting-the-active-console-session-id"></a>Abrufen der Sitzungs-ID der aktiven Konsole

Die folgende Definition von "Skinl.h" ist die statische Speicheradresse der sitzungs-ID der aktiven Terminaldienstekonsole. Diese aktive Konsolensitzungs-ID ist in Versionen des Microsoft Windows Betriebssystems vor Windows XP nicht definiert.

> [!Note]  
> Diese Definition kann sich in zukünftigen Releases von Windows ändern. Um sicherzustellen, dass Ihre Anwendung in Zukunft weiterhin ordnungsgemäß ausgeführt wird, muss Ihre Anwendung [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid)aufrufen.

 

``` syntax
#define INTERNAL_TS_ACTIVE_CONSOLE_ID    
        (*((volatile ULONG*)(0x7ffe02d8)))
```

 

 
