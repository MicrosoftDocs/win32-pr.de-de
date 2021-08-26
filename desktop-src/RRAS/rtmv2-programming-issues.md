---
title: RTMv2-Programmierprobleme
description: RTMv2-Funktionen werden mit den folgenden Annahmen geschrieben.
ms.assetid: c8c6f553-57cc-4eec-bbc0-b6b50897cc75
keywords:
- Programmierprobleme, RTMv2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 584568fc3c4e7a46a2a2114781b81465d893b80978471aa3149d93d38f0c8c5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035590"
---
# <a name="rtmv2-programming-issues"></a>RTMv2-Programmierprobleme

RTMv2-Funktionen werden mit den folgenden Annahmen geschrieben.

-   RTMv2-Funktionen weisen dem Client keinen Arbeitsspeicher zu. Der Client muss immer Arbeitsspeicher zuweisen.
-   Wenn die Registrierung eines Clients aufgehoben wird, muss er Bereinigungsvorgänge selbst durchführen, z. B. das Freigeben des zugeordneten Arbeitsspeichers.
-   Clients müssen Handles ordnungsgemäß veröffentlichen. Speicherverlusten können auftreten, wenn ein Client diese Vorgehensweise nicht beachtet.

 

 




