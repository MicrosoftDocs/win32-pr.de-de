---
title: Eindeutige Zeiger
description: In C-Programmen können mehr als ein Zeiger die Adresse der Daten enthalten.
ms.assetid: da4f466d-2c59-4e48-b6c5-1a49b933621a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3adb39d2505daa623f23f47c936fb73d0ecff6e0ad7749c951f9926fd66f33d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010992"
---
# <a name="unique-pointers"></a>Eindeutige Zeiger

In C-Programmen können mehr als ein Zeiger die Adresse der Daten enthalten. Die Zeiger sollen einen [*Alias*](a-glos.md) für die Daten erstellen. Aliase werden auch erstellt, wenn Zeiger auf deklarierte Variablen zeigen. Das folgende Codefragment veranschaulicht beide Methoden des Aliasings:


```C++
int iAnInteger=50;

// The next statement makes ipAnIntegerPointer an
// alias for iAnInteger.
int *ipAnIntegerPointer = &iAnInteger;

// This statement creates an alias for ipAnIntegerPointer.
int *ipAnotherIntegerPointer = ipAnIntegerPointer;
```



In einem typischen C-Programm können Sie eine binäre Struktur mit der folgenden Definition angeben:


```C++
typedef struct _treetype 
{
    long               lValue;
    struct _treetype * left;
    struct _treetype * right;
} TREETYPE;

TREETYPE * troot;
```



Mehrere Zeiger können auf den Inhalt eines Strukturknotens zugreifen. Dies ist in der Regel für nicht verteilte Anwendungen in Ordnung. Dieser Programmierstil generiert jedoch komplizierteren RPC-Unterstützungscode. Die Client- und Serverstubs erfordern den zusätzlichen Code, um die Daten und Zeiger zu verwalten. Der zugrunde liegende Stubcode muss die verschiedenen Zeiger auf die Adressen auflösen und bestimmen, welche Kopie der Daten die neueste Version darstellt.

Die Verarbeitungsmenge kann reduziert werden, wenn Sie garantieren, dass Ihr Zeiger die einzige Möglichkeit ist, mit der die Anwendung auf diesen Speicherbereich zugreifen kann. Der Zeiger kann weiterhin viele der Features eines C-Zeigers aufweisen. Sie kann z. B. zwischen **NULL-** und **Nicht-NULL-Werten** wechseln oder gleich bleiben. Dies wird anhand des folgenden Beispiels veranschaulicht. Der Zeiger **ist** null vor dem Aufruf und zeigt nach dem Aufruf auf eine gültige Zeichenfolge:

![Zeigerwechsel zwischen NULL- und Nicht-NULL-Werten](images/prog-a01.png)

Standardmäßig wendet der MIDL-Compiler das \[ [eindeutige](/windows/desktop/Midl/unique) \] Zeigerattribut auf alle Zeiger an, die keine Parameter sind. Diese Standardeinstellung kann mit dem \[ [ \_ Zeigerstandardattribut](/windows/desktop/Midl/pointer-default) geändert \] werden.

Ein eindeutiger Zeiger weist die folgenden Merkmale auf:

-   Sie kann den Wert **NULL** aufweisen.
-   Sie kann während des Aufrufs von **NULL** in **Nicht-NULL** geändert werden. Wenn sich der Wert in ungleich **NULL** ändert, wird bei der Rückgabe neuer Arbeitsspeicher zugeordnet.
-   Sie kann während des Aufrufs von ungleich **NULL** in **NULL** geändert werden. Wenn der Wert in **NULL** geändert wird, ist die Anwendung für das Freigeben des Arbeitsspeichers verantwortlich.
-   Der Wert kann von einem Wert ungleich **NULL** in einen anderen geändert werden.
-   Auf den Speicher, auf den ein eindeutiger Zeiger zeigt, kann von keinem anderen Zeiger oder Namen im Vorgang zugegriffen werden.
-   Rückgabedaten werden in den vorhandenen Speicher geschrieben, wenn der Zeiger nicht über den Wert **NULL verfügt.**

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

In diesem Beispiel ist der -Parameter *ein* eindeutiger Zeiger auf Zeichendaten, die an einen Server gesendet werden, der mit der RemoteFn-Routine verarbeitet werden soll.

 

 