---
title: Query. addcondition-Methode
description: Die addcondition-Methode fügt dem Query-Objekt mithilfe der-und der-Logik eine Bedingung hinzu.
ms.assetid: 29b5d372-eddf-4b70-882b-d2dde79d9287
keywords:
- addcondition-Methode (Windows Media Player)
- addcondition-Methode, Windows Media Player, Abfrage Klasse
- Query-Klasse, Windows Media Player, addcondition-Methode
topic_type:
- apiref
api_name:
- Query.addCondition
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4035d2877cf0081e9153277c88feb545a529568d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352893"
---
# <a name="queryaddcondition-method"></a><span data-ttu-id="af1e1-106">Query. addcondition-Methode</span><span class="sxs-lookup"><span data-stu-id="af1e1-106">Query.addCondition method</span></span>

<span data-ttu-id="af1e1-107">Die **addcondition** -Methode fügt dem **Query** -Objekt mithilfe der-und der-Logik eine Bedingung hinzu.</span><span class="sxs-lookup"><span data-stu-id="af1e1-107">The **addCondition** method adds a condition to the **Query** object using AND logic.</span></span>

## <a name="syntax"></a><span data-ttu-id="af1e1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="af1e1-108">Syntax</span></span>


```JScript
Query.addCondition(
  attribute,
  operator,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="af1e1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="af1e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af1e1-110">*Attribut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af1e1-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af1e1-111">**Zeichenfolge** , die den Attributnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="af1e1-111">**String** containing the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="af1e1-112">*Operator* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af1e1-112">*operator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af1e1-113">**Zeichenfolge** , die den Operator enthält.</span><span class="sxs-lookup"><span data-stu-id="af1e1-113">**String** containing the operator.</span></span> <span data-ttu-id="af1e1-114">Siehe Hinweise zu unterstützten Werten.</span><span class="sxs-lookup"><span data-stu-id="af1e1-114">See Remarks for supported values.</span></span>

</dd> <dt>

<span data-ttu-id="af1e1-115">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af1e1-115">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af1e1-116">**Zeichenfolge** , die den Attribut Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="af1e1-116">**String** containing the attribute value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af1e1-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af1e1-117">Return value</span></span>

<span data-ttu-id="af1e1-118">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="af1e1-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="af1e1-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af1e1-119">Remarks</span></span>

<span data-ttu-id="af1e1-120">Bei Verbund Abfragen mit **Abfrage** wird die Groß-/Kleinschreibung nicht beachtet</span><span class="sxs-lookup"><span data-stu-id="af1e1-120">Compound queries using **Query** are not case sensitive.</span></span>

<span data-ttu-id="af1e1-121">Eine Liste der Werte für den *Attribut* Parameter finden Sie im Abschnitt " [alphabetische Attribut Verweis](alphabetical-attribute-reference.md) ".</span><span class="sxs-lookup"><span data-stu-id="af1e1-121">A list of values for the *attribute* parameter can be found in the [Alphabetical Attribute Reference](alphabetical-attribute-reference.md) section.</span></span>

<span data-ttu-id="af1e1-122">Bedingungen, die in einem **Abfrage** Objekt enthalten sind, werden in Bedingungs Gruppen organisiert.</span><span class="sxs-lookup"><span data-stu-id="af1e1-122">Conditions contained in a **Query** object are organized into condition groups.</span></span> <span data-ttu-id="af1e1-123">Mehrere Bedingungen innerhalb einer Bedingungs Gruppe werden stets mithilfe der-und der-Logik verkettet.</span><span class="sxs-lookup"><span data-stu-id="af1e1-123">Multiple conditions within a condition group are always concatenated using AND logic.</span></span> <span data-ttu-id="af1e1-124">Bedingungs Gruppen werden mit der-oder der-Logik immer aufeinander verkettet.</span><span class="sxs-lookup"><span data-stu-id="af1e1-124">Condition groups are always concatenated to each other using OR logic.</span></span> <span data-ttu-id="af1e1-125">Zum Starten einer neuen Bedingungs Gruppe aufrufen Sie **Query. beginnextgroup**.</span><span class="sxs-lookup"><span data-stu-id="af1e1-125">To start a new condition group, call **Query.beginNextGroup**.</span></span>

<span data-ttu-id="af1e1-126">In der folgenden Tabelle sind die unterstützten Werte für den- *Operator* aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="af1e1-126">The following table lists the supported values for *operator*.</span></span>



| <span data-ttu-id="af1e1-127">Operator</span><span class="sxs-lookup"><span data-stu-id="af1e1-127">Operator</span></span>            | <span data-ttu-id="af1e1-128">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="af1e1-128">Applies to</span></span>     |
|---------------------|----------------|
| <span data-ttu-id="af1e1-129">BeginsWith</span><span class="sxs-lookup"><span data-stu-id="af1e1-129">BeginsWith</span></span>          | <span data-ttu-id="af1e1-130">Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="af1e1-130">Strings</span></span>        |
| <span data-ttu-id="af1e1-131">Enthält</span><span class="sxs-lookup"><span data-stu-id="af1e1-131">Contains</span></span>            | <span data-ttu-id="af1e1-132">Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="af1e1-132">Strings</span></span>        |
| <span data-ttu-id="af1e1-133">Equals</span><span class="sxs-lookup"><span data-stu-id="af1e1-133">Equals</span></span>              | <span data-ttu-id="af1e1-134">Alle Typen</span><span class="sxs-lookup"><span data-stu-id="af1e1-134">All types</span></span>      |
| <span data-ttu-id="af1e1-135">GreaterThan</span><span class="sxs-lookup"><span data-stu-id="af1e1-135">GreaterThan</span></span>         | <span data-ttu-id="af1e1-136">Zahlen, Datumsangaben</span><span class="sxs-lookup"><span data-stu-id="af1e1-136">Numbers, Dates</span></span> |
| <span data-ttu-id="af1e1-137">Größer als oder gleich</span><span class="sxs-lookup"><span data-stu-id="af1e1-137">GreaterThanOrEquals</span></span> | <span data-ttu-id="af1e1-138">Zahlen, Datumsangaben</span><span class="sxs-lookup"><span data-stu-id="af1e1-138">Numbers, Dates</span></span> |
| <span data-ttu-id="af1e1-139">LessThan</span><span class="sxs-lookup"><span data-stu-id="af1e1-139">LessThan</span></span>            | <span data-ttu-id="af1e1-140">Zahlen, Datumsangaben</span><span class="sxs-lookup"><span data-stu-id="af1e1-140">Numbers, Dates</span></span> |
| <span data-ttu-id="af1e1-141">Kleiner als oder gleich</span><span class="sxs-lookup"><span data-stu-id="af1e1-141">LessThanOrEquals</span></span>    | <span data-ttu-id="af1e1-142">Zahlen, Datumsangaben</span><span class="sxs-lookup"><span data-stu-id="af1e1-142">Numbers, Dates</span></span> |
| <span data-ttu-id="af1e1-143">Notbeginswith</span><span class="sxs-lookup"><span data-stu-id="af1e1-143">NotBeginsWith</span></span>       | <span data-ttu-id="af1e1-144">Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="af1e1-144">Strings</span></span>        |
| <span data-ttu-id="af1e1-145">NotContains</span><span class="sxs-lookup"><span data-stu-id="af1e1-145">NotContains</span></span>         | <span data-ttu-id="af1e1-146">Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="af1e1-146">Strings</span></span>        |
| <span data-ttu-id="af1e1-147">NotEquals</span><span class="sxs-lookup"><span data-stu-id="af1e1-147">NotEquals</span></span>           | <span data-ttu-id="af1e1-148">Alle Typen</span><span class="sxs-lookup"><span data-stu-id="af1e1-148">All types</span></span>      |



 

## <a name="examples"></a><span data-ttu-id="af1e1-149">Beispiele</span><span class="sxs-lookup"><span data-stu-id="af1e1-149">Examples</span></span>

<span data-ttu-id="af1e1-150">Im folgenden JScript-Beispiel wird **Query. addcondition** und **Query. beginnextgroup** verwendet, um eine Beispiel Abfrage auszuführen.</span><span class="sxs-lookup"><span data-stu-id="af1e1-150">The following JScript example uses **Query.addCondition** and **Query.beginNextGroup** to perform an example query.</span></span>


```JScript
// Perform an example query for media for which:
// The genre contains "jazz"
// and the title begins with "a"
// OR the genre contains "jazz"
// and the author begins with "b".

