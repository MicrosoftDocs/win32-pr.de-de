---
title: /Client-Schalter
description: Der/Client-Schalter weist den Mittelwert Compiler an, Client seitige C-Quelldateien für eine RPC-Schnittstelle zu generieren.
ms.assetid: bce5af72-2201-4b42-9348-cb97f08b7fdf
keywords:
- /Client-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /client
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf7e17e1893b918d926cd94a93eb8b1c372ee75
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312960"
---
# <a name="client-switch"></a><span data-ttu-id="33e1f-104">/Client-Schalter</span><span class="sxs-lookup"><span data-stu-id="33e1f-104">/client switch</span></span>

<span data-ttu-id="33e1f-105">Der **/Client** -Schalter weist den Mittelwert Compiler an, Client seitige C-Quelldateien für eine RPC-Schnittstelle zu generieren.</span><span class="sxs-lookup"><span data-stu-id="33e1f-105">The **/client** switch directs the MIDL compiler to generate client-side C source files for an RPC interface.</span></span>

``` syntax
midl /client { stub | none }
```

## <a name="switch-options"></a><span data-ttu-id="33e1f-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="33e1f-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span data-ttu-id="33e1f-107"><span id="stub"></span><span id="STUB"></span>Stub \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="33e1f-107"><span id="stub"></span><span id="STUB"></span>\*\*\*\*stub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="33e1f-108">Generiert die Client seitigen Dateien.</span><span class="sxs-lookup"><span data-stu-id="33e1f-108">Generates the client-side files.</span></span>

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span data-ttu-id="33e1f-109"><span id="none"></span><span id="NONE"></span>keine \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="33e1f-109"><span id="none"></span><span id="NONE"></span>\*\*\*\*none\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="33e1f-110">Generiert keine Client seitigen Dateien.</span><span class="sxs-lookup"><span data-stu-id="33e1f-110">Does not generate any client-side files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33e1f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33e1f-111">Remarks</span></span>

<span data-ttu-id="33e1f-112">Wenn der **/Client** -Schalter nicht angegeben wird, generiert der kompilierungscompiler die clientstubdatei.</span><span class="sxs-lookup"><span data-stu-id="33e1f-112">When the **/client** switch is not specified, the MIDL compiler generates the client stub file.</span></span> <span data-ttu-id="33e1f-113">Dieser Schalter wirkt sich nicht auf OLE-Schnittstellen aus.</span><span class="sxs-lookup"><span data-stu-id="33e1f-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="33e1f-114">Der **/Client** -Schalter hat Vorrang vor dem [**/cstub**](-cstub.md) -Schalter.</span><span class="sxs-lookup"><span data-stu-id="33e1f-114">The **/client** switch takes precedence over the [**/cstub**](-cstub.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="33e1f-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="33e1f-115">Examples</span></span>

<span data-ttu-id="33e1f-116">**Mittel l/Client keine Datei Name. idl**</span><span class="sxs-lookup"><span data-stu-id="33e1f-116">**midl /client none filename.idl**</span></span>

<span data-ttu-id="33e1f-117">**Mittel l/Client Stub-Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="33e1f-117">**midl /client stub filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="33e1f-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33e1f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33e1f-119">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="33e1f-119">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="33e1f-120">**/Server**</span><span class="sxs-lookup"><span data-stu-id="33e1f-120">**/server**</span></span>](-server.md)
</dt> <dt>

[<span data-ttu-id="33e1f-121">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="33e1f-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




