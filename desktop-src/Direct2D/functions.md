---
title: Direct2D-Funktionen
description: Direct2D stellt die folgenden Funktionen zur Verfügung.
ms.assetid: 1a7ae962-9b70-442c-a676-f172a2d9bfd3
keywords:
- Direct2D, Functions
ms.topic: article
ms.date: 09/19/2019
ms.openlocfilehash: 7df417bbaba8c442f61005b35900641c379da9d7b61fa91e898d41e0d73821d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874480"
---
# <a name="direct2d-functions"></a>Direct2D-Funktionen

Direct2D stellt die folgenden Funktionen zur Verfügung. Zusätzliche Funktionen werden im [D2D1-Namespace definiert.](d2d1-namespace.md)

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|-|-|
| [**D2D1ComputeMaximumScaleFactor**](/windows/desktop/api/d2d1_2/nf-d2d1_2-d2d1computemaximumscalefactor) | Berechnet den maximalen Faktor, um den eine bestimmte Transformation einen beliebigen Vektor strecken kann. |
| [**D2D1CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) | Erstellt ein neues Direct2D-Gerät, das dem bereitgestellten DXGI-Gerät zugeordnet ist.  |
| [**D2D1CreateDeviceContext**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevicecontext) | Erstellt einen neuen Direct2D-Gerätekontext, der einer DXGI-Oberfläche zugeordnet ist.  |
| [**D2D1CreateFactory(D2D1_FACTORY_TYPE,REFIID,void \* \* )**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory-r1) | Erstellt ein Factoryobjekt, das zum Erstellen von Direct2D-Ressourcen verwendet werden kann. |
| [**D2D1CreateFactory(D2D1_FACTORY_TYPE,REFIID,D2D1_FACTORY_OPTIONS \* ,void \* \* )**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) | Erstellt ein Factoryobjekt, das zum Erstellen von Direct2D-Ressourcen verwendet werden kann. |
| [**D2D1GetGradientMeshInteriorPointsFromCoonsPatch**](/windows/desktop/api/d2d1_3/nf-d2d1_3-d2d1getgradientmeshinteriorpointsfromcoonspatch) | Gibt die inneren Punkte für einen Farbverlaufsgitterpatch basierend auf den Punkten zurück, die einen Coons-Patch definieren. |
| [**D2D1InvertMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1invertmatrix) | Versucht, die angegebene Matrix rückgängig zu machen. |
| [**D2D1IsMatrixInvertible**](/windows/desktop/api/d2d1/nf-d2d1-d2d1ismatrixinvertible) | Gibt an, ob die angegebene Matrix invertierbar ist. |
| [**D2D1MakeRotateMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1makerotatematrix) | Erstellt eine Drehungstransformation, die um den angegebenen Winkel um den angegebenen Punkt gedreht wird. |
| [**D2D1MakeSkewMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1makeskewmatrix) | Erstellt eine Schiefetransformation mit dem angegebenen Winkel der x-Achse, dem Winkel der Y-Achse und dem Mittelpunkt.  |
| [**operator \* (const D2D1\MATRIX\3X2\F&,const D2D1\MATRIX\3X2\F&)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-setproduct) | Multipliziert zwei Matrizen und gibt das Ergebnis zurück. |
| [**BlobGetter**](blobgetter.md) | Ruft einen Getterrückruf der Memberfunktionseigenschaft für eine Blobtypeigenschaft auf. |
| [**BlobSetter**](blobsetter.md) | Ruft einen Memberfunktions-Eigenschaftens setter-Rückruf für eine Blobtypeigenschaft auf. |
| [**DeducingBlobGetter**](deducingblobgetter.md) | Deduces the class and arguments and then calls a member-function property getter callback for a blob-type property. |
| [**DeducingBlobSetter**](deducingblobsetter.md) | Deduces the class and arguments and then calls a member-function property setter callback for a blob-type property. |
| [**DeducingStringGetter**](deducingstringgetter.md) | Deduces the class and arguments and then calls a member-function property getter callback for a string-type property. |
| [**DeducingStringSetter**](deducingstringsetter.md) | Deduces the class and arguments and then calls a member-function property setter callback for a string-type property. |
| [**DeducingValueGetter**](deducingvaluegetter.md) | Deduces the class and arguments and then calls a member-function property getter callback for a value-type property. |
| [**DeducingValueSetter**](deducingvaluesetter.md) | Deduces the class and arguments and then calls a member-function property setter callback for a value-type property. |
| [**Gettype**](/previous-versions/windows/desktop/legacy/hh847962(v=vs.85)) | Ruft den Typ der angegebenen Eigenschaft ab. |
| [**StringGetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-stringgetter) | Ruft einen Getterrückruf der Memberfunktionseigenschaft für eine Eigenschaft vom Typ string auf. |
| [**StringSetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-stringsetter) | Ruft einen Memberfunktions-Eigenschaftens setter-Rückruf für eine Zeichenfolgentypeigenschaft auf. |
| [**ValueGetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-valuegetter) | Ruft einen Memberfunktions-Eigenschaftens setter-Rückruf für eine Werttypeigenschaft auf. |
| [**ValueSetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-valuesetter) | Ruft einen Memberfunktions-Eigenschaftens setter-Rückruf für eine Werttypeigenschaft auf. |
| [**D2D1ConvertColorSpace**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1convertcolorspace) | Konvertiert die gegebene Farbe von einem Farbraum in einen anderen. |
| [**D2D1SinCos**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1sincos) | Gibt den Sinus und den Kosinus eines Winkels zurück. |
| [**D2D1Tan**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1tan) | Gibt den Tangens eines Winkels zurück. |
| [**D2D1Vec3Length**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1vec3length) | Gibt die Länge eines dreidimensionalen Vektors zurück. |
| [**PD2D1\PROPERTY\GET\FUNCTION**](/windows/desktop/api/D2d1effectauthor/nc-d2d1effectauthor-pd2d1_property_get_function) | Ruft eine Eigenschaft aus einem Effekt ab. |
| [**PD2D1\PROPERTY\SET\FUNCTION**](/windows/desktop/api/D2d1effectauthor/nc-d2d1effectauthor-pd2d1_property_set_function) | Legt eine Eigenschaft für einen Effekt fest. |