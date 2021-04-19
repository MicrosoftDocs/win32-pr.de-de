---
title: Extern. navigatetaskpaneurl-Methode
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Extern. navigatetaskpaneurl-Methode
ms.assetid: c3a888c0-6589-4d21-9d47-37372d9069f4
keywords:
- Navigatetaskpaneurl-Methode, Windows Media Player
- Navigatetaskpaneurl-Methode, Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, navigatetaskpaneurl-Methode
topic_type:
- apiref
api_name:
- External.NavigateTaskPaneURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e70558c7616738f67d9dc1d6d29eca15e5c30d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371978"
---
# <a name="externalnavigatetaskpaneurl-method"></a><span data-ttu-id="64479-107">Extern. navigatetaskpaneurl-Methode</span><span class="sxs-lookup"><span data-stu-id="64479-107">External.NavigateTaskPaneURL method</span></span>

> [!Note]  
> <span data-ttu-id="64479-108">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="64479-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="64479-109">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="64479-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="64479-110">Die **navigatetaskpaneurl** -Methode öffnet eine Webseite im angegebenen Aufgabenbereich und ändert den Fokus auf den angegebenen Bereich.</span><span class="sxs-lookup"><span data-stu-id="64479-110">The **NavigateTaskPaneURL** method opens a webpage in the specified task pane, and changes focus to the specified pane.</span></span>

## <a name="syntax"></a><span data-ttu-id="64479-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="64479-111">Syntax</span></span>


```JScript
External.NavigateTaskPaneURL(
  bstrKeyName,
  bstrTaskPane,
  bstrParams
)
```



## <a name="parameters"></a><span data-ttu-id="64479-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="64479-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64479-113">*btrekeyname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64479-113">*bstrKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64479-114">**Zeichenfolge** , die den Schlüsselnamen für den Online Store enthält.</span><span class="sxs-lookup"><span data-stu-id="64479-114">**String** containing the key name for the online store.</span></span> <span data-ttu-id="64479-115">(erforderlich)</span><span class="sxs-lookup"><span data-stu-id="64479-115">(required)</span></span>

</dd> <dt>

<span data-ttu-id="64479-116">*bstrautaskpane* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64479-116">*bstrTaskPane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64479-117">**Zeichenfolge** , die den Namen des Aufgabenbereichs enthält, in dem die Webseite geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="64479-117">**String** containing the name of the task pane in which the webpage opens.</span></span> <span data-ttu-id="64479-118">(erforderlich)</span><span class="sxs-lookup"><span data-stu-id="64479-118">(required)</span></span>

</dd> <dt>

<span data-ttu-id="64479-119">*bstrinbiams* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64479-119">*bstrParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64479-120">Eine **Zeichenfolge** , die die Abfrage Zeichenfolgen-Parameter enthält, die an die URL angefügt werden sollen, die vom **Navigate** -Element des servicinput</span><span class="sxs-lookup"><span data-stu-id="64479-120">**String** containing the query string parameters to append to the URL specified by the **Navigate** element of the ServiceInfo document.</span></span> <span data-ttu-id="64479-121">(Optional)</span><span class="sxs-lookup"><span data-stu-id="64479-121">(optional)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64479-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64479-122">Return value</span></span>

<span data-ttu-id="64479-123">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="64479-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="64479-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64479-124">Remarks</span></span>

<span data-ttu-id="64479-125">Wenn Sie zu einem Bereich navigieren, den der Online Shop nicht unterstützt, kann sich der aktuelle Online Shop ändern.</span><span class="sxs-lookup"><span data-stu-id="64479-125">Navigating to a pane that your online store does not support may cause the current online store to change.</span></span>

<span data-ttu-id="64479-126">Der für *bstrinparameams* angegebene Wert ist nur gültig, wenn **navigatetaskpaneurl** von Webseiten aufgerufen wird, die vom Online Store bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="64479-126">The value specified for *bstrParams* is valid only when **NavigateTaskPaneURL** is called from webpages provided by the online store.</span></span>

<span data-ttu-id="64479-127">In der folgenden Tabelle sind gültige Werte für *bstrautaskpane* und der zugehörige Aufgabenbereich für jeden aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="64479-127">The following table lists of valid values for *bstrTaskPane* and the associated task pane for each.</span></span>



