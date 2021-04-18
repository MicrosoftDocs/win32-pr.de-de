---
title: /sstub-Schalter
description: Der/sstub-Schalter gibt den Namen der Server-Stub-Datei für eine RPC-Schnittstelle an.
ms.assetid: 8e695e81-7c1b-40c0-aeaa-5390512fa099
keywords:
- /sstub-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /sstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 131be3dd1890967f7107bea64c3dc2634833653d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106340668"
---
# <a name="sstub-switch"></a><span data-ttu-id="5ae5b-104">/sstub-Schalter</span><span class="sxs-lookup"><span data-stu-id="5ae5b-104">/sstub switch</span></span>

<span data-ttu-id="5ae5b-105">Der **/sstub** -Schalter gibt den Namen der Server-Stub-Datei für eine RPC-Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="5ae5b-105">The **/sstub** switch specifies the name of the server stub file for an RPC interface.</span></span>

``` syntax
midl /sstub stub_file_name
```

## <a name="switch-options"></a><span data-ttu-id="5ae5b-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="5ae5b-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="5ae5b-107">*Stub- \_ Dateiname \_*</span><span class="sxs-lookup"><span data-stu-id="5ae5b-107">*stub\_file\_name*</span></span> 
</dt> <dd>

<span data-ttu-id="5ae5b-108">Gibt einen Dateinamen an, der den Standard Dateinamen der Server-Stub-Datei überschreibt.</span><span class="sxs-lookup"><span data-stu-id="5ae5b-108">Specifies a file name that overrides the default server stub file name.</span></span> <span data-ttu-id="5ae5b-109">Dateinamen können mit doppelten Anführungszeichen (") explizit angegeben werden, um zu verhindern, dass die Shell die Sonderzeichen interpretiert.</span><span class="sxs-lookup"><span data-stu-id="5ae5b-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ae5b-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ae5b-110">Remarks</span></span>

<span data-ttu-id="5ae5b-111">Der angegebene Dateiname ersetzt den Standard Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="5ae5b-111">The specified file name replaces the default file name.</span></span> <span data-ttu-id="5ae5b-112">Standardmäßig wird der Dateiname abgerufen, indem \_ S. C dem Namen der IDL-Datei hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="5ae5b-112">By default, the file name is obtained by adding \_S.C to the name of the IDL file.</span></span> <span data-ttu-id="5ae5b-113">Dieser Schalter wirkt sich nicht auf OLE-Schnittstellen aus.</span><span class="sxs-lookup"><span data-stu-id="5ae5b-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="5ae5b-114">Wenn Sie Dateien importieren, gilt der angegebene Dateiname nur für eine Stubdatei – die Stubdatei, die der IDL-Datei entspricht, die in der Befehlszeile angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="5ae5b-114">When you are importing files, the specified file name applies to only one stub file — the stub file that corresponds to the IDL file specified on the command line.</span></span>

<span data-ttu-id="5ae5b-115">Wenn der *Stub- \_ Dateiname \_* keinen expliziten Pfad enthält, wird die Datei in das aktuelle Verzeichnis oder das durch den [**/out**](-out.md) -Schalter angegebene Verzeichnis geschrieben.</span><span class="sxs-lookup"><span data-stu-id="5ae5b-115">If *stub\_file\_name* does not include an explicit path, the file is written to the current directory or the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="5ae5b-116">Ein expliziter Pfad im *\_ stubdateinamen \_* überschreibt die **/out** -Switch-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="5ae5b-116">An explicit path in *stub\_file\_name* overrides the **/out** switch specification.</span></span>

<span data-ttu-id="5ae5b-117">Der Schalter **/Server** None hat Vorrang vor dem **/sstub** -Schalter.</span><span class="sxs-lookup"><span data-stu-id="5ae5b-117">The **/server** none switch takes precedence over the **/sstub** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="5ae5b-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ae5b-118">Examples</span></span>

<span data-ttu-id="5ae5b-119">**Mittel l/sstub My \_ sstub. c filename. idl**</span><span class="sxs-lookup"><span data-stu-id="5ae5b-119">**midl /sstub my\_sstub.c filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="5ae5b-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ae5b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ae5b-121">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="5ae5b-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="5ae5b-122">**/cstub**</span><span class="sxs-lookup"><span data-stu-id="5ae5b-122">**/cstub**</span></span>](-cstub.md)
</dt> <dt>

[<span data-ttu-id="5ae5b-123">**/Header**</span><span class="sxs-lookup"><span data-stu-id="5ae5b-123">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="5ae5b-124">**/Out**</span><span class="sxs-lookup"><span data-stu-id="5ae5b-124">**/out**</span></span>](-out.md)
</dt> </dl>

 

 




