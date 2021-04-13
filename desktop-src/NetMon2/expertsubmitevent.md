---
description: Die Funktion "ExpertSubmitEvent" gibt an, dass eine Ereignis Bedingung vorhanden ist, und stellt eine Datenstruktur bereit, die die Bedingung beschreibt.
ms.assetid: 2339b530-427b-4028-aef6-c2cdd1353f77
title: ExpertSubmitEvent-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertSubmitEvent
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 448d77e9cb009b8aced0aba752526dc08b503066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342759"
---
# <a name="expertsubmitevent-function"></a><span data-ttu-id="f2bca-103">ExpertSubmitEvent-Funktion</span><span class="sxs-lookup"><span data-stu-id="f2bca-103">ExpertSubmitEvent function</span></span>

<span data-ttu-id="f2bca-104">Die Funktion " **ExpertSubmitEvent** " gibt an, dass eine Ereignis Bedingung vorhanden ist, und stellt eine Datenstruktur bereit, die die Bedingung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="f2bca-104">The **ExpertSubmitEvent** function indicates that an event condition exists and provides a data structure that describes the condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2bca-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2bca-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertSubmitEvent(
  _In_ HEXPERTKEY   hExpertKey,
  _In_ PNMEVENTDATA pExpertEvent
);
```



## <a name="parameters"></a><span data-ttu-id="f2bca-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2bca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2bca-107">*hexpertkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2bca-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2bca-108">Eindeutiger Bezeichner des Experten.</span><span class="sxs-lookup"><span data-stu-id="f2bca-108">Unique identifier of the expert.</span></span> <span data-ttu-id="f2bca-109">Netzwerkmonitor übergibt *hexpertkey* an den Experten, wenn die Funktion [Run](run.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f2bca-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="f2bca-110">*pexpertevent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2bca-110">*pExpertEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2bca-111">Ein Zeiger auf eine **nmeventdata** -Struktur, die die Ereignis Bedingung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="f2bca-111">A pointer to an **NMEVENTDATA** structure that describes the event condition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2bca-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2bca-112">Return value</span></span>

<span data-ttu-id="f2bca-113">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="f2bca-113">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="f2bca-114">Wenn die Funktion nicht erfolgreich ist, gibt der Rückgabewert den Grund für den Fehler an.</span><span class="sxs-lookup"><span data-stu-id="f2bca-114">If the function is unsuccessful, the return value indicates the reason for the failure.</span></span> <span data-ttu-id="f2bca-115">Wenn der Rückgabewert nmerr- \_ Experte \_ beendet ist, bereinigt der Experte sofort und gibt ihn zurück.</span><span class="sxs-lookup"><span data-stu-id="f2bca-115">If the return value is NMERR\_EXPERT\_TERMINATE, the expert immediately cleans up and returns.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2bca-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2bca-116">Requirements</span></span>



| <span data-ttu-id="f2bca-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2bca-117">Requirement</span></span> | <span data-ttu-id="f2bca-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f2bca-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f2bca-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f2bca-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f2bca-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f2bca-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f2bca-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f2bca-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f2bca-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f2bca-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f2bca-123">Header</span><span class="sxs-lookup"><span data-stu-id="f2bca-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2bca-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2bca-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f2bca-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f2bca-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="f2bca-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2bca-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f2bca-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f2bca-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2bca-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2bca-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




