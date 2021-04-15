---
title: Direct2D-Funktionen
description: Direct2D bietet die folgenden Funktionen.
ms.assetid: 1a7ae962-9b70-442c-a676-f172a2d9bfd3
keywords:
- Direct2D, Funktionen
ms.topic: article
ms.date: 09/19/2019
ms.openlocfilehash: 9cbe07a6c1054036030395ff965610919ee48a97
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104474602"
---
# <a name="direct2d-functions"></a>Direct2D-Funktionen

Direct2D bietet die folgenden Funktionen. Zusätzliche Funktionen werden im D2D1- [Namespace](d2d1-namespace.md)definiert.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|-|-|
| [**D2D1ComputeMaximumScaleFactor**](/windows/desktop/api/d2d1_2/nf-d2d1_2-d2d1computemaximumscalefactor) | Berechnet den maximalen Faktor, um den eine bestimmte Transformation jeden Vektor ausdehnen kann. |
| [**D2D1CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) | Erstellt ein neues Direct2D-Gerät, das dem bereitgestellten DXGI-Gerät zugeordnet ist.  |
| [**D2D1CreateDeviceContext**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevicecontext) | Erstellt einen neuen Direct2D-Gerätekontext, der einer DXGI-Oberfläche zugeordnet ist.  |
| [**D2D1CreateFactory (D2D1_FACTORY_TYPE, refid, void \* \* )**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory-r1) | Erstellt ein Factory-Objekt, das zum Erstellen von Direct2D-Ressourcen verwendet werden kann. |
| [**D2D1CreateFactory (D2D1_FACTORY_TYPE, refid, D2D1_FACTORY_OPTIONS \* , void \* \* )**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) | Erstellt ein Factory-Objekt, das zum Erstellen von Direct2D-Ressourcen verwendet werden kann. |
| [**D2D1GetGradientMeshInteriorPointsFromCoonsPatch**](/windows/desktop/api/d2d1_3/nf-d2d1_3-d2d1getgradientmeshinteriorpointsfromcoonspatch) | Gibt die inneren Punkte für ein Verlaufs Gitter Patch basierend auf den Punkten zurück, die einen Coons-Patch definieren. |
| [**D2D1InvertMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1invertmatrix) | Versucht, die angegebene Matrix umzukehren. |
| [**D2D1IsMatrixInvertible**](/windows/desktop/api/d2d1/nf-d2d1-d2d1ismatrixinvertible) | Gibt an, ob die angegebene Matrix invertierbar ist. |
| [**D2D1MakeRotateMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1makerotatematrix) | Erstellt eine Dreh Transformation, die sich um den angegebenen Punkt um den angegebenen Punkt dreht. |
| [**D2D1MakeSkewMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1makeskewmatrix) | Erstellt eine schiefe Transformation, die über den angegebenen Winkel der x-Achse, den y-Achsen Winkel und den Mittelpunkt verfügt.  |
| [**Operator \* (Konstanten D2D1\MATRIX\3X2\F&, Konstanten D2D1\MATRIX\3X2\F&)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-setproduct) | Multipliziert zwei Matrizen und gibt das Ergebnis zurück. |
| [**Blobgetter**](blobgetter.md) | Ruft für eine BLOB-Typ-Eigenschaft einen getCallback-Rückruf für eine Element Funktion auf. |
| [**Blobsetter**](blobsetter.md) | Ruft einen Eigenschafts Setter-Rückruf für eine Element Funktion für eine BLOB-Type-Eigenschaft auf. |
| [**Deducingblobgetter**](deducingblobgetter.md) | Leitet die-Klasse und die-Argumente ab und ruft dann einen Get-Rückruf Rückruf für eine Element Funktion für eine BLOB-Type-Eigenschaft auf. |
| [**Deducingblobsetter**](deducingblobsetter.md) | Leitet die-Klasse und die-Argumente ab und ruft dann einen Eigenschaften Setter-Rückruf für eine Element Funktion für eine BLOB-Type-Eigenschaft auf. |
| [**Deducingstringgetter**](deducingstringgetter.md) | Leitet die-Klasse und die-Argumente ab und ruft dann für eine Eigenschaft vom Typ "String" einen Eigenschaften-Getter-Rückruf für eine Element Funktion auf. |
| [**Deducingstringsetter**](deducingstringsetter.md) | Leitet die-Klasse und die-Argumente ab und ruft dann einen Eigenschaften Setter-Rückruf für eine Element Funktion für eine Eigenschaft vom Typ "String" auf. |
| [**Deducingvaluegetter**](deducingvaluegetter.md) | Leitet die-Klasse und die-Argumente ab und ruft dann einen getget-Rückruf Rückruf für eine Element Funktion für eine Value-Type-Eigenschaft auf. |
| [**Deducingvaluesetter**](deducingvaluesetter.md) | Leitet die-Klasse und die-Argumente ab und ruft dann einen Eigenschaften Setter-Rückruf für eine Element Funktion für eine Value-Type-Eigenschaft auf. |
| [**GetType**](/previous-versions/windows/desktop/legacy/hh847962(v=vs.85)) | Ruft den Typ der angegebenen Eigenschaft ab. |
| [**Stringgetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-stringgetter) | Ruft für eine Eigenschaft vom Typ "String" einen Eigenschaften-Getter-Rückruf für eine Element Funktion auf. |
| [**Stringsetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-stringsetter) | Ruft einen Eigenschafts Setter-Rückruf für eine Element Funktion für eine Eigenschaft vom Typ "String" auf. |
| [**Valuegetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-valuegetter) | Ruft einen Eigenschafts Setter-Rückruf für eine Element Funktion für eine Werttyp Eigenschaft auf. |
| [**Valuesetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-valuesetter) | Ruft einen Eigenschafts Setter-Rückruf für eine Element Funktion für eine Werttyp Eigenschaft auf. |
| [**D2D1ConvertColorSpace**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1convertcolorspace) | Konvertiert die angegebene Farbe von einem colorspace in einen anderen. |
| [**D2D1SinCos**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1sincos) | Gibt den Sinus und Kosinus eines Winkels zurück. |
| [**D2D1Tan**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1tan) | Gibt den Tangens eines Winkels zurück. |
| [**D2D1Vec3Length**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1vec3length) | Gibt die Länge eines dreidimensionalen Vektors zurück. |
| [**PD2D1\PROPERTY\GET\FUNCTION**](/windows/desktop/api/D2d1effectauthor/nc-d2d1effectauthor-pd2d1_property_get_function) | Ruft eine Eigenschaft aus einem Effekt ab. |
| [**PD2D1\PROPERTY\SET\FUNCTION**](/windows/desktop/api/D2d1effectauthor/nc-d2d1effectauthor-pd2d1_property_set_function) | Legt eine Eigenschaft für einen Effekt fest. |