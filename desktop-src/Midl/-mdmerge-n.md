---
title: /n-Schalter
description: Der/n-Schalter gibt die Kompositions Tiefe für das Verfassen von Metadatendateien an.
ms.assetid: 7A1F8A9E-B3CC-4BB2-BF50-5662D4560280
keywords:
- /n-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /n
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78197c0f79c6bbe21ae4eb883620b95e6f0bd4c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366860"
---
# <a name="n-switch"></a><span data-ttu-id="27a2c-104">/n-Schalter</span><span class="sxs-lookup"><span data-stu-id="27a2c-104">/n switch</span></span>

<span data-ttu-id="27a2c-105">Der **/n** -Schalter gibt die Kompositions Tiefe für das Verfassen von Metadatendateien an.</span><span class="sxs-lookup"><span data-stu-id="27a2c-105">The **/n** switch specifies the composition depth for composing metadata files.</span></span>

``` syntax
mdmerge /n namespace_depth
```

## <a name="switch-options"></a><span data-ttu-id="27a2c-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="27a2c-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="27a2c-107">*Namespace \_ Tiefe*</span><span class="sxs-lookup"><span data-stu-id="27a2c-107">*namespace\_depth*</span></span> 
</dt> <dd>

<span data-ttu-id="27a2c-108">Gibt die Namespace Tiefe zum Verfassen in eine einzelne Metadatendatei an.</span><span class="sxs-lookup"><span data-stu-id="27a2c-108">Specifies the namespace depth to compose into a single metadata file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27a2c-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27a2c-109">Remarks</span></span>

<span data-ttu-id="27a2c-110">Im folgenden finden Sie die möglichen Werte Formate, die Sie mit dem **/n** -Schalter angeben können.</span><span class="sxs-lookup"><span data-stu-id="27a2c-110">Here are the possible value formats that you can specify with the **/n** switch.</span></span>



| <span data-ttu-id="27a2c-111">Wertformat</span><span class="sxs-lookup"><span data-stu-id="27a2c-111">Value format</span></span>                   | <span data-ttu-id="27a2c-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27a2c-112">Description</span></span>                                                                     |
|--------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="27a2c-113">Int32 > 0</span><span class="sxs-lookup"><span data-stu-id="27a2c-113">Int32 > 0</span></span>                   | <span data-ttu-id="27a2c-114">Verfassen Sie alle Typen in der im Switch angegebenen Namespace Tiefe.</span><span class="sxs-lookup"><span data-stu-id="27a2c-114">Compose all types at the namespace depth specified in the switch.</span></span>               |
| <span data-ttu-id="27a2c-115">-1</span><span class="sxs-lookup"><span data-stu-id="27a2c-115">-1</span></span>                             | <span data-ttu-id="27a2c-116">Erstellen Sie alle Typen in einer IDL-Datei pro Namespace.</span><span class="sxs-lookup"><span data-stu-id="27a2c-116">Compose all types into one IDL file per namespace.</span></span>                              |
| <span data-ttu-id="27a2c-117"><namespace>: Int32 > 0</span><span class="sxs-lookup"><span data-stu-id="27a2c-117"><namespace>:Int32 > 0</span></span> | <span data-ttu-id="27a2c-118">Verfassen Sie alle Typen mit einem entsprechenden Namespace in der im Switch angegebenen Tiefe.</span><span class="sxs-lookup"><span data-stu-id="27a2c-118">Compose all types with matching namespace at the depth specified in the switch.</span></span> |
| <span data-ttu-id="27a2c-119"><namespace>:-1</span><span class="sxs-lookup"><span data-stu-id="27a2c-119"><namespace>:-1</span></span>           | <span data-ttu-id="27a2c-120">Erstellen Sie alle Typen mit einem entsprechenden Namespace in eine Datei pro Namespace.</span><span class="sxs-lookup"><span data-stu-id="27a2c-120">Compose all types with matching namespace into one file per namespace.</span></span>          |



 

<span data-ttu-id="27a2c-121">In der folgenden Tabelle werden die Ergebnisse aus verschiedenen Kombinationen des **/n** -Schalters angezeigt, die für diese Namespaces funktionieren.</span><span class="sxs-lookup"><span data-stu-id="27a2c-121">The following table shows the results from different combinations of the **/n** switch working on these namespaces.</span></span>

