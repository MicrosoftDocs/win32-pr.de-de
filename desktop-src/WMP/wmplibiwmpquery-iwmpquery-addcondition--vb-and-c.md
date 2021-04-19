---
title: Iwmpquery-addcondition-Methode
description: Die addcondition-Methode fügt der Verbund Abfrage mithilfe der-und der-Logik eine Bedingung hinzu.
ms.assetid: 4594ee6f-b153-4d53-b3ee-cd1718a4d5dc
keywords:
- addcondition-Methode (Windows Media Player)
- addcondition-Methode, Windows Media Player, iwmpquery-Schnittstelle
- Iwmpquery Interface, Windows Media Player, addcondition-Methode
topic_type:
- apiref
api_name:
- IWMPQuery.addCondition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9de3015ef0389fef82934cbd8e9326b6f9ec2307
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352030"
---
# <a name="iwmpqueryaddcondition-method"></a><span data-ttu-id="2ba72-106">Iwmpquery:: addcondition-Methode</span><span class="sxs-lookup"><span data-stu-id="2ba72-106">IWMPQuery::addCondition method</span></span>

<span data-ttu-id="2ba72-107">Die **addcondition** -Methode fügt der Verbund Abfrage mithilfe der **-und der-** Logik eine Bedingung hinzu.</span><span class="sxs-lookup"><span data-stu-id="2ba72-107">The **addCondition** method adds a condition to the compound query using **AND** logic.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ba72-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ba72-108">Syntax</span></span>


```CSharp
public void addCondition(
  System.String bstrAttribute,
  System.String bstrOperator,
  System.String bstrValue
);
```


```VB

Public Sub addCondition( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrOperator As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPQuery.addCondition
```





## <a name="parameters"></a><span data-ttu-id="2ba72-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ba72-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ba72-110">*bstrattribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ba72-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ba72-111">Ein **System. String** -Wert, der der Name des Attributs ist, das der Abfrage hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2ba72-111">A **System.String** that is the name of the attribute to be added to the query.</span></span>

</dd> <dt>

<span data-ttu-id="2ba72-112">*bstroperator* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ba72-112">*bstrOperator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ba72-113">Ein **System. String** -Operator, der der-Operator ist.</span><span class="sxs-lookup"><span data-stu-id="2ba72-113">A **System.String** that is the operator.</span></span> <span data-ttu-id="2ba72-114">Siehe Hinweise zu unterstützten Werten.</span><span class="sxs-lookup"><span data-stu-id="2ba72-114">See Remarks for supported values.</span></span>

</dd> <dt>

<span data-ttu-id="2ba72-115">*bstrauvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ba72-115">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ba72-116">Ein **System. String** -Wert, der der Attribut Wert ist.</span><span class="sxs-lookup"><span data-stu-id="2ba72-116">A **System.String** that is the attribute value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ba72-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ba72-117">Return value</span></span>

<span data-ttu-id="2ba72-118">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2ba72-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ba72-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ba72-119">Remarks</span></span>

<span data-ttu-id="2ba72-120">In einer Verbund Abfrage enthaltene Bedingungen werden in Bedingungs Gruppen organisiert.</span><span class="sxs-lookup"><span data-stu-id="2ba72-120">Conditions contained in a compound query are organized into condition groups.</span></span> <span data-ttu-id="2ba72-121">Mehrere Bedingungen innerhalb einer Bedingungs Gruppe werden immer mithilfe der **-und der-** Logik verkettet.</span><span class="sxs-lookup"><span data-stu-id="2ba72-121">Multiple conditions within a condition group are always concatenated by using **AND** logic.</span></span> <span data-ttu-id="2ba72-122">Bedingungs Gruppen werden stets mithilfe der- **oder** -Logik miteinander verkettet.</span><span class="sxs-lookup"><span data-stu-id="2ba72-122">Condition groups are always concatenated to each other by using **OR** logic.</span></span> <span data-ttu-id="2ba72-123">Um eine neue Bedingungs Gruppe zu starten, nennen Sie [iwmpquery. beginnextgroup](wmplibiwmpquery-iwmpquery-beginnextgroup--vb-and-c.md).</span><span class="sxs-lookup"><span data-stu-id="2ba72-123">To start a new condition group, call [IWMPQuery.beginNextGroup](wmplibiwmpquery-iwmpquery-beginnextgroup--vb-and-c.md).</span></span>

<span data-ttu-id="2ba72-124">Bei Verbund Abfragen mit **iwmpquery** wird die Groß-/Kleinschreibung nicht beachtet</span><span class="sxs-lookup"><span data-stu-id="2ba72-124">Compound queries using **IWMPQuery** are not case sensitive.</span></span>

