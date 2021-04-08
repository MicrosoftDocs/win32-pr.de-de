---
title: Abrufen von Katalog Informationen
description: Abrufen von Katalog Informationen
ms.assetid: f2ec795f-6e6f-4c0c-9332-f1e96524221a
keywords:
- Windows Media Player Online Stores, Abrufen von Katalog Informationen
- Online Stores, Abrufen von Katalog Informationen
- Typ 1 Online Stores, Abrufen von Katalog Informationen
- Windows Media Player Online Stores, Diagnoseinformationen zu Katalogen
- Online Stores, Diagnoseinformationen zu Katalogen
- Typ 1 Online Stores, Diagnoseinformationen zu Katalogen
- Windows Media Player Online Stores catcomp.exe
- Online Stores, catcomp.exe
- Geben Sie 1 Online Stores, catcomp.exe
- catcomp.exe
- Diagnoseinformationen zu Katalogen
- Abrufen von Katalog Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e721d6ba3e4d6b5106cf44446d4c96ed842ccd61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712726"
---
# <a name="retrieving-catalog-information"></a>Abrufen von Katalog Informationen

Sie können Diagnoseinformationen in einem Katalog anzeigen, indem Sie "" mit der folgenden Syntax ausführen:


```C++
catcomp info <catalogpath> [track|artist|album] [ID]
```



Der folgende Befehl zeigt z. b. Informationen zu einem gesamten Katalog an, einschließlich Version, Gebiets Schema und interne Informationen zu Katalog Elementen:


```C++
catcomp info C:\Catalog210\catalog.wmdb
```



Im folgenden werden die Informationen für den Titel mit der ID 3256 angezeigt:


```C++
catcomp info C:\Catalog210\catalog.wmdb track 3256
```



 

 




