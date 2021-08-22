---
title: Auswählen einer Protokollsequenz
description: Bewährte Methoden für die Auswahl einer Protokollsequenz umfassen die Verwendung von ncacn \_ ip \_ tcp und ncalrpc, nicht ncacn \_ np, ncacn \_ spx und ncadg \_ \ .
ms.assetid: 4b81b534-f001-4522-bf63-044bf5f414f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 732e00d46f1b471870447e228935a794db8d5dc5aa6486e3296b9936cd1be7cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932223"
---
# <a name="choosing-a-protocol-sequence"></a>Auswählen einer Protokollsequenz

**Bewährte Methode:** Verwenden Sie [**ncacn \_ ip \_ tcp,**](/windows/desktop/Midl/ncacn-ip-tcp) wenn Sie einen Remoteaufruf tätigen. Verwenden Sie [**ncalrpc**](/windows/desktop/Midl/ncalrpc) für lokale Aufrufe. Verwenden Sie weder [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np)noch [**ncacn \_ spx**](/windows/desktop/Midl/ncacn-spx)oder eine der **\_ \* ncadg-Protokollsequenzen.** Sie sind weniger effizient und verfügen über unwahrscheinliche Funktionen.

 

 