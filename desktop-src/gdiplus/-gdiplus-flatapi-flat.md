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
# <a name="gdi-flat-api"></a><span data-ttu-id="efab4-103">GDI+ Flat-API</span><span class="sxs-lookup"><span data-stu-id="efab4-103">GDI+ Flat API</span></span>

<span data-ttu-id="efab4-104">Windows GDI+ macht eine flache API verfügbar, die aus ungefähr 600 Funktionen besteht, die in Gdiplus.dll implementiert und in "Gdiplus. h" deklariert sind.</span><span class="sxs-lookup"><span data-stu-id="efab4-104">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="efab4-105">Die Funktionen in der flatapi GDI+ werden von einer Sammlung von ungefähr 40 C++-Klassen umschließt.</span><span class="sxs-lookup"><span data-stu-id="efab4-105">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="efab4-106">Es wird empfohlen, die Funktionen in der flatapi nicht direkt aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="efab4-106">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="efab4-107">Wenn Sie GDI+ aufrufen, sollten Sie dies tun, indem Sie die Methoden und Funktionen aufrufen, die von den C++-Wrappern bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="efab4-107">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="efab4-108">Der Microsoft-Produktsupport bietet keine Unterstützung für Code, mit dem die flatapi direkt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="efab4-108">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span>

<span data-ttu-id="efab4-109">Als Alternative zu den C++-Wrappern bietet das Microsoft .NET Framework einen Satz von Wrapper Klassen für verwalteten Code für GDI+.</span><span class="sxs-lookup"><span data-stu-id="efab4-109">As an alternative to the C++ wrappers, the Microsoft .NET Framework provides a set of managed-code wrapper classes for GDI+.</span></span> <span data-ttu-id="efab4-110">Die Wrapper für verwalteten Code für GDI+ gehören zu den folgenden Namespaces.</span><span class="sxs-lookup"><span data-stu-id="efab4-110">The managed-code wrappers for GDI+ belong to the following namespaces.</span></span>

-   [<span data-ttu-id="efab4-111">System.Drawing</span><span class="sxs-lookup"><span data-stu-id="efab4-111">System.Drawing</span></span>](/dotnet/api/system.drawing?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="efab4-112">System. Drawing. Drawing2D</span><span class="sxs-lookup"><span data-stu-id="efab4-112">System.Drawing.Drawing2D</span></span>](/dotnet/api/system.drawing.drawing2d?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="efab4-113">System. Drawing. Imaging</span><span class="sxs-lookup"><span data-stu-id="efab4-113">System.Drawing.Imaging</span></span>](/dotnet/api/system.drawing.imaging?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="efab4-114">System. Drawing. Text</span><span class="sxs-lookup"><span data-stu-id="efab4-114">System.Drawing.Text</span></span>](/dotnet/api/system.drawing.text?view=dotnet-plat-ext-3.1&preserve-view=true)

