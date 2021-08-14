---
title: Abrufen von Kataloginformationen
description: Abrufen von Kataloginformationen
ms.assetid: f2ec795f-6e6f-4c0c-9332-f1e96524221a
keywords:
- Windows Media Player,Abrufen von Kataloginformationen
- Onlineshops,Abrufen von Kataloginformationen
- 'Typ 1: Onlineshops,Abrufen von Kataloginformationen'
- Windows Media Player,Diagnoseinformationen zu Katalogen
- Onlineshops,Diagnoseinformationen zu Katalogen
- 'Typ 1: Onlineshops,Diagnoseinformationen zu Katalogen'
- Windows Media Player Onlineshops,catcomp.exe
- Onlineshops,catcomp.exe
- Geben Sie 1 Onlineshops ein, catcomp.exe
- catcomp.exe
- Diagnoseinformationen zu Katalogen
- Abrufen von Kataloginformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3b28da6d2d5f5143dab0664c10d0c906f971a6a60e4fdb502f4331fa71f408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570201"
---
# <a name="retrieving-catalog-information"></a>Abrufen von Kataloginformationen

Sie können Diagnoseinformationen in einem Katalog anzeigen, indem Sie catcomp mit der folgenden Syntax ausführen:


```C++
catcomp info <catalogpath> [track|artist|album] [ID]
```



Der folgende Befehl zeigt z. B. Informationen zu einem gesamten Katalog an, einschließlich der Version, des Locale und interner Informationen zu Katalogelementen:


```C++
catcomp info C:\Catalog210\catalog.wmdb
```



Im Folgenden werden Informationen für die Spur mit der ID 3256 angezeigt:


```C++
catcomp info C:\Catalog210\catalog.wmdb track 3256
```



 

 




