---
description: Tritt auf, wenn sich die aktuelle Auswahl von Text im InkEdit-Steuerelement geändert hat oder die Einfügemarke verschoben wurde.
ms.assetid: 14ddffe7-bdfe-4a35-82c7-b3401b5b720c
title: InkEdit. selChange-Ereignis (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b51ef4edbf7d7fb02be17dc416c0a777a9519a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349315"
---
# <a name="inkeditselchange-event"></a><span data-ttu-id="8cee6-103">InkEdit. selChange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="8cee6-103">InkEdit.SelChange event</span></span>

<span data-ttu-id="8cee6-104">Tritt auf, wenn sich die aktuelle Auswahl von Text im [InkEdit](inkedit-control-reference.md) -Steuerelement geändert hat oder die Einfügemarke verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="8cee6-104">Occurs when the current selection of text in the [InkEdit](inkedit-control-reference.md) control has changed or the insertion point has moved.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cee6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cee6-105">Syntax</span></span>


```C++
void SelChange();
```



## <a name="parameters"></a><span data-ttu-id="8cee6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cee6-106">Parameters</span></span>

<span data-ttu-id="8cee6-107">Dieses Ereignis weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="8cee6-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8cee6-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8cee6-108">Return value</span></span>

<span data-ttu-id="8cee6-109">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8cee6-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cee6-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8cee6-110">Remarks</span></span>

<span data-ttu-id="8cee6-111">Sie können das **selChange** -Ereignis verwenden, um die verschiedenen Eigenschaften zu überprüfen, die Informationen über die aktuelle Auswahl (z. [**b. SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)) geben, damit Sie z. b. Schaltflächen in einer Symbolleiste aktualisieren können.</span><span class="sxs-lookup"><span data-stu-id="8cee6-111">You can use the **SelChange** event to check the various properties that give information about the current selection (such as [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)) so you can update buttons in a toolbar, for example.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cee6-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8cee6-112">Requirements</span></span>



| <span data-ttu-id="8cee6-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8cee6-113">Requirement</span></span> | <span data-ttu-id="8cee6-114">Wert</span><span class="sxs-lookup"><span data-stu-id="8cee6-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cee6-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8cee6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8cee6-116">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8cee6-116">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8cee6-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8cee6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8cee6-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8cee6-118">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8cee6-119">Header</span><span class="sxs-lookup"><span data-stu-id="8cee6-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cee6-120"><dt>In "-. h" (auch als "gezeichneten \_ i. c" erforderlich)</dt></span><span class="sxs-lookup"><span data-stu-id="8cee6-120"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8cee6-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8cee6-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="8cee6-122"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cee6-122"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8cee6-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cee6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cee6-124">InkEdit</span><span class="sxs-lookup"><span data-stu-id="8cee6-124">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 




