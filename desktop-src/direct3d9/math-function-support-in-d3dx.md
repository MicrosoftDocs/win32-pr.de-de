---
description: Erfahren Sie mehr über die Unterstützung mathematischer Funktionen in D3DX. D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bereitstellt. Es handelt sich um eine Ebene oberhalb der Direct3D-Komponente.
ms.assetid: a44d25de-f79d-4132-a75a-0c22ccd84341
title: Unterstützung mathematischer Funktionen in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c77e3d75c692d4801e6a8af64bd980e72eb88f0d3276ff4e1364302b5a62357d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119368970"
---
# <a name="math-function-support-in-d3dx-direct3d-9"></a>Unterstützung mathematischer Funktionen in D3DX (Direct3D 9)

D3DX ist eine Hilfsprogrammbibliothek, die Hilfsdienste bereitstellt. Es handelt sich um eine Ebene oberhalb der Direct3D-Komponente.

## <a name="math"></a>Mathematik

Mathematische Unterstützung, die in einer Reihe von Funktionen enthalten ist, wird für:

-   Farbberechnungen
-   Flugzeuge
-   Matrixbearbeitung
-   Quaternionen
-   2D-Vektoren
-   3D-Vektoren
-   4D-Vektoren

Beachten Sie, dass in Verbindung mit den C++-Überladungen die Unterstützung für grundlegende 3D-Mathematische Typen umfangreich ist.

Weitere Informationen zu diesen Funktionen finden Sie unter [D3DX-Funktionen.](dx9-graphics-reference-d3dx-functions.md) Um die benötigte Funktion zu finden, werden sie in mehrere Ordner aufgeteilt.

## <a name="float16"></a>FLOAT16

Wenn Sie den FLOAT16-Datentyp verwenden, achten Sie darauf, die Werte auf ein Maximum von D3DX \_ 16F MAX zu \_ beschränken. Jeder FLOAT16-Wert, der diesen wert überschreitet, führt zu einem nicht definierten Verhalten in der Pipeline. Weitere Informationen finden Sie unter [Andere D3DX-Konstanten.](other-d3dx-constants.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3dx](d3dx.md)
</dt> </dl>

 

 



