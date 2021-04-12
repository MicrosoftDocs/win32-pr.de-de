---
title: /cstub-Schalter
description: Der/cstub-Schalter gibt den Namen der Client-Stub-Datei für eine RPC-Schnittstelle an.
ms.assetid: f2c9e083-3511-4e72-b1d1-14a3a662ffaf
keywords:
- /cstub-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /cstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 878f6eee47deaac3887c3f9936c18b0185cc807a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312959"
---
# <a name="cstub-switch"></a><span data-ttu-id="01a2c-104">/cstub-Schalter</span><span class="sxs-lookup"><span data-stu-id="01a2c-104">/cstub switch</span></span>

<span data-ttu-id="01a2c-105">Der **/cstub** -Schalter gibt den Namen der Client-Stub-Datei für eine RPC-Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="01a2c-105">The **/cstub** switch specifies the name of the client stub file for an RPC interface.</span></span>

``` syntax
midl /cstub stub_file_name
```

## <a name="switch-options"></a><span data-ttu-id="01a2c-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="01a2c-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="01a2c-107">*Stub- \_ Dateiname \_*</span><span class="sxs-lookup"><span data-stu-id="01a2c-107">*stub\_file\_name*</span></span> 
</dt> <dd>

<span data-ttu-id="01a2c-108">Gibt einen Dateinamen an, der den standardmäßigen Client-Stub-Dateinamen überschreibt.</span><span class="sxs-lookup"><span data-stu-id="01a2c-108">Specifies a file name that overrides the default client stub file name.</span></span> <span data-ttu-id="01a2c-109">Dateinamen können mit doppelten Anführungszeichen (") explizit angegeben werden, um zu verhindern, dass die Shell die Sonderzeichen interpretiert.</span><span class="sxs-lookup"><span data-stu-id="01a2c-109">File names can be explicitly quoted using double quotes (") to prevent the shell from interpreting the special characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01a2c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01a2c-110">Remarks</span></span>

<span data-ttu-id="01a2c-111">Der angegebene Dateiname ersetzt den Standard Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="01a2c-111">The specified file name replaces the default file name.</span></span> <span data-ttu-id="01a2c-112">Standardmäßig wird der Dateiname durch Hinzufügen der Erweiterung \_ c. c zum Namen der IDL-Datei abgerufen.</span><span class="sxs-lookup"><span data-stu-id="01a2c-112">By default, the file name is obtained by adding the extension \_c.c to the name of the IDL file.</span></span> <span data-ttu-id="01a2c-113">Dieser Schalter wirkt sich nicht auf OLE-Schnittstellen aus.</span><span class="sxs-lookup"><span data-stu-id="01a2c-113">This switch does not affect OLE interfaces.</span></span>

<span data-ttu-id="01a2c-114">Wenn Sie Dateien importieren, gilt der angegebene Dateiname nur für eine Stubdatei – die Stubdatei, die der IDL-Datei entspricht, die in der Befehlszeile angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="01a2c-114">When you are importing files, the specified file name applies to only one stub file — the stub file that corresponds to the IDL file specified on the command line.</span></span>

<span data-ttu-id="01a2c-115">Wenn der *Stub- \_ Dateiname \_* keinen expliziten Pfad enthält, wird die Datei in das aktuelle Verzeichnis oder das durch den [**/out**](-out.md) -Schalter angegebene Verzeichnis geschrieben.</span><span class="sxs-lookup"><span data-stu-id="01a2c-115">If *stub\_file\_name* does not include an explicit path, the file is written to the current directory or the directory specified by the [**/out**](-out.md) switch.</span></span> <span data-ttu-id="01a2c-116">Ein expliziter Pfad im *\_ stubdateinamen \_* überschreibt die **/out** -Switch-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="01a2c-116">An explicit path in *stub\_file\_name* overrides the **/out** switch specification.</span></span>

<span data-ttu-id="01a2c-117">Der Schalter **/Client** None hat Vorrang vor dem **/cstub** -Schalter.</span><span class="sxs-lookup"><span data-stu-id="01a2c-117">The **/client** none switch takes precedence over the **/cstub** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="01a2c-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="01a2c-118">Examples</span></span>

<span data-ttu-id="01a2c-119">**Mittel l/cstub My \_ cstub. c filename. idl**</span><span class="sxs-lookup"><span data-stu-id="01a2c-119">**midl /cstub my\_cstub.c filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="01a2c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01a2c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01a2c-121">**/Header**</span><span class="sxs-lookup"><span data-stu-id="01a2c-121">**/header**</span></span>](-header.md)
</dt> <dt>

[<span data-ttu-id="01a2c-122">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="01a2c-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="01a2c-123">**/Out**</span><span class="sxs-lookup"><span data-stu-id="01a2c-123">**/out**</span></span>](-out.md)
</dt> <dt>

[<span data-ttu-id="01a2c-124">**/sstub**</span><span class="sxs-lookup"><span data-stu-id="01a2c-124">**/sstub**</span></span>](-sstub.md)
</dt> </dl>

 

 




