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
# <a name="combined-world-to-page-space-transformations"></a><span data-ttu-id="89855-103">Kombinierte Transformationen für Welt-zu-Seite-Raum</span><span class="sxs-lookup"><span data-stu-id="89855-103">Combined World-to-Page Space Transformations</span></span>

<span data-ttu-id="89855-104">Die fünf Welt-zu-Seite-Transformationen können zu einer einzigen 3-x-3-Matrix kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="89855-104">The five world-to-page transformations can be combined into a single 3-by-3 matrix.</span></span> <span data-ttu-id="89855-105">Die [**combinetransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform) -Funktion kann verwendet werden, um zwei Welt Raum Transformationen mit Seiten Raum Transformationen zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="89855-105">The [**CombineTransform**](/windows/desktop/api/Wingdi/nf-wingdi-combinetransform) function can be used to combine two world-space to page-space transformations.</span></span> <span data-ttu-id="89855-106">Die kombinierten Transformationen können verwendet werden, um die Ausgabe eines bestimmten Geräte Kontexts (DC) zu ändern, indem die [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) -Funktion aufgerufen und die Elemente für diese Matrix bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="89855-106">The combined transformations can be used to alter output associated with a particular device context (DC) by calling the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function and supplying the elements for this matrix.</span></span> <span data-ttu-id="89855-107">Wenn eine Anwendung **setworldtransform** aufruft, speichert Sie die Elemente der 3 x 3-Matrix in einer [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="89855-107">When an application calls **SetWorldTransform**, it stores the elements of the 3-by-3 matrix in an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure.</span></span> <span data-ttu-id="89855-108">Die Elemente dieser Struktur entsprechen den ersten beiden Spalten einer 3-mal-3-Matrix. die letzte Spalte der Matrix ist nicht erforderlich, da ihre Werte konstant sind.</span><span class="sxs-lookup"><span data-stu-id="89855-108">The members of this structure correspond to the first two columns of a 3-by-3 matrix; the last column of the matrix is not required because its values are constant.</span></span>

<span data-ttu-id="89855-109">Die Elemente der Transformationsmatrix der aktuellen Welt können durch Aufrufen der [**getworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform) -Funktion und Bereitstellen eines Zeigers auf eine [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) -Struktur wiederbelebt werden.</span><span class="sxs-lookup"><span data-stu-id="89855-109">The elements of the current world transformation matrix can be revived by calling the [**GetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-getworldtransform) function and supplying a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure.</span></span>

 

 



