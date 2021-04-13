---
title: EN_ENDCOMPOSITION Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass der Benutzer neue Daten eingegeben hat oder die Eingabe von Daten während der Verwendung von IME oder Text Services Framework abgeschlossen hat.
ms.assetid: 3956313F-F82F-41A2-AEDA-52E63218977C
keywords:
- Windows-Steuerelemente für EN_ENDCOMPOSITION Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_ENDCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df1c2b5d08b2da73c67edeb6fe7ca4ac639000c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475390"
---
# <a name="en_endcomposition-notification-code"></a><span data-ttu-id="fd5af-104">EN \_ endcomposition-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="fd5af-104">EN\_ENDCOMPOSITION notification code</span></span>

<span data-ttu-id="fd5af-105">Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass der Benutzer neue Daten eingegeben hat oder die Eingabe von Daten während der Verwendung von IME oder [Text Services Framework](/windows/desktop/TSF/text-services-framework)abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="fd5af-105">Notifies a rich edit control parent window that the user has entered new data or has finished entering data while using IME or [Text Services Framework](/windows/desktop/TSF/text-services-framework).</span></span>


```C++
EN_ENDCOMPOSITION

     pEndComp = (ENDCOMPOSITIONNOTIFY *)lParam;
```



## <a name="parameters"></a><span data-ttu-id="fd5af-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd5af-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd5af-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fd5af-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd5af-108">Eine [**endcompositionnotify**](/windows/win32/api/richedit/ns-richedit-endcompositionnotify) -Struktur, die Informationen über die End-Kompositions Bedingung empfängt.</span><span class="sxs-lookup"><span data-stu-id="fd5af-108">A [**ENDCOMPOSITIONNOTIFY**](/windows/win32/api/richedit/ns-richedit-endcompositionnotify) structure that receives information about the end composition condition.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd5af-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd5af-109">Requirements</span></span>



| <span data-ttu-id="fd5af-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd5af-110">Requirement</span></span> | <span data-ttu-id="fd5af-111">Wert</span><span class="sxs-lookup"><span data-stu-id="fd5af-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd5af-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd5af-112">Minimum supported client</span></span><br/> | <span data-ttu-id="fd5af-113">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd5af-113">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="fd5af-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd5af-114">Minimum supported server</span></span><br/> | <span data-ttu-id="fd5af-115">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd5af-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fd5af-116">Header</span><span class="sxs-lookup"><span data-stu-id="fd5af-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd5af-117"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd5af-117"><dt>Richedit.h</dt></span></span> </dl> |



 

