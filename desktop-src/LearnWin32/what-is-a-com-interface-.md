---
title: Was ist eine COM-Schnittstelle?
description: Was ist eine COM-Schnittstelle?
ms.assetid: 36f27a58-cc63-4b67-bdcb-8f9a19650c6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da703569beae7a9aa2fc41bcea0214cc9aa488ad
ms.sourcegitcommit: 8eac40ea4d87a85e036ed5bbffec7b7a3dab39ec
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2019
ms.locfileid: "104388830"
---
# <a name="what-is-a-com-interface"></a><span data-ttu-id="d41bc-103">Was ist eine COM-Schnittstelle?</span><span class="sxs-lookup"><span data-stu-id="d41bc-103">What Is a COM Interface?</span></span>

<span data-ttu-id="d41bc-104">Wenn Sie c# oder Java kennen, sollten Schnittstellen ein bekanntes Konzept sein.</span><span class="sxs-lookup"><span data-stu-id="d41bc-104">If you know C# or Java, interfaces should be a familiar concept.</span></span> <span data-ttu-id="d41bc-105">Eine *Schnittstelle* definiert eine Reihe von Methoden, die von einem Objekt unterstützt werden können, ohne dass etwas über die Implementierung definiert wird.</span><span class="sxs-lookup"><span data-stu-id="d41bc-105">An *interface* defines a set of methods that an object can support, without dictating anything about the implementation.</span></span> <span data-ttu-id="d41bc-106">Die-Schnittstelle markiert eine klare Grenze zwischen dem Code, der eine Methode aufruft, und dem Code, der die-Methode implementiert.</span><span class="sxs-lookup"><span data-stu-id="d41bc-106">The interface marks a clear boundary between code that calls a method and the code that implements the method.</span></span> <span data-ttu-id="d41bc-107">In Bezug auf die Computerwissenschaft wird der Aufrufer von der-Implementierung *entkoppelt* .</span><span class="sxs-lookup"><span data-stu-id="d41bc-107">In computer science terms, the caller is *decoupled* from the implementation.</span></span>

![Darstellung der Schnittstellen Grenze zwischen einem Objekt und einer Anwendung](images/com01.png)

<span data-ttu-id="d41bc-109">In C++ ist das nächstgelegene Äquivalent zu einer Schnittstelle eine rein virtuelle Klasse – d. h. eine Klasse, die nur rein virtuelle Methoden und keine anderen Member enthält.</span><span class="sxs-lookup"><span data-stu-id="d41bc-109">In C++, the nearest equivalent to an interface is a pure virtual class—that is, a class that contains only pure virtual methods and no other members.</span></span> <span data-ttu-id="d41bc-110">Im folgenden finden Sie ein hypothetisches Beispiel für eine Schnittstelle:</span><span class="sxs-lookup"><span data-stu-id="d41bc-110">Here is a hypothetical example of an interface:</span></span>

```C++
// The following is not actual COM.

// Pseudo-C++:

interface IDrawable
{
    void Draw();
};
```

<span data-ttu-id="d41bc-111">Die Idee dieses Beispiels ist, dass ein Satz von Objekten in einer Grafikbibliothek drawable ist.</span><span class="sxs-lookup"><span data-stu-id="d41bc-111">The idea of this example is that a set of objects in some graphics library are drawable.</span></span> <span data-ttu-id="d41bc-112">Die- `IDrawable` Schnittstelle definiert die Vorgänge, die jedes drawable-Objekt unterstützen muss.</span><span class="sxs-lookup"><span data-stu-id="d41bc-112">The `IDrawable` interface defines the operations that any drawable object must support.</span></span> <span data-ttu-id="d41bc-113">(Gemäß der Konvention beginnen Schnittstellennamen mit "I".) In diesem Beispiel definiert die- `IDrawable` Schnittstelle einen einzelnen Vorgang: `Draw` .</span><span class="sxs-lookup"><span data-stu-id="d41bc-113">(By convention, interface names start with "I".) In this example, the `IDrawable` interface defines a single operation: `Draw`.</span></span>

