---
description: Das Farbattribut gibt die Farbe des Stifts an.
ms.assetid: ce775359-65fc-40d0-8725-b392cc0464a6
title: Stiftfarbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e88d73fc80f6fe02a6d9e1de1d33568c94e05768f113c8bee0754c5d8afb418
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117886205"
---
# <a name="pen-color"></a>Stiftfarbe

Das Farbattribut gibt die Farbe des Stifts an. Eine Anwendung kann einen farbigen Stift mit einer eindeutigen Farbe erstellen, indem das [**RGB-Makro**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) verwendet wird, um das rote, grüne und blaue Triplet zu speichern, das die gewünschte Farbe in einer [COLORREF-Struktur](colorref.md) angibt und die Adresse dieser Struktur an die [**CreatePen-,**](/windows/desktop/api/Wingdi/nf-wingdi-createpen) [**CreatePenIndirect-**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)oder [**ExtCreatePen-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) übergibt. (Die Stockstifte sind auf Schwarz, Weiß und unsichtbar beschränkt.) Weitere Informationen zu RGB-Triplets und -Farben finden Sie unter [Farben.](colors.md)

 

 



