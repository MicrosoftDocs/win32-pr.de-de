---
title: Die IDL-Datei
description: Die IDL-Datei besteht aus einer oder mehreren Schnittstellendefinitionen, die jeweils über einen Header und einen Text verfügen.
ms.assetid: 64a30a12-a53e-4c53-b8cf-7af85ffd0a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862adfad2a43f10dac3598279554fd6e1f00a302
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473293"
---
# <a name="the-idl-file"></a><span data-ttu-id="5e441-103">Die IDL-Datei</span><span class="sxs-lookup"><span data-stu-id="5e441-103">The IDL File</span></span>

<span data-ttu-id="5e441-104">Die IDL-Datei besteht aus einer oder mehreren Schnittstellendefinitionen, die jeweils über einen Header und einen Text verfügen.</span><span class="sxs-lookup"><span data-stu-id="5e441-104">The IDL file consists of one or more interface definitions, each of which has a header and a body.</span></span> <span data-ttu-id="5e441-105">Der-Header enthält Informationen, die für die gesamte Schnittstelle gelten, z. b. die UUID.</span><span class="sxs-lookup"><span data-stu-id="5e441-105">The header contains information that applies to the entire interface, such as the UUID.</span></span> <span data-ttu-id="5e441-106">Diese Informationen werden in eckige Klammern eingeschlossen, gefolgt von der-Schlüsselwort **Schnittstelle** und dem Schnittstellennamen.</span><span class="sxs-lookup"><span data-stu-id="5e441-106">This information is enclosed in square brackets and is followed by the keyword **interface** and the interface name.</span></span> <span data-ttu-id="5e441-107">Der Text enthält Datentyp Definitionen im C-Stil und Funktionsprototypen, ergänzt mit Attributen, die beschreiben, wie die Daten über das Netzwerk übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="5e441-107">The body contains C-style data type definitions and function prototypes, augmented with attributes that describe how the data is transmitted over the network.</span></span>

<span data-ttu-id="5e441-108">In diesem Beispiel enthält der Schnittstellen Header nur die UUID und die Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="5e441-108">In this example, the interface header contains only the UUID and the version number.</span></span> <span data-ttu-id="5e441-109">Durch die Versionsnummer wird sichergestellt, dass bei mehreren Versionen einer RPC-Schnittstelle nur kompatible Versionen des Clients und des Servers verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="5e441-109">The version number ensures that when there are multiple versions of an RPC interface, only compatible versions of the client and server will be connected.</span></span>

<span data-ttu-id="5e441-110">Der Schnittstellen Text enthält den Funktionsprototyp für **helloproc**.</span><span class="sxs-lookup"><span data-stu-id="5e441-110">The interface body contains the function prototype for **HelloProc**.</span></span> <span data-ttu-id="5e441-111">In diesem Prototyp weist der Funktionsparameter pszstring die Attribute **\[** [**in**](/windows/desktop/Midl/in) **\]** und der **\[** [**Zeichenfolge**](/windows/desktop/Midl/string)auf **\]** .</span><span class="sxs-lookup"><span data-stu-id="5e441-111">In this prototype, the function parameter pszString has the attributes **\[**[**in**](/windows/desktop/Midl/in)**\]** and **\[**[**string**](/windows/desktop/Midl/string)**\]**.</span></span> <span data-ttu-id="5e441-112">Das **\[ in \]** -Attribut teilt der Lauf Zeit Bibliothek mit, dass der-Parameter nur vom Client an den Server übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5e441-112">The **\[in\]** attribute tells the run-time library that the parameter is passed only from the client to the server.</span></span> <span data-ttu-id="5e441-113">Das **\[ String \]** -Attribut gibt an, dass der Stub den-Parameter als Zeichenfolge im C-Format behandeln soll.</span><span class="sxs-lookup"><span data-stu-id="5e441-113">The **\[string\]** attribute specifies that the stub should treat the parameter as a C-style character string.</span></span>

<span data-ttu-id="5e441-114">Die Client Anwendung sollte die Serveranwendung Herunterfahren können, sodass die-Schnittstelle einen Prototyp für eine andere Remote Funktion,**herunter** fahren, enthält, die später in diesem Tutorial implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="5e441-114">The client application should be able to shut down the server application, so the interface contains a prototype for another remote function,**Shutdown** , that will be implemented later in this tutorial.</span></span>

``` syntax
//file hello.idl
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface hello
{
    void HelloProc([in, string] unsigned char * pszString);
    void Shutdown(void);
}
```

 

 