| <span data-ttu-id="64479-128">Wert</span><span class="sxs-lookup"><span data-stu-id="64479-128">Value</span></span>            | <span data-ttu-id="64479-129">Aufgabenbereich</span><span class="sxs-lookup"><span data-stu-id="64479-129">Task Pane</span></span>                      |
|------------------|--------------------------------|
| <span data-ttu-id="64479-130">**ServiceTask1**</span><span class="sxs-lookup"><span data-stu-id="64479-130">**ServiceTask1**</span></span> | <span data-ttu-id="64479-131">Der erste Aufgabenbereich für den Online Shop.</span><span class="sxs-lookup"><span data-stu-id="64479-131">First online store task pane.</span></span>  |
| <span data-ttu-id="64479-132">**ServiceTask2**</span><span class="sxs-lookup"><span data-stu-id="64479-132">**ServiceTask2**</span></span> | <span data-ttu-id="64479-133">Zweiter Online Store-Aufgabenbereich.</span><span class="sxs-lookup"><span data-stu-id="64479-133">Second online store task pane.</span></span> |
| <span data-ttu-id="64479-134">**ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="64479-134">**ServiceTask3**</span></span> | <span data-ttu-id="64479-135">Dritter Aufgabenbereich für den Online Shop.</span><span class="sxs-lookup"><span data-stu-id="64479-135">Third online store task pane.</span></span>  |



 

<span data-ttu-id="64479-136">Der Webseiten Code sollte beim Laden einen Wert für " [extern. selectedtaskpane](external-selectedtaskpane.md) " angeben, um sicherzustellen, dass die richtige Aufgabenbereichs Schaltfläche nach Abschluss der Navigation hervorgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="64479-136">Your webpage code should specify a value for [External.SelectedTaskPane](external-selectedtaskpane.md) when loading to ensure that the correct task pane button is highlighted after navigation is completed.</span></span>

## <a name="examples"></a><span data-ttu-id="64479-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64479-137">Examples</span></span>

<span data-ttu-id="64479-138">Der folgende Beispielcode zeigt, wie **navigatetaskpaneurl** die URL der Webseite erstellt, die für **ServiceTask1** angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="64479-138">The following example code shows how **NavigateTaskPaneURL** creates the URL of the webpage to display for **ServiceTask1**.</span></span>

<span data-ttu-id="64479-139">Beispiel für das **Navigate** -Element:</span><span class="sxs-lookup"><span data-stu-id="64479-139">Example of the **Navigate** element:</span></span>


```XML
<Navigate
    BaseURL = "https://www.proseware.com/online store/html/navigate.asp">
</Navigate>
```



<span data-ttu-id="64479-140">Beispiel für einen aufzurufenden Befehl der **navigatetaskpaneurl** -Methode:</span><span class="sxs-lookup"><span data-stu-id="64479-140">Example call to the **NavigateTaskPaneURL** method:</span></span>


```XML
external.NavigateTaskPaneURL("Proseware", "ServiceTask1", "Pane=Store");
```



<span data-ttu-id="64479-141">Beispiel für eine resultierende URL, die für die in **ServiceTask1** angezeigte Webseite verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="64479-141">Example of resulting URL used for the webpage displayed in **ServiceTask1**:</span></span>


```XML
https://www.proseware.com/online store/html/navigate.asp?Pane=Store
```



## <a name="requirements"></a><span data-ttu-id="64479-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64479-142">Requirements</span></span>



| <span data-ttu-id="64479-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64479-143">Requirement</span></span> | <span data-ttu-id="64479-144">Wert</span><span class="sxs-lookup"><span data-stu-id="64479-144">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="64479-145">Version</span><span class="sxs-lookup"><span data-stu-id="64479-145">Version</span></span><br/> | <span data-ttu-id="64479-146">Windows Media Player 10 oder höher</span><span class="sxs-lookup"><span data-stu-id="64479-146">Windows Media Player 10 or later</span></span><br/>                                        |
| <span data-ttu-id="64479-147">DLL</span><span class="sxs-lookup"><span data-stu-id="64479-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="64479-148"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64479-148"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64479-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64479-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64479-150">**Externes Objekt für den Typ 2-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="64479-150">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="64479-151">**Extern. selectedtaskpane**</span><span class="sxs-lookup"><span data-stu-id="64479-151">**External.SelectedTaskPane**</span></span>](external-selectedtaskpane.md)
</dt> </dl>

 

 





