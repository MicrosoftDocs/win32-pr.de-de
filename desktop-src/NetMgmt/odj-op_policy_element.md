---
title: OP_POLICY_ELEMENT
description: OP_POLICY_ELEMENT IDL-Definition
ms.assetid: 69f6e0e7-3f47-4fee-8a4c-df94093dcffa
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: df6fc6852a5efd0a6a2e01a805878ed51bc7c263
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "104316905"
---
# <a name="op_policy_element-structure"></a><span data-ttu-id="e72e9-103">OP_POLICY_ELEMENT Struktur</span><span class="sxs-lookup"><span data-stu-id="e72e9-103">OP_POLICY_ELEMENT structure</span></span>

<span data-ttu-id="e72e9-104">Definiert einen Registrierungsschlüssel und einen Wertnamen,-Typ und-Wert, die unter diesem Schlüssel konfiguriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e72e9-104">Defines a registry key and a value name, type, and value that should be configured under that key.</span></span>

## <a name="syntax"></a><span data-ttu-id="e72e9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e72e9-105">Syntax</span></span>

```C++
typedef struct _OP_POLICY_ELEMENT
{
    [string] wchar_t                *pKeyPath;
    [string] wchar_t                *pValueName;
    ULONG                           ulValueType;
    ULONG                           cbValueData;
    [size_is(cbValueData)]  PBYTE   pValueData;
} OP_POLICY_ELEMENT, *POP_POLICY_ELEMENT;
```

## <a name="members"></a><span data-ttu-id="e72e9-106">Member</span><span class="sxs-lookup"><span data-stu-id="e72e9-106">Members</span></span>

### <a name="pkeypath"></a><span data-ttu-id="e72e9-107">pkeypath</span><span class="sxs-lookup"><span data-stu-id="e72e9-107">pKeyPath</span></span>

<span data-ttu-id="e72e9-108">Enthält den Pfad des Registrierungsschlüssels.</span><span class="sxs-lookup"><span data-stu-id="e72e9-108">Contains the path of the registry key.</span></span>

### <a name="pvaluename"></a><span data-ttu-id="e72e9-109">pvaluename</span><span class="sxs-lookup"><span data-stu-id="e72e9-109">pValueName</span></span>

<span data-ttu-id="e72e9-110">Enthält den Namen des Registrierungs Werts.</span><span class="sxs-lookup"><span data-stu-id="e72e9-110">Contains the name of the registry value.</span></span>

### <a name="ulvaluetype"></a><span data-ttu-id="e72e9-111">ulvaluetype</span><span class="sxs-lookup"><span data-stu-id="e72e9-111">ulValueType</span></span>

<span data-ttu-id="e72e9-112">Enthält einen der Werte aus [Registrierungs Werttypen](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="e72e9-112">Contains one of the values from [Registry Value Types](../sysinfo/registry-value-types.md).</span></span>

### <a name="cbvaluedata"></a><span data-ttu-id="e72e9-113">cbvaluedata</span><span class="sxs-lookup"><span data-stu-id="e72e9-113">cbValueData</span></span>

<span data-ttu-id="e72e9-114">Enthält die Größe von pvaluedata in Bytes.</span><span class="sxs-lookup"><span data-stu-id="e72e9-114">Contains the size of pValueData in bytes.</span></span>

### <a name="ulvaluetype"></a><span data-ttu-id="e72e9-115">ulvaluetype</span><span class="sxs-lookup"><span data-stu-id="e72e9-115">ulValueType</span></span>

<span data-ttu-id="e72e9-116">Enthält den Wert des Registrierungs Werts.</span><span class="sxs-lookup"><span data-stu-id="e72e9-116">Contains the value of the registry value.</span></span>

## <a name="see-also"></a><span data-ttu-id="e72e9-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e72e9-117">See also</span></span>

[<span data-ttu-id="e72e9-118">**IDL-Definitionen im Offline-Domänen Beitritt**</span><span class="sxs-lookup"><span data-stu-id="e72e9-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)