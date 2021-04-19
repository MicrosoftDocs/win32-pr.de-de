---
description: Gibt an, ob die erkannte Zeichenfolge dieses icontextnode aus dem System Wörterbuch, dem Benutzerwörterbuch oder der Wort Liste stammt.
ms.assetid: 9eaee549-ae78-4a67-a39e-2096c7d5d9cd
title: 'Icontextnode:: IsStringSupported-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 853b244cdd6f9e61d4474876190daeccaa2c8779
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357352"
---
# <a name="icontextnodeisstringsupported-method"></a><span data-ttu-id="10e39-103">Icontextnode:: IsStringSupported-Methode</span><span class="sxs-lookup"><span data-stu-id="10e39-103">IContextNode::IsStringSupported method</span></span>

<span data-ttu-id="10e39-104">Gibt an, ob die erkannte Zeichenfolge dieses [**icontextnode**](icontextnode.md) aus dem System Wörterbuch, dem Benutzerwörterbuch oder der Wort Liste stammt.</span><span class="sxs-lookup"><span data-stu-id="10e39-104">Indicates whether recognized string of this [**IContextNode**](icontextnode.md) came from the system dictionary, user dictionary, or word list.</span></span>

## <a name="syntax"></a><span data-ttu-id="10e39-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="10e39-105">Syntax</span></span>


```C++
HRESULT IsStringSupported(
  [out, retval] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a><span data-ttu-id="10e39-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="10e39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10e39-107">*pfissupported* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="10e39-107">*pfIsSupported* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="10e39-108">**Variant \_ TRUE** , wenn der erkannte Zeichen folgen Wert dieses [**icontextnode**](icontextnode.md) von [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) unterstützt wird, wenn alle entsprechenden Hinweis Knoten angewendet werden. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="10e39-108">**VARIANT\_TRUE** if the recognized string value of this [**IContextNode**](icontextnode.md) is supported by the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) with any corresponding hint nodes applied; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10e39-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="10e39-109">Return value</span></span>

<span data-ttu-id="10e39-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="10e39-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="10e39-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10e39-111">Requirements</span></span>



| <span data-ttu-id="10e39-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10e39-112">Requirement</span></span> | <span data-ttu-id="10e39-113">Wert</span><span class="sxs-lookup"><span data-stu-id="10e39-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10e39-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10e39-114">Minimum supported client</span></span><br/> | <span data-ttu-id="10e39-115">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10e39-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="10e39-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10e39-116">Minimum supported server</span></span><br/> | <span data-ttu-id="10e39-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="10e39-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="10e39-118">Header</span><span class="sxs-lookup"><span data-stu-id="10e39-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="10e39-119"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="10e39-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="10e39-120">DLL</span><span class="sxs-lookup"><span data-stu-id="10e39-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10e39-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10e39-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="10e39-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10e39-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10e39-123">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="10e39-123">**IContextNode**</span></span>](icontextnode.md)
</dt> </dl>

 

 




