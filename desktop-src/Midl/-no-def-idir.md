---
title: /no_def_idir Schalter
description: Wenn Verzeichnisse mit dem/I-Schalter angegeben werden, weist der/No \_ DEF \_ Idir-Schalter den Mittelwert-Compiler an, nur Verzeichnisse zu durchsuchen, die mit dem/I-Schalter angegeben wurden.
ms.assetid: 9a396de4-332d-4832-8e8b-291690cd3a10
keywords:
- /no_def_idir-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /no_def_idir
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62ed845c73c36fbbfe4ea7dea952ee4541b043a7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857584"
---
# <a name="no_def_idir-switch"></a><span data-ttu-id="9ab3c-104">/No \_ DEF ( \_ Idir-Schalter)</span><span class="sxs-lookup"><span data-stu-id="9ab3c-104">/no\_def\_idir switch</span></span>

<span data-ttu-id="9ab3c-105">Wenn Verzeichnisse mit dem [**/I**](-i.md) -Schalter angegeben werden, weist der **/No \_ DEF \_ Idir** -Schalter den Mittelwert-Compiler an, nur die Verzeichnisse zu durchsuchen, die mit dem **/I** -Schalter angegeben werden, wobei das aktuelle Verzeichnis sowie die von der INCLUDE-Umgebungsvariablen angegebenen Verzeichnisse ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="9ab3c-105">When directories are specified with the [**/I**](-i.md) switch, the **/no\_def\_idir** switch instructs the MIDL compiler to search only the directories specified with the **/I** switch, ignoring the current directory as well as the directories specified by the INCLUDE environment variable.</span></span>

``` syntax
midl /no_def_idir
```

## <a name="switch-options"></a><span data-ttu-id="9ab3c-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="9ab3c-106">Switch Options</span></span>

<span data-ttu-id="9ab3c-107">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9ab3c-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ab3c-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ab3c-108">Remarks</span></span>

<span data-ttu-id="9ab3c-109">Wenn keine Verzeichnisse mit dem [**/I**](-i.md) -Schalter angegeben werden, weist der **/No \_ DEF \_ Idir** -Schalter den Mittelwert Compiler an, nur das aktuelle Verzeichnis zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="9ab3c-109">When no directories are specified with the [**/I**](-i.md) switch, the **/no\_def\_idir** switch instructs the MIDL compiler to search only the current directory.</span></span>

## <a name="examples"></a><span data-ttu-id="9ab3c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ab3c-110">Examples</span></span>

``` syntax
; search only the current directory 
midl /no_def_idir filename.idl  

; search only the specified directories 
midl /no_def_idir /I c:\c700\include filename.idl 
```

## <a name="see-also"></a><span data-ttu-id="9ab3c-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9ab3c-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ab3c-112">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="9ab3c-112">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="9ab3c-113">**/acf**</span><span class="sxs-lookup"><span data-stu-id="9ab3c-113">**/acf**</span></span>](-acf.md)
</dt> <dt>

[<span data-ttu-id="9ab3c-114">**/I**</span><span class="sxs-lookup"><span data-stu-id="9ab3c-114">**/I**</span></span>](-i.md)
</dt> </dl>

 

 




