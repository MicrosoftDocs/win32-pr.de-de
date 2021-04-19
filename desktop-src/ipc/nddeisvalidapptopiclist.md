---
description: Bestimmt, ob eine Anwendung und eine Themen Zeichenfolge (&\# 0034; AppName \| TopicName&\# 0034;) verwendet die richtige Syntax.
ms.assetid: bcf5442b-452e-4b42-95e9-f09bf885be40
title: Nddeisvalidapptopiclist-Funktion (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidAppTopicList
- NDdeIsValidAppTopicListA
- NDdeIsValidAppTopicListW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: fb990830583f6684502438f132c1c98f5741a0ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362665"
---
# <a name="nddeisvalidapptopiclist-function"></a><span data-ttu-id="6a55f-103">Nddeisvalidapptopiclist-Funktion</span><span class="sxs-lookup"><span data-stu-id="6a55f-103">NDdeIsValidAppTopicList function</span></span>

<span data-ttu-id="6a55f-104">\[Network DDE wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6a55f-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="6a55f-105">Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]</span><span class="sxs-lookup"><span data-stu-id="6a55f-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="6a55f-106">Bestimmt, ob eine Anwendung und eine Themen Zeichenfolge ("*appname* \| *TopicName*") die richtige Syntax verwendet.</span><span class="sxs-lookup"><span data-stu-id="6a55f-106">Determines whether an application and topic string ("*AppName*\|*TopicName*") uses the proper syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a55f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a55f-107">Syntax</span></span>


```C++
BOOL NDdeIsValidAppTopicList(
  _In_ LPTSTR targetTopic
);
```



## <a name="parameters"></a><span data-ttu-id="6a55f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a55f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a55f-109">*targettopisch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a55f-109">*targetTopic* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a55f-110">Ein Zeiger auf die zu validierende Anwendungs-und Themen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6a55f-110">A pointer to the application and topic string to validate.</span></span> <span data-ttu-id="6a55f-111">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="6a55f-111">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a55f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a55f-112">Return value</span></span>

<span data-ttu-id="6a55f-113">Wenn der *targettopparameter* über eine gültige Syntax verfügt, ist der Rückgabewert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="6a55f-113">If the *targetTopic* parameter has valid syntax, the return value is nonzero.</span></span>

<span data-ttu-id="6a55f-114">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="6a55f-114">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a55f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a55f-115">Remarks</span></span>

<span data-ttu-id="6a55f-116">Diese Funktion wird auch von [**ndabshareadd**](nddeshareadd.md) aufgerufen, wenn Sie die DDE-Freigabe erstellt.</span><span class="sxs-lookup"><span data-stu-id="6a55f-116">This function is also called by [**NDdeShareAdd**](nddeshareadd.md) when it creates the DDE share.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a55f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a55f-117">Requirements</span></span>



| <span data-ttu-id="6a55f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a55f-118">Requirement</span></span> | <span data-ttu-id="6a55f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="6a55f-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a55f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6a55f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6a55f-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a55f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6a55f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6a55f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6a55f-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a55f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6a55f-124">Header</span><span class="sxs-lookup"><span data-stu-id="6a55f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a55f-125"><dt>Ndde API. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a55f-125"><dt>Nddeapi.h</dt></span></span> </dl>      |
| <span data-ttu-id="6a55f-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6a55f-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="6a55f-127"><dt>Ndde API. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a55f-127"><dt>Nddeapi.lib</dt></span></span> </dl>    |
| <span data-ttu-id="6a55f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6a55f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a55f-129"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a55f-129"><dt>Nddeapi.dll</dt></span></span> </dl>    |
| <span data-ttu-id="6a55f-130">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="6a55f-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6a55f-131">**Nddeisvalidapptopiclistw** (Unicode) und **nddeisvalidapptopiclista** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6a55f-131">**NDdeIsValidAppTopicListW** (Unicode) and **NDdeIsValidAppTopicListA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6a55f-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a55f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a55f-133">Übersicht über das Netzwerk dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="6a55f-133">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="6a55f-134">Network DDE-Funktionen</span><span class="sxs-lookup"><span data-stu-id="6a55f-134">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="6a55f-135">**Ndabshareadd**</span><span class="sxs-lookup"><span data-stu-id="6a55f-135">**NDdeShareAdd**</span></span>](nddeshareadd.md)
</dt> </dl>

 

 




