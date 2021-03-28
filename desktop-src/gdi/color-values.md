---
description: Farbe ist als eine Kombination aus drei Primärfarben Rot, grün und Blau definiert.
ms.assetid: 6e44935c-2b3b-4062-8273-f1f3e70300d2
title: Farbwerte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e46cd7ee87871c660702bed120958e7096745d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130809"
---
# <a name="color-values"></a>Farbwerte

Farbe ist als eine Kombination aus drei Primärfarben Rot, grün und Blau definiert. Das System identifiziert eine Farbe, indem es einen Farbwert (manchmal als RGB-dreier bezeichnet) angibt, der aus 3 8-Bit-Werten besteht, die die Intensitäten der Farbkomponenten angeben. Schwarz hat die minimale Intensität für Rot, grün und blau, sodass der Farbwert für schwarz (0,0) ist. Weiß hat die maximale Intensität für Rot, grün und blau, sodass der Farbwert (255, 255, 255) ist.

> [!Note]  
> Wenn Bild Farbabgleich aktiviert ist, hängt die Definition der Farbe und die Bedeutung eines Farbwerts vom Typ des Farbraum ab, der derzeit für den Gerätekontext festgelegt ist.

 

Das System und die Anwendungen verwenden Parameter und Variablen mit dem [COLORREF](colorref.md) -Typ, um Farbwerte zu übergeben und zu speichern. Beispielsweise identifiziert die [**enumubjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) -Funktion die Farbe jedes Stifts, indem der **lopncolor** -Member in einer [**logpen**](/windows/win32/api/wingdi/ns-wingdi-logpen) -Struktur auf einen Farbwert festgelegt wird. Anwendungen können die einzelnen Werte der roten, grünen und blauen Komponenten aus einem Farbwert extrahieren, indem Sie die-Makros [**getrvalue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [**getgvalue**](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)und [**getbvalue**](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) verwenden. Anwendungen können mit dem [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) -Makro einen Farbwert aus einzelnen Komponenten Werten erstellen. Beim Erstellen oder untersuchen einer logischen Palette verwendet eine Anwendung die [**rgbquad**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) -Struktur, um Farbwerte zu definieren und einzelne Komponenten Werte zu untersuchen.

 

 



