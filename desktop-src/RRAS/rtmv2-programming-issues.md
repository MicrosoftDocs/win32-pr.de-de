---
title: RTMv2-Programmierprobleme
description: RTMv2-Funktionen werden mit den folgenden Annahmen geschrieben.
ms.assetid: c8c6f553-57cc-4eec-bbc0-b6b50897cc75
keywords:
- Programmierprobleme, RTMv2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b607adc939ff72a4d9fee99c15f6aa5192fa4c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309963"
---
# <a name="rtmv2-programming-issues"></a>RTMv2-Programmierprobleme

RTMv2-Funktionen werden mit den folgenden Annahmen geschrieben.

-   RTMv2-Funktionen weisen keinen Arbeitsspeicher für den Client zu. Der Client muss immer Arbeitsspeicher zuweisen.
-   Wenn die Registrierung eines Clients aufgehoben wird, muss er Bereinigungs Vorgänge selbst durchführen, z. b. den gesamten zugeordneten Arbeitsspeicher freigeben.
-   Clients müssen Handles ordnungsgemäß freigeben. Speicher Verluste können auftreten, wenn ein Client diese Vorgehensweise nicht beachtet.

 

 




