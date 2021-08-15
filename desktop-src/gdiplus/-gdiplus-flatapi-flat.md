---
description: Windows GDI+ macht eine flache API verfügbar, die aus etwa 600 Funktionen besteht. Microsoft .NET Framework stellt eine Reihe von Wrapperklassen für verwalteten Code für GDI+ bereit.
ms.assetid: afd8cf81-8a20-4592-bd0a-46341742cc9b
title: GDI+ Flat-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37dee1288bdbbf86c39d201d5ccc066c1eab16cb600950edd5e848cd250e0ed8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977550"
---
# <a name="gdi-flat-api"></a>GDI+ Flat-API

Windows GDI+ macht eine flache API verfügbar, die aus etwa 600 Funktionen besteht, die in Gdiplus.dll implementiert und in Gdiplusflat.h deklariert werden. Die Funktionen in der GDI+ flachen API werden von einer Sammlung von etwa 40 C++-Klassen umschlossen. Es wird empfohlen, die Funktionen in der flachen API nicht direkt aufzurufen. Wenn Sie aufruft, GDI+, sollten Sie dazu die Methoden und Funktionen aufrufen, die von den C++-Wrappern bereitgestellt werden. Microsoft Product Support Services bietet keine Unterstützung für Code, der die flache API direkt aufruft.

Als Alternative zu den C++-Wrappern stellt microsoft .NET Framework eine Reihe von Wrapperklassen mit verwaltetem Code für GDI+ bereit. Die Wrapper für verwalteten Code für GDI+ zu den folgenden Namespaces gehören.

-   [System.Drawing](/dotnet/api/system.drawing?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System.Drawing.Drawing2D](/dotnet/api/system.drawing.drawing2d?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System.drawing.imaging](/dotnet/api/system.drawing.imaging?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System.drawing.text](/dotnet/api/system.drawing.text?view=dotnet-plat-ext-3.1&preserve-view=true)

Beide Wrappersätze (C++ und verwalteter Code) verwenden einen objektorientierten Ansatz, sodass es einige Unterschiede zwischen der Art und Weise gibt, wie Parameter an die Wrappermethoden übergeben werden, und der Art und Weise, wie Parameter an Funktionen in der flachen API übergeben werden. Beispielsweise ist einer der C++-Wrapper die [**Matrix-Klasse.**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) Jedes **Matrixobjekt** verfügt über das Feld **nativeMatrix,** das auf eine interne Variable vom Typ **GpMatrix** verweist. Wenn Sie Parameter an eine Methode eines **Matrixobjekts** übergeben, übergibt diese Methode diese Parameter (oder einen Satz verwandter Parameter) zusammen an eine der Funktionen in der GDI+ flachen API. Diese Methode übergibt jedoch auch das **nativeMatrix-Feld** (als Eingabeparameter) an die flache API-Funktion. Der folgende Code zeigt, wie die [**Matrix::Shear-Methode**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) die **GdipShearMatrix(GpMatrix \* matrix, REAL shearX, REAL shearY, GpMatrixOrder order)-Funktion** aufruft.


```
Status Shear(
      IN REAL shearX, 
      IN REAL shearY,
      IN MatrixOrder order = MatrixOrderPrepend)
{
   ...
   GdipShearMatrix(nativeMatrix, shearX, shearY, order);
   ...
}
```



Die [**Matrixkonstruktoren**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) übergeben die Adresse einer GpMatrix-Zeigervariablen (als Ausgabeparameter) an die  **GdipCreateMatrix(GpMatrix \* \* matrix)-Funktion.** **GdipCreateMatrix** erstellt und initialisiert eine interne **GpMatrix-Variable** und weist dann die Adresse der **GpMatrix** der Zeigervariablen zu. Anschließend kopiert der Konstruktor den Wert des Zeigers in das **nativeMatrix-Feld.**


```
Matrix()
{
   GpMatrix *matrix = NULL;
   lastResult = DllExports::GdipCreateMatrix(&matrix);
   SetNativeMatrix(matrix);
}

VOID SetNativeMatrix(GpMatrix *nativeMatrix)
{
   this->nativeMatrix = nativeMatrix;
}
```



Klonmethoden in den Wrapperklassen erhalten keine Parameter, übergeben jedoch häufig zwei Parameter an die zugrunde liegende Funktion in der GDI+ flachen API. Beispielsweise übergibt die [**Matrix::Clone-Methode**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) **nativeMatrix** (als Eingabeparameter) und die Adresse einer GpMatrix-Zeigervariablen (als Ausgabeparameter) an die  **GdipCloneMatrix-Funktion.** Der folgende Code zeigt, wie die **Matrix::Clone-Methode** die **GdipCloneMatrix(GpMatrix \* matrix, GpMatrix \* \* cloneMatrix)-Funktion** aufruft.


