---
description: Ein Muster (oder benutzerdefinierter) Pinsel wird aus einer Anwendungs definierten Bitmap oder einer geräteunabhängigen Bitmap (DIB) erstellt. Die folgenden Rechtecke wurden mit unterschiedlichen Muster Pinseln gezeichnet.
ms.assetid: 0de89a6f-d9c7-4f33-8088-c24a48a3ceee
title: Muster Pinsel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d39dd499d6a95b3fb61624b2aab8b421f51c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988178"
---
# <a name="pattern-brush"></a>Muster Pinsel

Ein Muster (oder benutzerdefinierter) Pinsel wird aus einer Anwendungs definierten Bitmap oder einer geräteunabhängigen Bitmap (DIB) erstellt. Die folgenden Rechtecke wurden mit unterschiedlichen Muster Pinseln gezeichnet.

![Abbildung, die drei Felder anzeigt, die jeweils mit einem anderen Muster gefüllt sind](images/csbru-05.png)

Zum Erstellen eines logischen Muster Pinsels muss eine Anwendung zuerst eine Bitmap erstellen. Nach dem Erstellen der Bitmap kann die Anwendung den logischen Muster Pinsel erstellen, indem Sie die [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) -oder [**createdibpatternbrushpt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) -Funktion aufrufen und ein Handle bereitstellen, das die Bitmap (oder DIB) identifiziert. Die Pinsel, die in der obigen Abbildung angezeigt werden, wurden aus Monochrom-Bitmaps erstellt. Eine Beschreibung der Bitmaps, Disb und der Funktionen, die Sie erstellen, finden Sie unter [Bitmaps](bitmaps.md).

 

 



