---
title: Auswählen einer Protokoll Sequenz
description: Zu den bewährten Methoden für die Auswahl einer Protokoll Sequenz gehört die Verwendung von ncacn \_ IP \_ TCP und Ncalrpc, nicht ncacn \_ NP, ncacn \_ SPX und ncadg \_ \.
ms.assetid: 4b81b534-f001-4522-bf63-044bf5f414f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3dea44868b96361ccaddc6e339f94fde92704f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039523"
---
# <a name="choosing-a-protocol-sequence"></a>Auswählen einer Protokoll Sequenz

**Bewährte Methoden:** Verwenden Sie [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp) beim Ausführen eines Remote Aufrufes. Verwenden Sie [**Ncalrpc**](/windows/desktop/Midl/ncalrpc) für lokale Aufrufe. Verwenden Sie nicht [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np), [**ncacn \_ SPX**](/windows/desktop/Midl/ncacn-spx)oder eine der **ncadg \_ \*** -Protokoll Sequenzen, Sie sind weniger effizient und verfügen über untergeordnete Funktionen.

 

 