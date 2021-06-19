---
description: Windows GDI+ macht eine flache API verfügbar, die aus etwa 600 Funktionen besteht. Microsoft .NET Framework stellt eine Reihe von Wrapperklassen mit verwaltetem Code für GDI+ bereit.
ms.assetid: afd8cf81-8a20-4592-bd0a-46341742cc9b
title: GDI+ Flat-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65f91c3c925b7de31f27e91c70cbd1bf0cbbb2a4
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394985"
---
# <a name="gdi-flat-api"></a><span data-ttu-id="ad279-104">GDI+ Flat-API</span><span class="sxs-lookup"><span data-stu-id="ad279-104">GDI+ Flat API</span></span>

<span data-ttu-id="ad279-105">Windows GDI+ macht eine flache API verfügbar, die aus etwa 600 Funktionen besteht, die in Gdiplus.dll implementiert und in Gdiplusflat.h deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="ad279-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="ad279-106">Die Funktionen in der flachen GDI+-API werden von einer Sammlung von etwa 40 C++-Klassen umschlossen.</span><span class="sxs-lookup"><span data-stu-id="ad279-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="ad279-107">Es wird empfohlen, die Funktionen in der flachen API nicht direkt aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ad279-107">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="ad279-108">Wenn Sie GDI+ aufrufen, sollten Sie dazu die Methoden und Funktionen aufrufen, die von den C++-Wrappern bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ad279-108">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="ad279-109">Microsoft Product Support Services bietet keine Unterstützung für Code, der die flache API direkt aufruft.</span><span class="sxs-lookup"><span data-stu-id="ad279-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span>

<span data-ttu-id="ad279-110">Als Alternative zu den C++-Wrappern stellt das Microsoft .NET Framework eine Reihe von Wrapperklassen mit verwaltetem Code für GDI+ bereit.</span><span class="sxs-lookup"><span data-stu-id="ad279-110">As an alternative to the C++ wrappers, the Microsoft .NET Framework provides a set of managed-code wrapper classes for GDI+.</span></span> <span data-ttu-id="ad279-111">Die Wrapper für verwalteten Code für GDI+ gehören zu den folgenden Namespaces.</span><span class="sxs-lookup"><span data-stu-id="ad279-111">The managed-code wrappers for GDI+ belong to the following namespaces.</span></span>

-   [<span data-ttu-id="ad279-112">System.Drawing</span><span class="sxs-lookup"><span data-stu-id="ad279-112">System.Drawing</span></span>](/dotnet/api/system.drawing?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="ad279-113">System.Drawing.Drawing2D</span><span class="sxs-lookup"><span data-stu-id="ad279-113">System.Drawing.Drawing2D</span></span>](/dotnet/api/system.drawing.drawing2d?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="ad279-114">System.drawing.imaging</span><span class="sxs-lookup"><span data-stu-id="ad279-114">System.Drawing.Imaging</span></span>](/dotnet/api/system.drawing.imaging?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="ad279-115">System.drawing.text</span><span class="sxs-lookup"><span data-stu-id="ad279-115">System.Drawing.Text</span></span>](/dotnet/api/system.drawing.text?view=dotnet-plat-ext-3.1&preserve-view=true)

<span data-ttu-id="ad279-116">Beide Wrappersätze (C++ und verwalteter Code) verwenden einen objektorientierten Ansatz, sodass es einige Unterschiede zwischen der Art und Weise gibt, wie Parameter an die Wrappermethoden übergeben werden, und der Art und Weise, wie Parameter an Funktionen in der flachen API übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="ad279-116">Both sets of wrappers (C++ and managed code) use an object-oriented approach, so there are some differences between the way parameters are passed to the wrapper methods and the way parameters are passed to functions in the flat API.</span></span> <span data-ttu-id="ad279-117">Beispielsweise ist einer der C++-Wrapper die [**Matrix-Klasse.**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix)</span><span class="sxs-lookup"><span data-stu-id="ad279-117">For example, one of the C++ wrappers is the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class.</span></span> <span data-ttu-id="ad279-118">Jedes **Matrixobjekt** verfügt über das Feld **nativeMatrix,** das auf eine interne Variable vom Typ **GpMatrix** verweist.</span><span class="sxs-lookup"><span data-stu-id="ad279-118">Each **Matrix** object has a field, **nativeMatrix**, that points to an internal variable of type **GpMatrix**.</span></span> <span data-ttu-id="ad279-119">Wenn Sie Parameter an eine Methode eines **Matrixobjekts** übergeben, übergibt diese Methode diese Parameter (oder einen Satz verwandter Parameter) zusammen an eine der Funktionen in der flachen GDI+-API.</span><span class="sxs-lookup"><span data-stu-id="ad279-119">When you pass parameters to a method of a **Matrix** object, that method passes those parameters (or a set of related parameters) along to one of the functions in the GDI+ flat API.</span></span> <span data-ttu-id="ad279-120">Diese Methode übergibt jedoch auch das **nativeMatrix-Feld** (als Eingabeparameter) an die flache API-Funktion.</span><span class="sxs-lookup"><span data-stu-id="ad279-120">But that method also passes the **nativeMatrix** field (as an input parameter) to the flat API function.</span></span> <span data-ttu-id="ad279-121">Der folgende Code zeigt, wie die [**Matrix::Shear-Methode**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) die **GdipShearMatrix(GpMatrix \* matrix, REAL shearX, REAL shearY, GpMatrixOrder order)-Funktion** aufruft.</span><span class="sxs-lookup"><span data-stu-id="ad279-121">The following code shows how the [**Matrix::Shear**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) method calls the **GdipShearMatrix(GpMatrix \*matrix, REAL shearX, REAL shearY, GpMatrixOrder order)** function.</span></span>


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



