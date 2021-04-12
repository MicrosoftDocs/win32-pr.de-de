---
title: /oldtlb-Schalter
description: Der/oldtlb-Schalter weist den Mittel l-Compiler an, eine Typbibliothek im alten Format zu generieren.
ms.assetid: cf5fe000-7262-4812-a6ab-f12a558ac068
keywords:
- /oldtlb-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /oldtlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a08e468d0acff16aa1df4a45fcacafeb676b00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390202"
---
# <a name="oldtlb-switch"></a><span data-ttu-id="77b15-104">/oldtlb-Schalter</span><span class="sxs-lookup"><span data-stu-id="77b15-104">/oldtlb switch</span></span>

<span data-ttu-id="77b15-105">Der **/oldtlb** -Schalter weist den Mittel l-Compiler an, eine Typbibliothek im alten Format zu generieren.</span><span class="sxs-lookup"><span data-stu-id="77b15-105">The **/oldtlb** switch directs the MIDL compiler to generate an old-format type library.</span></span>

``` syntax
midl /oldtlb
```

## <a name="switch-options"></a><span data-ttu-id="77b15-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="77b15-106">Switch Options</span></span>

<span data-ttu-id="77b15-107">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="77b15-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="77b15-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77b15-108">Remarks</span></span>

<span data-ttu-id="77b15-109">Der **/oldtlb** -Schalter überschreibt den Standardwert und leitet den Mittelwert des compl-Compilers so um, dass Typbibliotheken im alten Format selbst bei aktuellen Versionen von Windows generiert werden [, indem "" anstelle von](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) " [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2)" die Verwendung von "</span><span class="sxs-lookup"><span data-stu-id="77b15-109">The **/oldtlb** switch overrides the default and directs the MIDL compiler to generate old-format type libraries even on current versions of Windows by using [CreateTypeLib](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib) instead of [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2).</span></span>

## <a name="examples"></a><span data-ttu-id="77b15-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="77b15-110">Examples</span></span>

<span data-ttu-id="77b15-111">**Mittel l/oldtlb Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="77b15-111">**midl /oldtlb filename.idl**</span></span>

<span data-ttu-id="77b15-112">**Mittel l/oldtlb myoldodl. ODL**</span><span class="sxs-lookup"><span data-stu-id="77b15-112">**midl /oldtlb myoldodl.odl**</span></span>

## <a name="see-also"></a><span data-ttu-id="77b15-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77b15-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77b15-114">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="77b15-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="77b15-115">**/newtlb**</span><span class="sxs-lookup"><span data-stu-id="77b15-115">**/newtlb**</span></span>](-newtlb.md)
</dt> </dl>

 

 