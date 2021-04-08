---
title: OP_POLICY_ELEMENT_LIST
description: OP_POLICY_ELEMENT_LIST IDL-Definition
ms.assetid: 1eebbdd2-655b-4bd3-938c-6bc687ffe7bb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 3c46e7208e6c142b9f58a7704be9bd3461c845b2
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2020
ms.locfileid: "103734697"
---
# <a name="op_policy_element_list-structure"></a><span data-ttu-id="960ee-103">OP_POLICY_ELEMENT_LIST Struktur</span><span class="sxs-lookup"><span data-stu-id="960ee-103">OP_POLICY_ELEMENT_LIST structure</span></span>

<span data-ttu-id="960ee-104">Definiert einen Stamm Registrierungsschlüssel und ein Array von Registrierungsschlüssel Elementen, die unter diesem Schlüssel konfiguriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="960ee-104">Defines  a root registry key and an array of registry key elements to be configured under that key.</span></span>

## <a name="syntax"></a><span data-ttu-id="960ee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="960ee-105">Syntax</span></span>

```C++
typedef struct _OP_POLICY_ELEMENT_LIST
{
    [string] wchar_t                            *pSource;
    ULONG                                       ulRootKeyId;
    ULONG                                       cElements;
    [size_is(cElements)]    POP_POLICY_ELEMENT  pElements;
} OP_POLICY_ELEMENT_LIST, *POP_POLICY_ELEMENT_LIST;
```

## <a name="members"></a><span data-ttu-id="960ee-106">Member</span><span class="sxs-lookup"><span data-stu-id="960ee-106">Members</span></span>

### <a name="psource"></a><span data-ttu-id="960ee-107">psource</span><span class="sxs-lookup"><span data-stu-id="960ee-107">pSource</span></span>

<span data-ttu-id="960ee-108">Enthält den Pfad der Gruppenrichtlinie-Datei, aus der die enthaltenen Elemente stammen.</span><span class="sxs-lookup"><span data-stu-id="960ee-108">Contains the path of the Group Policy file that the contained elements were sourced from.</span></span>

### <a name="ulrootkeyid"></a><span data-ttu-id="960ee-109">ulrootkeyid</span><span class="sxs-lookup"><span data-stu-id="960ee-109">ulRootKeyId</span></span>

<span data-ttu-id="960ee-110">Enthält den Bezeichner des Stamm Registrierungsschlüssels. muss derzeit auf HKEY_LOCAL_MACHINE festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="960ee-110">Contains the identifier of the root registry key; currently must be set to HKEY_LOCAL_MACHINE.</span></span>

### <a name="celements"></a><span data-ttu-id="960ee-111">cElements</span><span class="sxs-lookup"><span data-stu-id="960ee-111">cElements</span></span>

<span data-ttu-id="960ee-112">Enthält die Anzahl der Elemente in pelements.</span><span class="sxs-lookup"><span data-stu-id="960ee-112">Contains the number of elements in pElements.</span></span>

### <a name="pelements"></a><span data-ttu-id="960ee-113">pelements</span><span class="sxs-lookup"><span data-stu-id="960ee-113">pElements</span></span>

<span data-ttu-id="960ee-114">Enthält ein Array von OP_POLICY_ELEMENT Elementen.</span><span class="sxs-lookup"><span data-stu-id="960ee-114">Contains an array of OP_POLICY_ELEMENT elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="960ee-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="960ee-115">See also</span></span>

[<span data-ttu-id="960ee-116">**IDL-Definitionen im Offline-Domänen Beitritt**</span><span class="sxs-lookup"><span data-stu-id="960ee-116">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="960ee-117">**OP- \_ Richtlinien \_ Element**</span><span class="sxs-lookup"><span data-stu-id="960ee-117">**OP\_POLICY\_ELEMENT**</span></span>](odj-op_policy_element.md)
