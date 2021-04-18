---
description: Die imagehlp-Funktionen werden hauptsächlich von Programmier Tools, Anwendungssetup-Hilfsprogramme und anderen Programmen verwendet, die Zugriff auf die in einem PE-Image enthaltenen Daten benötigen.
ms.assetid: 831d7bb2-bf01-4422-a940-173f9856a513
title: Informationen zu imagehlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76da517a396536640df0e9bfcfa05368e4d0b76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344593"
---
# <a name="about-imagehlp"></a>Informationen zu imagehlp

Die imagehlp-Funktionen werden hauptsächlich von Programmier Tools, Anwendungssetup-Hilfsprogramme und anderen Programmen verwendet, die Zugriff auf die in einem PE-Image enthaltenen Daten benötigen. Alle imagehlp-Funktionen sind Single Thread. Daher führen Aufrufe von mehr als einem Thread zu dieser Funktion wahrscheinlich zu unerwartetem Verhalten oder einer Beschädigung des Arbeitsspeichers. Um dies zu vermeiden, müssen Sie alle gleichzeitigen Aufrufe von mehr als einem Thread an diese Funktion synchronisieren.

In den folgenden Themen werden PE-Images und die von den imagehlp-Funktionen bereitgestellten Funktionen beschrieben.

-   [PE-Format](pe-format.md)
-   [Bild Zugriffs Funktionen](image-access-functions.md)
-   [Bild Integritäts Funktionen](image-integrity-functions.md)
-   [Funktionen zum Ändern von Bildern](image-modification-functions.md)

 

 



