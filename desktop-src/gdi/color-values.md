---
description: Farbe ist als Kombination aus drei Primärfarben rot, grün und blau definiert.
ms.assetid: 6e44935c-2b3b-4062-8273-f1f3e70300d2
title: Farbwerte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b1518060e1ad4af7ada1c244ecdcac742f27a36133080f31199714dd8059d5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761930"
---
# <a name="color-values"></a>Farbwerte

Farbe ist als Kombination aus drei Primärfarben rot, grün und blau definiert. das System identifiziert eine Farbe, indem es ihm einen Farbwert (manchmal auch als RGB-Triplet bezeichnet) gibt, der aus drei 8-Bit-Werten besteht, die die Intensitäten seiner Farbkomponenten angeben. Schwarz hat die minimale Intensität für Rot, Grün und Blau, sodass der Farbwert für Schwarz (0, 0, 0) ist. Weiß weist die maximale Intensität für Rot, Grün und Blau auf, sodass der Farbwert (255, 255, 255) lautet.

> [!Note]  
> Wenn der Farbabgleich für Bilder aktiviert ist, hängt die Definition der Farbe und die Bedeutung eines Farbwerts vom Typ des Farbraums ab, der derzeit für den Gerätekontext festgelegt ist.

 

Das System und die Anwendungen verwenden Parameter und Variablen mit dem [COLORREF-Typ,](colorref.md) um Farbwerte zu übergeben und zu speichern. Die [**EnumObjects-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) identifiziert z. B. die Farbe jedes Stifts, indem der **lopnColor-Member** in einer [**LOGPEN-Struktur**](/windows/win32/api/wingdi/ns-wingdi-logpen) auf einen Farbwert festgelegt wird. Anwendungen können die einzelnen Werte der roten, grünen und blauen Komponenten aus einem Farbwert extrahieren, indem sie die Makros [**GetRValue,**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue) [**GetGValue**](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)bzw. [**GetBValue**](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) verwenden. Anwendungen können mithilfe des [**RGB-Makros**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) einen Farbwert aus einzelnen Komponentenwerten erstellen. Beim Erstellen oder Untersuchen einer logischen Palette verwendet eine Anwendung die [**RGBQUAD-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) um Farbwerte zu definieren und einzelne Komponentenwerte zu untersuchen.

 

 



