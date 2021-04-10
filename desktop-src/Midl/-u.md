---
title: /U-Schalter
description: Der/U-Schalter entfernt alle vorherigen Definitionen eines Namens, indem er den Namen an den C-Präprozessor übergibt, wie bei einer \ Präprozessordefinitionen aufheben-Direktive.
ms.assetid: 3c253fb3-9448-4b55-bfd5-852e6feec280
keywords:
- /U-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /U
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d018d47dd5cbcc8192dee490965bd06c56d0e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100926"
---
# <a name="u-switch"></a><span data-ttu-id="921a3-104">/U-Schalter</span><span class="sxs-lookup"><span data-stu-id="921a3-104">/U switch</span></span>

<span data-ttu-id="921a3-105">Der **/U** -Schalter entfernt alle vorherigen Definitionen eines Namens, indem er den Namen an den C-Präprozessor übergibt, wie bei einer **\# Präprozessordefinitionen aufheben** -Direktive.</span><span class="sxs-lookup"><span data-stu-id="921a3-105">The **/U** switch removes any previous definition of a name by passing the name to the C preprocessor as if by a **\#undefine** directive.</span></span>

``` syntax
midl /U name
```

## <a name="switch-options"></a><span data-ttu-id="921a3-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="921a3-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="921a3-107">*name*</span><span class="sxs-lookup"><span data-stu-id="921a3-107">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="921a3-108">Gibt einen definierten Namen an, der an den C-Präprozessor als if durch eine **\# Präprozessordefinitionen aufheben** -Direktive übermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="921a3-108">Specifies a defined name to be passed to the C preprocessor as if by a **\#undefine** directive.</span></span> <span data-ttu-id="921a3-109">Der Name wird vom C-Präprozessor oder zuvor vom Benutzer definiert.</span><span class="sxs-lookup"><span data-stu-id="921a3-109">The name is predefined by the C preprocessor or previously defined by the user.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="921a3-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="921a3-110">Remarks</span></span>

<span data-ttu-id="921a3-111">Mehrere **/U** -Direktiven können in einer Befehlszeile verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="921a3-111">Multiple **/U** directives can be used in a command line.</span></span> <span data-ttu-id="921a3-112">Leerraum zwischen dem Schalter **/U** und dem nicht definierten Namen ist optional.</span><span class="sxs-lookup"><span data-stu-id="921a3-112">White space between the **/U** switch and the undefined name is optional.</span></span>

<span data-ttu-id="921a3-113">Wenn der [**/cpp- \_ cmd**](-cpp-cmd.md) -Schalter vorhanden und [**der/cpp- \_ opt**](-cpp-opt.md) -Switch nicht ist, verkettet der Mittell-Compiler die durch den/cpp cmd-Schalter angegebene Zeichenfolge \_ mit den Optionen [**/I**](-i.md), [**/D**](-d.md)und **/U** und verwendet diese verketteten Zeichenfolge, um den C-Präprozessor für jede IDL-und ACF-Quelldatei aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="921a3-113">When the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not, the MIDL compiler concatenates the string specified by the /cpp\_cmd switch with the [**/I**](-i.md), [**/D**](-d.md), and **/U** options and uses this concatenated string to invoke the C preprocessor for each IDL and ACF source file.</span></span> <span data-ttu-id="921a3-114">Der Mittell-Compilerschalter **/U** wird ignoriert, wenn der Mittelwert-Compilerschalter **/No \_ cpp** oder **/cpp \_ opt** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="921a3-114">The MIDL compiler switch **/U** is ignored when the MIDL compiler switch **/no\_cpp** or **/cpp\_opt** is specified.</span></span>

## <a name="examples"></a><span data-ttu-id="921a3-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="921a3-115">Examples</span></span>

<span data-ttu-id="921a3-116">**Mittel l/UUNICODE Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="921a3-116">**midl /UUNICODE filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="921a3-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="921a3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="921a3-118">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="921a3-118">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="921a3-119">**/cpp- \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="921a3-119">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="921a3-120">**/cpp \_ Opt**</span><span class="sxs-lookup"><span data-stu-id="921a3-120">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="921a3-121">**/D**</span><span class="sxs-lookup"><span data-stu-id="921a3-121">**/D**</span></span>](-d.md)
</dt> <dt>

[<span data-ttu-id="921a3-122">**/I**</span><span class="sxs-lookup"><span data-stu-id="921a3-122">**/I**</span></span>](-i.md)
</dt> <dt>

[<span data-ttu-id="921a3-123">**/No \_ cpp**</span><span class="sxs-lookup"><span data-stu-id="921a3-123">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> </dl>

 

 