<span data-ttu-id="d41bc-114">Alle Schnittstellen sind *abstrakt*, sodass ein Programm keine Instanz eines `IDrawable` Objekts als solche erstellen konnte.</span><span class="sxs-lookup"><span data-stu-id="d41bc-114">All interfaces are *abstract*, so a program could not create an instance of an `IDrawable` object as such.</span></span> <span data-ttu-id="d41bc-115">Der folgende Code wird z. b. nicht kompiliert.</span><span class="sxs-lookup"><span data-stu-id="d41bc-115">For example, the following code would not compile.</span></span>

```C++
IDrawable draw;
draw.Draw();
```

<span data-ttu-id="d41bc-116">Stattdessen stellt die Grafikbibliothek Objekte bereit,  die die- `IDrawable` Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="d41bc-116">Instead, the graphics library provides objects that *implement* the `IDrawable` interface.</span></span> <span data-ttu-id="d41bc-117">Die Bibliothek kann z. b. ein Shape-Objekt für Zeichnungsformen und ein Bitmap-Objekt zum Zeichnen von Bildern bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d41bc-117">For example, the library might provide a shape object for drawing shapes and a bitmap object for drawing images.</span></span> <span data-ttu-id="d41bc-118">In C++ wird dies durch die Vererbung von einer gemeinsamen abstrakten Basisklasse erreicht:</span><span class="sxs-lookup"><span data-stu-id="d41bc-118">In C++, this is done by inheriting from a common abstract base class:</span></span>

```C++
class Shape : public IDrawable
{
public:
    virtual void Draw();    // Override Draw and provide implementation.
};

class Bitmap : public IDrawable
{
public:
    virtual void Draw();    // Override Draw and provide implementation.
};
```

<span data-ttu-id="d41bc-119">Die `Shape` `Bitmap` Klassen und definieren zwei unterschiedliche Typen von drawable-Objekten.</span><span class="sxs-lookup"><span data-stu-id="d41bc-119">The `Shape` and `Bitmap` classes define two distinct types of drawable object.</span></span> <span data-ttu-id="d41bc-120">Jede Klasse erbt von `IDrawable` und stellt eine eigene Implementierung der- `Draw` Methode bereit.</span><span class="sxs-lookup"><span data-stu-id="d41bc-120">Each class inherits from `IDrawable` and provides its own implementation of the `Draw` method.</span></span> <span data-ttu-id="d41bc-121">Natürlich können sich die beiden Implementierungen erheblich unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="d41bc-121">Naturally, the two implementations might differ considerably.</span></span> <span data-ttu-id="d41bc-122">Beispielsweise kann die- `Shape::Draw` Methode eine Reihe von Zeilen Rasterisieren, während `Bitmap::Draw` ein Array von Pixeln blieren würde.</span><span class="sxs-lookup"><span data-stu-id="d41bc-122">For example, the `Shape::Draw` method might rasterize a set of lines, while `Bitmap::Draw` would blit an array of pixels.</span></span>

<span data-ttu-id="d41bc-123">Ein Programm, das diese Grafikbibliothek verwendet `Shape` , würde-und- `Bitmap` Objekte durch `IDrawable` Zeiger bearbeiten, anstatt `Shape` oder- `Bitmap` Zeiger direkt zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d41bc-123">A program using this graphics library would manipulate `Shape` and `Bitmap` objects through `IDrawable` pointers, rather than using `Shape` or `Bitmap` pointers directly.</span></span>

```C++
IDrawable *pDrawable = CreateTriangleShape();

if (pDrawable)
{
    pDrawable->Draw();
}
```

<span data-ttu-id="d41bc-124">Hier ist ein Beispiel, das ein Array von `IDrawable` Zeigern durchläuft.</span><span class="sxs-lookup"><span data-stu-id="d41bc-124">Here is an example that loops over an array of `IDrawable` pointers.</span></span> <span data-ttu-id="d41bc-125">Das Array kann eine heterogene Palette von Formen, Bitmaps und anderen Grafikobjekten enthalten, solange jedes Objekt im Array erbt `IDrawable` .</span><span class="sxs-lookup"><span data-stu-id="d41bc-125">The array might contain a heterogeneous assortment of shapes, bitmaps, and other graphics objects, as long as each object in the array inherits `IDrawable`.</span></span>

