---
title: /h-Schalter
description: Die/h-Option ist funktionell gleichwertig mit der/Header-Option.
ms.assetid: 1b74d5f2-6624-4b71-832d-fb55a0e84c86
keywords:
- /h-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /h
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ff2cd7aa5e4b8386e0c9faecfaccd860207403
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038085"
---
# <a name="h-switch"></a><span data-ttu-id="bc1af-104">/h-Schalter</span><span class="sxs-lookup"><span data-stu-id="bc1af-104">/h switch</span></span>

<span data-ttu-id="bc1af-105">Die **/h** -Option ist funktionell gleichwertig mit der [**/Header**](-header.md) -Option.</span><span class="sxs-lookup"><span data-stu-id="bc1af-105">The **/h** option is functionally equivalent to the [**/header**](-header.md) option.</span></span>

``` syntax
midl /h filename
```

## <a name="switch-options"></a><span data-ttu-id="bc1af-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="bc1af-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="bc1af-107">*filename*</span><span class="sxs-lookup"><span data-stu-id="bc1af-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="bc1af-108">Gibt einen Header Dateinamen an, der den Standard Header Dateinamen überschreibt.</span><span class="sxs-lookup"><span data-stu-id="bc1af-108">Specifies a header file name that overrides the default header file name.</span></span> <span data-ttu-id="bc1af-109">Dateinamen können mit doppelten Anführungszeichen (") explizit angegeben werden, um zu verhindern, dass die Shell Sonderzeichen interpretiert.</span><span class="sxs-lookup"><span data-stu-id="bc1af-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc1af-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc1af-110">Remarks</span></span>

<span data-ttu-id="bc1af-111">Der Schalter **/h** gibt *filename* als Namen für eine Header Datei an, die alle Definitionen enthält, die in der IDL-Datei enthalten sind, ohne die IDL-Syntax.</span><span class="sxs-lookup"><span data-stu-id="bc1af-111">The **/h** switch specifies *filename* as the name for a header file that contains all the definitions contained in the IDL file, without the IDL syntax.</span></span> <span data-ttu-id="bc1af-112">Diese Datei kann als C-oder C++-Header Datei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bc1af-112">This file can be used as a C or C++ header file.</span></span>

## <a name="examples"></a><span data-ttu-id="bc1af-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc1af-113">Examples</span></span>

<span data-ttu-id="bc1af-114">**Mittel l/h tlibhead. h Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="bc1af-114">**midl /h tlibhead.h filename.idl**</span></span>

<span data-ttu-id="bc1af-115">**Mittel l/h "mittlerer l. h" Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="bc1af-115">**midl /h "midl.h" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="bc1af-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc1af-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc1af-117">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="bc1af-117">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="bc1af-118">**/Header**</span><span class="sxs-lookup"><span data-stu-id="bc1af-118">**/header**</span></span>](-header.md)
</dt> </dl>

 

 




