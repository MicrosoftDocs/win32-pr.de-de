---
title: Anwendungs Konfigurationsdatei (ACF)
description: Es gibt möglicherweise Aspekte ihrer verteilten Anwendung, die sich auf eine Komponente auswirken, aber nichts mit einem anderen tun müssen.
ms.assetid: 017d93fd-1701-4713-a786-752a7695b5a6
keywords:
- ACF-Mittell
- Microsoft Interface Definition Language mittlere, beschriebene Anwendungs Konfigurationsdatei
- Anwendungs Konfigurationsdatei-Mittel l
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9066e5641d6b71e68ba670984765661f1b9f6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341876"
---
# <a name="application-configuration-file-acf"></a><span data-ttu-id="03fef-106">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="03fef-106">Application Configuration File (ACF)</span></span>

<span data-ttu-id="03fef-107">Es gibt möglicherweise Aspekte ihrer verteilten Anwendung, die sich auf eine Komponente auswirken, aber nichts mit einem anderen tun müssen.</span><span class="sxs-lookup"><span data-stu-id="03fef-107">There may be aspects of your distributed application that affect one component, but have nothing to do with another.</span></span> <span data-ttu-id="03fef-108">Ein-Objekt kann z. b. eine große, komplexe Datenstruktur enthalten und den Inhalt dieser Datenstruktur an ein anderes-Objekt übergeben.</span><span class="sxs-lookup"><span data-stu-id="03fef-108">For example, an object may contain a large, complex data structure and pass the contents of this data structure to another object.</span></span> <span data-ttu-id="03fef-109">Das genaue Layout dieser Datenstruktur ist für die empfangende Anwendung möglicherweise bedeutungslos.</span><span class="sxs-lookup"><span data-stu-id="03fef-109">The exact layout of this data structure may be meaningless to the receiving application.</span></span> <span data-ttu-id="03fef-110">Die Struktur kann auch Datentypen enthalten, die vom-compilercompiler nicht erkannt werden, und es kann kein Marshalling und kein Marshalling von Code generiert werden.</span><span class="sxs-lookup"><span data-stu-id="03fef-110">Also, the structure may contain data types that the MIDL compiler does not recognize and cannot generate marshaling and unmarshaling code.</span></span>

<span data-ttu-id="03fef-111">Client Anwendungen können die gleiche Schnittstelle verwenden, aber auf unterschiedlichen Plattformen ausgeführt werden. Sie benötigen möglicherweise jeweils einen eigenen Satz von Marshallingroutinen.</span><span class="sxs-lookup"><span data-stu-id="03fef-111">Client applications may share the same interface but run on different platforms; they may each need their own set of marshaling routines.</span></span> <span data-ttu-id="03fef-112">Schließlich benötigen einzelne Clients möglicherweise nicht immer denselben Funktions Satz.</span><span class="sxs-lookup"><span data-stu-id="03fef-112">Finally, individual clients may not always need the same set of functions.</span></span> <span data-ttu-id="03fef-113">Es ist ineffizient, Stub-Code für Funktionen zu generieren, die nie in einer bestimmten Client Anwendung implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="03fef-113">It is inefficient to generate stub code for functions that will never be implemented in a particular client application.</span></span>

<span data-ttu-id="03fef-114">Wenn Sie diese lokalen Aspekte Ihrer Schnittstelle in einer Anwendungs Konfigurationsdatei (ACF) definieren, können Sie die Unterschiede zwischen den Client Schnittstellen von ihrer Netzwerkdarstellung trennen, sodass der Serverdaten in einem konsistenten Format senden und empfangen und den Stub-Code kompakter und effizienter gestalten kann.</span><span class="sxs-lookup"><span data-stu-id="03fef-114">By defining these local aspects of your interface in an application configuration file (ACF), you can separate the differences between the client interfaces from their network representation, allowing the server to send and receive data in a consistent format, and making your stub code more compact and efficient.</span></span>

<span data-ttu-id="03fef-115">Die Struktur und die Syntax einer ACF-Schnittstellen Definition sind identisch mit der IDL-Definition:</span><span class="sxs-lookup"><span data-stu-id="03fef-115">The structure and syntax of an ACF interface definition are identical to the IDL definition:</span></span>

``` syntax
[ interface-attribute-list] interface interface-name {. . .}
```

<span data-ttu-id="03fef-116">Standardmäßig muss der Name der ACF-Schnittstelle mit dem Namen in der IDL-Definition identisch sein.</span><span class="sxs-lookup"><span data-stu-id="03fef-116">By default, the ACF interface name must match its name in the IDL definition.</span></span> <span data-ttu-id="03fef-117">Wenn Sie jedoch mit der kompil-Compileroption/ [**ACF**](-acf.md) einen ACF-Dateinamen explizit angeben, müssen die Schnittstellennamen nicht identisch sein.</span><span class="sxs-lookup"><span data-stu-id="03fef-117">However, when you use the MIDL compiler option / [**acf**](-acf.md) to explicitly specify an ACF file name, the interface names do not have to match.</span></span> <span data-ttu-id="03fef-118">Diese Funktion ermöglicht es, dass mehrere Schnittstellen eine einzelne ACF-Spezifikation gemeinsam verwenden.</span><span class="sxs-lookup"><span data-stu-id="03fef-118">This feature allows several interfaces to share a single ACF specification.</span></span>

 

 




