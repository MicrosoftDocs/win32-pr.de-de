---
description: Die Modulefiles-Eigenschaft des GetFiles-Objekts gibt alle Primärschlüssel der Dateitabelle für das aktuell geöffnete Modul zurück.
ms.assetid: e1c8049c-b271-4def-abde-89ea99393574
title: GetFiles. Modulefiles-Eigenschaft (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles.ModuleFiles
- IMsmGetFiles.get_ModuleFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: d13d624f2cfb24bfa6946ca6c45fe799602f55b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371533"
---
# <a name="getfilesmodulefiles-property"></a><span data-ttu-id="2e2e0-103">GetFiles. Modulefiles (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2e2e0-103">GetFiles.ModuleFiles property</span></span>

<span data-ttu-id="2e2e0-104">Die **Modulefiles** -Eigenschaft des [**GetFiles**](getfiles-object.md) -Objekts gibt alle Primärschlüssel der [Dateitabelle](file-table.md) für das aktuell geöffnete Modul zurück.</span><span class="sxs-lookup"><span data-stu-id="2e2e0-104">**ModuleFiles** property of the [**GetFiles**](getfiles-object.md) object returns all the primary keys of the [File table](file-table.md) for the currently open module.</span></span> <span data-ttu-id="2e2e0-105">Die Primärschlüssel werden als eine Auflistung von Zeichen folgen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2e2e0-105">The primary keys are returned as a collection of strings.</span></span> <span data-ttu-id="2e2e0-106">Das Modul muss durch einen Aufruf der [**OpenModule**](merge-openmodule.md) -Methode des [Merge-Objekts](merge-object.md) geöffnet werden, bevor **Modulefiles** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2e2e0-106">The module must be opened by a call to the [**OpenModule**](merge-openmodule.md) method of the [Merge object](merge-object.md) before calling **ModuleFiles**.</span></span>

<span data-ttu-id="2e2e0-107">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2e2e0-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e2e0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e2e0-108">Syntax</span></span>


```JScript
propVal = GetFiles.ModuleFiles
```



## <a name="property-value"></a><span data-ttu-id="2e2e0-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2e2e0-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="2e2e0-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e2e0-110">Remarks</span></span>

<span data-ttu-id="2e2e0-111">Beachten Sie, dass die Reihenfolge der in der Auflistung aufgelisteten Dateien möglicherweise nicht in derselben Reihenfolge wie in der Dateitabelle aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="2e2e0-111">Note that order of the files listed in the collection may not be in the same sequence as listed in the File table.</span></span>

<span data-ttu-id="2e2e0-112">Wenn das Modul keine Dateitabelle hat oder keine Dateien in der jeweiligen Sprache enthält, gibt Modulefiles eine leere Auflistung von Zeichen folgen zurück.</span><span class="sxs-lookup"><span data-stu-id="2e2e0-112">If the module has no File table, or contains no files in the particular language, ModuleFiles returns an empty collection of strings.</span></span>

### <a name="c"></a><span data-ttu-id="2e2e0-113">C++</span><span class="sxs-lookup"><span data-stu-id="2e2e0-113">C++</span></span>

<span data-ttu-id="2e2e0-114">Weitere Informationen finden [**Sie unter Get \_ Modulefiles**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles) function.</span><span class="sxs-lookup"><span data-stu-id="2e2e0-114">See [**get\_ModuleFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e2e0-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2e2e0-115">Requirements</span></span>



| <span data-ttu-id="2e2e0-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2e2e0-116">Requirement</span></span> | <span data-ttu-id="2e2e0-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2e2e0-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e2e0-118">Version</span><span class="sxs-lookup"><span data-stu-id="2e2e0-118">Version</span></span><br/> | <span data-ttu-id="2e2e0-119">Mergemod.dll 1,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="2e2e0-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="2e2e0-120">Header</span><span class="sxs-lookup"><span data-stu-id="2e2e0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2e2e0-121"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e2e0-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e2e0-122">DLL</span><span class="sxs-lookup"><span data-stu-id="2e2e0-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="2e2e0-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e2e0-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
