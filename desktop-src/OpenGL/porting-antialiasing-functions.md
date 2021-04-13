---
title: Portieren von Antialiasing-Funktionen
description: Portieren von Antialiasing-Funktionen
ms.assetid: 7f79f0fa-4a08-4678-bc73-8611e8d9e91a
keywords:
- IRIS GL portieren, Antialiasing
- Portieren von IRIS GL, Antialiasing
- Portieren auf OpenGL von IRIS GL, Antialiasing
- OpenGL-Portierung von IRIS GL, Antialiasing
- Antialiasing (antialiasing)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec2fcae4fe7b6909e00efb0fb892821a5c12765
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388731"
---
# <a name="porting-antialiasing-functions"></a>Portieren von Antialiasing-Funktionen

In OpenGL ist der subpixelmodus immer eingeschaltet. Folglich ist das IRIS GL- **funktionssubpixel**(**true**) nicht erforderlich und hat keine OpenGL-Entsprechung. In den folgenden Themen werden Aspekte der Portierung von IRIS GL-Antialiasing-Code beschrieben.

-   [Portieren von Mischungs Code](porting-blending-code.md)
-   [Portieren von Test Funktionen](porting-afunction-test-functions.md)
-   [Verwenden von Antialiasing-Funktionen](using-antialiasing-functions.md)

 

 




