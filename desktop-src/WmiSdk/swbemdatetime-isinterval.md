---
description: Boolescher Wert, der angibt, ob ein Feld in einem CIM-DateTime-Wert als Intervall interpretiert werden soll.
ms.assetid: ba5fcf17-7c26-4960-9da9-e380d90e5f3e
ms.tgt_platform: multiple
title: "' Taubemdatetime. isinterval '-Eigenschaft (wbemdisp. h)"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.IsInterval
- ISWbemDateTime.IsInterval
- ISWbemDateTime.get_IsInterval
- ISWbemDateTime.put_IsInterval
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 468ea16de4f1206a9a15c58c2c7891df8afd4c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218486"
---
# <a name="swbemdatetimeisinterval-property"></a><span data-ttu-id="54a0c-103">' Taubemdatetime. isinterval '-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="54a0c-103">SWbemDateTime.IsInterval property</span></span>

<span data-ttu-id="54a0c-104">Die **isinterval** -Eigenschaft des " [**Swap DateTime**](swbemdatetime.md) "-Objekts ist ein boolescher Wert, der angibt, ob ein Feld in einem CIM-DateTime-Wert als Intervall interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="54a0c-104">The **IsInterval** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether any field in a CIM datetime value should be interpreted as an interval.</span></span>

<span data-ttu-id="54a0c-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="54a0c-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="54a0c-106">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="54a0c-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="54a0c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="54a0c-107">Syntax</span></span>


```VB
SWbemDateTime.IsInterval As boolean
```



## <a name="property-value"></a><span data-ttu-id="54a0c-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="54a0c-108">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="54a0c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54a0c-109">Examples</span></span>

<span data-ttu-id="54a0c-110">Beispiele für die Verwendung des Objekts " [**slibemdatetime**](swbemdatetime.md) " zum Konvertieren von CIM-DateTime-Werten in das bzw. aus dem **DateTime** -oder **VT \_ Date** -Format finden Sie unter [WMI-Tasks: Datums-und Uhrzeitangaben](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="54a0c-110">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM datetime values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="54a0c-111">Eine Beschreibung des CIM-DateTime-Formats finden Sie unter [Datums-und Uhrzeit Format](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="54a0c-111">For a description of the CIM datetime format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="54a0c-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54a0c-112">Requirements</span></span>



| <span data-ttu-id="54a0c-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54a0c-113">Requirement</span></span> | <span data-ttu-id="54a0c-114">Wert</span><span class="sxs-lookup"><span data-stu-id="54a0c-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54a0c-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54a0c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="54a0c-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54a0c-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="54a0c-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54a0c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="54a0c-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54a0c-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="54a0c-119">Header</span><span class="sxs-lookup"><span data-stu-id="54a0c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="54a0c-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="54a0c-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="54a0c-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="54a0c-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="54a0c-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="54a0c-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="54a0c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="54a0c-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54a0c-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54a0c-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="54a0c-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="54a0c-125">CLSID</span></span><br/>                    | <span data-ttu-id="54a0c-126">CLSID- \_ Swap-DateTime</span><span class="sxs-lookup"><span data-stu-id="54a0c-126">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="54a0c-127">IID</span><span class="sxs-lookup"><span data-stu-id="54a0c-127">IID</span></span><br/>                      | <span data-ttu-id="54a0c-128">IID \_ iswbemdatetime</span><span class="sxs-lookup"><span data-stu-id="54a0c-128">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="54a0c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54a0c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54a0c-130">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="54a0c-130">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="54a0c-131">Datums-und Uhrzeit Format</span><span class="sxs-lookup"><span data-stu-id="54a0c-131">Date and Time Format</span></span>](date-and-time-format.md)
</dt> </dl>

 

 