<span data-ttu-id="ad279-122">Die [**Matrixkonstruktoren**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) übergeben die Adresse einer GpMatrix-Zeigervariablen (als Ausgabeparameter) an die  **GdipCreateMatrix(GpMatrix \* \* matrix)-Funktion.**</span><span class="sxs-lookup"><span data-stu-id="ad279-122">The [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) constructors pass the address of a **GpMatrix** pointer variable (as an output parameter) to the **GdipCreateMatrix(GpMatrix \*\*matrix)** function.</span></span> <span data-ttu-id="ad279-123">**GdipCreateMatrix** erstellt und initialisiert eine interne **GpMatrix-Variable** und weist dann die Adresse der **GpMatrix** der Zeigervariablen zu.</span><span class="sxs-lookup"><span data-stu-id="ad279-123">**GdipCreateMatrix** creates and initializes an internal **GpMatrix** variable and then assigns the address of the **GpMatrix** to the pointer variable.</span></span> <span data-ttu-id="ad279-124">Anschließend kopiert der Konstruktor den Wert des Zeigers in das **nativeMatrix-Feld.**</span><span class="sxs-lookup"><span data-stu-id="ad279-124">Then the constructor copies the value of the pointer to the **nativeMatrix** field.</span></span>


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



<span data-ttu-id="ad279-125">Klonmethoden in den Wrapperklassen erhalten keine Parameter, übergeben jedoch häufig zwei Parameter an die zugrunde liegende Funktion in der flachen GDI+-API.</span><span class="sxs-lookup"><span data-stu-id="ad279-125">Clone methods in the wrapper classes receive no parameters but often pass two parameters to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="ad279-126">Beispielsweise übergibt die [**Matrix::Clone-Methode**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) **nativeMatrix** (als Eingabeparameter) und die Adresse einer GpMatrix-Zeigervariablen (als Ausgabeparameter) an die  **GdipCloneMatrix-Funktion.**</span><span class="sxs-lookup"><span data-stu-id="ad279-126">For example, the [**Matrix::Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) method passes **nativeMatrix** (as an input parameter) and the address of a **GpMatrix** pointer variable (as an output parameter) to the **GdipCloneMatrix** function.</span></span> <span data-ttu-id="ad279-127">Der folgende Code zeigt, wie die **Matrix::Clone-Methode** die **GdipCloneMatrix(GpMatrix \* matrix, GpMatrix \* \* cloneMatrix)-Funktion** aufruft.</span><span class="sxs-lookup"><span data-stu-id="ad279-127">The following code shows how the **Matrix::Clone** method calls the **GdipCloneMatrix(GpMatrix \*matrix, GpMatrix \*\*cloneMatrix)** function.</span></span>


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



<span data-ttu-id="ad279-128">Die Funktionen in der flachen API geben einen Wert vom Typ GpStatus zurück.</span><span class="sxs-lookup"><span data-stu-id="ad279-128">The functions in the flat API return a value of type GpStatus.</span></span> <span data-ttu-id="ad279-129">Die GpStatus-Enumeration ist [](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) identisch mit der Status-Enumeration, die von den Wrappermethoden verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ad279-129">The GpStatus enumeration is identical to the [**Status**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) enumeration used by the wrapper methods.</span></span> <span data-ttu-id="ad279-130">In GdiplusGpStubs.h wird GpStatus wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="ad279-130">In GdiplusGpStubs.h, GpStatus is defined as follows:</span></span>