```C++
void DrawSomeShapes(IDrawable **drawableArray, size_t count)
{
    for (size_t i = 0; i < count; i++)
    {
        drawableArray[i]->Draw();
    }
}
```

<span data-ttu-id="d41bc-126">Ein wichtiger Punkt für com besteht darin, dass der aufrufenden Code den Typ der abgeleiteten Klasse nicht sieht.</span><span class="sxs-lookup"><span data-stu-id="d41bc-126">A key point about COM is that the calling code never sees the type of the derived class.</span></span> <span data-ttu-id="d41bc-127">Anders ausgedrückt: Sie würden niemals eine Variable vom Typ `Shape` oder `Bitmap` in Ihrem Code deklarieren.</span><span class="sxs-lookup"><span data-stu-id="d41bc-127">In other words, you would never declare a variable of type `Shape` or `Bitmap` in your code.</span></span> <span data-ttu-id="d41bc-128">Alle Vorgänge für Formen und Bitmaps werden mithilfe von `IDrawable` Zeigern ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d41bc-128">All operations on shapes and bitmaps are performed using `IDrawable` pointers.</span></span> <span data-ttu-id="d41bc-129">Auf diese Weise behält com eine strikte Trennung Zwischenschnitt Stelle und Implementierung bei.</span><span class="sxs-lookup"><span data-stu-id="d41bc-129">In this way, COM maintains a strict separation between interface and implementation.</span></span> <span data-ttu-id="d41bc-130">Die Implementierungsdetails der `Shape` -Klasse und der- `Bitmap` Klasse können sich ändern, z. –. um Fehler zu beheben oder neue Funktionen hinzuzufügen – ohne Änderungen am aufrufenden Code.</span><span class="sxs-lookup"><span data-stu-id="d41bc-130">The implementation details of the `Shape` and `Bitmap` classes can change—for example, to fix bugs or add new capabilities—with no changes to the calling code.</span></span>

<span data-ttu-id="d41bc-131">In einer C++-Implementierung werden Schnittstellen mit einer Klasse oder Struktur deklariert.</span><span class="sxs-lookup"><span data-stu-id="d41bc-131">In a C++ implementation, interfaces are declared using a class or structure.</span></span>

> [!Note]  
> <span data-ttu-id="d41bc-132">Die Codebeispiele in diesem Thema sollen allgemeine Konzepte vermitteln, nicht in der Praxis.</span><span class="sxs-lookup"><span data-stu-id="d41bc-132">The code examples in this topic are meant to convey general concepts, not real-world practice.</span></span> <span data-ttu-id="d41bc-133">Das Definieren neuer COM-Schnittstellen geht über den Rahmen dieser Reihe hinaus, aber Sie würden eine Schnittstelle nicht direkt in einer Header Datei definieren.</span><span class="sxs-lookup"><span data-stu-id="d41bc-133">Defining new COM interfaces is beyond the scope of this series, but you would not define an interface directly in a header file.</span></span> <span data-ttu-id="d41bc-134">Stattdessen wird eine COM-Schnittstelle mithilfe einer Sprache namens Interface Definition Language (IDL) definiert.</span><span class="sxs-lookup"><span data-stu-id="d41bc-134">Instead, a COM interface is defined using a language called Interface Definition Language (IDL).</span></span> <span data-ttu-id="d41bc-135">Die IDL-Datei wird von einem IDL-Compiler verarbeitet, der eine C++-Header Datei generiert.</span><span class="sxs-lookup"><span data-stu-id="d41bc-135">The IDL file is processed by an IDL compiler, which generates a C++ header file.</span></span>

```C++
class IDrawable
{
public:
    virtual void Draw() = 0;
};
```

