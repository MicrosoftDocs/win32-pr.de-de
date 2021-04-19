---
description: Standardmäßig sind die Windows Search-Engine und der-Katalog nicht mit diakritischen Zeichen versehen, bei denen es sich um Akzente zum Ändern der Bedeutung oder Aussprache eines Worts handelt.
ms.assetid: 71007bd4-5232-469c-982b-ff0d24bd0c1f
title: Diakritische Empfindlichkeit bei Such Vorgängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46fb68676418fc109fa24ed2d55fb9602b7ad41d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346497"
---
# <a name="diacritic-sensitivity-in-searches"></a>Diakritische Empfindlichkeit bei Such Vorgängen

Standardmäßig sind die Windows Search-Engine und der-Katalog nicht mit diakritischen Zeichen versehen, bei denen es sich um Akzente zum Ändern der Bedeutung oder Aussprache eines Worts handelt. Mithilfe von Windows Search können Sie dies jedoch für Ihren Katalog ändern, indem Sie den [Katalog-Manager](-search-3x-wds-mngidx-catalog-manager.md) verwenden, um die diakritische Empfindlichkeit festzulegen. Wenn z. b. die diakritische Sensitivität auf **false** festgelegt ist, würde der Katalog "Resume" und "Resumé" so behandeln, als wären Sie das gleiche Wort.

Auf der Abfrage Ebene werden Abfrage Begriffe mit Diakritik in fretext-und enthält-Klauseln an die-Engine weitergegeben und dann normalisiert (wie Sie bei der Index Zeit), um Übereinstimmungen abzugleichen. Die Übereinstimmung mit dem Katalog ist immer diakritisch sensibel.

> [!Note]  
> Dies ist für die Zeichen Bereiche 0x2e81-F8FF liegt und 0x1100-0x11ff nicht der Fall.

 

 

 



