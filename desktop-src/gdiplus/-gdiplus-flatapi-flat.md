---
description: Windows GDI+ macht eine flache API verfügbar, die aus ungefähr 600 Funktionen besteht, die in Gdiplus.dll implementiert und in "Gdiplus. h" deklariert sind.
ms.assetid: afd8cf81-8a20-4592-bd0a-46341742cc9b
title: GDI+ Flat-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450f89439b6ead3b8cd9a49f52a6620571f6db54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994247"
---
# <a name="gdi-flat-api"></a>GDI+ Flat-API

Windows GDI+ macht eine flache API verfügbar, die aus ungefähr 600 Funktionen besteht, die in Gdiplus.dll implementiert und in "Gdiplus. h" deklariert sind. Die Funktionen in der flatapi GDI+ werden von einer Sammlung von ungefähr 40 C++-Klassen umschließt. Es wird empfohlen, die Funktionen in der flatapi nicht direkt aufzurufen. Wenn Sie GDI+ aufrufen, sollten Sie dies tun, indem Sie die Methoden und Funktionen aufrufen, die von den C++-Wrappern bereitgestellt werden. Der Microsoft-Produktsupport bietet keine Unterstützung für Code, mit dem die flatapi direkt aufgerufen wird.

Als Alternative zu den C++-Wrappern bietet das Microsoft .NET Framework einen Satz von Wrapper Klassen für verwalteten Code für GDI+. Die Wrapper für verwalteten Code für GDI+ gehören zu den folgenden Namespaces.

-   [System.Drawing](/dotnet/api/system.drawing?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System. Drawing. Drawing2D](/dotnet/api/system.drawing.drawing2d?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System. Drawing. Imaging](/dotnet/api/system.drawing.imaging?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System. Drawing. Text](/dotnet/api/system.drawing.text?view=dotnet-plat-ext-3.1&preserve-view=true)

Beide Wrapper Sätze (C++ und verwalteter Code) verwenden einen objektorientierten Ansatz, daher gibt es einige Unterschiede zwischen der Art und Weise, wie Parameter an die Wrapper Methoden und wie Parameter an Funktionen in der flatapi übermittelt werden. Beispielsweise ist einer der C++-Wrapper die [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) -Klasse. Jedes **Matrix** Objekt verfügt über das Feld **nativematrix**, das auf eine interne Variable des Typs **gpmatrix** zeigt. Wenn Sie Parameter an eine Methode eines **Matrix** Objekts übergeben, übergibt diese Methode diese Parameter (oder einen Satz verwandter Parameter) an eine der Funktionen in der GDI+-flatapi. Diese Methode übergibt jedoch auch das Feld " **nativematrix** " (als Eingabeparameter) an die flatapi-Funktion. Der folgende Code zeigt, wie die [**Matrix:: Shear**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) -Methode die Funktion **gdipshearmatrix aufruft (gpmatrix \* Matrix, Real shearX, Real shearY, gpmatrixorder Order)** .


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



Die [**matrixkonstruktoren**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) übergeben die Adresse einer **gpmatrix** -Zeiger Variablen (als Ausgabeparameter) an die Funktion **gdipanatematrix (gpmatrix \* \* Matrix)** . **Gdipkreatematrix** erstellt und Initialisiert eine interne **gpmatrix** -Variable und weist dann die Adresse der **gpmatrix** der Zeiger Variablen zu. Anschließend kopiert der Konstruktor den Wert des Zeigers in das Feld **nativematrix** .


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



Klon Methoden in den Wrapper Klassen empfangen keine Parameter, übergeben jedoch oft zwei Parameter an die zugrunde liegende Funktion in der GDI+-flatapi. Die [**Matrix:: Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) -Methode übergibt z. b. **nativematrix** (als Eingabeparameter) und die Adresse einer **gpmatrix** -Zeiger Variablen (als Ausgabeparameter) an die **gdipclonematrix** -Funktion. Der folgende Code zeigt, wie die **Matrix:: Clone** -Methode die **gdipclonematrix-Funktion (gpmatrix- \* Matrix, gpmatrix \* \* clonematrix)** aufruft.


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



Die Funktionen in der flatapi geben einen Wert vom Typ gpstatus zurück. Die gpstatus-Enumeration ist identisch mit der [**statusenumeration**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) , die von den Wrapper Methoden verwendet wird. In "gdiplusgpstusb. h" ist gpstatus wie folgt definiert:

