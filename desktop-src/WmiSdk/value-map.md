---
description: Eine Werte Zuordnung ist ein Array, das mit einer Eigenschaft mit dem Wert und den ValueMap-Qualifizierern verknüpft ist.
ms.assetid: 7667e87f-b997-4fd9-81ea-b27c9d2a9335
ms.tgt_platform: multiple
title: ValueMap-und Wert Qualifizierer
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df85342df9543e4d62b04482785ec31bb5bd3982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356297"
---
# <a name="valuemap-and-value-qualifiers"></a><span data-ttu-id="22d48-103">ValueMap-und Wert Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="22d48-103">ValueMap and Value Qualifiers</span></span>

<span data-ttu-id="22d48-104">Eine Werte Zuordnung ist ein Array, das mit einer Eigenschaft mit dem **Wert** und den **ValueMap** -Qualifizierern verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="22d48-104">A value map is an array linked to a property with the **Value** and **ValueMap** qualifiers.</span></span>

<span data-ttu-id="22d48-105">Die-Eigenschaft fungiert als Index für das Array, das einen Wert enthält, der einen der Werte im Array darstellt.</span><span class="sxs-lookup"><span data-stu-id="22d48-105">The property acts as an index into the array, holding a value that represents one of the values in the array.</span></span> <span data-ttu-id="22d48-106">Mithilfe von MOF-Code können Sie über die folgenden Typen von Wert Maps verfügen:</span><span class="sxs-lookup"><span data-stu-id="22d48-106">Using MOF code, you can have the following types of value maps:</span></span>

