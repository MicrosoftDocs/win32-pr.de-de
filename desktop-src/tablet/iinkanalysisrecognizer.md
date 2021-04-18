---
description: Ermöglicht den Zugriff auf Handschrift erkennungsungen für die Verwendung mit der Ink-Analyse.
ms.assetid: de536cca-889e-413e-a6f7-c2229a77c801
title: Iinkanalysiserkenzer-Schnittstelle (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b091b47d14929e155548dc057ef0fdb1731133a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368098"
---
# <a name="iinkanalysisrecognizer-interface"></a><span data-ttu-id="50ccd-103">Iinkanalysiserkenzer-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="50ccd-103">IInkAnalysisRecognizer interface</span></span>

<span data-ttu-id="50ccd-104">Ermöglicht den Zugriff auf Handschrift erkennungsungen für die Verwendung mit der Ink-Analyse.</span><span class="sxs-lookup"><span data-stu-id="50ccd-104">Provides access to handwriting recognizers for use with ink analysis.</span></span>

## <a name="members"></a><span data-ttu-id="50ccd-105">Member</span><span class="sxs-lookup"><span data-stu-id="50ccd-105">Members</span></span>

<span data-ttu-id="50ccd-106">Die **iinkanalysiserkenzer** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="50ccd-106">The **IInkAnalysisRecognizer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="50ccd-107">**Iinkanalysiserkenzer** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="50ccd-107">**IInkAnalysisRecognizer** also has these types of members:</span></span>

-   [<span data-ttu-id="50ccd-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="50ccd-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="50ccd-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="50ccd-109">Methods</span></span>

<span data-ttu-id="50ccd-110">Die **iinkanalysiserkenzer** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="50ccd-110">The **IInkAnalysisRecognizer** interface has these methods.</span></span>



| <span data-ttu-id="50ccd-111">Methode</span><span class="sxs-lookup"><span data-stu-id="50ccd-111">Method</span></span>                                                                          | <span data-ttu-id="50ccd-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="50ccd-112">Description</span></span>                                                                                                                    |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50ccd-113">**GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="50ccd-113">**GetCapabilities**</span></span>](iinkanalysisrecognizer-getcapabilities.md)               | <span data-ttu-id="50ccd-114">Ruft die Funktionen des Erkennungs Moduls ab.</span><span class="sxs-lookup"><span data-stu-id="50ccd-114">Retrieves the capabilities of the recognizer.</span></span><br/>                                                                       |
| [<span data-ttu-id="50ccd-115">**GetGuid**</span><span class="sxs-lookup"><span data-stu-id="50ccd-115">**GetGuid**</span></span>](iinkanalysisrecognizer-getguid.md)                               | <span data-ttu-id="50ccd-116">Ruft den Globally Unique Identifier (GUID) der Erkennung ab.</span><span class="sxs-lookup"><span data-stu-id="50ccd-116">Retrieves the globally unique identifier (GUID) of the recognizer.</span></span><br/>                                                  |
| [<span data-ttu-id="50ccd-117">**GetLanguages**</span><span class="sxs-lookup"><span data-stu-id="50ccd-117">**GetLanguages**</span></span>](iinkanalysisrecognizer-getlanguages.md)                     | <span data-ttu-id="50ccd-118">Ruft die Bezeichner für die Gebiets Schemas ab, die von diesem **iinkanalysiserkenzer** unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="50ccd-118">Retrieves the identifiers for the locales that this **IInkAnalysisRecognizer** supports.</span></span><br/>                            |
| [<span data-ttu-id="50ccd-119">**GetName**</span><span class="sxs-lookup"><span data-stu-id="50ccd-119">**GetName**</span></span>](iinkanalysisrecognizer-getname.md)                               | <span data-ttu-id="50ccd-120">Ruft den Namen der Erkennung ab.</span><span class="sxs-lookup"><span data-stu-id="50ccd-120">Retrieves the name of the recognizer.</span></span><br/>                                                                               |
| [<span data-ttu-id="50ccd-121">**GetSupportedProperties**</span><span class="sxs-lookup"><span data-stu-id="50ccd-121">**GetSupportedProperties**</span></span>](iinkanalysisrecognizer-getsupportedproperties.md) | <span data-ttu-id="50ccd-122">Ruft die GUIDs (Global Unique Bezeichner) für die Eigenschaften ab, die von diesem **iinkanalysiserkenzer** unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="50ccd-122">Retrieves the globally unique identifiers (GUIDs) for the properties that this **IInkAnalysisRecognizer** supports.</span></span><br/> |
| [<span data-ttu-id="50ccd-123">**Getvendor**</span><span class="sxs-lookup"><span data-stu-id="50ccd-123">**GetVendor**</span></span>](iinkanalysisrecognizer-getvendor.md)                           | <span data-ttu-id="50ccd-124">Ruft den Herstellernamen des **iinkanalysiserkenzer**-Elements ab.</span><span class="sxs-lookup"><span data-stu-id="50ccd-124">Retrieves the vendor name of the **IInkAnalysisRecognizer**.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="50ccd-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50ccd-125">Remarks</span></span>

<span data-ttu-id="50ccd-126">Eine Erkennung verfügt über bestimmte Attribute und Eigenschaften, mit deren Hilfe Sie eine Erkennung durchführen können.</span><span class="sxs-lookup"><span data-stu-id="50ccd-126">A recognizer has specific attributes and properties that allow it to perform recognition.</span></span> <span data-ttu-id="50ccd-127">Die Eigenschaften einer Erkennung müssen festgelegt werden, bevor eine Erkennung erfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="50ccd-127">The properties of a recognizer must be determined before recognition can occur.</span></span> <span data-ttu-id="50ccd-128">Die Typen von Eigenschaften, die von einer Erkennung unterstützt werden, bestimmen, welche Erkennungs Typen Sie ausführen können.</span><span class="sxs-lookup"><span data-stu-id="50ccd-128">The types of properties that a recognizer supports determine the types of recognition that it can perform.</span></span> <span data-ttu-id="50ccd-129">Wenn eine Erkennung beispielsweise keine Kursive Handschrift unterstützt, gibt Sie falsche Ergebnisse zurück, wenn ein Benutzer in einem Cursor schreibt.</span><span class="sxs-lookup"><span data-stu-id="50ccd-129">For instance, if a recognizer does not support cursive handwriting, it returns inaccurate results when a user writes in cursive.</span></span>

<span data-ttu-id="50ccd-130">Eine Erkennung verfügt auch über eine integrierte Funktionalität, mit der viele Aspekte der Handschrift automatisch verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="50ccd-130">A recognizer also has built-in functionality that automatically manages many aspects of handwriting.</span></span> <span data-ttu-id="50ccd-131">Beispielsweise bestimmt Sie die Metriken für die Zeilen, in denen Striche gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="50ccd-131">For instance, it determines the metrics for the lines on which strokes are drawn.</span></span> <span data-ttu-id="50ccd-132">Sie können die Zeilennummer eines Strichs zurückgeben. Sie müssen jedoch nie angeben, wie diese Zeilenmetriken aufgrund der integrierten Funktionalität der Erkennung bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="50ccd-132">You can return the line number of a stroke, but you never need to specify how those line metrics are determined because of the built-in functionality of the recognizer.</span></span>

<span data-ttu-id="50ccd-133">[**Iinkanalyzer**](iinkanalyzer.md) verwaltet eine Liste der verfügbaren erkenzer.</span><span class="sxs-lookup"><span data-stu-id="50ccd-133">The [**IInkAnalyzer**](iinkanalyzer.md) maintains a list of available recognizers.</span></span> <span data-ttu-id="50ccd-134">Um auf diese Liste zuzugreifen, verwenden Sie die [**iinkanalyzer:: getinkanalysiserkenzersbypriority-Methoden**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) Methode.</span><span class="sxs-lookup"><span data-stu-id="50ccd-134">To access this list, use the [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="50ccd-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50ccd-135">Requirements</span></span>



| <span data-ttu-id="50ccd-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50ccd-136">Requirement</span></span> | <span data-ttu-id="50ccd-137">Wert</span><span class="sxs-lookup"><span data-stu-id="50ccd-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50ccd-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50ccd-138">Minimum supported client</span></span><br/> | <span data-ttu-id="50ccd-139">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50ccd-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="50ccd-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50ccd-140">Minimum supported server</span></span><br/> | <span data-ttu-id="50ccd-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="50ccd-141">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="50ccd-142">Header</span><span class="sxs-lookup"><span data-stu-id="50ccd-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="50ccd-143"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="50ccd-143"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="50ccd-144">DLL</span><span class="sxs-lookup"><span data-stu-id="50ccd-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50ccd-145"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50ccd-145"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="50ccd-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50ccd-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50ccd-147">**Iinkanalysiserkenzers**</span><span class="sxs-lookup"><span data-stu-id="50ccd-147">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="50ccd-148">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="50ccd-148">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="50ccd-149">**Iinkanalyzer:: kreatecustomerkenzer-Methode**</span><span class="sxs-lookup"><span data-stu-id="50ccd-149">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="50ccd-150">Kontext Knoten Typen</span><span class="sxs-lookup"><span data-stu-id="50ccd-150">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="50ccd-151">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="50ccd-151">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

