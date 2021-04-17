---
title: force_allocate-Attribut
description: Das ACF-Attribut \ Force Allocation \_ \ erzwingt, dass ein Zeiger Parameter mithilfe der Benutzer Zuordnung von mittlerer l zugewiesen wird, \_ \_ anstatt die Zuordnung zu optimieren.
ms.assetid: 40e3a7d9-7e4f-4e3d-8c82-fb6ef567f293
keywords:
- force_allocate Attribut-Mittel l
topic_type:
- apiref
api_name:
- force_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f73d0386d786e4d3004c78b1acccda7e9be8fc16
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472844"
---
# <a name="force_allocate-attribute"></a><span data-ttu-id="b2c67-104">Attribut "zuordnen" erzwingen \_</span><span class="sxs-lookup"><span data-stu-id="b2c67-104">force\_allocate attribute</span></span>

<span data-ttu-id="b2c67-105">Mit der ACF-Attribut \[ **Erzwingung wird erzwungen \_** \] , dass ein Zeiger Parameter mithilfe der [**Mittel \_ \_**](midl-user-allocate-1.md) Wertzuordnung zugewiesen wird, anstatt die Zuordnung zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="b2c67-105">The ACF attribute \[**force\_allocate**\] forces a pointer parameter to be allocated using [**midl\_user\_allocate**](midl-user-allocate-1.md) instead of optimizing away the allocation.</span></span>

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ force_allocate [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="parameters"></a><span data-ttu-id="b2c67-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2c67-106">Parameters</span></span>

<span data-ttu-id="b2c67-107">Dieses Attribut hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b2c67-107">This attribute has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2c67-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2c67-108">Remarks</span></span>

<span data-ttu-id="b2c67-109">RPC versucht, Speicher Belegungen auf dem Server zu minimieren, indem Zeiger auf interne Speicherpuffer bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b2c67-109">RPC attempts to minimize memory allocations on the server by supplying pointers to internal memory buffers.</span></span> <span data-ttu-id="b2c67-110">Diese Vorgehensweise kann Probleme bei Anwendungen verursachen, die versuchen, den [**\_ Benutzer \_ kostenlos**](midl-user-free-1.md) für die von RPC bereitgestellten Zeiger aufzurufen, da ein optimierter Zeiger nicht freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="b2c67-110">This approach can cause problems for applications that attempt to directly call [**midl\_user\_free**](midl-user-free-1.md) on RPC-supplied pointers, because a pointer that has been optimized cannot be freed.</span></span> <span data-ttu-id="b2c67-111">Wenn Sie einen Parameter mit " **\[ erzwingen" \_ zuweisen \]** , wird diese Optimierung für alle Zeiger, die ihn ableiten, verhindert.</span><span class="sxs-lookup"><span data-stu-id="b2c67-111">Marking a parameter with **\[force\_allocate\]** will prevent this optimization for all pointers deriving it.</span></span>

<span data-ttu-id="b2c67-112">Eine weitere häufige Verwendung für die **\[ Zwangs \_ \]** Zuordnungen besteht darin, die Ausrichtung des Speichers zu gewährleisten, auf den verwiesen wird, wenn eine Anwendung eine Ausrichtung erfordert, die größer ist als der Speicher, auf den verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="b2c67-112">Another common use for **\[force\_allocate\]** is to guarantee the alignment of the memory being pointed to if an application requires an alignment greater than that of the memory pointed to.</span></span> <span data-ttu-id="b2c67-113">Beispielsweise übergeben Anwendungen häufig Daten in einem generischen Bytearray, anstatt den eigentlichen Typ zu verwenden, aber ein Byte wird nur bei 1 sichergestellt, was für Anwendungen, die eine größere Ausrichtung annehmen, zu Problemen führen kann.</span><span class="sxs-lookup"><span data-stu-id="b2c67-113">For example, applications often pass data in a generic array of bytes rather than using the actual type, but a byte is only guaranteed to be aligned at 1, which may cause problems for applications that assume a larger alignment.</span></span> <span data-ttu-id="b2c67-114">Durch Markieren des Parameters mit der Zuweisungs **\[ \_ Zuteilung \]** kann die Anwendung sicherstellen, dass für den gesamten Speicher, auf den verwiesen wird, eine Ausrichtung entspricht, die durch die [**\_ Benutzer \_**](midl-user-allocate-1.md)Zuordnungen garantiert wird.</span><span class="sxs-lookup"><span data-stu-id="b2c67-114">By marking the parameter with **\[force\_allocate\]**, the application can guarantee all memory pointed to will have an alignment equal to that guaranteed by [**midl\_user\_allocate**](midl-user-allocate-1.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b2c67-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b2c67-115">Examples</span></span>

``` syntax
/* IDL file */
void Func1([in, out, string] char **ppstr);
void Func2([in] long s, [in, size_is(s)] byte *pData);

/* ACF file */

/* e.g. The application wishes to call midl_user_free on *ppstr and supply a new pointer */
Func1([force_allocate] pstr);

/* e.g. pData really points to a structure that needs an alignment greater than 1 */
Func2([force_allocate] pData);
```

## <a name="see-also"></a><span data-ttu-id="b2c67-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b2c67-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2c67-117">Vermeiden von Informationen ausblenden</span><span class="sxs-lookup"><span data-stu-id="b2c67-117">Avoiding Information Hiding</span></span>](/windows/desktop/WinProg64/avoiding-information-hiding)
</dt> <dt>

[<span data-ttu-id="b2c67-118">Entwerfen von 64-Bit-kompatiblen Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b2c67-118">Designing 64-bit-Compatible Interfaces</span></span>](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces)
</dt> <dt>

[<span data-ttu-id="b2c67-119">**mittlere Benutzer Zuordnungen \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b2c67-119">**midl\_user\_allocate**</span></span>](midl-user-allocate-1.md)
</dt> <dt>

[<span data-ttu-id="b2c67-120">**mittlerer l- \_ Benutzer \_ kostenlos**</span><span class="sxs-lookup"><span data-stu-id="b2c67-120">**midl\_user\_free**</span></span>](midl-user-free-1.md)
</dt> <dt>

[<span data-ttu-id="b2c67-121">**allocate**</span><span class="sxs-lookup"><span data-stu-id="b2c67-121">**allocate**</span></span>](allocate.md)
</dt> </dl>

 

 