`typedef Status GpStatus;`

<span data-ttu-id="ad279-131">Die meisten Methoden in den Wrapperklassen geben einen Statuswert zurück, der angibt, ob die Methode erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="ad279-131">Most of the methods in the wrapper classes return a status value that indicates whether the method succeeded.</span></span> <span data-ttu-id="ad279-132">Einige der Wrappermethoden geben jedoch Zustandswerte zurück.</span><span class="sxs-lookup"><span data-stu-id="ad279-132">However, some of the wrapper methods return state values.</span></span> <span data-ttu-id="ad279-133">Wenn Sie eine Wrappermethode aufrufen, die einen Zustandswert zurückgibt, übergibt die Wrappermethode die entsprechenden Parameter an die zugrunde liegende Funktion in der flachen GDI+-API.</span><span class="sxs-lookup"><span data-stu-id="ad279-133">When you call a wrapper method that returns a state value, the wrapper method passes the appropriate parameters to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="ad279-134">Die [**Matrix-Klasse**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) verfügt beispielsweise über eine [**Matrix::IsInvertible-Methode,**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) die das **nativeMatrix-Feld** und die Adresse einer **BOOL-Variablen** (als Ausgabeparameter) an die **GdipIsMatrixInvertible-Funktion** übergibt.</span><span class="sxs-lookup"><span data-stu-id="ad279-134">For example, the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class has an [**Matrix::IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) method that passes the **nativeMatrix** field and and the address of a **BOOL** variable (as an output parameter) to the **GdipIsMatrixInvertible** function.</span></span> <span data-ttu-id="ad279-135">Der folgende Code zeigt, wie die **Matrix::IsInvertible-Methode** die **GdipIsMatrixInvertible(GDIPCONST GpMatrix \* matrix, BOOL \* result)-Funktion** aufruft.</span><span class="sxs-lookup"><span data-stu-id="ad279-135">The following code shows how the **Matrix::IsInvertible** method calls the **GdipIsMatrixInvertible(GDIPCONST GpMatrix \*matrix, BOOL \*result)** function.</span></span>


```
BOOL IsInvertible() const
{
   BOOL result = FALSE;
   ...
   GdipIsMatrixInvertible(nativeMatrix, &result);
   return result;
}
```



<span data-ttu-id="ad279-136">Ein weiterer Wrapper ist die [**Color-Klasse.**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color)</span><span class="sxs-lookup"><span data-stu-id="ad279-136">Another one of the wrappers is the [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) class.</span></span> <span data-ttu-id="ad279-137">Ein **Color-Objekt** verfügt über ein einzelnes Feld vom Typ **ARGB**, das als **DWORD** definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ad279-137">A **Color** object has a single field of type **ARGB**, which is defined as a **DWORD**.</span></span> <span data-ttu-id="ad279-138">Wenn Sie ein **Color-Objekt** an eine der Wrappermethoden übergeben, übergibt diese Methode das **ARGB-Feld** zusammen an die zugrunde liegende Funktion in der flachen GDI+-API.</span><span class="sxs-lookup"><span data-stu-id="ad279-138">When you pass a **Color** object to one of the wrapper methods, that method passes the **ARGB** field along to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="ad279-139">Der folgende Code zeigt, wie die [**Pen::SetColor-Methode**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) die **GdipSetPenColor(GpPen \* pen, ARGB argb)-Funktion** aufruft.</span><span class="sxs-lookup"><span data-stu-id="ad279-139">The following code shows how the [**Pen::SetColor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) method calls the **GdipSetPenColor(GpPen \*pen, ARGB argb)** function.</span></span> <span data-ttu-id="ad279-140">Die [**Color::GetValue-Methode**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) gibt den Wert des **ARGB-Felds** zurück.</span><span class="sxs-lookup"><span data-stu-id="ad279-140">The [**Color::GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) method returns the value of the **ARGB** field.</span></span>


```
Status SetColor(IN const Color& color)
{
   ...
   GdipSetPenColor(nativePen, color.GetValue());
}
```



<span data-ttu-id="ad279-141">Die folgenden Themen zeigen die Beziehung zwischen der GDI+-Flat-API und den C++-Wrappermethoden.</span><span class="sxs-lookup"><span data-stu-id="ad279-141">The following topics show the relationship between the GDI+ flat API and the C++ wrapper methods.</span></span>