<span data-ttu-id="d41bc-136">Wenn Sie mit com arbeiten, ist es wichtig zu beachten, dass es sich bei Schnittstellen nicht um Objekte handelt.</span><span class="sxs-lookup"><span data-stu-id="d41bc-136">When you work with COM, it is important to remember that interfaces are not objects.</span></span> <span data-ttu-id="d41bc-137">Sie sind Auflistungen von Methoden, die von Objekten implementiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d41bc-137">They are collections of methods that objects must implement.</span></span> <span data-ttu-id="d41bc-138">Mehrere-Objekte können dieselbe-Schnittstelle implementieren, wie in `Shape` den `Bitmap` Beispielen und gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d41bc-138">Several objects can implement the same interface, as shown with the `Shape` and `Bitmap` examples.</span></span> <span data-ttu-id="d41bc-139">Außerdem kann ein Objekt mehrere Schnittstellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="d41bc-139">Moreover, one object can implement several interfaces.</span></span> <span data-ttu-id="d41bc-140">Beispielsweise kann die Grafikbibliothek eine Schnittstelle mit dem Namen definieren `ISerializable` , die das Speichern und Laden von Grafikobjekten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d41bc-140">For example, the graphics library might define an interface named `ISerializable` that supports saving and loading graphics objects.</span></span> <span data-ttu-id="d41bc-141">Beachten Sie nun die folgenden Klassen Deklarationen:</span><span class="sxs-lookup"><span data-stu-id="d41bc-141">Now consider the following class declarations:</span></span>

```C++
// An interface for serialization.
class ISerializable
{
public:
    virtual void Load(PCWSTR filename) = 0;    // Load from file.
    virtual void Save(PCWSTR filename) = 0;    // Save to file.
};

// Declarations of drawable object types.

class Shape : public IDrawable
{
    ...
};

class Bitmap : public IDrawable, public ISerializable
{
    ...
};
```

<span data-ttu-id="d41bc-142">In diesem Beispiel implementiert die- `Bitmap` Klasse `ISerializable` .</span><span class="sxs-lookup"><span data-stu-id="d41bc-142">In this example, the `Bitmap` class implements `ISerializable`.</span></span> <span data-ttu-id="d41bc-143">Das Programm kann diese Methode verwenden, um die Bitmap zu speichern oder zu laden.</span><span class="sxs-lookup"><span data-stu-id="d41bc-143">The program could use this method to save or load the bitmap.</span></span> <span data-ttu-id="d41bc-144">Die- `Shape` Klasse implementiert jedoch nicht `ISerializable` , sodass diese Funktionalität nicht verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="d41bc-144">However, the `Shape` class does not implement `ISerializable`, so it does not expose that functionality.</span></span> <span data-ttu-id="d41bc-145">Das folgende Diagramm zeigt die Vererbungs Beziehungen in diesem Beispiel.</span><span class="sxs-lookup"><span data-stu-id="d41bc-145">The following diagram shows the inheritance relations in this example.</span></span>

![Darstellung der Schnittstellen Vererbung mit den Formen und bitmapklassen, die auf idrawable zeigen, aber nur Bitmap, die auf iserialisierbar zeigt](images/com02.png)

<span data-ttu-id="d41bc-147">In diesem Abschnitt wurde die konzeptionelle Grundlage der Schnittstellen untersucht, bisher haben wir jedoch noch nicht den tatsächlichen com-Code gesehen.</span><span class="sxs-lookup"><span data-stu-id="d41bc-147">This section has examined the conceptual basis of interfaces, but so far we have not seen actual COM code.</span></span> <span data-ttu-id="d41bc-148">Wir beginnen mit dem ersten, was jede com-Anwendung tun muss: Initialisieren Sie die com-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="d41bc-148">We'll start with the first thing that any COM application must do: Initialize the COM library.</span></span>

## <a name="next"></a><span data-ttu-id="d41bc-149">Nächste</span><span class="sxs-lookup"><span data-stu-id="d41bc-149">Next</span></span>

[<span data-ttu-id="d41bc-150">Initialisieren der com-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d41bc-150">Initializing the COM Library</span></span>](initializing-the-com-library.md)