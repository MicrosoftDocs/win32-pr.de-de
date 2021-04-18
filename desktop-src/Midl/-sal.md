---
title: /SAL-Schalter
description: Der/SAL-Schalter leitet die mittlere Anmerkung in den generierten Stub-Dateien mit der-Option.
ms.assetid: 452A19CA-6F72-416F-8059-77937412DA88
keywords:
- /SAL-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /sal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef52eb510c71bfdb153b95a5d05e992359e39b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106338229"
---
# <a name="sal-switch"></a><span data-ttu-id="8040a-104">/SAL-Schalter</span><span class="sxs-lookup"><span data-stu-id="8040a-104">/sal switch</span></span>

<span data-ttu-id="8040a-105">Der **/SAL** -Schalter leitet die mittlere Anmerkung in den generierten Stub-Dateien mit der-Option.</span><span class="sxs-lookup"><span data-stu-id="8040a-105">The **/sal** switch directs MIDL to generate SAL annotations in the generated stub files.</span></span>

``` syntax
midl /sal
```

## <a name="switch-options"></a><span data-ttu-id="8040a-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="8040a-106">Switch Options</span></span>

<span data-ttu-id="8040a-107">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="8040a-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="8040a-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8040a-108">Remarks</span></span>

<span data-ttu-id="8040a-109">In der mittleren l werden Zeiger-und Array Parameter mit Anmerkungen markiert, die die Parameter Beschreibung in der IDL-Datei entsprechend der von RPC und der NDR-Marshalling-Engine übergebenen Parameter Beschreibung widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="8040a-109">MIDL will mark pointer and array parameters with annotations that reflect the parameter description in the IDL file as enforced by RPC and the NDR marshaling engine.</span></span> <span data-ttu-id="8040a-110">In der mittleren l werden keine Anmerkungen für Parameter in Schnittstellen Methoden erstellt, die mit dem [**\[ lokalen \]**](local.md)Attribut markiert sind, es sei denn, [**/SAL \_ local**](-sal-local.md) ist auch in der Befehlszeile vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8040a-110">MIDL does not create annotations for parameters in interface methods marked with the [**\[local\]**](local.md)attribute unless [**/sal\_local**](-sal-local.md) is also present on the command line.</span></span> <span data-ttu-id="8040a-111">Verwenden Sie zum Überschreiben der in der Mitte generierten Anmerkung Das [**\[ kommentieren \]**](annotate.md) -Attribut.</span><span class="sxs-lookup"><span data-stu-id="8040a-111">To override the MIDL-generated annotation, use the [**\[annotate\]**](annotate.md) attribute.</span></span>

<span data-ttu-id="8040a-112">Bei in der Mitte generierten Anmerkungen wird immer \_ \_ RPC \_ vorangestellt, und die Verwendung des **rpcsal. h** -Headers erfordert die Übersetzung der Anmerkung in standardmäßige SAL-Anmerkungen.</span><span class="sxs-lookup"><span data-stu-id="8040a-112">MIDL-generated annotations are always prefixed with \_\_RPC\_, and require use of the **rpcsal.h** header to translate the annotation into standard SAL annotations.</span></span>

## <a name="see-also"></a><span data-ttu-id="8040a-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8040a-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8040a-114">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="8040a-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="8040a-115">**/SAL \_ lokal**</span><span class="sxs-lookup"><span data-stu-id="8040a-115">**/sal\_local**</span></span>](-sal-local.md)
</dt> <dt>

<span data-ttu-id="8040a-116">[**\[kommentieren\]**](annotate.md)</span><span class="sxs-lookup"><span data-stu-id="8040a-116">[**\[annotate\]**](annotate.md)</span></span>
</dt> </dl>

 

 