```
Matrix *Clone() const
{
   GpMatrix *cloneMatrix = NULL;
   ...
   GdipCloneMatrix(nativeMatrix, &cloneMatrix));
   ...
   return new Matrix(cloneMatrix);
 }
```



Die Funktionen in der flachen API geben einen Wert vom Typ GpStatus zurück. Die GpStatus-Enumeration ist [](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) identisch mit der Status-Enumeration, die von den Wrappermethoden verwendet wird. In GdiplusGpStubs.h wird GpStatus wie folgt definiert:

`typedef Status GpStatus;`

Die meisten Methoden in den Wrapperklassen geben einen Statuswert zurück, der angibt, ob die Methode erfolgreich war. Einige der Wrappermethoden geben jedoch Zustandswerte zurück. Wenn Sie eine Wrappermethode aufrufen, die einen Zustandswert zurückgibt, übergibt die Wrappermethode die entsprechenden Parameter an die zugrunde liegende Funktion in der GDI+ flachen API. Die [**Matrix-Klasse**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) verfügt beispielsweise über eine [**Matrix::IsInvertible-Methode,**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) die das **nativeMatrix-Feld** und die Adresse einer **BOOL-Variablen** (als Ausgabeparameter) an die **GdipIsMatrixInvertible-Funktion** übergibt. Der folgende Code zeigt, wie die **Matrix::IsInvertible-Methode** die **GdipIsMatrixInvertible(GDIPCONST GpMatrix \* matrix, BOOL \* result)-Funktion** aufruft.


```
BOOL IsInvertible() const
{
   BOOL result = FALSE;
   ...
   GdipIsMatrixInvertible(nativeMatrix, &result);
   return result;
}
```



Ein weiterer Wrapper ist die [**Color-Klasse.**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) Ein **Color-Objekt** verfügt über ein einzelnes Feld vom Typ **ARGB**, das als **DWORD** definiert ist. Wenn Sie ein **Color-Objekt** an eine der Wrappermethoden übergeben, übergibt diese Methode das **ARGB-Feld** zusammen an die zugrunde liegende Funktion in der GDI+ flachen API. Der folgende Code zeigt, wie die [**Pen::SetColor-Methode**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) die **GdipSetPenColor(GpPen \* pen, ARGB argb)-Funktion** aufruft. Die [**Color::GetValue-Methode**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) gibt den Wert des **ARGB-Felds** zurück.


```
Status SetColor(IN const Color& color)
{
   ...
   GdipSetPenColor(nativePen, color.GetValue());
}
```



Die folgenden Themen zeigen die Beziehung zwischen der GDI+ flachen API und den C++-Wrappermethoden.

-   [AdjustableArrowCap-Funktionen](-gdiplus-adjustablearrowcap-flat.md)
-   [Bitmapfunktionen](-gdiplus-bitmap-flat.md)
-   [Pinselfunktionen](-gdiplus-brush-flat.md)
-   [CachedBitmap-Funktionen](-gdiplus-cachedbitmap-flat.md)
-   [CustomLineCap-Funktionen](-gdiplus-customlinecap-flat.md)
-   [Schriftartfunktionen](-gdiplus-font-flat.md)
-   [FontFamilyFunctions](-gdiplus-fontfamily-flat.md)
-   [Grafikfunktionen](-gdiplus-graphics-flat.md)
-   [GraphicsPath-Funktionen](-gdiplus-graphicspath-flat.md)
-   [HatchBrush-Funktionen](-gdiplus-hatchbrush-flat.md)
-   [Bildfunktionen](-gdiplus-image-flat.md)
-   [ImageAttributes-Funktionen](-gdiplus-imageattributes-flat.md)
-   [LinearGradientBrush-Funktionen](-gdiplus-lineargradientbrush-flat.md)
-   [Matrixfunktionen](-gdiplus-matrix-flat.md)
-   [Arbeitsspeicherfunktionen](-gdiplus-memory-flat.md)
-   [Benachrichtigungsfunktionen](-gdiplus-notification-flat.md)
-   [PathGradientBrush-Funktionen](-gdiplus-pathgradientbrush-flat.md)
-   [PathIterator-Funktionen](-gdiplus-pathiterator-flat.md)
-   [Stiftfunktionen](-gdiplus-pen-flat.md)
-   [Regionsfunktionen](-gdiplus-region-flat.md)
-   [SolidBrush-Funktionen](-gdiplus-solidbrush-flat.md)
-   [Zeichenfolgenformatfunktionen](-gdiplus-stringformat-flat.md)
-   [Textfunktionen](-gdiplus-text-flat.md)
-   [Texturpinselfunktionen](-gdiplus-texturebrush-flat.md)

 

 
