---
title: Datentypen im Schnittstellen Text
description: Der Schnittstellen Text, der in geschweiften Klammern () eingeschlossen ist, enthält die Datentypen, die in Remote Prozedur aufrufen und Prototypen für die Funktionen verwendet werden, die Remote ausgeführt werden.
ms.assetid: a5130744-6b14-48a4-b439-16f0ecaf08c2
keywords:
- Schnittstellen-Mittell, Datentypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5bdbbb90c4cbecd4a6a4e3cc74ba9775772dd0a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339196"
---
# <a name="data-types-in-the-interface-body"></a><span data-ttu-id="6cca0-104">Datentypen im Schnittstellen Text</span><span class="sxs-lookup"><span data-stu-id="6cca0-104">Data Types in the Interface Body</span></span>

<span data-ttu-id="6cca0-105">Der Schnittstellen Text, der in geschweiften Klammern ({}) eingeschlossen ist, enthält die Datentypen, die in Remote Prozedur aufrufen und Prototypen für die Funktionen verwendet werden, die Remote ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6cca0-105">The interface body, which is enclosed in braces ({ }), contains the data types that will be used in remote procedure calls and prototypes for the functions that will be executed remotely.</span></span> <span data-ttu-id="6cca0-106">Ein Schnittstellen Text kann Importe, Pragmas, Konstante Deklarationen, Typdeklarationen und Funktions Deklarationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="6cca0-106">An interface body can contain imports, pragmas, constant declarations, type declarations, and function declarations.</span></span> <span data-ttu-id="6cca0-107">Mit Ausnahme des OSF-Kompatibilitätsmodus lässt der Mittelwert Compiler auch implizite Deklarationen in Form von Variablen Definitionen zu.</span><span class="sxs-lookup"><span data-stu-id="6cca0-107">Except in OSF-compatibility mode, the MIDL compiler also allows implicit declarations in the form of variable definitions.</span></span>

<span data-ttu-id="6cca0-108">Beachten Sie, dass die OSF-DCE-Spezifikation für RPC-Schnittstellen nicht mehrere Schnittstellen in einer einzelnen IDL-Datei zulässt.</span><span class="sxs-lookup"><span data-stu-id="6cca0-108">Note that the OSF-DCE specification for RPC interfaces does not allow multiple interfaces in a single IDL file.</span></span> <span data-ttu-id="6cca0-109">Wenn Sie also im OSF-Kompatibilitätsmodus ( [**/OSF**](-osf.md)) von mittlerer l kompilieren, kann die IDL-Datei nur eine Schnittstelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="6cca0-109">Therefore, if you are compiling in MIDL's OSF-compatibility mode ( [**/osf**](-osf.md)), your IDL file can contain only one interface.</span></span>

<span data-ttu-id="6cca0-110">Ausführliche Informationen zur Verwendung des-Mittell-Compilers zum Erstellen von Typbibliotheken finden Sie unter Erstellen [einer Typbibliothek mit mittlerer l](generating-a-type-library-with-midl-2.md).</span><span class="sxs-lookup"><span data-stu-id="6cca0-110">For details on using the MIDL compiler to produce type libraries, see [Generating a Type Library with MIDL](generating-a-type-library-with-midl-2.md).</span></span>

<span data-ttu-id="6cca0-111">In Microsoft RPC kann eine IDL-Datei mehrere Schnittstellen enthalten, und diese Schnittstellen können vorwärts (innerhalb der IDL-Datei, die Sie definiert) als deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="6cca0-111">In Microsoft RPC, an IDL file can contain multiple interfaces and these interfaces can be forward declared (within the IDL file that defines them).</span></span> <span data-ttu-id="6cca0-112">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="6cca0-112">For example:</span></span>

``` syntax
interface ITwo; //forward declaration
interface IOne 
{
...uses ITwo...
}
interface ITwo 
{
...uses IOne...
}
```

 

 




