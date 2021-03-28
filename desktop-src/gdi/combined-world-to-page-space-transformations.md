---
description: Die fünf Welt-zu-Seite-Transformationen können zu einer einzigen 3-x-3-Matrix kombiniert werden.
ms.assetid: d17ba826-8e8d-4121-8afd-0f256121b54c
title: Kombinierte Transformationen für Welt-zu-Seite-Raum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b770ef614fe1538a528de640cacc5ad54b28c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978729"
---
# <a name="combined-world-to-page-space-transformations"></a>Kombinierte Transformationen für Welt-zu-Seite-Raum

Die fünf Welt-zu-Seite-Transformationen können zu einer einzigen 3-x-3-Matrix kombiniert werden. Die [**combinetransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform) -Funktion kann verwendet werden, um zwei Welt Raum Transformationen mit Seiten Raum Transformationen zu kombinieren. Die kombinierten Transformationen können verwendet werden, um die Ausgabe eines bestimmten Geräte Kontexts (DC) zu ändern, indem die [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) -Funktion aufgerufen und die Elemente für diese Matrix bereitgestellt werden. Wenn eine Anwendung **setworldtransform** aufruft, speichert Sie die Elemente der 3 x 3-Matrix in einer [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) -Struktur. Die Elemente dieser Struktur entsprechen den ersten beiden Spalten einer 3-mal-3-Matrix. die letzte Spalte der Matrix ist nicht erforderlich, da ihre Werte konstant sind.

Die Elemente der Transformationsmatrix der aktuellen Welt können durch Aufrufen der [**getworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform) -Funktion und Bereitstellen eines Zeigers auf eine [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) -Struktur wiederbelebt werden.

 

 



