---
description: Diese Flags geben das Verhalten des medienlocators an.
ms.assetid: 60afb2e8-cdd1-493e-8fc8-6fa581720b8d
title: Dateiname-Validierungsflags (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SFN_VALIDATEF_CHECK
- SFN_VALIDATEF_POPUP
- SFN_VALIDATEF_TELLME
- SFN_VALIDATEF_REPLACE
- SFN_VALIDATEF_USELOCAL
- SFN_VALIDATEF_NOFIND
- SFN_VALIDATEF_IGNOREMUTED
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: d8930241be0306c637bcab36207fec1de2e489c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372039"
---
# <a name="file-name-validation-flags"></a><span data-ttu-id="9445c-103">Dateiname-Überprüfung</span><span class="sxs-lookup"><span data-stu-id="9445c-103">File Name Validation Flags</span></span>

<span data-ttu-id="9445c-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="9445c-104">\[Deprecated.</span></span> <span data-ttu-id="9445c-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="9445c-105">This API may be removed from future releases of Windows.\]</span></span>

<span data-ttu-id="9445c-106">Diese Flags geben das Verhalten des medienlocators an.</span><span class="sxs-lookup"><span data-stu-id="9445c-106">These flags specify the behavior of the media locator.</span></span>



| <span data-ttu-id="9445c-107">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="9445c-107">Constant/value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="9445c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9445c-108">Description</span></span>                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFN_VALIDATEF_CHECK"></span><span id="sfn_validatef_check"></span><dl> <span data-ttu-id="9445c-109"><dt>**SFN \_ Validatef- \_ Überprüfung**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="9445c-109"><dt>**SFN\_VALIDATEF\_CHECK**</dt> <dt>0x01</dt></span></span> </dl>                   | <span data-ttu-id="9445c-110">Überprüfen Sie die Gültigkeit von Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="9445c-110">Check the validity of file names.</span></span> <span data-ttu-id="9445c-111">Sie müssen dieses Flag festlegen, um Dateinamen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9445c-111">You must set this flag to validate file names.</span></span> <span data-ttu-id="9445c-112">Andernfalls haben die anderen Flags keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="9445c-112">If not, the other flags have no effect.</span></span><br/>                                                                                            |
| <span id="SFN_VALIDATEF_POPUP"></span><span id="sfn_validatef_popup"></span><dl> <span data-ttu-id="9445c-113"><dt>**SFN \_ Validatef- \_ Popup**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="9445c-113"><dt>**SFN\_VALIDATEF\_POPUP**</dt> <dt>0x02</dt></span></span> </dl>                   | <span data-ttu-id="9445c-114">Wenn eine Datei nicht gefunden wird, können Sie das Dialogfeld Datei öffnen für den Endbenutzer anzeigen.</span><span class="sxs-lookup"><span data-stu-id="9445c-114">If a file is not located, display an Open File dialog box for the end user.</span></span><br/>                                                                                                                                         |
| <span id="SFN_VALIDATEF_TELLME"></span><span id="sfn_validatef_tellme"></span><dl> <span data-ttu-id="9445c-115"><dt>**SFN \_ Validatef- \_ Tellme**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="9445c-115"><dt>**SFN\_VALIDATEF\_TELLME**</dt> <dt>0x04</dt></span></span> </dl>                | <span data-ttu-id="9445c-116">Wenn eine fehlende Datei gefunden wird, zeigen Sie kurz ein Meldungs Feld mit dem Namen und dem Speicherort der Datei an.</span><span class="sxs-lookup"><span data-stu-id="9445c-116">If a missing file is located, briefly display a message box with the name and location of the file.</span></span> <span data-ttu-id="9445c-117">Dieses Flag ist hauptsächlich für Testzwecke nützlich. das Meldungs Feld eignet sich wahrscheinlich nicht für ein Einzelhandelsprodukt.</span><span class="sxs-lookup"><span data-stu-id="9445c-117">This flag is mostly useful for testing purposes; the message box is probably not suitable for a retail product.</span></span><br/> |
| <span id="SFN_VALIDATEF_REPLACE"></span><span id="sfn_validatef_replace"></span><dl> <span data-ttu-id="9445c-118"><dt>**SFN \_ Validatef \_ Replace**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="9445c-118"><dt>**SFN\_VALIDATEF\_REPLACE**</dt> <dt>0x08</dt></span></span> </dl>             | <span data-ttu-id="9445c-119">Wenn eine fehlende Datei gefunden wird, aktualisieren Sie den Namen des Quell Objekts.</span><span class="sxs-lookup"><span data-stu-id="9445c-119">If a missing file is located, update the name of the source object.</span></span> <span data-ttu-id="9445c-120">(Nur gültig in der [**iamtimeline:: validatesourcenames**](iamtimeline-validatesourcenames.md) -Methode.)</span><span class="sxs-lookup"><span data-stu-id="9445c-120">(Only valid in the [**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md) method.)</span></span><br/>                                         |
| <span id="SFN_VALIDATEF_USELOCAL"></span><span id="sfn_validatef_uselocal"></span><dl> <span data-ttu-id="9445c-121"><dt>**SFN \_ Validatef \_ uselocal**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="9445c-121"><dt>**SFN\_VALIDATEF\_USELOCAL**</dt> <dt>0x10</dt></span></span> </dl>          | <span data-ttu-id="9445c-122">Verwenden Sie immer eine lokale Datei, auch wenn eine Version der Datei im Netzwerk vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9445c-122">Always use a local file, even if a version of the file exists on the network.</span></span><br/>                                                                                                                                       |
| <span id="SFN_VALIDATEF_NOFIND"></span><span id="sfn_validatef_nofind"></span><dl> <span data-ttu-id="9445c-123"><dt>**SFN \_ Validatef \_ NoFind**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="9445c-123"><dt>**SFN\_VALIDATEF\_NOFIND**</dt> <dt>0x20</dt></span></span> </dl>                | <span data-ttu-id="9445c-124">Nicht nach fehlenden Dateien suchen.</span><span class="sxs-lookup"><span data-stu-id="9445c-124">Do not search for missing files.</span></span> <span data-ttu-id="9445c-125">Dateinamen werden nach wie vor überprüft, wenn Sie das \_ Check-Flag SFN validatef festlegen \_ .</span><span class="sxs-lookup"><span data-stu-id="9445c-125">File names are still validated if you set the SFN\_VALIDATEF\_CHECK flag.</span></span><br/>                                                                                                          |
| <span id="SFN_VALIDATEF_IGNOREMUTED"></span><span id="sfn_validatef_ignoremuted"></span><dl> <span data-ttu-id="9445c-126"><dt>**SFN \_ Validatef \_ ignoremuted**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="9445c-126"><dt>**SFN\_VALIDATEF\_IGNOREMUTED**</dt> <dt>0x40</dt></span></span> </dl> | <span data-ttu-id="9445c-127">Musterte Quell Objekte ignorieren.</span><span class="sxs-lookup"><span data-stu-id="9445c-127">Ignore muted source objects.</span></span> <span data-ttu-id="9445c-128">(Nur gültig in der [**iamtimeline:: validatesourcenames**](iamtimeline-validatesourcenames.md) -Methode.)</span><span class="sxs-lookup"><span data-stu-id="9445c-128">(Only valid in the [**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md) method.)</span></span><br/>                                                                                |



## <a name="requirements"></a><span data-ttu-id="9445c-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9445c-129">Requirements</span></span>



| <span data-ttu-id="9445c-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9445c-130">Requirement</span></span> | <span data-ttu-id="9445c-131">Wert</span><span class="sxs-lookup"><span data-stu-id="9445c-131">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9445c-132">Header</span><span class="sxs-lookup"><span data-stu-id="9445c-132">Header</span></span><br/> | <dl> <span data-ttu-id="9445c-133"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="9445c-133"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9445c-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9445c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9445c-135">**Imedialocator:: findmediafile**</span><span class="sxs-lookup"><span data-stu-id="9445c-135">**IMediaLocator::FindMediaFile**</span></span>](imedialocator-findmediafile.md)
</dt> <dt>

[<span data-ttu-id="9445c-136">**"Unenderengine:: setsourcenamevalidation"**</span><span class="sxs-lookup"><span data-stu-id="9445c-136">**IRenderEngine::SetSourceNameValidation**</span></span>](irenderengine-setsourcenamevalidation.md)
</dt> </dl>

 

 




