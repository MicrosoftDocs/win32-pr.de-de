---
title: /System Switch
description: Der Schalter/System leitet den Mittel l-Compiler, um eine Typbibliothek für das angegebene System zu generieren. Der Standardwert ist das aktuelle Betriebssystem.
ms.assetid: 0fb69ffc-5ab4-49f3-b34d-859da776ce9e
keywords:
- /System Schalter-Mittel l
topic_type:
- apiref
api_name:
- / system
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e09f2cf97f8edb86ad831cff35420fad9a07d76
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312654"
---
# <a name="system-switch"></a><span data-ttu-id="119eb-105">/<system> Not</span><span class="sxs-lookup"><span data-stu-id="119eb-105">/<system> switch</span></span>

<span data-ttu-id="119eb-106">Der- **/<system>** Schalter weist den Mittel l-Compiler an, eine Typbibliothek für das angegebene System zu generieren.</span><span class="sxs-lookup"><span data-stu-id="119eb-106">The **/<system>** switch directs the MIDL compiler to generate a type library for the specified system.</span></span> <span data-ttu-id="119eb-107">Der Standardwert ist das aktuelle Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="119eb-107">The default is the current operating system.</span></span>

``` syntax
midl /{win32 | ia64 | amd64}
```

## <a name="switch-options"></a><span data-ttu-id="119eb-108">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="119eb-108">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span data-ttu-id="119eb-109"><span id="win32"></span><span id="WIN32"></span>Win32 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="119eb-109"><span id="win32"></span><span id="WIN32"></span>\*\*\*\*win32\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="119eb-110">Windows 2000, Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="119eb-110">Windows 2000, Windows XP, Windows Vista, Windows 7</span></span>

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span data-ttu-id="119eb-111"><span id="ia64"></span><span id="IA64"></span>ia64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="119eb-111"><span id="ia64"></span><span id="IA64"></span>\*\*\*\*ia64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="119eb-112">Eine Intel-basierte 64-Bit-Windows-Umgebung, z. b. Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="119eb-112">An Intel-based 64-bit Windows environment such as Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista, or Windows 7.</span></span>

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span data-ttu-id="119eb-113"><span id="amd64"></span><span id="AMD64"></span>amd64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="119eb-113"><span id="amd64"></span><span id="AMD64"></span>\*\*\*\*amd64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="119eb-114">Eine Windows-64 basierte Windows-Umgebung (Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista oder Windows 7).</span><span class="sxs-lookup"><span data-stu-id="119eb-114">An American Micro Devices-based 64-bit Windows environment such as Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista, or Windows 7.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="119eb-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="119eb-115">Remarks</span></span>

<span data-ttu-id="119eb-116">Der **/<system>** Switch ist funktional identisch mit der Option "Mittel l [**/env**](-env.md) " und wird vom Mittelwert Compiler ausschließlich aus Gründen der Abwärtskompatibilität mit MkTypLib erkannt.</span><span class="sxs-lookup"><span data-stu-id="119eb-116">The **/<system>** switch is functionally the same as the MIDL [**/env**](-env.md) option and is recognized by the MIDL compiler solely for backward compatibility with MkTypLib.</span></span> <span data-ttu-id="119eb-117">Wenn Sie ein neues Makefile-Skript erstellen, verwenden Sie den **/env** -Schalter.</span><span class="sxs-lookup"><span data-stu-id="119eb-117">If you are generating a new makefile, use the **/env** switch.</span></span>

## <a name="examples"></a><span data-ttu-id="119eb-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="119eb-118">Examples</span></span>

<span data-ttu-id="119eb-119">**Mittel l/Win32 Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="119eb-119">**midl /win32 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="119eb-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="119eb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="119eb-121">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="119eb-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="119eb-122">**/ENV**</span><span class="sxs-lookup"><span data-stu-id="119eb-122">**/env**</span></span>](-env.md)
</dt> </dl>

 

 




