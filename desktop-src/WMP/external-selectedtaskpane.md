---
title: Extern. selectedtaskpane
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die selectedtaskpane-Eigenschaft gibt den aktuell ausgewählten Aufgabenbereich an oder ruft ihn ab.
ms.assetid: af7b4627-1336-444c-9b4e-5f2e07d9eea7
keywords:
- Externe. selectedtaskpane-Fenster Media Player
topic_type:
- apiref
api_name:
- External.SelectedTaskPane
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28535e0497362a2153bcaad439425174e9c1bdc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355274"
---
# <a name="externalselectedtaskpane"></a><span data-ttu-id="942b6-106">Extern. selectedtaskpane</span><span class="sxs-lookup"><span data-stu-id="942b6-106">External.SelectedTaskPane</span></span>

> [!Note]  
> <span data-ttu-id="942b6-107">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="942b6-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="942b6-108">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="942b6-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="942b6-109">Die **selectedtaskpane** -Eigenschaft gibt den aktuell ausgewählten Aufgabenbereich an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="942b6-109">The **SelectedTaskPane** property specifies or retrieves the currently selected task pane.</span></span>

## <a name="syntax"></a><span data-ttu-id="942b6-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="942b6-110">Syntax</span></span>

<span data-ttu-id="942b6-111">Window. extern. selectedtaskpane = *Servicetask*</span><span class="sxs-lookup"><span data-stu-id="942b6-111">window.external.SelectedTaskPane = *servicetask*</span></span>

## <a name="possible-values"></a><span data-ttu-id="942b6-112">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="942b6-112">Possible Values</span></span>

<span data-ttu-id="942b6-113">Diese Eigenschaft ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="942b6-113">This property is a read/write **String**.</span></span> <span data-ttu-id="942b6-114">Mögliche Werte sind "ServiceTask1", "ServiceTask2" und "ServiceTask3".</span><span class="sxs-lookup"><span data-stu-id="942b6-114">Possible values are "ServiceTask1", "ServiceTask2", and "ServiceTask3".</span></span>

## <a name="remarks"></a><span data-ttu-id="942b6-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="942b6-115">Remarks</span></span>

<span data-ttu-id="942b6-116">Wenn Sie einen Wert für diese Eigenschaft angeben, wird die Schaltfläche für diesen Bereich hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="942b6-116">Specifying a value for this property highlights the button for that pane.</span></span> <span data-ttu-id="942b6-117">Der angegebene Aufgabenbereich wird nicht aktiv.</span><span class="sxs-lookup"><span data-stu-id="942b6-117">It does not make the specified task pane active.</span></span> <span data-ttu-id="942b6-118">Geben Sie einen Wert für diese Eigenschaft an, um die aktuelle Aufgabenbereichs Schaltfläche für die Webseite festzulegen, wenn die Seite geladen wird, um sicherzustellen, dass die Schaltfläche korrekter Aufgabenbereich aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="942b6-118">You should specify a value for this property to set the current task pane button for your webpage when the page loads to ensure that the correct task pane button is active.</span></span>

<span data-ttu-id="942b6-119">Um einen bestimmten Aufgabenbereich als aktiven Bereich festzulegen, verwenden Sie die **navigatetaskpaneurl** -Methode.</span><span class="sxs-lookup"><span data-stu-id="942b6-119">To make a particular task pane the active one, use the **NavigateTaskPaneURL** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="942b6-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="942b6-120">Requirements</span></span>



| <span data-ttu-id="942b6-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="942b6-121">Requirement</span></span> | <span data-ttu-id="942b6-122">Wert</span><span class="sxs-lookup"><span data-stu-id="942b6-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="942b6-123">Version</span><span class="sxs-lookup"><span data-stu-id="942b6-123">Version</span></span><br/> | <span data-ttu-id="942b6-124">Windows Media Player 10 oder höher</span><span class="sxs-lookup"><span data-stu-id="942b6-124">Windows Media Player 10 or later</span></span><br/>                                        |
| <span data-ttu-id="942b6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="942b6-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="942b6-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="942b6-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="942b6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="942b6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="942b6-128">**Externes Objekt für den Typ 2-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="942b6-128">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="942b6-129">**Extern. navigatetaskpaneurl**</span><span class="sxs-lookup"><span data-stu-id="942b6-129">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> </dl>

 

 