-   <span data-ttu-id="22d48-107">Array Zuordnung zu einer Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="22d48-107">Array mapping to an integer.</span></span>

    <span data-ttu-id="22d48-108">Sie können ein Array mit dem **Wert** Qualifizierer definieren und das Array direkt mit einer ganzzahligen Eigenschaft verknüpfen, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="22d48-108">You can define an array with the **Value** qualifier and link the array directly to an integer property, as shown in the following example:</span></span>

    ``` syntax
    [Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    <span data-ttu-id="22d48-109">In diesem Beispiel ist der **Status** -Eigenschafts Wert ein Index in das durch den **Wert** definierte Zeichen folgen Array.</span><span class="sxs-lookup"><span data-stu-id="22d48-109">In this example, the **Status** property value is an index into the string array defined by **Value**.</span></span> <span data-ttu-id="22d48-110">Die-Eigenschaft kann nur Werte verwenden, die den Ordinalpositionen im **Wert** Array minus 1 entsprechen.</span><span class="sxs-lookup"><span data-stu-id="22d48-110">The property can only take on values that correspond to the ordinal positions in the **Value** array minus 1.</span></span> <span data-ttu-id="22d48-111">Wenn Sie z. b. **Status** auf "1" festlegen, wird der Wert "Error" (Fehler) zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="22d48-111">For example, setting **Status** to "1" maps to the "Error" value.</span></span> <span data-ttu-id="22d48-112">Die Index-Eigenschaft kann nur Werte annehmen, die den Positionen im **Wert** Array entsprechen.</span><span class="sxs-lookup"><span data-stu-id="22d48-112">The index property can take only values that correspond to positions in the **Value** array.</span></span> <span data-ttu-id="22d48-113">Wenn das Array z. b. 10 Einträge enthält, kann die Index-Eigenschaft die Story 0 bis 9, nicht 30 oder 177.</span><span class="sxs-lookup"><span data-stu-id="22d48-113">For example, if the array has 10 entries, the index property can story 0 through 9, not 30 or 177.</span></span>

-   <span data-ttu-id="22d48-114">Array Zuordnung zu einem anderen Array, das einer Ganzzahl entspricht.</span><span class="sxs-lookup"><span data-stu-id="22d48-114">Array mapping to another array mapping to an integer.</span></span>

    <span data-ttu-id="22d48-115">Wenn Sie einen Index erstellen möchten, der kein ordinales System der Zählung verwendet, verwenden Sie den **ValueMap** -Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="22d48-115">If you wish to create an index that does not use an ordinal system of counting, use the **ValueMap** qualifier.</span></span> <span data-ttu-id="22d48-116">Der **ValueMap** -Qualifizierer richtet ein anderes Array ein, das ein beliebiges Index Nummerierungssystem enthält, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="22d48-116">The **ValueMap** qualifier sets up another array that holds an arbitrary index numbering system, as shown in the following example:</span></span>

    ``` syntax
    [ValueMap {"1", "3", "99", "0"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    <span data-ttu-id="22d48-117">Obwohl Sie die Werte von **ValueMap** in Anführungszeichen platzieren müssen, berücksichtigt WMI die Werte Ganzzahlen.</span><span class="sxs-lookup"><span data-stu-id="22d48-117">Although you must place the values of **ValueMap** in quotations, WMI considers the values integers.</span></span> <span data-ttu-id="22d48-118">Daher können Sie in diesem Beispiel die Eigenschaft **Status** auf eine Ganzzahl im **ValueMap** -Satz festlegen: 1, 3, 99 oder 0.</span><span class="sxs-lookup"><span data-stu-id="22d48-118">Therefore, In this example you can set the **Status** property to an integer in the **ValueMap** set: 1, 3, 99, or 0.</span></span> <span data-ttu-id="22d48-119">WMI ordnet jede Ganzzahl von einer Ordinalposition im **ValueMap** -Zeichen folgen Array einer entsprechenden Position im **Werte** Array zu.</span><span class="sxs-lookup"><span data-stu-id="22d48-119">WMI maps each integer from an ordinal position in the **ValueMap** string array to a corresponding position in the **Value** array.</span></span> <span data-ttu-id="22d48-120">Wenn Sie z. b. **Status** auf 0 festlegen, wird "unbekannt" zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="22d48-120">For example, setting **Status** to 0 maps to "Unknown".</span></span>

-   <span data-ttu-id="22d48-121">Array Zuordnung zu einer anderen Array Zuordnung zu einer Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="22d48-121">Array mapping to another array mapping to a string.</span></span>

    <span data-ttu-id="22d48-122">Wenn Sie keine Ganzzahl zum Indizieren Ihres Arrays verwenden möchten, können Sie stattdessen eine Zeichenfolge verwenden, um einen der möglichen Werte in Ihrem Array zu speichern.</span><span class="sxs-lookup"><span data-stu-id="22d48-122">If you do not want to use an integer to index your array, you can instead use a string to hold one of the possible values in your array.</span></span> <span data-ttu-id="22d48-123">Zu diesem Zweck müssen Sie sowohl ein **value** -als auch ein **ValueMap** -Array definieren, das beide Zeichen folgen enthält, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="22d48-123">To do so, you must define both a **Value** and **ValueMap** array that both contain strings, as shown in the following example:</span></span>

    ``` syntax
    [ValueMap {"OK", "Error", "Degraded", "Unknown"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    string Status;
    ```

    <span data-ttu-id="22d48-124">Bei einer Zeichen folgen Eigenschaft sind die tatsächlichen zulässigen Werte der Eigenschaft die Einträge im **ValueMap** -Array.</span><span class="sxs-lookup"><span data-stu-id="22d48-124">With a string property, the actual allowable values of the property are the entries in the **ValueMap** array.</span></span> <span data-ttu-id="22d48-125">Beispielsweise können Sie den **Status** auf "OK" oder "unbekannt" festlegen.</span><span class="sxs-lookup"><span data-stu-id="22d48-125">For example, you can set **Status** to "OK" or "Unknown".</span></span>

<span data-ttu-id="22d48-126">Es liegt in der Anwendung, die Zuordnungen auf nützliche Weise zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="22d48-126">It is up to the application to take advantage of mappings in a useful way.</span></span> <span data-ttu-id="22d48-127">Der Anbieter muss einen gültigen Wertebereich erzwingen.</span><span class="sxs-lookup"><span data-stu-id="22d48-127">It is up to the provider to enforce a legal range of values.</span></span>

## <a name="remarks"></a><span data-ttu-id="22d48-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22d48-128">Remarks</span></span>

<span data-ttu-id="22d48-129">Wenn Sie entscheiden, ob Sie den **ValueMap**- / **Wert** oder **Bitmap**- / **BitValues** -Qualifizierer verwenden möchten, stellen Sie fest, ob einer der aufgeführten Werte gleichzeitig auftreten könnte.</span><span class="sxs-lookup"><span data-stu-id="22d48-129">In deciding whether to use the **ValueMap**/**Value** or **BitMap**/**BitValues** qualifiers, determine whether any of the values being indicated could occur concurrently.</span></span> <span data-ttu-id="22d48-130">Wenn mehrere gleichzeitige Werte vorhanden sein können, müssen **Bitmap**- / **Bitwerte** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22d48-130">If multiple concurrent values can exist, you must use **BitMap**/**BitValues**.</span></span> <span data-ttu-id="22d48-131">Wenn sich alle Werte gegenseitig ausschließen, sollten Sie die **ValueMap**- / **Wert** Qualifizierer verwenden.</span><span class="sxs-lookup"><span data-stu-id="22d48-131">If all the values are mutually exclusive, you should use the **ValueMap**/**Value** qualifiers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22d48-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="22d48-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22d48-133">Bitmap und BitValues</span><span class="sxs-lookup"><span data-stu-id="22d48-133">BitMap and BitValues</span></span>](bitmap-and-bitvalues.md)
</dt> </dl>

 

 



