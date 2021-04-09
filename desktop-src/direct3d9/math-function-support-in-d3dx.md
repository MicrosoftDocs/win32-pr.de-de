---
description: D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bereitstellt. Es handelt sich um eine Ebene oberhalb der Direct3D-Komponente.
ms.assetid: a44d25de-f79d-4132-a75a-0c22ccd84341
title: Unterstützung mathematischer Funktionen in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac69e0385919b015d1f8d3e7d47e221c06a04fbb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124477"
---
# <a name="math-function-support-in-d3dx-direct3d-9"></a>Unterstützung mathematischer Funktionen in D3DX (Direct3D 9)

D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bereitstellt. Es handelt sich um eine Ebene oberhalb der Direct3D-Komponente.

## <a name="math"></a>Mathematik

Mathematische Unterstützung, die in einer Reihe von Funktionen enthalten ist, wird für Folgendes bereitgestellt:

-   Farb Berechnungen
-   Back
-   Matrix Bearbeitung
-   Quaternionen
-   2D-Vektoren
-   3D-Vektoren
-   4D-Vektoren

Beachten Sie, dass bei einer Verbindung mit den C++-über Ladungen die Unterstützung für grundlegende 3D-mathematische Typen sehr umfangreich ist.

Weitere Informationen zu diesen Funktionen finden Sie unter [D3DX Functions](dx9-graphics-reference-d3dx-functions.md). Um die benötigte Funktion zu finden, werden Sie in mehreren Ordnern untergliedert.

## <a name="float16"></a>FLOAT16

Bei Verwendung des FLOAT16-Datentyps sollten Sie die Werte auf maximal D3DX \_ 16f begrenzen \_ . Alle FLOAT16-Werte, die diesen Wert überschreiten, führen zu einem nicht definierten Verhalten in der Pipeline. Siehe [andere D3DX-Konstanten](other-d3dx-constants.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 