-   [<span data-ttu-id="ad279-142">AdjustableArrowCap-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ad279-142">AdjustableArrowCap Functions</span></span>](-gdiplus-adjustablearrowcap-flat.md)
-   [<span data-ttu-id="ad279-143">Bitmapfunktionen</span><span class="sxs-lookup"><span data-stu-id="ad279-143">Bitmap Functions</span></span>](-gdiplus-bitmap-flat.md)
-   [<span data-ttu-id="ad279-144">Pinselfunktionen</span><span class="sxs-lookup"><span data-stu-id="ad279-144">Brush Functions</span></span>](-gdiplus-brush-flat.md)
-   [<span data-ttu-id="ad279-145">CachedBitmap-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ad279-145">CachedBitmap Functions</span></span>](-gdiplus-cachedbitmap-flat.md)
-   [<span data-ttu-id="ad279-146">CustomLineCap-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ad279-146">CustomLineCap Functions</span></span>](-gdiplus-customlinecap-flat.md)
-   [<span data-ttu-id="ad279-147">Schriftartfunktionen</span><span class="sxs-lookup"><span data-stu-id="ad279-147">Font Functions</span></span>](-gdiplus-font-flat.md)
-   [<span data-ttu-id="ad279-148">FontFamilyFunctions</span><span class="sxs-lookup"><span data-stu-id="ad279-148">FontFamilyFunctions</span></span>](-gdiplus-fontfamily-flat.md)
-   [<span data-ttu-id="ad279-149">Grafikfunktionen</span><span class="sxs-lookup"><span data-stu-id="ad279-149">Graphics Functions</span></span>](-gdiplus-graphics-flat.md)
-   [<span data-ttu-id="ad279-150">GraphicsPath-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ad279-150">GraphicsPath Functions</span></span>](-gdiplus-graphicspath-flat.md)
-   [<span data-ttu-id="ad279-151">HatchBrush-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ad279-151">HatchBrush Functions</span></span>](-gdiplus-hatchbrush-flat.md)
-   [<span data-ttu-id="ad279-152">Bildfunktionen</span><span class="sxs-lookup"><span data-stu-id="ad279-152">Image Functions</span></span>](-gdiplus-image-flat.md)
-   [<span data-ttu-id="ad279-153">ImageAttributes-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ad279-153">ImageAttributes Functions</span></span>](-gdiplus-imageattributes-flat.md)
-   [<span data-ttu-id="ad279-154">LinearGradientBrush-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ad279-154">LinearGradientBrush Functions</span></span>](-gdiplus-lineargradientbrush-flat.md)
-   [<span data-ttu-id="ad279-155">Matrixfunktionen</span><span class="sxs-lookup"><span data-stu-id="ad279-155">Matrix Functions</span></span>](-gdiplus-matrix-flat.md)
-   [<span data-ttu-id="ad279-156">Arbeitsspeicherfunktionen</span><span class="sxs-lookup"><span data-stu-id="ad279-156">Memory Functions</span></span>](-gdiplus-memory-flat.md)
-   [<span data-ttu-id="ad279-157">Benachrichtigungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="ad279-157">Notification Functions</span></span>](-gdiplus-notification-flat.md)
-   [<span data-ttu-id="ad279-158">PathGradientBrush-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ad279-158">PathGradientBrush Functions</span></span>](-gdiplus-pathgradientbrush-flat.md)
-   [<span data-ttu-id="ad279-159">PathIterator-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ad279-159">PathIterator Functions</span></span>](-gdiplus-pathiterator-flat.md)
-   [<span data-ttu-id="ad279-160">Stiftfunktionen</span><span class="sxs-lookup"><span data-stu-id="ad279-160">Pen Functions</span></span>](-gdiplus-pen-flat.md)
-   [<span data-ttu-id="ad279-161">Regionsfunktionen</span><span class="sxs-lookup"><span data-stu-id="ad279-161">Region Functions</span></span>](-gdiplus-region-flat.md)
-   [<span data-ttu-id="ad279-162">SolidBrush-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ad279-162">SolidBrush Functions</span></span>](-gdiplus-solidbrush-flat.md)
-   [<span data-ttu-id="ad279-163">Zeichenfolgenformatfunktionen</span><span class="sxs-lookup"><span data-stu-id="ad279-163">String Format Functions</span></span>](-gdiplus-stringformat-flat.md)
-   [<span data-ttu-id="ad279-164">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="ad279-164">Text Functions</span></span>](-gdiplus-text-flat.md)
-   [<span data-ttu-id="ad279-165">Texturpinselfunktionen</span><span class="sxs-lookup"><span data-stu-id="ad279-165">Texture Brush Functions</span></span>](-gdiplus-texturebrush-flat.md)

 

 