-   <span data-ttu-id="27a2c-122">Windows. Foundation. Collections. iiterable</span><span class="sxs-lookup"><span data-stu-id="27a2c-122">Windows.Foundation.Collections.IIterable</span></span>
-   <span data-ttu-id="27a2c-123">Windows. UI. directui. Controls. Button</span><span class="sxs-lookup"><span data-stu-id="27a2c-123">Windows.UI.DirectUI.Controls.Button</span></span>
-   <span data-ttu-id="27a2c-124">Windows. UI. directui. Controls. ListView</span><span class="sxs-lookup"><span data-stu-id="27a2c-124">Windows.UI.DirectUI.Controls.ListView</span></span>
-   <span data-ttu-id="27a2c-125">Windows. UI. immersive. Application. playto. Target</span><span class="sxs-lookup"><span data-stu-id="27a2c-125">Windows.UI.Immersive.Application.PlayTo.Target</span></span>
-   <span data-ttu-id="27a2c-126">Windows. Web. Syndikation. RSS</span><span class="sxs-lookup"><span data-stu-id="27a2c-126">Windows.Web.Syndication.RSS</span></span>



| <span data-ttu-id="27a2c-127">Switches</span><span class="sxs-lookup"><span data-stu-id="27a2c-127">Switches</span></span>                         | <span data-ttu-id="27a2c-128">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="27a2c-128">Result</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="27a2c-129">Erklärung</span><span class="sxs-lookup"><span data-stu-id="27a2c-129">Explanation</span></span>                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27a2c-130">**/n:-1**  / **n:1**</span><span class="sxs-lookup"><span data-stu-id="27a2c-130">**/n:-1** /**n:1**</span></span>               | <span data-ttu-id="27a2c-131">Windows.winmd</span><span class="sxs-lookup"><span data-stu-id="27a2c-131">Windows.winmd</span></span>                                                                                                                                                                                                                                                | <span data-ttu-id="27a2c-132">Der letzte/n-Schalter überschreibt alle vorherigen – n-Switches.</span><span class="sxs-lookup"><span data-stu-id="27a2c-132">The last /n switch overrides all previous –n switches.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="27a2c-133">**/n:-1/n: Windows. UI: 2**</span><span class="sxs-lookup"><span data-stu-id="27a2c-133">**/n:-1/n:Windows.UI:2**</span></span>         | <dl> <span data-ttu-id="27a2c-134"><dt>Windows. Foundation. winmd</dt> <dt>Windows. UI. winmd</dt> <dt>Windows. Web. Syndikation. winmd</dt></span><span class="sxs-lookup"><span data-stu-id="27a2c-134"><dt>Windows.Foundation.winmd</dt> <dt>Windows.UI.winmd</dt> <dt>Windows.Web.Syndication.winmd</dt></span></span> </dl> | <dl> <span data-ttu-id="27a2c-135"><dt>**Windows. Foundation** besteht immer aus – n:2</dt></span><span class="sxs-lookup"><span data-stu-id="27a2c-135"><dt>**Windows.Foundation** is always composed at –n:2.</dt></span></span> <span data-ttu-id="27a2c-136"><dt>**Windows. UI** -Typen werden gruppiert.</dt></span><span class="sxs-lookup"><span data-stu-id="27a2c-136"><dt>**Windows.UI** types are grouped.</dt></span></span> <span data-ttu-id="27a2c-137"><dt>" **Windows. Web. Syndikation** " wird unter "n:-1." erstellt.</dt></span><span class="sxs-lookup"><span data-stu-id="27a2c-137"><dt>**Windows.Web.Syndication** is composed at n:-1.</dt></span></span> </dl>       |
| <span data-ttu-id="27a2c-138">**/n: 1/n: Windows. UI. directui: 3**</span><span class="sxs-lookup"><span data-stu-id="27a2c-138">**/n:1/n:Windows.UI.DirectUI:3**</span></span> | <dl> <span data-ttu-id="27a2c-139">Windows <dt>. Foundation. winmd</dt> Windows <dt>. UI. directui. winmd</dt> <dt>Windows. winmd</dt></span><span class="sxs-lookup"><span data-stu-id="27a2c-139"><dt>Windows.Foundation.winmd</dt> <dt>Windows.UI.DirectUI.winmd </dt> <dt>Windows.winmd</dt></span></span> </dl>       | <dl> <span data-ttu-id="27a2c-140"><dt>**Windows. Foundation** besteht immer aus – n:2</dt></span><span class="sxs-lookup"><span data-stu-id="27a2c-140"><dt>**Windows.Foundation** is always composed at –n:2.</dt></span></span> <span data-ttu-id="27a2c-141"><dt>**Windows. UI. directui** ist auf Ebene 3 verfasst.</dt></span><span class="sxs-lookup"><span data-stu-id="27a2c-141"><dt>**Windows.UI.DirectUI** is composed at level 3.</dt></span></span> <span data-ttu-id="27a2c-142"><dt>Alle anderen Typen werden auf Ebene 1 zusammengesetzt.</dt></span><span class="sxs-lookup"><span data-stu-id="27a2c-142"><dt>All other types are composed at level 1.</dt></span></span> </dl> |



 

