---
description: Gibt an, ob die angegebene erkannte Zeichenfolge aus dem System Wörterbuch, dem Benutzerwörterbuch oder der Wort Liste stammt.
ms.assetid: 1504e633-5917-4ac6-b043-95d4bc75b020
title: 'Icontextnode:: isdatasestringsupported-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsAlternateStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 93dfcdc59851aad3b06fb1451178e97b36ee0a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345078"
---
# <a name="icontextnodeisalternatestringsupported-method"></a><span data-ttu-id="e6592-103">Icontextnode:: isalternative estringsupported-Methode</span><span class="sxs-lookup"><span data-stu-id="e6592-103">IContextNode::IsAlternateStringSupported method</span></span>

<span data-ttu-id="e6592-104">Gibt an, ob die angegebene erkannte Zeichenfolge aus dem System Wörterbuch, dem Benutzerwörterbuch oder der Wort Liste stammt.</span><span class="sxs-lookup"><span data-stu-id="e6592-104">Indicates whether the specified recognized string came from the system dictionary, user dictionary, or word list.</span></span> <span data-ttu-id="e6592-105">Alle einschränkenden Daten, wie z. b. wordlists, Führungslinien oder Faktoide, werden verwendet, um zu bestimmen, ob die Zeichenfolge unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="e6592-105">Any restricting data, like wordlists, guides or factoids, in any corresponding hint node will be used to determine if the string is supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6592-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6592-106">Syntax</span></span>


```C++
HRESULT IsAlternateStringSupported(
  [in]  BSTR         bstrAlternateString,
  [out] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a><span data-ttu-id="e6592-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6592-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6592-108">*bstrauchanestring* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6592-108">*bstrAlternateString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6592-109">Erkannte Zeichenfolge zur Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="e6592-109">Recognized string to verify.</span></span>

</dd> <dt>

<span data-ttu-id="e6592-110">*pfissupported* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e6592-110">*pfIsSupported* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6592-111">**Variant \_ TRUE** , wenn die angegebene Zeichenfolge von [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) mit den angewendeten entsprechenden Hinweis Knoten unterstützt wird. **Variant \_ FALSE** , wenn nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e6592-111">**VARIANT\_TRUE** if the specified string is supported by the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) with any corresponding hint nodes applied; **VARIANT\_FALSE** if not supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6592-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6592-112">Return value</span></span>

<span data-ttu-id="e6592-113">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e6592-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e6592-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6592-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e6592-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e6592-115">Requirements</span></span>



| <span data-ttu-id="e6592-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6592-116">Requirement</span></span> | <span data-ttu-id="e6592-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e6592-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6592-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6592-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e6592-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6592-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e6592-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6592-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e6592-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e6592-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e6592-122">Header</span><span class="sxs-lookup"><span data-stu-id="e6592-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6592-123"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e6592-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e6592-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e6592-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6592-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6592-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e6592-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6592-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6592-127">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="e6592-127">**IContextNode**</span></span>](icontextnode.md)
</dt> </dl>

 

 




