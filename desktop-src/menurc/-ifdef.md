---
title: " ifdef"
description: Die \ ifdef-Direktive steuert die bedingte Kompilierung der Ressourcen Datei, indem der angegebene Name überprüft wird.
ms.assetid: 877c6b58-d8a1-4e68-8b69-29fe106d6cbd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38170fb2140f8405a86529c0899c1e4d4e93c026
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388343"
---
# <a name="ifdef"></a><span data-ttu-id="e3833-103">\#ifdef</span><span class="sxs-lookup"><span data-stu-id="e3833-103">\#ifdef</span></span>

<span data-ttu-id="e3833-104">Die **\# ifdef** -Direktive steuert die bedingte Kompilierung der Ressourcen Datei, indem der angegebene Name überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="e3833-104">The **\#ifdef** directive controls conditional compilation of the resource file by checking the specified name.</span></span> <span data-ttu-id="e3833-105">Wenn der Name mithilfe einer **\# define** -Direktive oder mithilfe der Befehlszeilenoption **/d** mit dem Ressourcen Compiler definiert wurde, weist **\# ifdef** den Compiler an, mit der Anweisung unmittelbar nach der **\# ifdef** -Direktive fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="e3833-105">If the name has been defined by using a **\#define** directive or by using the **/d** command-line option with the resource compiler, **\#ifdef** directs the compiler to continue with the statement immediately after the **\#ifdef** directive.</span></span> <span data-ttu-id="e3833-106">Wenn der Name nicht definiert wurde, weist **\# ifdef** den Compiler an, alle Anweisungen bis zur nächsten **\# EndIf** -Direktive zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="e3833-106">If the name has not been defined, **\#ifdef** directs the compiler to skip all statements up to the next **\#endif** directive.</span></span>

``` syntax
#ifdef name
```

<dl> <dt>

<span data-ttu-id="e3833-107"><span id="name"></span><span id="NAME"></span>*Benennen*</span><span class="sxs-lookup"><span data-stu-id="e3833-107"><span id="name"></span><span id="NAME"></span>*name*</span></span>
</dt> <dd>

<span data-ttu-id="e3833-108">Der Name, der von der Direktive geprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="e3833-108">Name to be checked by the directive.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="e3833-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e3833-109">Example</span></span>

<span data-ttu-id="e3833-110">In diesem Beispiel wird die [**Bitmap**](bitmap-resource.md) -Anweisung nur kompiliert, wenn DEBUG definiert ist:</span><span class="sxs-lookup"><span data-stu-id="e3833-110">This example compiles the [**BITMAP**](bitmap-resource.md) statement only if Debug is defined:</span></span>

``` syntax
#ifdef Debug
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a><span data-ttu-id="e3833-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e3833-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3833-112">Präprozessordirektiven</span><span class="sxs-lookup"><span data-stu-id="e3833-112">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