`typedef Status GpStatus;`

Die meisten Methoden in den Wrapper Klassen geben einen Statuswert zurück, der angibt, ob die Methode erfolgreich ausgeführt wurde. Einige der Wrapper Methoden geben jedoch Zustands Werte zurück. Wenn Sie eine Wrapper Methode aufzurufen, die einen Zustandswert zurückgibt, übergibt die Wrapper Methode die entsprechenden Parameter an die zugrunde liegende Funktion in der GDI+-flatapi. Die [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) Klasse verfügt beispielsweise über eine [**Matrix:: IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) -Methode, die das Feld " **nativematrix** " und die Adresse einer **booleschen** Variablen (als Ausgabeparameter) an die **gdipismatrixinvertible** -Funktion übergibt. Der folgende Code zeigt, wie die **Matrix:: IsInvertible** -Methode die **gdipismatrixinvertible-Funktion (gdipkonstanten gpmatrix \* Matrix, bool \* result)** aufruft.


```
BOOL IsInvertible() const
{
   BOOL result = FALSE;
   ...
   GdipIsMatrixInvertible(nativeMatrix, &result);
   return result;
}
```



Ein weiterer Wrapper ist die [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) -Klasse. Ein **Color** -Objekt verfügt über ein einzelnes Feld vom Typ **ARGB**, das als **DWORD** definiert ist. Wenn Sie ein **Color** -Objekt an eine der Wrapper Methoden übergeben, übergibt diese Methode das **ARGB** -Feld an die zugrunde liegende Funktion in der GDI+-flatapi. Der folgende Code zeigt, wie die [**Pen:: SetColor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) -Methode die **gdipsetpencolor (gppen \* Pen, ARGB ARGB)** -Funktion aufruft. Die [**Color:: GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) -Methode gibt den Wert des **ARGB** -Felds zurück.


```
Status SetColor(IN const Color& color)
{
   ...
   GdipSetPenColor(nativePen, color.GetValue());
}
```



In den folgenden Themen wird die Beziehung zwischen der flatapi GDI+ und den C++-Wrapper Methoden veranschaulicht.

-   [AdjustableArrowCap-Funktionen](-gdiplus-adjustablearrowcap-flat.md)
-   [Bitmap-Funktionen](-gdiplus-bitmap-flat.md)
-   [Pinsel Funktionen](-gdiplus-brush-flat.md)
-   [CachedBitmap-Funktionen](-gdiplus-cachedbitmap-flat.md)
-   [CustomLineCap-Funktionen](-gdiplus-customlinecap-flat.md)
-   [Schriftart Funktionen](-gdiplus-font-flat.md)
-   [Fontfamilyfunctions](-gdiplus-fontfamily-flat.md)
-   [Grafikfunktionen](-gdiplus-graphics-flat.md)
-   [GraphicsPath-Funktionen](-gdiplus-graphicspath-flat.md)
-   [HatchBrush-Funktionen](-gdiplus-hatchbrush-flat.md)
-   [Bildfunktionen](-gdiplus-image-flat.md)
-   [Imageattribute-Funktionen](-gdiplus-imageattributes-flat.md)
-   [LinearGradientBrush-Funktionen](-gdiplus-lineargradientbrush-flat.md)
-   [Matrix Funktionen](-gdiplus-matrix-flat.md)
-   [Speicherfunktionen](-gdiplus-memory-flat.md)
-   [Benachrichtigungsfunktionen](-gdiplus-notification-flat.md)
-   [PathGradientBrush-Funktionen](-gdiplus-pathgradientbrush-flat.md)
-   [Funktionen von "pthiterator"](-gdiplus-pathiterator-flat.md)
-   [Stift Funktionen](-gdiplus-pen-flat.md)
-   [Regions Funktionen](-gdiplus-region-flat.md)
-   [SolidBrush-Funktionen](-gdiplus-solidbrush-flat.md)
-   [Zeichen folgen Format-Funktionen](-gdiplus-stringformat-flat.md)
-   [Text Funktionen](-gdiplus-text-flat.md)
-   [Textur Pinsel Funktionen](-gdiplus-texturebrush-flat.md)

 

 
