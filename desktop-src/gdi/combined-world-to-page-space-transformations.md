---
description: Die fünf Welt-zu-Seite-Transformationen können in einer einzelnen 3 by 3-Matrix kombiniert werden.
ms.assetid: d17ba826-8e8d-4121-8afd-0f256121b54c
title: Kombinierte Welt-zu-Seite-Raumtransformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70be3bca8687b89bbb2a50fefaaae70fea9b5f86c1762c4414a3974793ea8d32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117887500"
---
# <a name="combined-world-to-page-space-transformations"></a>Kombinierte Welt-zu-Seite-Raumtransformationen

Die fünf Welt-zu-Seite-Transformationen können in einer einzelnen 3 by 3-Matrix kombiniert werden. Die [**CombineTransform-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform) kann verwendet werden, um zwei Transformationen zwischen Welt- und Seitenraum zu kombinieren. Die kombinierten Transformationen können verwendet werden, um die Ausgabe zu ändern, die einem bestimmten Gerätekontext (DC) zugeordnet ist, indem die [**SetWorldTransform-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) aufruft und die Elemente für diese Matrix übergeben werden. Wenn eine Anwendung **SetWorldTransform aufruft,** speichert sie die Elemente der 3 by 3-Matrix in einer [**XFORM-Struktur.**](/windows/win32/api/wingdi/ns-wingdi-xform) Die Member dieser Struktur entsprechen den ersten beiden Spalten einer 3:3-Matrix. Die letzte Spalte der Matrix ist nicht erforderlich, da ihre Werte konstant sind.

Die Elemente der aktuellen Welttransformationsmatrix können durch Aufrufen der [**GetWorldTransform-Funktion und**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform) durch Die Bereitstellung eines Zeigers auf eine [**XFORM-Struktur umgeformt**](/windows/win32/api/wingdi/ns-wingdi-xform) werden.

 

 



