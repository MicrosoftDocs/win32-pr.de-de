---
description: Ein Musterpinsel (oder benutzerdefinierter Pinsel) wird aus einer von der Anwendung definierten Bitmap oder geräteunabhängigen Bitmap (Device-Independent Bitmap, DIB) erstellt. Die folgenden Rechtecke wurden mithilfe verschiedener Musterpinsel gezeichnet.
ms.assetid: 0de89a6f-d9c7-4f33-8088-c24a48a3ceee
title: Musterpinsel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48b7d5f3bc5c4b0fd86eda28a35bb56f02e5ba998353d36d829a71655aa66f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831520"
---
# <a name="pattern-brush"></a>Musterpinsel

Ein Musterpinsel (oder benutzerdefinierter Pinsel) wird aus einer von der Anwendung definierten Bitmap oder geräteunabhängigen Bitmap (Device-Independent Bitmap, DIB) erstellt. Die folgenden Rechtecke wurden mithilfe verschiedener Musterpinsel gezeichnet.

![Abbildung mit drei Feldern, die jeweils mit einem anderen Muster gefüllt sind](images/csbru-05.png)

Um einen logischen Musterpinsel zu erstellen, muss eine Anwendung zuerst eine Bitmap erstellen. Nach dem Erstellen der Bitmap kann die Anwendung den logischen Musterpinsel erstellen, indem sie die [**Funktion CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) oder [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) aufruft und ein Handle zur Identifizierung der Bitmap (oder DIB) angibt. Die Pinsel, die in der vorherigen Abbildung angezeigt werden, wurden aus monofarbigen Bitmaps erstellt. Eine Beschreibung der Bitmaps, DIBs und der Funktionen, die sie erstellen, finden Sie unter [Bitmaps](bitmaps.md).

 

 



