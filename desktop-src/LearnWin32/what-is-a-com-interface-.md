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
# <a name="what-is-a-com-interface"></a>Was ist eine COM-Schnittstelle?

Wenn Sie c# oder Java kennen, sollten Schnittstellen ein bekanntes Konzept sein. Eine *Schnittstelle* definiert eine Reihe von Methoden, die von einem Objekt unterstützt werden können, ohne dass etwas über die Implementierung definiert wird. Die-Schnittstelle markiert eine klare Grenze zwischen dem Code, der eine Methode aufruft, und dem Code, der die-Methode implementiert. In Bezug auf die Computerwissenschaft wird der Aufrufer von der-Implementierung *entkoppelt* .

![Darstellung der Schnittstellen Grenze zwischen einem Objekt und einer Anwendung](images/com01.png)

In C++ ist das nächstgelegene Äquivalent zu einer Schnittstelle eine rein virtuelle Klasse – d. h. eine Klasse, die nur rein virtuelle Methoden und keine anderen Member enthält. Im folgenden finden Sie ein hypothetisches Beispiel für eine Schnittstelle:

```C++
// The following is not actual COM.

// Pseudo-C++:

interface IDrawable
{
    void Draw();
};
```

Die Idee dieses Beispiels ist, dass ein Satz von Objekten in einer Grafikbibliothek drawable ist. Die- `IDrawable` Schnittstelle definiert die Vorgänge, die jedes drawable-Objekt unterstützen muss. (Gemäß der Konvention beginnen Schnittstellennamen mit "I".) In diesem Beispiel definiert die- `IDrawable` Schnittstelle einen einzelnen Vorgang: `Draw` .

Alle Schnittstellen sind *abstrakt*, sodass ein Programm keine Instanz eines `IDrawable` Objekts als solche erstellen konnte. Der folgende Code wird z. b. nicht kompiliert.

```C++
IDrawable draw;
draw.Draw();
```

Stattdessen stellt die Grafikbibliothek Objekte bereit,  die die- `IDrawable` Schnittstelle implementieren. Die Bibliothek kann z. b. ein Shape-Objekt für Zeichnungsformen und ein Bitmap-Objekt zum Zeichnen von Bildern bereitstellen. In C++ wird dies durch die Vererbung von einer gemeinsamen abstrakten Basisklasse erreicht:

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

Die `Shape` `Bitmap` Klassen und definieren zwei unterschiedliche Typen von drawable-Objekten. Jede Klasse erbt von `IDrawable` und stellt eine eigene Implementierung der- `Draw` Methode bereit. Natürlich können sich die beiden Implementierungen erheblich unterscheiden. Beispielsweise kann die- `Shape::Draw` Methode eine Reihe von Zeilen Rasterisieren, während `Bitmap::Draw` ein Array von Pixeln blieren würde.

Ein Programm, das diese Grafikbibliothek verwendet `Shape` , würde-und- `Bitmap` Objekte durch `IDrawable` Zeiger bearbeiten, anstatt `Shape` oder- `Bitmap` Zeiger direkt zu verwenden.

```C++
IDrawable *pDrawable = CreateTriangleShape();

if (pDrawable)
{
    pDrawable->Draw();
}
```

Hier ist ein Beispiel, das ein Array von `IDrawable` Zeigern durchläuft. Das Array kann eine heterogene Palette von Formen, Bitmaps und anderen Grafikobjekten enthalten, solange jedes Objekt im Array erbt `IDrawable` .

```C++
void DrawSomeShapes(IDrawable **drawableArray, size_t count)
{
    for (size_t i = 0; i < count; i++)
    {
        drawableArray[i]->Draw();
    }
}
```

Ein wichtiger Punkt für com besteht darin, dass der aufrufenden Code den Typ der abgeleiteten Klasse nicht sieht. Anders ausgedrückt: Sie würden niemals eine Variable vom Typ `Shape` oder `Bitmap` in Ihrem Code deklarieren. Alle Vorgänge für Formen und Bitmaps werden mithilfe von `IDrawable` Zeigern ausgeführt. Auf diese Weise behält com eine strikte Trennung Zwischenschnitt Stelle und Implementierung bei. Die Implementierungsdetails der `Shape` -Klasse und der- `Bitmap` Klasse können sich ändern, z. –. um Fehler zu beheben oder neue Funktionen hinzuzufügen – ohne Änderungen am aufrufenden Code.

In einer C++-Implementierung werden Schnittstellen mit einer Klasse oder Struktur deklariert.

> [!Note]  
> Die Codebeispiele in diesem Thema sollen allgemeine Konzepte vermitteln, nicht in der Praxis. Das Definieren neuer COM-Schnittstellen geht über den Rahmen dieser Reihe hinaus, aber Sie würden eine Schnittstelle nicht direkt in einer Header Datei definieren. Stattdessen wird eine COM-Schnittstelle mithilfe einer Sprache namens Interface Definition Language (IDL) definiert. Die IDL-Datei wird von einem IDL-Compiler verarbeitet, der eine C++-Header Datei generiert.

```C++
class IDrawable
{
public:
    virtual void Draw() = 0;
};
```

Wenn Sie mit com arbeiten, ist es wichtig zu beachten, dass es sich bei Schnittstellen nicht um Objekte handelt. Sie sind Auflistungen von Methoden, die von Objekten implementiert werden müssen. Mehrere-Objekte können dieselbe-Schnittstelle implementieren, wie in `Shape` den `Bitmap` Beispielen und gezeigt. Außerdem kann ein Objekt mehrere Schnittstellen implementieren. Beispielsweise kann die Grafikbibliothek eine Schnittstelle mit dem Namen definieren `ISerializable` , die das Speichern und Laden von Grafikobjekten unterstützt. Beachten Sie nun die folgenden Klassen Deklarationen:

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

In diesem Beispiel implementiert die- `Bitmap` Klasse `ISerializable` . Das Programm kann diese Methode verwenden, um die Bitmap zu speichern oder zu laden. Die- `Shape` Klasse implementiert jedoch nicht `ISerializable` , sodass diese Funktionalität nicht verfügbar gemacht wird. Das folgende Diagramm zeigt die Vererbungs Beziehungen in diesem Beispiel.

![Darstellung der Schnittstellen Vererbung mit den Formen und bitmapklassen, die auf idrawable zeigen, aber nur Bitmap, die auf iserialisierbar zeigt](images/com02.png)

In diesem Abschnitt wurde die konzeptionelle Grundlage der Schnittstellen untersucht, bisher haben wir jedoch noch nicht den tatsächlichen com-Code gesehen. Wir beginnen mit dem ersten, was jede com-Anwendung tun muss: Initialisieren Sie die com-Bibliothek.

## <a name="next"></a>Nächste

[Initialisieren der com-Bibliothek](initializing-the-com-library.md)