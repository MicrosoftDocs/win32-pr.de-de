---
title: /Cpp_opt Schalter
description: Der \_ Schalter/cpp opt gibt Optionen an, die an den C/C++-Präprozessor übergeben werden.
ms.assetid: f0059caa-aff3-4e96-95f8-a0014d6a6556
keywords:
- /Cpp_opt-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /cpp_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00e352a89ddadfc0a92e33e964afb5f0d9e9df6e
ms.sourcegitcommit: 97d62bfd3213d9c4ce46c3cd2b1177caf720681a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "104391285"
---
# <a name="cpp_opt-switch"></a><span data-ttu-id="1a60f-104">/cpp \_ opt-Schalter</span><span class="sxs-lookup"><span data-stu-id="1a60f-104">/cpp\_opt switch</span></span>

<span data-ttu-id="1a60f-105">Der Schalter **/cpp \_ opt** gibt Optionen an, die an den C/C++-Präprozessor übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="1a60f-105">The **/cpp\_opt** switch specifies options to pass to the C/C++ preprocessor.</span></span>

``` syntax
midl /cpp_opt "C_preprocessor_option" file.idl
```

## <a name="switch-options"></a><span data-ttu-id="1a60f-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="1a60f-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="1a60f-107">*C- \_ \_ Präprozessoroption*</span><span class="sxs-lookup"><span data-stu-id="1a60f-107">*C\_preprocessor\_option*</span></span> 
</dt> <dd>

<span data-ttu-id="1a60f-108">Gibt die Befehlszeilenoption an, die dem aufgerufenen Präprozessor zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1a60f-108">Specifies command-line option associated with the invoked preprocessor.</span></span> 

<span data-ttu-id="1a60f-109">**Hinweis**: für die Microsoft c/C++-Präprozessoren müssen Sie den `/E` Schalter als Teil der *c- \_ präprozessoroptionszeichenfolge \_* angeben.</span><span class="sxs-lookup"><span data-stu-id="1a60f-109">**Note**: For the Microsoft C/C++ preprocessors you must supply the `/E` switch as part of the *C\_preprocessor\_option* string.</span></span> 

<span data-ttu-id="1a60f-110">Anführungszeichen sind erforderlich, wenn mehr als eine Option und Leerzeichen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a60f-110">Quotes are required when more than one option is used, and for spaces.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a60f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a60f-111">Remarks</span></span>

<span data-ttu-id="1a60f-112">Verwenden Sie diesen Switch nur, wenn es einen bestimmten Grund dafür gibt.</span><span class="sxs-lookup"><span data-stu-id="1a60f-112">Do not use this switch unless there is a specific reason for doing so.</span></span> <span data-ttu-id="1a60f-113">Wichtige Informationen zur Vorverarbeitung finden Sie unter [C-präprozessoranforderungen für Mittel l](c-preprocessor-requirements-for-midl.md) .</span><span class="sxs-lookup"><span data-stu-id="1a60f-113">Consult [C-Preprocessor Requirements for MIDL](c-preprocessor-requirements-for-midl.md) for important information regarding preprocessing.</span></span>

<span data-ttu-id="1a60f-114">Der Schalter " **/cpp \_ opt** " kann mit oder ohne den Schalter " [**/cpp \_ cmd**](-cpp-cmd.md) " verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a60f-114">The **/cpp\_opt** switch can be used with or without the [**/cpp\_cmd**](-cpp-cmd.md) switch.</span></span> <span data-ttu-id="1a60f-115">Weitere Informationen zur Erstellung der präprozessorbefehlszeile in beiden Fällen finden Sie unter **/cpp \_ cmd** .</span><span class="sxs-lookup"><span data-stu-id="1a60f-115">Consult **/cpp\_cmd** for details of how the preprocessor command line is constructed in either case.</span></span>

<span data-ttu-id="1a60f-116">Der **/cpp \_ opt** -Schalter muss, falls angegeben, immer enthalten, um `/E` ordnungsgemäß zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="1a60f-116">The **/cpp\_opt** switch, if specified, must always include `/E` in order to function correctly.</span></span>

## <a name="examples"></a><span data-ttu-id="1a60f-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1a60f-117">Examples</span></span>

<span data-ttu-id="1a60f-118">**Mittel l/cpp \_ cmd d: \\ NT \\ Tools \\ ia64 \\cl.exe/DFLAG = true/IC: \\ Inc filename. idl**</span><span class="sxs-lookup"><span data-stu-id="1a60f-118">**midl /cpp\_cmd d:\\nt\\tools\\ia64\\cl.exe /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="1a60f-119">**Mittel l/cpp \_ cmd "mycpp"/DFLAG = true/IC: \\ Inc filename. idl**</span><span class="sxs-lookup"><span data-stu-id="1a60f-119">**midl /cpp\_cmd "mycpp" /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="1a60f-120">**Mittel l/cpp \_ Opt "/E/DFLAG = true/IC: \\ Inc" Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="1a60f-120">**midl /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

<span data-ttu-id="1a60f-121">**Mittel l/cpp \_ cmd "CL"/cpp \_ Opt "/E/DFLAG = true/IC: \\ Inc" Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="1a60f-121">**midl /cpp\_cmd "cl" /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="1a60f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a60f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a60f-123">**/savePP**</span><span class="sxs-lookup"><span data-stu-id="1a60f-123">**/savePP**</span></span>](-savepp.md)
</dt> <dt>

[<span data-ttu-id="1a60f-124">**/cpp- \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="1a60f-124">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="1a60f-125">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="1a60f-125">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="1a60f-126">**/No \_ cpp**</span><span class="sxs-lookup"><span data-stu-id="1a60f-126">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> <dt>

[<span data-ttu-id="1a60f-127">C-präprozessoranforderungen für die Mittel l</span><span class="sxs-lookup"><span data-stu-id="1a60f-127">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




