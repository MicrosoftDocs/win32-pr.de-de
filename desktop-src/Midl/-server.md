---
title: /Server-Schalter
description: Der/Server-Schalter leitet den Mittelwert Compiler zum Generieren serverseitiger C-Quelldateien für eine RPC-Schnittstelle.
ms.assetid: c5ca6a47-e8b0-4a13-ba73-2d35a9ac8240
keywords:
- /Server-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /server
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31449133fa795a90d1f11d8c06b960b74909548d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038006"
---
# <a name="server-switch"></a><span data-ttu-id="57a1d-104">/Server-Schalter</span><span class="sxs-lookup"><span data-stu-id="57a1d-104">/server switch</span></span>

<span data-ttu-id="57a1d-105">Der **/Server** -Schalter leitet den Mittelwert Compiler zum Generieren serverseitiger C-Quelldateien für eine RPC-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="57a1d-105">The **/server** switch directs the MIDL compiler to generate server-side C source files for an RPC interface.</span></span>

``` syntax
midl /server { stub | none }
```

## <a name="switch-options"></a><span data-ttu-id="57a1d-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="57a1d-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span data-ttu-id="57a1d-107"><span id="stub"></span><span id="STUB"></span>Stub \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="57a1d-107"><span id="stub"></span><span id="STUB"></span>\*\*\*\*stub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="57a1d-108">Generiert die serverseitigen Dateien.</span><span class="sxs-lookup"><span data-stu-id="57a1d-108">Generates the server-side files.</span></span>

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span data-ttu-id="57a1d-109"><span id="none"></span><span id="NONE"></span>keine \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="57a1d-109"><span id="none"></span><span id="NONE"></span>\*\*\*\*none\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="57a1d-110">Generiert keine serverseitigen Dateien.</span><span class="sxs-lookup"><span data-stu-id="57a1d-110">Does not generate server-side files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57a1d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57a1d-111">Remarks</span></span>

<span data-ttu-id="57a1d-112">Wenn der **/Server** -Schalter nicht angegeben wird, generiert der kompil-Compiler die Server-Stub-Datei.</span><span class="sxs-lookup"><span data-stu-id="57a1d-112">When the **/server** switch is not specified, the MIDL compiler generates the server stub file.</span></span> <span data-ttu-id="57a1d-113">Dieser Schalter wirkt sich nicht auf OLE-Schnittstellen aus.</span><span class="sxs-lookup"><span data-stu-id="57a1d-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="57a1d-114">Die Option **None** bewirkt, dass keine Dateien generiert werden.</span><span class="sxs-lookup"><span data-stu-id="57a1d-114">The **none** option causes no files to be generated.</span></span>

<span data-ttu-id="57a1d-115">Der **/Server** -Schalter hat Vorrang vor dem **/sstub** -Schalter.</span><span class="sxs-lookup"><span data-stu-id="57a1d-115">The **/server** switch takes precedence over the **/sstub** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="57a1d-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57a1d-116">Examples</span></span>

<span data-ttu-id="57a1d-117">**Mittel l/Server keine**</span><span class="sxs-lookup"><span data-stu-id="57a1d-117">**midl /server none**</span></span>

<span data-ttu-id="57a1d-118">**Mittel l/Server Stub**</span><span class="sxs-lookup"><span data-stu-id="57a1d-118">**midl /server stub**</span></span>

## <a name="see-also"></a><span data-ttu-id="57a1d-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57a1d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57a1d-120">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="57a1d-120">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="57a1d-121">**/Client**</span><span class="sxs-lookup"><span data-stu-id="57a1d-121">**/client**</span></span>](-client.md)
</dt> <dt>

[<span data-ttu-id="57a1d-122">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="57a1d-122">**/sstub**</span></span>](-sstub.md)
</dt> </dl>

 

 




