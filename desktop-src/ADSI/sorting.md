---
title: Sortieren (ADSI)
description: Ein Client kann einen Server anfordern, um das Resultset zu sortieren.
ms.assetid: 795d27f0-0bfa-417e-aa1f-f2471f92dc45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555b4b6f1868b2e4fddc1891cdf349ef6f44bc47dca6eb80e021ec49cb91b5d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082224"
---
# <a name="sorting-adsi"></a>Sortieren (ADSI)

Ein Client kann einen Server anfordern, um das Resultset zu sortieren. Sie können Folgendes angeben:

-   Sortierreihenfolge: Die Sortierreihenfolge kann entweder aufsteigend oder absteigend angegeben werden.
-   Sortierattribute: Mehrere Attribute können in einer Sortierzeichenfolge angegeben werden. Sortieren Sie z. B. nach Nachname und dann nach Vorname.

Wenn Sie die Sortierreihenfolge angeben, sollten Sie versuchen, eines der indizierten Attribute zu verwenden. Andernfalls muss der Server ein vollständiges Resultset berechnen, bevor es an den Client gesendet wird. Dies gilt auch, wenn Sie eine seitenseitige Suche angefordert und eine Seitengröße angegeben haben.

> [!Note]  
> Nicht alle Verzeichnisserver unterstützen mehrere Attributsortier- oder Sortierreihenfolge.

 

 

 