// Create the query object.
var Query = Player.mediaCollection.createQuery();

// Add the first condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Title", "BeginsWith", "a");

// Begin the new condition group ("or").
Query.beginNextGroup();

// Add the second condition group.
Query.addCondition("WM/Genre", "Contains", "jazz");
Query.addCondition("Author", "BeginsWith", "b");

// Perform the query on "audio" media.
var Playlist = Player.mediaCollection.getPlaylistByQuery(
    Query,      // query
    "audio",    // mediaType
    "",         // sortAttribute
    false);     // sortAscending
```



## <a name="requirements"></a><span data-ttu-id="af1e1-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af1e1-151">Requirements</span></span>



| <span data-ttu-id="af1e1-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af1e1-152">Requirement</span></span> | <span data-ttu-id="af1e1-153">Wert</span><span class="sxs-lookup"><span data-stu-id="af1e1-153">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="af1e1-154">Version</span><span class="sxs-lookup"><span data-stu-id="af1e1-154">Version</span></span><br/> | <span data-ttu-id="af1e1-155">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="af1e1-155">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="af1e1-156">DLL</span><span class="sxs-lookup"><span data-stu-id="af1e1-156">DLL</span></span><br/>     | <dl> <span data-ttu-id="af1e1-157"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af1e1-157"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af1e1-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af1e1-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af1e1-159">**Mediacollection. kreatequery**</span><span class="sxs-lookup"><span data-stu-id="af1e1-159">**MediaCollection.createQuery**</span></span>](mediacollection-createquery.md)
</dt> <dt>

[<span data-ttu-id="af1e1-160">**Mediacollection. getplaylistbyquery**</span><span class="sxs-lookup"><span data-stu-id="af1e1-160">**MediaCollection.getPlaylistByQuery**</span></span>](mediacollection-getplaylistbyquery.md)
</dt> <dt>

[<span data-ttu-id="af1e1-161">**Mediacollection. getstringcollectionbyquery**</span><span class="sxs-lookup"><span data-stu-id="af1e1-161">**MediaCollection.getStringCollectionByQuery**</span></span>](mediacollection-getstringcollectionbyquery.md)
</dt> <dt>

[<span data-ttu-id="af1e1-162">**Query-Objekt**</span><span class="sxs-lookup"><span data-stu-id="af1e1-162">**Query Object**</span></span>](query-object.md)
</dt> <dt>

[<span data-ttu-id="af1e1-163">**Query. beginnextgroup**</span><span class="sxs-lookup"><span data-stu-id="af1e1-163">**Query.beginNextGroup**</span></span>](query-beginnextgroup.md)
</dt> </dl>

 

 





