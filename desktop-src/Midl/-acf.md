---
title: /ACF-Schalter
description: Mit dem Schalter/ACF kann der Benutzer einen expliziten ACF-Dateinamen angeben. Der Switch ermöglicht außerdem die Verwendung verschiedener Schnittstellennamen in den IDL-und ACF-Dateien.
ms.assetid: 8f0833ec-1dbc-4c8a-af7e-3de42169af8d
keywords:
- /ACF-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /acf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e24d66982628fbd0052e8a3f573901c430e8b8b1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103948241"
---
# <a name="acf-switch"></a><span data-ttu-id="0e63a-105">/ACF-Schalter</span><span class="sxs-lookup"><span data-stu-id="0e63a-105">/acf switch</span></span>

<span data-ttu-id="0e63a-106">Mit dem Schalter **/ACF** kann der Benutzer einen expliziten ACF-Dateinamen angeben.</span><span class="sxs-lookup"><span data-stu-id="0e63a-106">The **/acf** switch allows the user to supply an explicit ACF file name.</span></span> <span data-ttu-id="0e63a-107">Der Switch ermöglicht außerdem die Verwendung verschiedener Schnittstellennamen in den IDL-und ACF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="0e63a-107">The switch also allows the use of different interface names in the IDL and ACF files.</span></span>

``` syntax
midl /acf acf_filename
```

## <a name="switch-options"></a><span data-ttu-id="0e63a-108">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="0e63a-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="0e63a-109">*ACF \_ Dateiname*</span><span class="sxs-lookup"><span data-stu-id="0e63a-109">*acf\_filename*</span></span> 
</dt> <dd>

<span data-ttu-id="0e63a-110">Gibt den Namen der ACF an.</span><span class="sxs-lookup"><span data-stu-id="0e63a-110">Specifies the name of the ACF.</span></span> <span data-ttu-id="0e63a-111">Zwischen dem **/ACF** -Switch und dem Dateinamen kann ein Leerzeichen stehen oder nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="0e63a-111">White space may or may not be present between the **/acf** switch and the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e63a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e63a-112">Remarks</span></span>

<span data-ttu-id="0e63a-113">Standardmäßig erstellt der-compilercompiler den Namen der ACF, indem er die IDL-Dateinamenerweiterung (i. d. d. idl) durch. ACF ersetzt.</span><span class="sxs-lookup"><span data-stu-id="0e63a-113">By default, the MIDL compiler constructs the name of the ACF by replacing the IDL file name extension (usually .idl) with .acf.</span></span> <span data-ttu-id="0e63a-114">Wenn der **/ACF** -Schalter vorhanden ist, nimmt die ACF den Namen des angegebenen Datei namens an.</span><span class="sxs-lookup"><span data-stu-id="0e63a-114">When the **/acf** switch is present, the ACF takes its name from the specified file name.</span></span> <span data-ttu-id="0e63a-115">Der **/ACF** -Schalter gilt nur für die IDL-Datei, die in der Befehlszeile des compl-Compilers angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0e63a-115">The **/acf** switch applies only to the IDL file specified on the MIDL compiler command line.</span></span> <span data-ttu-id="0e63a-116">Es gilt nicht für importierte Dateien.</span><span class="sxs-lookup"><span data-stu-id="0e63a-116">It does not apply to imported files.</span></span>

<span data-ttu-id="0e63a-117">Wenn der **/ACF** -Schalter verwendet wird, muss der Schnittstellen Name in der ACF nicht mit dem Namen der Mittell-Schnittstelle identisch sein.</span><span class="sxs-lookup"><span data-stu-id="0e63a-117">When the **/acf** switch is used, the interface name in the ACF need not match the MIDL interface name.</span></span> <span data-ttu-id="0e63a-118">Diese Funktion ermöglicht es Schnittstellen, eine ACF-Spezifikation gemeinsam zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="0e63a-118">This feature allows interfaces to share an ACF specification.</span></span>

<span data-ttu-id="0e63a-119">Wenn kein absoluter Pfad zu einer ACF angegeben ist, sucht der Mittelwert Compiler im aktuellen Verzeichnis, den Verzeichnissen, die von der [**/I**](-i.md) -Option bereitgestellt werden, und den Verzeichnissen im Include-Pfad.</span><span class="sxs-lookup"><span data-stu-id="0e63a-119">When an absolute path to an ACF is not specified, the MIDL compiler searches in the current directory, directories supplied by the [**/I**](-i.md) option, and directories in the INCLUDE path.</span></span>

<span data-ttu-id="0e63a-120">Wenn die ACF nicht gefunden wird, geht der Mittelwert Compiler davon aus, dass für diese Schnittstelle keine ACF vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0e63a-120">If the ACF is not found, the MIDL compiler assumes there is no ACF for this interface.</span></span> <span data-ttu-id="0e63a-121">Weitere Informationen zur Reihenfolge der Verzeichnisse finden Sie in den Verweis Einträgen für die Schalter [**/I**](-i.md) und [**/No \_ DEF \_ Idir**](-no-def-idir.md) .</span><span class="sxs-lookup"><span data-stu-id="0e63a-121">For more information about the sequence of directories, see the reference entries for the [**/I**](-i.md) and [**/no\_def\_idir**](-no-def-idir.md) switches.</span></span> <span data-ttu-id="0e63a-122">Weitere Informationen zu **/ACF** finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="0e63a-122">For more information relating to **/acf**, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0e63a-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e63a-123">Examples</span></span>

<span data-ttu-id="0e63a-124">**Mittel l/ACF Bar. ACF Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="0e63a-124">**midl /acf bar.acf filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="0e63a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e63a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e63a-126">**/I**</span><span class="sxs-lookup"><span data-stu-id="0e63a-126">**/I**</span></span>](-i.md)
</dt> <dt>

[<span data-ttu-id="0e63a-127">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="0e63a-127">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="0e63a-128">**/No \_ DEF \_ Idir**</span><span class="sxs-lookup"><span data-stu-id="0e63a-128">**/no\_def\_idir**</span></span>](-no-def-idir.md)
</dt> </dl>

 

 




