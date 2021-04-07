---
title: Eindeutige Zeiger
description: In C-Programmen können mehr als ein Zeiger die Daten Adresse enthalten.
ms.assetid: da4f466d-2c59-4e48-b6c5-1a49b933621a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc8cf9a45965c82416ec838f8598c2796ba621a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039026"
---
# <a name="unique-pointers"></a>Eindeutige Zeiger

In C-Programmen können mehr als ein Zeiger die Daten Adresse enthalten. Die Zeiger werden als [*Alias*](a-glos.md) für die Daten bezeichnet. Aliase werden auch erstellt, wenn Zeiger auf deklarierte Variablen zeigen. Das folgende Code Fragment veranschaulicht beide Methoden der Aliasing:


```C++
int iAnInteger=50;

// The next statement makes ipAnIntegerPointer an
// alias for iAnInteger.
int *ipAnIntegerPointer = &iAnInteger;

// This statement creates an alias for ipAnIntegerPointer.
int *ipAnotherIntegerPointer = ipAnIntegerPointer;
```



In einem typischen C-Programm können Sie mithilfe der folgenden Definition eine binäre Struktur angeben:


```C++
typedef struct _treetype 
{
    long               lValue;
    struct _treetype * left;
    struct _treetype * right;
} TREETYPE;

TREETYPE * troot;
```



Mehr als ein Zeiger kann auf den Inhalt eines Struktur Knotens zugreifen. Dies eignet sich im Allgemeinen für nicht verteilte Anwendungen. Dieser Programmierstil generiert jedoch komplizierteren RPC-Unterstützungs Code. Die Client-und serverstubdateien erfordern zusätzlichen Code zum Verwalten der Daten und Zeiger. Der zugrunde liegende Stubcode muss die verschiedenen Zeiger auf die Adressen auflösen und ermitteln, welche Kopie der Daten die aktuellste Version darstellt.

Die Verarbeitungs Menge kann reduziert werden, wenn Sie sicherstellen, dass der Zeiger die einzige Möglichkeit ist, auf diesen Speicherbereich zuzugreifen. Der Zeiger kann noch viele der Features eines C-Zeigers aufweisen. Beispielsweise kann er zwischen **null** -Werten und nicht-**null** -Werten wechseln oder unverändert bleiben. Dies wird anhand des folgenden Beispiels veranschaulicht. Der Zeiger ist vor dem-Befehl **null** und zeigt auf eine gültige Zeichenfolge nach dem-Befehl:

![Zeiger Wechsel zwischen NULL-Werten und nicht-NULL-Werten](images/prog-a01.png)

Standardmäßig wendet der mittlerer l-Compiler das \[ [eindeutige](/windows/desktop/Midl/unique) \] Zeiger Attribut auf alle Zeiger an, die keine Parameter sind. Diese Standardeinstellung kann mit dem \[ [Zeiger \_ default](/windows/desktop/Midl/pointer-default) -Attribut geändert werden \] .

Ein eindeutiger Zeiger weist die folgenden Eigenschaften auf:

-   Der Wert kann **null** sein.
-   Sie kann während des-Aufrufes von **null** in ungleich **null** wechseln. Wenn der Wert in einen nicht-**null**-Wert geändert wird, wird bei der Rückgabe neuer Speicher zugeordnet.
-   Sie kann während des Aufrufes von ungleich **null** zu **null** wechseln. Wenn der Wert in **null** geändert wird, ist die Anwendung dafür verantwortlich, den Arbeitsspeicher freizugeben.
-   Der Wert kann von einem nicht-**null** -Wert in einen anderen Wert geändert werden.
-   Auf den Speicher, auf den ein eindeutiger Zeiger verweist, kann von keinem anderen Zeiger oder Namen im Vorgang zugegriffen werden.
-   Rückgabe Daten werden in den vorhandenen Speicher geschrieben, wenn der Zeiger nicht den Wert **null** hat.

Im folgenden Beispiel wird veranschaulicht, wie ein eindeutiger Zeiger definiert wird.

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, unique] char *ach);
}
```

In diesem Beispiel ist der Parameter " *Ach* " ein eindeutiger Zeiger auf Zeichendaten, die an einen Server gesendet werden, der mit der remotefn-Routine verarbeitet wird.

 

 