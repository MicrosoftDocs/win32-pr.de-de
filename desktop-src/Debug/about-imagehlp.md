---
description: Die ImageHlp-Funktionen werden hauptsächlich von Programmiertools, Hilfsprogrammen für die Anwendungseinrichtung und anderen Programmen verwendet, die Zugriff auf die in einem PE-Image enthaltenen Daten benötigen.
ms.assetid: 831d7bb2-bf01-4422-a940-173f9856a513
title: Informationen zu ImageHlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aee63eba22293fe1fb56cb6608110f4343a0c6bc26a4be597bfbd884cdf87cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815650"
---
# <a name="about-imagehlp"></a>Informationen zu ImageHlp

Die ImageHlp-Funktionen werden hauptsächlich von Programmiertools, Hilfsprogrammen für die Anwendungseinrichtung und anderen Programmen verwendet, die Zugriff auf die in einem PE-Image enthaltenen Daten benötigen. Alle ImageHlp-Funktionen sind Singlethreadfunktionen. Daher führen Aufrufe von mehr als einem Thread an diese Funktion wahrscheinlich zu unerwartetem Verhalten oder Speicherbeschädigung. Um dies zu vermeiden, müssen Sie alle gleichzeitigen Aufrufe von mehr als einem Thread mit dieser Funktion synchronisieren.

In den folgenden Themen werden PE-Images und die von den ImageHlp-Funktionen bereitgestellten Funktionen beschrieben.

-   [PE-Format](pe-format.md)
-   [Bildzugriffsfunktionen](image-access-functions.md)
-   [Bildintegritätsfunktionen](image-integrity-functions.md)
-   [Bildänderungsfunktionen](image-modification-functions.md)

 

 



