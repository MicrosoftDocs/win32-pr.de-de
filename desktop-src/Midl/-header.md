---
title: /Header-Schalter
description: Der/Header-Schalter gibt den Namen der Header Datei an.
ms.assetid: d36cb6c9-df57-4ef4-aff3-9968ac8ac001
keywords:
- /Header-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /header
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816310f0b584f3c30d351e0d036e1f18c2f23962
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389257"
---
# <a name="header-switch"></a><span data-ttu-id="e12cf-104">/Header-Schalter</span><span class="sxs-lookup"><span data-stu-id="e12cf-104">/header switch</span></span>

<span data-ttu-id="e12cf-105">Der **/Header** -Schalter gibt den Namen der Header Datei an.</span><span class="sxs-lookup"><span data-stu-id="e12cf-105">The **/header** switch specifies the name of the header file.</span></span>

``` syntax
midl /header filename
```

## <a name="switch-options"></a><span data-ttu-id="e12cf-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="e12cf-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="e12cf-107">*filename*</span><span class="sxs-lookup"><span data-stu-id="e12cf-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="e12cf-108">Gibt einen Header Dateinamen an, der den Standard Header Dateinamen überschreibt.</span><span class="sxs-lookup"><span data-stu-id="e12cf-108">Specifies a header file name that overrides the default header file name.</span></span> <span data-ttu-id="e12cf-109">Dateinamen können mit doppelten Anführungszeichen (") explizit angegeben werden, um zu verhindern, dass die Shell Sonderzeichen interpretiert.</span><span class="sxs-lookup"><span data-stu-id="e12cf-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e12cf-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e12cf-110">Remarks</span></span>

<span data-ttu-id="e12cf-111">Der angegebene Dateiname ersetzt den Standard Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="e12cf-111">The specified file name replaces the default file name.</span></span> <span data-ttu-id="e12cf-112">Der Standard Dateiname wird durch Ersetzen der IDL-Dateinamenerweiterung (i. d. d. d. h. idl) durch die Dateinamenerweiterung. h abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e12cf-112">The default file name is obtained by replacing the IDL file name extension (usually .idl) with the file name extension .h.</span></span> <span data-ttu-id="e12cf-113">Bei OLE-Schnittstellen überschreibt der Schalter **/Header** den Standardnamen der Schnittstellen Header Datei.</span><span class="sxs-lookup"><span data-stu-id="e12cf-113">For OLE interfaces, the **/header** switch overrides the default name of the interface header file.</span></span>

<span data-ttu-id="e12cf-114">Wenn Sie Dateien importieren, gilt der angegebene Dateiname nur für eine Header Datei – die Header Datei, die der IDL-Datei entspricht, die in der Befehlszeile angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e12cf-114">When you are importing files, the specified file name applies to only one header file — the header file that corresponds to the IDL file specified on the command line.</span></span>

<span data-ttu-id="e12cf-115">Wenn *filename* keinen expliziten Pfad enthält, wird die Datei in das aktuelle Verzeichnis oder das durch den Schalter [**/out**](-out.md) angegebene Verzeichnis geschrieben.</span><span class="sxs-lookup"><span data-stu-id="e12cf-115">If *filename* does not include an explicit path, the file is written to the current directory or the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="e12cf-116">Ein expliziter Pfad in *filename* überschreibt die **/out** -Switch-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="e12cf-116">An explicit path in *filename* overrides the **/out** switch specification.</span></span>

## <a name="examples"></a><span data-ttu-id="e12cf-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e12cf-117">Examples</span></span>

<span data-ttu-id="e12cf-118">**Mittel l/Header "Bar. h" Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="e12cf-118">**midl /header "bar.h" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="e12cf-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e12cf-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e12cf-120">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="e12cf-120">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="e12cf-121">**/h**</span><span class="sxs-lookup"><span data-stu-id="e12cf-121">**/h**</span></span>](-h.md)
</dt> <dt>

[<span data-ttu-id="e12cf-122">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="e12cf-122">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="e12cf-123">**/Out**</span><span class="sxs-lookup"><span data-stu-id="e12cf-123">**/out**</span></span>](-out.md)
</dt> <dt>

[<span data-ttu-id="e12cf-124">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="e12cf-124">**/sstub**</span></span>](-sstub.md)
</dt> <dt>

[<span data-ttu-id="e12cf-125">**/Proxy**</span><span class="sxs-lookup"><span data-stu-id="e12cf-125">**/proxy**</span></span>](-proxy.md)
</dt> </dl>

 

 




