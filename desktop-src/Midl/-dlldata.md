---
title: /dlldata-Schalter
description: Der Schalter/dlldata wird verwendet, um den Dateinamen für die generierte "dlldata-Datei für eine Proxy-dll anzugeben. Der Standard Dateiname "dlldata. c" wird verwendet, wenn der Schalter "/dlldata" nicht angegeben wird.
ms.assetid: 5211498b-c641-447f-9514-a98766e26ea9
keywords:
- /dlldata-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /dlldata
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e9c1d7f27c56f81905081fd9ef24c8c490391b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718690"
---
# <a name="dlldata-switch"></a><span data-ttu-id="baeef-105">/dlldata-Schalter</span><span class="sxs-lookup"><span data-stu-id="baeef-105">/dlldata switch</span></span>

<span data-ttu-id="baeef-106">Der Schalter **/dlldata** wird verwendet, um den Dateinamen für die generierte "dlldata-Datei für eine Proxy-dll anzugeben.</span><span class="sxs-lookup"><span data-stu-id="baeef-106">The **/dlldata** switch is used to specify the file name for the generated dlldata file for a proxy DLL.</span></span> <span data-ttu-id="baeef-107">Der Standard Dateiname "dlldata. c" wird verwendet, wenn der Schalter " **/dlldata** " nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="baeef-107">The default file name Dlldata.c is used if the **/dlldata** switch is not specified.</span></span>

``` syntax
midl /dlldata file-name
```

## <a name="switch-options"></a><span data-ttu-id="baeef-108">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="baeef-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="baeef-109">*Dateiname*</span><span class="sxs-lookup"><span data-stu-id="baeef-109">*file-name*</span></span> 
</dt> <dd>

<span data-ttu-id="baeef-110">Der Name der C-Quelldatei, die der mittlerer l-Compiler für die Proxy-dll generiert.</span><span class="sxs-lookup"><span data-stu-id="baeef-110">The name of the C source file the MIDL compiler will generate for the proxy DLL.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="baeef-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="baeef-111">Remarks</span></span>

<span data-ttu-id="baeef-112">Die durch *Dateiname* angegebene Datei muss mit der Proxy-DLL verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="baeef-112">The file specified by *file-name* must be linked to the proxy DLL.</span></span> <span data-ttu-id="baeef-113">Die "dlldata-Datei enthält Einstiegspunkte und Datenstrukturen, die von der Klassenfactory für die Proxy-dll benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="baeef-113">The dlldata file contains entry points and data structures required by the class factory for the proxy DLL.</span></span> <span data-ttu-id="baeef-114">Diese Datenstrukturen geben die Objekt Schnittstellen an, die in der Proxy-dll enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="baeef-114">These data structures specify the object interfaces contained in the proxy DLL.</span></span> <span data-ttu-id="baeef-115">In der "dlldata-Datei wird auch der Klassen Bezeichner der Klassenfactory für die Proxy-dll angegeben.</span><span class="sxs-lookup"><span data-stu-id="baeef-115">The dlldata file also specifies the class identifier of the class factory for the proxy DLL.</span></span> <span data-ttu-id="baeef-116">Dabei handelt es sich immer um die UUID (IID) der ersten Schnittstelle der ersten Proxy Datei (in alphabetischer Reihenfolge).</span><span class="sxs-lookup"><span data-stu-id="baeef-116">This is always the UUID (IID) of the first interface of the first proxy file (by alphabetical order).</span></span>

<span data-ttu-id="baeef-117">Die gleiche "dlldata-Datei sollte beim Aufrufen von" Mittel l "für alle IDL-Dateien angegeben werden, die in eine bestimmte Proxy-dll geleitet werden.</span><span class="sxs-lookup"><span data-stu-id="baeef-117">The same dlldata file should be specified when invoking MIDL on all the IDL files that will go into a particular proxy DLL.</span></span> <span data-ttu-id="baeef-118">Die "dlldata-Datei wird bei jeder mittleren Kompilierung erstellt oder aktualisiert, und es wird inkrementell eine Liste der Schnittstellen erstellt, die in die Proxy-dll aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="baeef-118">The dlldata file is created or updated during each MIDL compilation, incrementally building a list of the interfaces that will go into the proxy DLL.</span></span>

## <a name="examples"></a><span data-ttu-id="baeef-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="baeef-119">Examples</span></span>

<span data-ttu-id="baeef-120">**Mittel l/dlldata Data. c**</span><span class="sxs-lookup"><span data-stu-id="baeef-120">**midl /dlldata data.c**</span></span>

## <a name="see-also"></a><span data-ttu-id="baeef-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="baeef-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baeef-122">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="baeef-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