<span data-ttu-id="27a2c-143">Hier sind die Regeln zum Verarbeiten mehrerer Instanzen des **/n** -Schalters aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="27a2c-143">Here are the rules for handling multiple instances of the **/n** switch.</span></span>

-   <span data-ttu-id="27a2c-144">Die spezifischere Instanz hat Vorrang.</span><span class="sxs-lookup"><span data-stu-id="27a2c-144">The most specific instance prevails.</span></span> <span data-ttu-id="27a2c-145">Wenn Sie z. b. **– n:a.b.c: 4 – n:a.b: 5** angeben, löst mdmerge A. b. c. D auf Ebene 4 auf, da a. b. c spezifischer als A.B. ist.</span><span class="sxs-lookup"><span data-stu-id="27a2c-145">For example, if you specify **–n:A.B.C:4–n:A.B:5**, MDMERGE resolves A.B.C.D at level 4, because A.B.C is more specific than A.B.</span></span> <span data-ttu-id="27a2c-146">A. b. E. F wird in Tiefe 5 aufgelöst, da es mit A. b übereinstimmt, nicht jedoch mit A.B.C.</span><span class="sxs-lookup"><span data-stu-id="27a2c-146">A.B.E.F resolves at depth 5, because it matches A.B but not A.B.C.</span></span>
-   <span data-ttu-id="27a2c-147">Die letzte Instanz hat Vorrang.</span><span class="sxs-lookup"><span data-stu-id="27a2c-147">The last instance prevails.</span></span> <span data-ttu-id="27a2c-148">Wenn Sie z. b. **– n:5 – n:2** angeben, werden die Typen auf Ebene 2 zusammengesetzt.</span><span class="sxs-lookup"><span data-stu-id="27a2c-148">For example, if you specify **–n:5–n:2**, the types are composed at level 2.</span></span>
-   <span data-ttu-id="27a2c-149">Beide Regeln gelten.</span><span class="sxs-lookup"><span data-stu-id="27a2c-149">Both of these rules apply.</span></span> <span data-ttu-id="27a2c-150">Wenn Sie – n:a.b.c: 4 – n:a.b.c: 1 angeben, wird der Namespace A. B. c auf Ebene 1 zusammengesetzt.</span><span class="sxs-lookup"><span data-stu-id="27a2c-150">If you specify –n:A.B.C:4 –n:A.B.C:1, namespace A.B.C is composed at level 1.</span></span>

## <a name="examples"></a><span data-ttu-id="27a2c-151">Beispiele</span><span class="sxs-lookup"><span data-stu-id="27a2c-151">Examples</span></span>

<span data-ttu-id="27a2c-152">**mdmerge.exe-Metadata \_ dir $ (SDK \_ - \_ Metadatenpfad)-i $ (interner \_ SDK- \_ \_ Metadatenpfad)-o $ (obj- \_ Pfad) \\ $O \\ systemmetadata-v-n:-1-n:Windows.Foundation: 2**</span><span class="sxs-lookup"><span data-stu-id="27a2c-152">**mdmerge.exe -metadata\_dir $(SDK\_METADATA\_PATH) -i $(INTERNAL\_SDK\_METADATA\_PATH) -o $(OBJ\_PATH)\\$O\\SystemMetadata -v -n:-1 -n:Windows.Foundation:2**</span></span>

## <a name="requirements"></a><span data-ttu-id="27a2c-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27a2c-153">Requirements</span></span>



| <span data-ttu-id="27a2c-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27a2c-154">Requirement</span></span> | <span data-ttu-id="27a2c-155">Wert</span><span class="sxs-lookup"><span data-stu-id="27a2c-155">Value</span></span> |
|-------------------|--------------------------------|
| <span data-ttu-id="27a2c-156">Client</span><span class="sxs-lookup"><span data-stu-id="27a2c-156">Client</span></span><br/> | <span data-ttu-id="27a2c-157">Windows 8</span><span class="sxs-lookup"><span data-stu-id="27a2c-157">Windows 8</span></span><br/>           |
| <span data-ttu-id="27a2c-158">Server</span><span class="sxs-lookup"><span data-stu-id="27a2c-158">Server</span></span><br/> | <span data-ttu-id="27a2c-159">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="27a2c-159">Windows Server 2012</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="27a2c-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27a2c-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27a2c-161">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="27a2c-161">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





