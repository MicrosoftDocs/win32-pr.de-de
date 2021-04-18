---
description: Die evaluatecondition-Methode des Session-Objekts wertet einen logischen Ausdruck aus, der Symbole und Werte enthält. Diese Methode verwendet die msievaluatecondition-Funktion.
ms.assetid: 629f7efd-80fe-4a0e-95cc-b62d6258ae0a
title: Session. evaluatecondition-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.EvaluateCondition
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6eb207d826b641e9295e4a3fa4fcda16e0b2769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361301"
---
# <a name="sessionevaluatecondition-method"></a><span data-ttu-id="10111-104">Session. evaluatecondition-Methode</span><span class="sxs-lookup"><span data-stu-id="10111-104">Session.EvaluateCondition method</span></span>

<span data-ttu-id="10111-105">Die **evaluatecondition** -Methode des [**Session**](session-object.md) -Objekts wertet einen logischen Ausdruck aus, der Symbole und Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="10111-105">The **EvaluateCondition** method of the [**Session**](session-object.md) object evaluates a logical expression that contains symbols and values.</span></span> <span data-ttu-id="10111-106">Diese Methode verwendet die [**msievaluatecondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="10111-106">This method uses the [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="10111-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="10111-107">Syntax</span></span>


```JScript
Session.EvaluateCondition(
  condition
)
```



## <a name="parameters"></a><span data-ttu-id="10111-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="10111-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10111-109">*condition*</span><span class="sxs-lookup"><span data-stu-id="10111-109">*condition*</span></span> 
</dt> <dd>

<span data-ttu-id="10111-110">Erforderliche Zeichenfolge, die den logischen Ausdruck enthält.</span><span class="sxs-lookup"><span data-stu-id="10111-110">Required string that contains the logical expression.</span></span> <span data-ttu-id="10111-111">Weitere Informationen finden Sie unter [bedingte Anweisungs Syntax](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="10111-111">For more information, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10111-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="10111-112">Return value</span></span>

<span data-ttu-id="10111-113">Diese Methode gibt eine ganze Zahl zurück, die die Auswertung der Bedingung angibt.</span><span class="sxs-lookup"><span data-stu-id="10111-113">This method returns an integer that indicates the evaluation of the condition.</span></span>



| <span data-ttu-id="10111-114">Konstante</span><span class="sxs-lookup"><span data-stu-id="10111-114">Constant</span></span>                  | <span data-ttu-id="10111-115">Wert</span><span class="sxs-lookup"><span data-stu-id="10111-115">Value</span></span> | <span data-ttu-id="10111-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10111-116">Description</span></span>                               |
|---------------------------|-------|-------------------------------------------|
| <span data-ttu-id="10111-117">msievaluateconditionfalse</span><span class="sxs-lookup"><span data-stu-id="10111-117">msiEvaluateConditionFalse</span></span> | <span data-ttu-id="10111-118">0</span><span class="sxs-lookup"><span data-stu-id="10111-118">0</span></span>     | <span data-ttu-id="10111-119">Die Bedingung wird zu false ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="10111-119">The condition evaluates to false.</span></span>         |
| <span data-ttu-id="10111-120">msievaluateconditiontrue</span><span class="sxs-lookup"><span data-stu-id="10111-120">msiEvaluateConditionTrue</span></span>  | <span data-ttu-id="10111-121">1</span><span class="sxs-lookup"><span data-stu-id="10111-121">1</span></span>     | <span data-ttu-id="10111-122">Die Bedingung wird als true ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="10111-122">The condition evaluates to true.</span></span>          |
| <span data-ttu-id="10111-123">msievaluateconditionnone</span><span class="sxs-lookup"><span data-stu-id="10111-123">msiEvaluateConditionNone</span></span>  | <span data-ttu-id="10111-124">2</span><span class="sxs-lookup"><span data-stu-id="10111-124">2</span></span>     | <span data-ttu-id="10111-125">Ein bedingter Ausdruck wurde nicht bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="10111-125">A conditional expression is not provided.</span></span> |
| <span data-ttu-id="10111-126">msievaluateconditionerror</span><span class="sxs-lookup"><span data-stu-id="10111-126">msiEvaluateConditionError</span></span> | <span data-ttu-id="10111-127">3</span><span class="sxs-lookup"><span data-stu-id="10111-127">3</span></span>     | <span data-ttu-id="10111-128">Die Bedingung enthält einen Syntax Fehler.</span><span class="sxs-lookup"><span data-stu-id="10111-128">The condition contains a syntax error.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="10111-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10111-129">Remarks</span></span>

<span data-ttu-id="10111-130">Bedingte Ausdrücke können zum Vergleichen von Funktions-und Komponenten Zuständen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10111-130">Conditional expressions can be used to compare feature and component states.</span></span> <span data-ttu-id="10111-131">In der folgenden Tabelle sind die Funktions-und Komponenten Zustände aufgeführt, die von der evaluatecondition-Methode verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10111-131">The following table shows the feature and component states that the EvaluateCondition method uses.</span></span>



| <span data-ttu-id="10111-132">State</span><span class="sxs-lookup"><span data-stu-id="10111-132">State</span></span>                 | <span data-ttu-id="10111-133">Wert</span><span class="sxs-lookup"><span data-stu-id="10111-133">Value</span></span> | <span data-ttu-id="10111-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10111-134">Description</span></span>                                              |
|-----------------------|-------|----------------------------------------------------------|
| <span data-ttu-id="10111-135">Null</span><span class="sxs-lookup"><span data-stu-id="10111-135">Null</span></span>                  | <span data-ttu-id="10111-136">Null</span><span class="sxs-lookup"><span data-stu-id="10111-136">Null</span></span>  | <span data-ttu-id="10111-137">Für das Feature oder die Komponente wurde keine Aktion ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="10111-137">No action taken on feature or component.</span></span>                 |
| <span data-ttu-id="10111-138">msiinstallstatemissing</span><span class="sxs-lookup"><span data-stu-id="10111-138">msiInstallStateAbsent</span></span> | <span data-ttu-id="10111-139">2</span><span class="sxs-lookup"><span data-stu-id="10111-139">2</span></span>     | <span data-ttu-id="10111-140">Die Funktion oder Komponente ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="10111-140">Feature or component is not present.</span></span>                     |
| <span data-ttu-id="10111-141">msiinstallstatuelocal</span><span class="sxs-lookup"><span data-stu-id="10111-141">msiInstallStateLocal</span></span>  | <span data-ttu-id="10111-142">3</span><span class="sxs-lookup"><span data-stu-id="10111-142">3</span></span>     | <span data-ttu-id="10111-143">Die Funktion oder Komponente ist auf dem lokalen Computer installiert.</span><span class="sxs-lookup"><span data-stu-id="10111-143">Feature or component is installed on the local computer.</span></span> |
| <span data-ttu-id="10111-144">msiinstallstaatource</span><span class="sxs-lookup"><span data-stu-id="10111-144">msiInstallStateSource</span></span> | <span data-ttu-id="10111-145">4</span><span class="sxs-lookup"><span data-stu-id="10111-145">4</span></span>     | <span data-ttu-id="10111-146">Die Funktion oder Komponente wird zum Ausführen von der Quelle installiert.</span><span class="sxs-lookup"><span data-stu-id="10111-146">Feature or component is installed to run from source.</span></span>    |



 

> [!Note]  
> <span data-ttu-id="10111-147">Die Zustände werden erst festgelegt, wenn die [**setinstalllevel**](session-setinstalllevel.md) -Methode entweder direkt oder durch die [costfinalize-Aktion](costfinalize-action.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="10111-147">The states are not set until the [**SetInstallLevel**](session-setinstalllevel.md) method is called, either directly or by the [CostFinalize Action](costfinalize-action.md).</span></span> <span data-ttu-id="10111-148">Daher ist die Zustands Überprüfung nur in bedingtem Ausdruck in einer Aktions Sequenz Tabelle sinnvoll.</span><span class="sxs-lookup"><span data-stu-id="10111-148">Therefore, state checking is only useful in conditional expression in an action sequence table.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="10111-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10111-149">Requirements</span></span>



| <span data-ttu-id="10111-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10111-150">Requirement</span></span> | <span data-ttu-id="10111-151">Wert</span><span class="sxs-lookup"><span data-stu-id="10111-151">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10111-152">Version</span><span class="sxs-lookup"><span data-stu-id="10111-152">Version</span></span><br/> | <span data-ttu-id="10111-153">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="10111-153">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="10111-154">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="10111-154">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="10111-155">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="10111-155">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="10111-156">DLL</span><span class="sxs-lookup"><span data-stu-id="10111-156">DLL</span></span><br/>     | <dl> <span data-ttu-id="10111-157"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10111-157"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="10111-158">IID</span><span class="sxs-lookup"><span data-stu-id="10111-158">IID</span></span><br/>     | <span data-ttu-id="10111-159">IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="10111-159">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="10111-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10111-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10111-161">Syntax der bedingten Anweisung</span><span class="sxs-lookup"><span data-stu-id="10111-161">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> </dl>

 

 




