---
description: Farbe wird als Kombination aus drei Primärfarben rot, grün und blau definiert.
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

Farbe wird als Kombination aus drei Primärfarben rot, grün und blau definiert. das System identifiziert eine Farbe, indem es ihr einen Farbwert (manchmal auch als RGB-Triplet bezeichnet) gibt, der aus drei 8-Bit-Werten besteht, die die Intensitäten ihrer Farbkomponenten angeben. Schwarz hat die minimale Intensität für Rot, Grün und Blau, daher ist der Farbwert für Schwarz (0, 0, 0). Weiß hat die maximale Intensität für Rot, Grün und Blau, daher ist der Farbwert (255, 255, 255).

> [!Note]  
> Wenn der Abgleich von Bildfarben aktiviert ist, hängen die Definition der Farbe und die Bedeutung eines Farbwerts vom Typ des Farbraums ab, der derzeit für den Gerätekontext festgelegt ist.

 

Das System und die Anwendungen verwenden Parameter und Variablen mit dem [COLORREF-Typ,](colorref.md) um Farbwerte zu übergeben und zu speichern. Die [**EnumObjects-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) identifiziert z. B. die Farbe jedes Stifts, indem das **lopnColor-Member** in einer [**LOGPEN-Struktur**](/windows/win32/api/wingdi/ns-wingdi-logpen) auf einen Farbwert festlegen. Anwendungen können die einzelnen Werte der roten, grünen und blauen Komponenten mithilfe der Makros [**GetRValue,**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue) [**GetGValue**](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)und [**GetBValue**](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) aus einem Farbwert extrahieren. Anwendungen können mithilfe des RGB-Makros einen Farbwert aus einzelnen [**Komponentenwerten**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) erstellen. Beim Erstellen oder Untersuchen einer logischen Palette verwendet eine Anwendung die [**RGBQUAD-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) um Farbwerte zu definieren und einzelne Komponentenwerte zu untersuchen.

 

 



