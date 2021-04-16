---
title: /notlb-Schalter
description: Der/notlb-Schalter verhindert, dass der Mittell-Compiler eine Typbibliotheks Datei (TLB-Datei) erzeugt.
ms.assetid: 58f4210d-d3c3-42ce-b311-4ddd85bc396a
keywords:
- /notlb-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /notlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81911b6afb00d61713f966ba9e1981b979e51008
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104471965"
---
# <a name="notlb-switch"></a><span data-ttu-id="aa351-104">/notlb-Schalter</span><span class="sxs-lookup"><span data-stu-id="aa351-104">/notlb switch</span></span>

<span data-ttu-id="aa351-105">Der **/notlb** -Schalter verhindert, dass der Mittell-Compiler eine Typbibliotheks Datei (TLB-Datei) erzeugt.</span><span class="sxs-lookup"><span data-stu-id="aa351-105">The **/notlb** switch prevents the MIDL compiler from generating a type library (TLB) file.</span></span>

``` syntax
midl /notlb
```

## <a name="switch-options"></a><span data-ttu-id="aa351-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="aa351-106">Switch Options</span></span>

<span data-ttu-id="aa351-107">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="aa351-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa351-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa351-108">Remarks</span></span>

<span data-ttu-id="aa351-109">Standardmäßig generiert der mittlerer l-Compiler eine TLB-Datei, wenn eine [**Library**](library.md) -Anweisung gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="aa351-109">By default, the MIDL compiler will generate a TLB file whenever it encounters a [**LIBRARY**](library.md) statement.</span></span> <span data-ttu-id="aa351-110">Dieser Schalter überschreibt das Standardverhalten.</span><span class="sxs-lookup"><span data-stu-id="aa351-110">This switch overrides the default behavior.</span></span>

<span data-ttu-id="aa351-111">Wenn die **/notlb** -Option angegeben wird, werden alle anderen Stub-, Header-usw. wie üblich generiert.</span><span class="sxs-lookup"><span data-stu-id="aa351-111">When the **/notlb** option is specified, all other stubs, headers, etc. are generated as usual.</span></span>

## <a name="see-also"></a><span data-ttu-id="aa351-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa351-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa351-113">**/TLB**</span><span class="sxs-lookup"><span data-stu-id="aa351-113">**/tlb**</span></span>](-tlb.md)
</dt> </dl>

 

 




