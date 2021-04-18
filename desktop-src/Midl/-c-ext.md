---
title: /c_ext Schalter
description: Dieser Schalter ist in Version 3,0 des Mittelwert Compilers veraltet. Wenn Sie jedoch den \_ Schalter c EXT verwenden, wird kein Compilerfehler generiert, sodass Sie keine Verweise auf/MS \_ ext oder/c \_ ext aus einem vorhandenen Makefile entfernen müssen.
ms.assetid: 3d4072ba-5563-4014-a4ed-2e3aa26bb00a
keywords:
- /c_ext-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /c_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b3f179c2ce56b8e8ab6802b2d4bf5dd96c458e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106338425"
---
# <a name="c_ext-switch"></a><span data-ttu-id="399e2-105">/c \_ ext-Schalter</span><span class="sxs-lookup"><span data-stu-id="399e2-105">/c\_ext switch</span></span>

<span data-ttu-id="399e2-106">Dieser Schalter ist in Version 3,0 des Mittelwert Compilers veraltet.</span><span class="sxs-lookup"><span data-stu-id="399e2-106">This switch is obsolete as of version 3.0 of the MIDL compiler.</span></span> <span data-ttu-id="399e2-107">Wenn Sie jedoch den Schalter **c \_ ext** verwenden, wird kein Compilerfehler generiert, sodass Sie keine Verweise auf [**/MS \_ ext**](-ms-ext.md) oder **/c \_ ext** aus einem vorhandenen Makefile entfernen müssen.</span><span class="sxs-lookup"><span data-stu-id="399e2-107">However, using the **c\_ext** switch will not generate a compiler error, so you do not have to remove references to [**/ms\_ext**](-ms-ext.md) or **/c\_ext** from an existing makefile.</span></span>

``` syntax
midl /c_ext
```

## <a name="switch-options"></a><span data-ttu-id="399e2-108">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="399e2-108">Switch Options</span></span>

<span data-ttu-id="399e2-109">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="399e2-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="399e2-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="399e2-110">Remarks</span></span>

<span data-ttu-id="399e2-111">Die folgenden Funktionen sind jetzt standardmäßig verfügbar:</span><span class="sxs-lookup"><span data-stu-id="399e2-111">The following features are now available by default:</span></span>

-   <span data-ttu-id="399e2-112">Viele vorhandene Header Dateien definieren Typen mit Qualifizierern, z. b. " **weit** " und " **StdCall"**, die nicht Teil der DCE-IDL sind.</span><span class="sxs-lookup"><span data-stu-id="399e2-112">Many existing header files define types with qualifiers, such as **far** and **stdcall**, that are not part of the DCE IDL.</span></span> <span data-ttu-id="399e2-113">Diese Compiler (und der mittlerer l-Compiler im DCE-Kompatibilitätsmodus) generieren Fehler, wenn Sie versuchen, diese Qualifizierer zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="399e2-113">Those compilers (and the MIDL compiler in DCE-compatibility mode) generate errors when they attempt to process these qualifiers.</span></span> <span data-ttu-id="399e2-114">Der-Mittell-Compiler ermöglicht das Kompilieren von IDL-Dateien, die diese Qualifizierer enthalten.</span><span class="sxs-lookup"><span data-stu-id="399e2-114">The MIDL compiler allows you to compile IDL files that contain these qualifiers.</span></span> <span data-ttu-id="399e2-115">Die Typqualifizierer beeinflussen nicht die Art und Weise, wie die Daten im Netzwerk übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="399e2-115">The type qualifiers do not affect the way the data is transmitted on the network.</span></span>
-   <span data-ttu-id="399e2-116">Sie können direktionale Attribute wie z. b. [**\[ in \]**](in.md) oder [**\[ out \]**](out-idl.md)weglassen.</span><span class="sxs-lookup"><span data-stu-id="399e2-116">You can omit directional attributes such as [**\[in\]**](in.md) or [**\[out\]**](out-idl.md).</span></span>

<span data-ttu-id="399e2-117">Die folgenden C-Spracherweiterungen werden im Standardmodus unterstützt:</span><span class="sxs-lookup"><span data-stu-id="399e2-117">The following C-language extensions are supported in default mode:</span></span>

-   <span data-ttu-id="399e2-118">Bitfelder in Strukturen und Unions</span><span class="sxs-lookup"><span data-stu-id="399e2-118">Bit fields in structures and unions</span></span>
-   <span data-ttu-id="399e2-119">Kommentare, die mit zwei Schrägstrichen beginnen (//)</span><span class="sxs-lookup"><span data-stu-id="399e2-119">Comments that start with two slash characters (//)</span></span>
-   <span data-ttu-id="399e2-120">Externe Deklarationen</span><span class="sxs-lookup"><span data-stu-id="399e2-120">External declarations</span></span>
-   <span data-ttu-id="399e2-121">Prozeduren mit Ellipsen in der Parameterliste (...)</span><span class="sxs-lookup"><span data-stu-id="399e2-121">Procedures with ellipses in the parameter list (…)</span></span>
-   <span data-ttu-id="399e2-122">Auf 32-Bit-Plattformen ist [**int**](int.md) ein nativer 32-Bit-Basistyp. auf 16-Bit-Plattformen wird **int** erkannt, ist aber kein Remote barer Typ.</span><span class="sxs-lookup"><span data-stu-id="399e2-122">On 32-bit platforms, [**int**](int.md) is a native 32-bit base type; on 16-bit platforms, **int** is recognized but is not a remotable type</span></span>
-   <span data-ttu-id="399e2-123">Typ [**" \* void**](void.md) ", der in Remote Vorgängen nicht verwendet wird</span><span class="sxs-lookup"><span data-stu-id="399e2-123">Type [**void \***](void.md) that is not used in remote operations</span></span>
-   <span data-ttu-id="399e2-124">Typqualifizierer – einschließlich des Formulars mit dem ANSI-konforme Präfix – enthalten zwei Unterstriche: **cdecl**, **\_ \_ cdecl**, [**const**](const.md), **\_ \_ const**, **Export**, **\_ \_ Export**, **weit**, **\_ \_ weit**, **loadds**, **\_ \_ loadds**, **near**, **\_ \_ near**, **Pascal**, **\_ \_ Pascal**, **StdCall,** **\_ \_ StdCall,** **volatile** und **\_ \_ volatile**.</span><span class="sxs-lookup"><span data-stu-id="399e2-124">Type qualifiers—including the form with the ANSI-conformant prefix—contain two underscore characters: **cdecl**, **\_\_cdecl**, [**const**](const.md), **\_\_const**, **export**, **\_\_export**, **far**, **\_\_far**, **loadds**, **\_\_loadds**, **near**, **\_\_near**, **pascal**, **\_\_pascal**, **stdcall**, **\_\_stdcall**, **volatile**, and **\_\_volatile**.</span></span>

<span data-ttu-id="399e2-125">Weitere Informationen zu Deklarations Qualifizierern finden Sie in der Microsoft C/C++-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="399e2-125">For more information about declaration qualifiers, see your Microsoft C/C++ documentation.</span></span>

## <a name="see-also"></a><span data-ttu-id="399e2-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="399e2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="399e2-127">**/APP- \_ Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="399e2-127">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="399e2-128">**/osf**</span><span class="sxs-lookup"><span data-stu-id="399e2-128">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="399e2-129">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="399e2-129">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




