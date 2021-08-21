---
description: Standardmäßig sind die Windows Search-Engine und der Katalog nicht von diakritischen Zeichen, bei denen es sich um Akzente handelt, die Buchstaben hinzugefügt werden, um die Bedeutung oder Aussprache eines Worts zu ändern.
ms.assetid: 71007bd4-5232-469c-982b-ff0d24bd0c1f
title: Diakritische Empfindlichkeit bei Suchvorgängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fcde4eb6cde6fe7a0b25a1d58f8026176de2fe30b6b0e2f020275821891a404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863683"
---
# <a name="diacritic-sensitivity-in-searches"></a>Diakritische Empfindlichkeit bei Suchvorgängen

Standardmäßig sind die Windows Search-Engine und der Katalog nicht von diakritischen Zeichen, bei denen es sich um Akzente handelt, die Buchstaben hinzugefügt werden, um die Bedeutung oder Aussprache eines Worts zu ändern. Mit der Windows können Sie dies jedoch für Ihren Katalog ändern, indem Sie den [Katalog-Manager](-search-3x-wds-mngidx-catalog-manager.md) verwenden, um die diakritische Vertraulichkeit zu aktivieren. Wenn die diakritische Empfindlichkeit beispielsweise auf **FALSE** festgelegt ist, behandelt der Katalog "resume" und "resumé" so, als wären sie dasselbe Wort.

Auf Abfrageebene werden Abfragebegriffe mit diakritischen Zeichen in FREETEXT- und CONTAINS-Klauseln an die Engine übergeben und dann normalisiert (wie sie zur Indexzeit wären) für den Abgleich. Der Abgleich mit dem Katalog ist immer diakritischer.

> [!Note]  
> Dies gilt nicht für die Zeichenbereiche 0x2e81-f8ff und 0x1100-0x11ff.

 

 

 



