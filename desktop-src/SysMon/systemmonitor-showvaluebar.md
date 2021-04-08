---
title: Systemmonitor. showvaluebar (Eigenschaft)
description: Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob der Wert Balken (der Satz von statistischen Werten unterhalb des Diagramms) auf dem Steuerelement angezeigt wird.
ms.assetid: 320fbbbb-c4ea-4772-9b10-1e123849c255
keywords:
- Showvaluebar-Eigenschaft (Sysmon)
- Showvaluebar-Eigenschaft (Sysmon), Systemmonitor-Klasse
- Systemmonitor-Klasse sysmon, showvaluebar (Eigenschaft)
topic_type:
- apiref
api_name:
- SystemMonitor.ShowValueBar
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f393b36162fae6aed996d2afaccd4749f22598f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740624"
---
# <a name="systemmonitorshowvaluebar-property"></a><span data-ttu-id="c9184-106">Systemmonitor. showvaluebar (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c9184-106">SystemMonitor.ShowValueBar property</span></span>

<span data-ttu-id="c9184-107">Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob der Wert Balken (der Satz von statistischen Werten unterhalb des Diagramms) auf dem Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c9184-107">Retrieves or sets a value that determines whether the value bar (the set of statistical values below the graph) is displayed on the control.</span></span>

<span data-ttu-id="c9184-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c9184-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9184-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9184-109">Syntax</span></span>


```VB
Property ShowValueBar As Boolean
```



## <a name="property-value"></a><span data-ttu-id="c9184-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c9184-110">Property value</span></span>

<span data-ttu-id="c9184-111">True gibt an, dass die Wert Leiste auf dem Steuerelement angezeigt wird. andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="c9184-111">True indicates that the value bar is displayed on the control; otherwise false.</span></span> <span data-ttu-id="c9184-112">Der Standardwert dieser Eigenschaft ist „TRUE“.</span><span class="sxs-lookup"><span data-stu-id="c9184-112">The default value for this property is true.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9184-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9184-113">Remarks</span></span>

<span data-ttu-id="c9184-114">Die angezeigten Statistiken enthalten den letzten Wert, den Durchschnittswert und die Mindest-und Höchstwerte des aktuell ausgewählten Zählers für das angezeigte Zeitintervall.</span><span class="sxs-lookup"><span data-stu-id="c9184-114">The displayed statistics include the last value, the average value, and the minimum and maximum values of the currently selected counter over the displayed time interval.</span></span> <span data-ttu-id="c9184-115">Um die anzuzeigenden Werte für den anzuzeigenden Wert auszuwählen, muss der Benutzer den-Wert im Legenden Bereich des-Steuer Elements auswählen.</span><span class="sxs-lookup"><span data-stu-id="c9184-115">To select the counter values to display, the user must select the counter in the Legend pane of the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9184-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9184-116">Requirements</span></span>



| <span data-ttu-id="c9184-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9184-117">Requirement</span></span> | <span data-ttu-id="c9184-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c9184-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9184-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9184-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c9184-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9184-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c9184-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c9184-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c9184-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9184-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c9184-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c9184-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9184-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="c9184-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9184-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9184-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9184-126">**System Monitor**</span><span class="sxs-lookup"><span data-stu-id="c9184-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





