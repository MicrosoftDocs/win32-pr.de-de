---
title: Was ist eine COM-Schnittstelle?
description: Was ist eine COM-Schnittstelle?
ms.assetid: 36f27a58-cc63-4b67-bdcb-8f9a19650c6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a6eac63fb6395e04f36c89826a392046c906a70105e19bb6b9514975d89197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387603"
---
# <a name="what-is-a-com-interface"></a>Was ist eine COM-Schnittstelle?

Wenn Sie C# oder Java kennen, sollten Schnittstellen ein vertrautes Konzept sein. Eine *Schnittstelle* definiert einen Satz von Methoden, die ein Objekt unterstützen kann, ohne etwas über die Implementierung zu diktieren. Die -Schnittstelle markiert eine klare Grenze zwischen Code, der eine Methode aufruft, und dem Code, der die -Methode implementiert. In der Computer science ist der Aufrufer von der Implementierung *entkoppelt.*

![Abbildung der Schnittstellengrenze zwischen einem Objekt und einer Anwendung](images/com01.png)

In C++ ist die nächste Entsprechung zu einer Schnittstelle eine reine virtuelle Klasse, d. h. eine Klasse, die nur reine virtuelle Methoden und keine anderen Member enthält. Hier ist ein hypothetisches Beispiel für eine Schnittstelle:

```C++
// The following is not actual COM.

// Pseudo-C++:

interface IDrawable
{
    void Draw();
};
```

Die Idee dieses Beispiels ist, dass ein Satz von Objekten in einigen Grafikbibliotheken gezeichnet werden kann. Die `IDrawable` -Schnittstelle definiert die Vorgänge, die jedes drawable-Objekt unterstützen muss. (Gemäß Konvention beginnen Schnittstellennamen mit "I".) In diesem Beispiel definiert die `IDrawable` -Schnittstelle einen einzelnen Vorgang: `Draw` .

Alle Schnittstellen sind *abstrakt,* sodass ein Programm keine Instanz eines Objekts als solches erstellen `IDrawable` konnte. Beispielsweise würde der folgende Code nicht kompiliert werden.

```C++
IDrawable draw;
draw.Draw();
```

Stattdessen stellt die Grafikbibliothek Objekte bereit, die die  `IDrawable` -Schnittstelle implementieren. Beispielsweise kann die Bibliothek ein Shape-Objekt zum Zeichnen von Formen und ein Bitmapobjekt zum Zeichnen von Bildern bereitstellen. In C++ wird dies durch Erben von einer gemeinsamen abstrakten Basisklasse erreicht:

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

Die `Shape` Klassen und definieren zwei `Bitmap` unterschiedliche Typen von drawable-Objekten. Jede Klasse erbt von `IDrawable` und stellt eine eigene Implementierung der `Draw` -Methode bereit. Natürlich können sich die beiden Implementierungen erheblich unterscheiden. Die -Methode kann z. B. `Shape::Draw` eine Reihe von Zeilen rastern, während ein Array von `Bitmap::Draw` Pixeln mit einem Bliting ausstrickst.

Ein Programm, das diese Grafikbibliothek verwendet, würde `Shape` - und `Bitmap` -Objekte über Zeiger `IDrawable` bearbeiten, anstatt oder -Zeiger direkt zu `Shape` `Bitmap` verwenden.

```C++
IDrawable *pDrawable = CreateTriangleShape();

if (pDrawable)
{
    pDrawable->Draw();
}
```

Hier ist ein Beispiel, das eine Schleife über ein Array von `IDrawable` Zeigern durchläuft. Das Array kann eine heterogene Auswahl von Formen, Bitmaps und anderen Grafikobjekten enthalten, solange jedes Objekt im Array `IDrawable` erbt.

```C++
void DrawSomeShapes(IDrawable **drawableArray, size_t count)
{
    for (size_t i = 0; i < count; i++)
    {
        drawableArray[i]->Draw();
    }
}
```

Ein wichtiger Punkt bei COM ist, dass der aufrufende Code nie den Typ der abgeleiteten Klasse erkennt. Anders ausgedrückt: Sie würden niemals eine Variable vom Typ `Shape` oder im Code deklarieren. `Bitmap` Alle Vorgänge für Formen und Bitmaps werden mit `IDrawable` Zeigern ausgeführt. Auf diese Weise verwaltet COM eine strikte Trennung zwischen Schnittstelle und Implementierung. Die Implementierungsdetails der `Shape` Klassen und können sich ändern , `Bitmap` z. B. um Fehler zu beheben oder neue Funktionen hinzuzufügen, ohne Änderungen am aufrufenden Code vorzunehmen.

In einer C++-Implementierung werden Schnittstellen mithilfe einer Klasse oder Struktur deklariert.

> [!Note]  
> Die Codebeispiele in diesem Thema sollen allgemeine Konzepte vermitteln, nicht reale Praxis. Das Definieren neuer COM-Schnittstellen würde den Rahmen dieser Reihe sprengen, aber Sie würden keine Schnittstelle direkt in einer Headerdatei definieren. Stattdessen wird eine COM-Schnittstelle mithilfe einer Sprache namens Interface Definition Language (IDL) definiert. Die IDL-Datei wird von einem IDL-Compiler verarbeitet, der eine C++-Headerdatei generiert.

```C++
class IDrawable
{
public:
    virtual void Draw() = 0;
};
```

Wenn Sie mit COM arbeiten, ist es wichtig zu beachten, dass Schnittstellen keine Objekte sind. Dabei handelt es sich um Auflistungen von Methoden, die Objekte implementieren müssen. Mehrere Objekte können die gleiche Schnittstelle implementieren, wie in den `Shape` Beispielen und `Bitmap` gezeigt. Darüber hinaus kann ein Objekt mehrere Schnittstellen implementieren. Beispielsweise kann die Grafikbibliothek eine Schnittstelle namens `ISerializable` definieren, die das Speichern und Laden von Grafikobjekten unterstützt. Betrachten Sie nun die folgenden Klassendeklarationen:

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

In diesem Beispiel implementiert die `Bitmap` -Klasse `ISerializable` . Das Programm kann diese Methode verwenden, um die Bitmap zu speichern oder zu laden. Die -Klasse implementiert jedoch `Shape` nicht `ISerializable` , sodass sie diese Funktionalität nicht verfügbar macht. Das folgende Diagramm zeigt die Vererbungsbeziehungen in diesem Beispiel.

![Abbildung der Schnittstellenvererbung, wobei die Form- und Bitmapklassen auf idrawable zeigen, aber nur Bitmap, die auf iserializable zeigt](images/com02.png)

In diesem Abschnitt wurde die konzeptionelle Grundlage von Schnittstellen untersucht, aber bisher haben wir keinen tatsächlichen COM-Code gesehen. Wir beginnen mit dem ersten, was jede COM-Anwendung tun muss: Initialisieren der COM-Bibliothek.

## <a name="next"></a>Nächste

[Initialisieren der COM-Bibliothek](initializing-the-com-library.md)