<span data-ttu-id="efab4-115">Beide Wrapper Sätze (C++ und verwalteter Code) verwenden einen objektorientierten Ansatz, daher gibt es einige Unterschiede zwischen der Art und Weise, wie Parameter an die Wrapper Methoden und wie Parameter an Funktionen in der flatapi übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="efab4-115">Both sets of wrappers (C++ and managed code) use an object-oriented approach, so there are some differences between the way parameters are passed to the wrapper methods and the way parameters are passed to functions in the flat API.</span></span> <span data-ttu-id="efab4-116">Beispielsweise ist einer der C++-Wrapper die [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="efab4-116">For example, one of the C++ wrappers is the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class.</span></span> <span data-ttu-id="efab4-117">Jedes **Matrix** Objekt verfügt über das Feld **nativematrix**, das auf eine interne Variable des Typs **gpmatrix** zeigt.</span><span class="sxs-lookup"><span data-stu-id="efab4-117">Each **Matrix** object has a field, **nativeMatrix**, that points to an internal variable of type **GpMatrix**.</span></span> <span data-ttu-id="efab4-118">Wenn Sie Parameter an eine Methode eines **Matrix** Objekts übergeben, übergibt diese Methode diese Parameter (oder einen Satz verwandter Parameter) an eine der Funktionen in der GDI+-flatapi.</span><span class="sxs-lookup"><span data-stu-id="efab4-118">When you pass parameters to a method of a **Matrix** object, that method passes those parameters (or a set of related parameters) along to one of the functions in the GDI+ flat API.</span></span> <span data-ttu-id="efab4-119">Diese Methode übergibt jedoch auch das Feld " **nativematrix** " (als Eingabeparameter) an die flatapi-Funktion.</span><span class="sxs-lookup"><span data-stu-id="efab4-119">But that method also passes the **nativeMatrix** field (as an input parameter) to the flat API function.</span></span> <span data-ttu-id="efab4-120">Der folgende Code zeigt, wie die [**Matrix:: Shear**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) -Methode die Funktion **gdipshearmatrix aufruft (gpmatrix \* Matrix, Real shearX, Real shearY, gpmatrixorder Order)** .</span><span class="sxs-lookup"><span data-stu-id="efab4-120">The following code shows how the [**Matrix::Shear**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) method calls the **GdipShearMatrix(GpMatrix \*matrix, REAL shearX, REAL shearY, GpMatrixOrder order)** function.</span></span>


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



<span data-ttu-id="efab4-121">Die [**matrixkonstruktoren**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) übergeben die Adresse einer **gpmatrix** -Zeiger Variablen (als Ausgabeparameter) an die Funktion **gdipanatematrix (gpmatrix \* \* Matrix)** .</span><span class="sxs-lookup"><span data-stu-id="efab4-121">The [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) constructors pass the address of a **GpMatrix** pointer variable (as an output parameter) to the **GdipCreateMatrix(GpMatrix \*\*matrix)** function.</span></span> <span data-ttu-id="efab4-122">**Gdipkreatematrix** erstellt und Initialisiert eine interne **gpmatrix** -Variable und weist dann die Adresse der **gpmatrix** der Zeiger Variablen zu.</span><span class="sxs-lookup"><span data-stu-id="efab4-122">**GdipCreateMatrix** creates and initializes an internal **GpMatrix** variable and then assigns the address of the **GpMatrix** to the pointer variable.</span></span> <span data-ttu-id="efab4-123">Anschließend kopiert der Konstruktor den Wert des Zeigers in das Feld **nativematrix** .</span><span class="sxs-lookup"><span data-stu-id="efab4-123">Then the constructor copies the value of the pointer to the **nativeMatrix** field.</span></span>


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



<span data-ttu-id="efab4-124">Klon Methoden in den Wrapper Klassen empfangen keine Parameter, übergeben jedoch oft zwei Parameter an die zugrunde liegende Funktion in der GDI+-flatapi.</span><span class="sxs-lookup"><span data-stu-id="efab4-124">Clone methods in the wrapper classes receive no parameters but often pass two parameters to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="efab4-125">Die [**Matrix:: Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) -Methode übergibt z. b. **nativematrix** (als Eingabeparameter) und die Adresse einer **gpmatrix** -Zeiger Variablen (als Ausgabeparameter) an die **gdipclonematrix** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="efab4-125">For example, the [**Matrix::Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) method passes **nativeMatrix** (as an input parameter) and the address of a **GpMatrix** pointer variable (as an output parameter) to the **GdipCloneMatrix** function.</span></span> <span data-ttu-id="efab4-126">Der folgende Code zeigt, wie die **Matrix:: Clone** -Methode die **gdipclonematrix-Funktion (gpmatrix- \* Matrix, gpmatrix \* \* clonematrix)** aufruft.</span><span class="sxs-lookup"><span data-stu-id="efab4-126">The following code shows how the **Matrix::Clone** method calls the **GdipCloneMatrix(GpMatrix \*matrix, GpMatrix \*\*cloneMatrix)** function.</span></span>


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



<span data-ttu-id="efab4-127">Die Funktionen in der flatapi geben einen Wert vom Typ gpstatus zurück.</span><span class="sxs-lookup"><span data-stu-id="efab4-127">The functions in the flat API return a value of type GpStatus.</span></span> <span data-ttu-id="efab4-128">Die gpstatus-Enumeration ist identisch mit der [**statusenumeration**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) , die von den Wrapper Methoden verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="efab4-128">The GpStatus enumeration is identical to the [**Status**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) enumeration used by the wrapper methods.</span></span> <span data-ttu-id="efab4-129">In "gdiplusgpstusb. h" ist gpstatus wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="efab4-129">In GdiplusGpStubs.h, GpStatus is defined as follows:</span></span>

`typedef Status GpStatus;`

<span data-ttu-id="efab4-130">Die meisten Methoden in den Wrapper Klassen geben einen Statuswert zurück, der angibt, ob die Methode erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="efab4-130">Most of the methods in the wrapper classes return a status value that indicates whether the method succeeded.</span></span> <span data-ttu-id="efab4-131">Einige der Wrapper Methoden geben jedoch Zustands Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="efab4-131">However, some of the wrapper methods return state values.</span></span> <span data-ttu-id="efab4-132">Wenn Sie eine Wrapper Methode aufzurufen, die einen Zustandswert zurückgibt, übergibt die Wrapper Methode die entsprechenden Parameter an die zugrunde liegende Funktion in der GDI+-flatapi.</span><span class="sxs-lookup"><span data-stu-id="efab4-132">When you call a wrapper method that returns a state value, the wrapper method passes the appropriate parameters to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="efab4-133">Die [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) Klasse verfügt beispielsweise über eine [**Matrix:: IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) -Methode, die das Feld " **nativematrix** " und die Adresse einer **booleschen** Variablen (als Ausgabeparameter) an die **gdipismatrixinvertible** -Funktion übergibt.</span><span class="sxs-lookup"><span data-stu-id="efab4-133">For example, the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class has an [**Matrix::IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) method that passes the **nativeMatrix** field and and the address of a **BOOL** variable (as an output parameter) to the **GdipIsMatrixInvertible** function.</span></span> <span data-ttu-id="efab4-134">Der folgende Code zeigt, wie die **Matrix:: IsInvertible** -Methode die **gdipismatrixinvertible-Funktion (gdipkonstanten gpmatrix \* Matrix, bool \* result)** aufruft.</span><span class="sxs-lookup"><span data-stu-id="efab4-134">The following code shows how the **Matrix::IsInvertible** method calls the **GdipIsMatrixInvertible(GDIPCONST GpMatrix \*matrix, BOOL \*result)** function.</span></span>


```
BOOL IsInvertible() const
{
   BOOL result = FALSE;
   ...
   GdipIsMatrixInvertible(nativeMatrix, &result);
   return result;
}
```



<span data-ttu-id="efab4-135">Ein weiterer Wrapper ist die [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="efab4-135">Another one of the wrappers is the [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) class.</span></span> <span data-ttu-id="efab4-136">Ein **Color** -Objekt verfügt über ein einzelnes Feld vom Typ **ARGB**, das als **DWORD** definiert ist.</span><span class="sxs-lookup"><span data-stu-id="efab4-136">A **Color** object has a single field of type **ARGB**, which is defined as a **DWORD**.</span></span> <span data-ttu-id="efab4-137">Wenn Sie ein **Color** -Objekt an eine der Wrapper Methoden übergeben, übergibt diese Methode das **ARGB** -Feld an die zugrunde liegende Funktion in der GDI+-flatapi.</span><span class="sxs-lookup"><span data-stu-id="efab4-137">When you pass a **Color** object to one of the wrapper methods, that method passes the **ARGB** field along to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="efab4-138">Der folgende Code zeigt, wie die [**Pen:: SetColor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) -Methode die **gdipsetpencolor (gppen \* Pen, ARGB ARGB)** -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="efab4-138">The following code shows how the [**Pen::SetColor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) method calls the **GdipSetPenColor(GpPen \*pen, ARGB argb)** function.</span></span> <span data-ttu-id="efab4-139">Die [**Color:: GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) -Methode gibt den Wert des **ARGB** -Felds zurück.</span><span class="sxs-lookup"><span data-stu-id="efab4-139">The [**Color::GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) method returns the value of the **ARGB** field.</span></span>


```
Status SetColor(IN const Color& color)
{
   ...
   GdipSetPenColor(nativePen, color.GetValue());
}
```



<span data-ttu-id="efab4-140">In den folgenden Themen wird die Beziehung zwischen der flatapi GDI+ und den C++-Wrapper Methoden veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="efab4-140">The following topics show the relationship between the GDI+ flat API and the C++ wrapper methods.</span></span>

-   [<span data-ttu-id="efab4-141">AdjustableArrowCap-Funktionen</span><span class="sxs-lookup"><span data-stu-id="efab4-141">AdjustableArrowCap Functions</span></span>](-gdiplus-adjustablearrowcap-flat.md)
-   [<span data-ttu-id="efab4-142">Bitmap-Funktionen</span><span class="sxs-lookup"><span data-stu-id="efab4-142">Bitmap Functions</span></span>](-gdiplus-bitmap-flat.md)
-   [<span data-ttu-id="efab4-143">Pinsel Funktionen</span><span class="sxs-lookup"><span data-stu-id="efab4-143">Brush Functions</span></span>](-gdiplus-brush-flat.md)
-   [<span data-ttu-id="efab4-144">CachedBitmap-Funktionen</span><span class="sxs-lookup"><span data-stu-id="efab4-144">CachedBitmap Functions</span></span>](-gdiplus-cachedbitmap-flat.md)
-   [<span data-ttu-id="efab4-145">CustomLineCap-Funktionen</span><span class="sxs-lookup"><span data-stu-id="efab4-145">CustomLineCap Functions</span></span>](-gdiplus-customlinecap-flat.md)
-   [<span data-ttu-id="efab4-146">Schriftart Funktionen</span><span class="sxs-lookup"><span data-stu-id="efab4-146">Font Functions</span></span>](-gdiplus-font-flat.md)
-   [<span data-ttu-id="efab4-147">Fontfamilyfunctions</span><span class="sxs-lookup"><span data-stu-id="efab4-147">FontFamilyFunctions</span></span>](-gdiplus-fontfamily-flat.md)
-   [<span data-ttu-id="efab4-148">Grafikfunktionen</span><span class="sxs-lookup"><span data-stu-id="efab4-148">Graphics Functions</span></span>](-gdiplus-graphics-flat.md)
-   [<span data-ttu-id="efab4-149">GraphicsPath-Funktionen</span><span class="sxs-lookup"><span data-stu-id="efab4-149">GraphicsPath Functions</span></span>](-gdiplus-graphicspath-flat.md)
-   [<span data-ttu-id="efab4-150">HatchBrush-Funktionen</span><span class="sxs-lookup"><span data-stu-id="efab4-150">HatchBrush Functions</span></span>](-gdiplus-hatchbrush-flat.md)
-   [<span data-ttu-id="efab4-151">Bildfunktionen</span><span class="sxs-lookup"><span data-stu-id="efab4-151">Image Functions</span></span>](-gdiplus-image-flat.md)
-   [<span data-ttu-id="efab4-152">Imageattribute-Funktionen</span><span class="sxs-lookup"><span data-stu-id="efab4-152">ImageAttributes Functions</span></span>](-gdiplus-imageattributes-flat.md)
-   [<span data-ttu-id="efab4-153">LinearGradientBrush-Funktionen</span><span class="sxs-lookup"><span data-stu-id="efab4-153">LinearGradientBrush Functions</span></span>](-gdiplus-lineargradientbrush-flat.md)
-   [<span data-ttu-id="efab4-154">Matrix Funktionen</span><span class="sxs-lookup"><span data-stu-id="efab4-154">Matrix Functions</span></span>](-gdiplus-matrix-flat.md)
-   [<span data-ttu-id="efab4-155">Speicherfunktionen</span><span class="sxs-lookup"><span data-stu-id="efab4-155">Memory Functions</span></span>](-gdiplus-memory-flat.md)
-   [<span data-ttu-id="efab4-156">Benachrichtigungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="efab4-156">Notification Functions</span></span>](-gdiplus-notification-flat.md)
-   [<span data-ttu-id="efab4-157">PathGradientBrush-Funktionen</span><span class="sxs-lookup"><span data-stu-id="efab4-157">PathGradientBrush Functions</span></span>](-gdiplus-pathgradientbrush-flat.md)
-   [<span data-ttu-id="efab4-158">Funktionen von "pthiterator"</span><span class="sxs-lookup"><span data-stu-id="efab4-158">PathIterator Functions</span></span>](-gdiplus-pathiterator-flat.md)
-   [<span data-ttu-id="efab4-159">Stift Funktionen</span><span class="sxs-lookup"><span data-stu-id="efab4-159">Pen Functions</span></span>](-gdiplus-pen-flat.md)
-   [<span data-ttu-id="efab4-160">Regions Funktionen</span><span class="sxs-lookup"><span data-stu-id="efab4-160">Region Functions</span></span>](-gdiplus-region-flat.md)
-   [<span data-ttu-id="efab4-161">SolidBrush-Funktionen</span><span class="sxs-lookup"><span data-stu-id="efab4-161">SolidBrush Functions</span></span>](-gdiplus-solidbrush-flat.md)
-   [<span data-ttu-id="efab4-162">Zeichen folgen Format-Funktionen</span><span class="sxs-lookup"><span data-stu-id="efab4-162">String Format Functions</span></span>](-gdiplus-stringformat-flat.md)
-   [<span data-ttu-id="efab4-163">Text Funktionen</span><span class="sxs-lookup"><span data-stu-id="efab4-163">Text Functions</span></span>](-gdiplus-text-flat.md)
-   [<span data-ttu-id="efab4-164">Textur Pinsel Funktionen</span><span class="sxs-lookup"><span data-stu-id="efab4-164">Texture Brush Functions</span></span>](-gdiplus-texturebrush-flat.md)

 

 
