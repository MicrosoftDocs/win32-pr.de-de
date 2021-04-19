---
title: /out-Schalter
description: Der/out-Schalter gibt das Standardverzeichnis an, in dem der Mittell-Compiler Ausgabedateien schreibt.
ms.assetid: 37cfe989-137a-4336-8c66-e6b9c23473df
keywords:
- /out-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d688f17957170c6f3a8887030ea2c67140c0ff8c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106338032"
---
# <a name="out-switch"></a><span data-ttu-id="aa863-104">/out-Schalter</span><span class="sxs-lookup"><span data-stu-id="aa863-104">/out switch</span></span>

<span data-ttu-id="aa863-105">Der **/out** -Schalter gibt das Standardverzeichnis an, in dem der Mittell-Compiler Ausgabedateien schreibt.</span><span class="sxs-lookup"><span data-stu-id="aa863-105">The **/out** switch specifies the default directory where the MIDL compiler writes output files.</span></span>

``` syntax
midl /out path-specification
```

## <a name="switch-options"></a><span data-ttu-id="aa863-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="aa863-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="aa863-107">*Path-Spezifikation*</span><span class="sxs-lookup"><span data-stu-id="aa863-107">*path-specification*</span></span> 
</dt> <dd>

<span data-ttu-id="aa863-108">Gibt den Pfad zu dem Verzeichnis an, in dem die Stub-, Header-und switchdateien generiert werden.</span><span class="sxs-lookup"><span data-stu-id="aa863-108">Specifies the path to the directory in which the stub, header, and switch files are generated.</span></span> <span data-ttu-id="aa863-109">Es kann eine Laufwerk Spezifikation, ein absoluter Verzeichnispfad oder beides angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="aa863-109">A drive specification, an absolute directory path, or both can be specified.</span></span> <span data-ttu-id="aa863-110">Pfade können mit doppelten Anführungszeichen (") explizit in Anführungszeichen eingeschlossen werden, um zu verhindern, dass die Shell die Sonderzeichen interpretiert.</span><span class="sxs-lookup"><span data-stu-id="aa863-110">Paths can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa863-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa863-111">Remarks</span></span>

<span data-ttu-id="aa863-112">Das Ausgabeverzeichnis kann mit einem Laufwerk Buchstaben, einem absoluten Pfadnamen oder beidem angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="aa863-112">The output directory can be specified with a drive letter, an absolute path name, or both.</span></span> <span data-ttu-id="aa863-113">Die **/out** -Option kann mit allen Schaltern verwendet werden, die die Angabe einzelner Ausgabedateien ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="aa863-113">The **/out** option can be used with any of the switches that enable individual output file specification.</span></span>

<span data-ttu-id="aa863-114">Wenn der Schalter **/out** nicht angegeben wird, werden die Dateien in das aktuelle Verzeichnis geschrieben.</span><span class="sxs-lookup"><span data-stu-id="aa863-114">When the **/out** switch is not specified, files are written to the current directory.</span></span>

<span data-ttu-id="aa863-115">Das vom **/out** -Schalter angegebene Standardverzeichnis kann durch einen expliziten Pfadnamen überschrieben werden, der als Teil des [**/cstub**](-cstub.md)-, [**/Header**](-header.md)-, [**/Proxy**](-proxy.md)-oder [**/sstub**](-sstub.md) -Schalters angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="aa863-115">The default directory specified by the **/out** switch can be overridden by an explicit path name specified as part of the [**/cstub**](-cstub.md), [**/header**](-header.md), [**/proxy**](-proxy.md), or [**/sstub**](-sstub.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="aa863-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa863-116">Examples</span></span>

<span data-ttu-id="aa863-117">**Mittel l/Out c: \\ "MyDir" \\ meinsubdir \\ SubDir2 tiefere Dateinamen. idl**</span><span class="sxs-lookup"><span data-stu-id="aa863-117">**midl /out c:\\mydir\\mysubdir\\subdir2 deeper filename.idl**</span></span>

<span data-ttu-id="aa863-118">**Mittel l/Out c: Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="aa863-118">**midl /out c: filename.idl**</span></span>

<span data-ttu-id="aa863-119">**Mittel l/out \\ "MyDir" \\ mysubdir \\ ein anderer Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="aa863-119">**midl /out \\mydir\\mysubdir\\another filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="aa863-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa863-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa863-121">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="aa863-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="aa863-122">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="aa863-122">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="aa863-123">**/Header**</span><span class="sxs-lookup"><span data-stu-id="aa863-123">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="aa863-124">**/Proxy**</span><span class="sxs-lookup"><span data-stu-id="aa863-124">**/proxy**</span></span>](-proxy.md)
</dt> <dt>

[<span data-ttu-id="aa863-125">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="aa863-125">**/sstub**</span></span>](-sstub.md)
</dt> </dl>

 

 