<span data-ttu-id="2ba72-125">Eine Liste der Werte für den *bstrattribute* -Parameter finden Sie in der [alphabetischen Attribut Referenz](alphabetical-attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="2ba72-125">A list of values for the *bstrAttribute* parameter can be found in [Alphabetical Attribute Reference](alphabetical-attribute-reference.md).</span></span>

<span data-ttu-id="2ba72-126">In der folgenden Tabelle sind die unterstützten Werte für *bstroperator* aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ba72-126">The following table lists the supported values for *bstrOperator*.</span></span>



| <span data-ttu-id="2ba72-127">String</span><span class="sxs-lookup"><span data-stu-id="2ba72-127">String</span></span>              | <span data-ttu-id="2ba72-128">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="2ba72-128">Applies to</span></span>     |
|---------------------|----------------|
| <span data-ttu-id="2ba72-129">BeginsWith</span><span class="sxs-lookup"><span data-stu-id="2ba72-129">BeginsWith</span></span>          | <span data-ttu-id="2ba72-130">Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="2ba72-130">Strings</span></span>        |
| <span data-ttu-id="2ba72-131">Enthält</span><span class="sxs-lookup"><span data-stu-id="2ba72-131">Contains</span></span>            | <span data-ttu-id="2ba72-132">Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="2ba72-132">Strings</span></span>        |
| <span data-ttu-id="2ba72-133">Equals</span><span class="sxs-lookup"><span data-stu-id="2ba72-133">Equals</span></span>              | <span data-ttu-id="2ba72-134">Alle Typen</span><span class="sxs-lookup"><span data-stu-id="2ba72-134">All types</span></span>      |
| <span data-ttu-id="2ba72-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="2ba72-135">GreaterThan</span></span>         | <span data-ttu-id="2ba72-136">Zahlen, Datumsangaben</span><span class="sxs-lookup"><span data-stu-id="2ba72-136">Numbers, Dates</span></span> |
| <span data-ttu-id="2ba72-137">Größer als oder gleich</span><span class="sxs-lookup"><span data-stu-id="2ba72-137">GreaterThanOrEquals</span></span> | <span data-ttu-id="2ba72-138">Zahlen, Datumsangaben</span><span class="sxs-lookup"><span data-stu-id="2ba72-138">Numbers, Dates</span></span> |
| <span data-ttu-id="2ba72-139">LessThan</span><span class="sxs-lookup"><span data-stu-id="2ba72-139">LessThan</span></span>            | <span data-ttu-id="2ba72-140">Zahlen, Datumsangaben</span><span class="sxs-lookup"><span data-stu-id="2ba72-140">Numbers, Dates</span></span> |
| <span data-ttu-id="2ba72-141">Kleiner als oder gleich</span><span class="sxs-lookup"><span data-stu-id="2ba72-141">LessThanOrEquals</span></span>    | <span data-ttu-id="2ba72-142">Zahlen, Datumsangaben</span><span class="sxs-lookup"><span data-stu-id="2ba72-142">Numbers, Dates</span></span> |
| <span data-ttu-id="2ba72-143">Notbeginswith</span><span class="sxs-lookup"><span data-stu-id="2ba72-143">NotBeginsWith</span></span>       | <span data-ttu-id="2ba72-144">Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="2ba72-144">Strings</span></span>        |
| <span data-ttu-id="2ba72-145">NotContains</span><span class="sxs-lookup"><span data-stu-id="2ba72-145">NotContains</span></span>         | <span data-ttu-id="2ba72-146">Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="2ba72-146">Strings</span></span>        |
| <span data-ttu-id="2ba72-147">NotEquals</span><span class="sxs-lookup"><span data-stu-id="2ba72-147">NotEquals</span></span>           | <span data-ttu-id="2ba72-148">Alle Typen</span><span class="sxs-lookup"><span data-stu-id="2ba72-148">All types</span></span>      |



 

## <a name="examples"></a><span data-ttu-id="2ba72-149">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ba72-149">Examples</span></span>

<span data-ttu-id="2ba72-150">Im folgenden Beispiel wird eine Abfrage erstellt, zwei Bedingungen hinzugefügt und diese Abfrage verwendet, um die Ergebnisse der Abfrage als Zeichen folgen Auflistung zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="2ba72-150">The following example creates a query, adds two conditions to it, and uses that query to extract the results of the query as a string collection.</span></span> <span data-ttu-id="2ba72-151">Die Ergebnisse werden dann in einem Listenfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2ba72-151">The results are then displayed in a list box.</span></span> <span data-ttu-id="2ba72-152">Das **AxWMPLib. AxWindowsMediaPlayer** -Objekt wird durch die Variable mit dem Namen "Player" dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2ba72-152">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add two conditions to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");
q.addCondition("Title", "Contains", "Trio");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    queryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

&#39; Add two conditions to the Query. 
q.addCondition(&quot;WM/Composer&quot;, &quot;Equals&quot;, &quot;Antonio Vivaldi&quot;)
q.addCondition(&quot;Title&quot;, &quot;Contains&quot;, &quot;Trio&quot;)

&#39; Query the media collection and get a string collection containing the result.
&#39; In this case, the string collection will contain the titles of all audio items that
&#39; match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, q, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    queryResults.Items.Add(result.Item(i))

Next i
```





## <a name="requirements"></a><span data-ttu-id="2ba72-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ba72-153">Requirements</span></span>



| <span data-ttu-id="2ba72-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ba72-154">Requirement</span></span> | <span data-ttu-id="2ba72-155">Wert</span><span class="sxs-lookup"><span data-stu-id="2ba72-155">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ba72-156">Version</span><span class="sxs-lookup"><span data-stu-id="2ba72-156">Version</span></span><br/>   | <span data-ttu-id="2ba72-157">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="2ba72-157">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="2ba72-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="2ba72-158">Namespace</span></span><br/> | <span data-ttu-id="2ba72-159">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2ba72-159">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2ba72-160">Assembly</span><span class="sxs-lookup"><span data-stu-id="2ba72-160">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2ba72-161"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2ba72-161"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ba72-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ba72-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ba72-163">**Alphabetische Attribut Referenz**</span><span class="sxs-lookup"><span data-stu-id="2ba72-163">**Alphabetical Attribute Reference**</span></span>](alphabetical-attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="2ba72-164">**IWMPMediaCollection2. kreatequery (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2ba72-164">**IWMPMediaCollection2.createQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2ba72-165">**IWMPMediaCollection2. getplaylistbyquery (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2ba72-165">**IWMPMediaCollection2.getPlaylistByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2ba72-166">**IWMPMediaCollection2. getstringcollectionbyquery (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2ba72-166">**IWMPMediaCollection2.getStringCollectionByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2ba72-167">**Iwmpquery-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="2ba72-167">**IWMPQuery Interface**</span></span>](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





