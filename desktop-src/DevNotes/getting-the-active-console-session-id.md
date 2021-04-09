---
description: Die folgende "winternl. h"-Definition ist die statische Speicheradresse der aktiven Terminal Dienste-Konsolen Sitzungs-ID. Diese aktive Konsolen Sitzungs-ID ist nicht in Versionen des Microsoft Windows-Betriebssystems vor Windows XP definiert.
ms.assetid: f3022ab8-60ea-490b-a87d-cc1afc99d26f
title: Die ID der aktiven Konsolen Sitzung wird erhalten.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936db3f8038348864fc90fc55eeb4287a67c45d6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860996"
---
# <a name="getting-the-active-console-session-id"></a>Die ID der aktiven Konsolen Sitzung wird erhalten.

Die folgende "winternl. h"-Definition ist die statische Speicheradresse der aktiven Terminal Dienste-Konsolen Sitzungs-ID. Diese aktive Konsolen Sitzungs-ID ist nicht in Versionen des Microsoft Windows-Betriebssystems vor Windows XP definiert.

> [!Note]  
> Diese Definition kann sich in zukünftigen Versionen von Windows ändern. Um sicherzustellen, dass Ihre Anwendung in Zukunft weiterhin ordnungsgemäß ausgeführt wird, muss die Anwendung [**WFS getactiveconsolesessionid**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid)aufrufen.

 

``` syntax
#define INTERNAL_TS_ACTIVE_CONSOLE_ID    
        (*((volatile ULONG*)(0x7ffe02d8)))
```

 

 
