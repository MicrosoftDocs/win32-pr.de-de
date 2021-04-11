---
title: /D-Schalter
description: Der Schalter/D definiert einen Namen und einen optionalen Wert, der an den C-Präprozessor als If by a \ define-Direktive übermittelt werden soll. Mehrere/D-Direktiven können in einer Befehlszeile verwendet werden.
ms.assetid: 65642bf6-8e25-400b-8b1c-43513ab6b313
keywords:
- /D-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d51cdcbecb5386acb1a97d933be8b25f68720ee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100971"
---
# <a name="d-switch"></a><span data-ttu-id="4e7fc-105">/D-Schalter</span><span class="sxs-lookup"><span data-stu-id="4e7fc-105">/D switch</span></span>

<span data-ttu-id="4e7fc-106">Der Schalter **/D** definiert einen Namen und einen optionalen Wert, der an den C-Präprozessor wie bei einer **\# define** -Direktive übermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4e7fc-106">The **/D** switch defines a name and an optional value to be passed to the C preprocessor as if by a **\#define** directive.</span></span> <span data-ttu-id="4e7fc-107">Mehrere **/D** -Direktiven können in einer Befehlszeile verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e7fc-107">Multiple **/D** directives can be used in a command line.</span></span>

``` syntax
midl /Dname[=definition]
```

## <a name="switch-options"></a><span data-ttu-id="4e7fc-108">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="4e7fc-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="4e7fc-109">*name*</span><span class="sxs-lookup"><span data-stu-id="4e7fc-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="4e7fc-110">Gibt einen definierten Namen an, der an den C-Präprozessor übergeben wird, wenn der [**/cpp- \_ cmd**](-cpp-cmd.md) -Schalter vorhanden ist, und der [**/cpp- \_ opt**](-cpp-opt.md) -Switch ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4e7fc-110">Specifies a defined name that is passed to the C preprocessor when the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not present.</span></span>

</dd> <dt>

<span data-ttu-id="4e7fc-111">*Definition*</span><span class="sxs-lookup"><span data-stu-id="4e7fc-111">*definition*</span></span> 
</dt> <dd>

<span data-ttu-id="4e7fc-112">Gibt einen Wert an, der mit dem definierten Namen verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="4e7fc-112">Specifies a value associated with the defined name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e7fc-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e7fc-113">Remarks</span></span>

<span data-ttu-id="4e7fc-114">Leerraum zwischen dem **/D** -Switch und dem definierten Namen ist optional.</span><span class="sxs-lookup"><span data-stu-id="4e7fc-114">White space between the **/D** switch and the defined name is optional.</span></span>

<span data-ttu-id="4e7fc-115">Wenn der [**/cpp \_ -cmd**](-cpp-cmd.md) -Schalter vorhanden und der [**/cpp- \_ opt**](-cpp-opt.md) -Switch nicht ist, verkettet der Mittell-Compiler die durch den **/cpp \_ cmd** -Schalter angegebene Zeichenfolge mit den Optionen [**/I**](-i.md), **/D** und [**/U**](-u.md) und verwendet diese verketteten Zeichenfolge, um den C-Präprozessor für jede IDL-und ACF-Quelldatei aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="4e7fc-115">When the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the [**/I**](-i.md), **/D**, and [**/U**](-u.md) options and uses this concatenated string to invoke the C preprocessor for each IDL and ACF source file.</span></span>

<span data-ttu-id="4e7fc-116">Der Mittell-Compilerschalter **/D** wird ignoriert, wenn der Mittelwert-Compilerschalter [/No \_ cpp](-no-cpp-nocpp.md) oder [**/cpp \_ opt**](-cpp-opt.md) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4e7fc-116">The MIDL compiler switch **/D** is ignored when the MIDL compiler switch [/no\_cpp](-no-cpp-nocpp.md) or [**/cpp\_opt**](-cpp-opt.md) is specified.</span></span>

## <a name="examples"></a><span data-ttu-id="4e7fc-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e7fc-117">Examples</span></span>

<span data-ttu-id="4e7fc-118">**Dateiname-dunicode-Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="4e7fc-118">**midl -DUNICODE filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="4e7fc-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e7fc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e7fc-120">**/cpp- \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="4e7fc-120">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="4e7fc-121">**/cpp \_ Opt**</span><span class="sxs-lookup"><span data-stu-id="4e7fc-121">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="4e7fc-122">**/I**</span><span class="sxs-lookup"><span data-stu-id="4e7fc-122">**/I**</span></span>](-i.md)
</dt> <dt>

[<span data-ttu-id="4e7fc-123">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="4e7fc-123">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="4e7fc-124">**/No \_ cpp**</span><span class="sxs-lookup"><span data-stu-id="4e7fc-124">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> <dt>

[<span data-ttu-id="4e7fc-125">**/U**</span><span class="sxs-lookup"><span data-stu-id="4e7fc-125">**/U**</span></span>](-u.md)
</dt> </dl>

 

 




