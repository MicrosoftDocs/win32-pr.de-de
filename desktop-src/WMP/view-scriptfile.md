---
title: Scriptfile anzeigen
description: Das scriptfile-Attribut gibt die Dateinamen der begleitenden JScript-Dateien an.
ms.assetid: c285c467-5ba7-4f46-b316-977e833c3cdd
keywords:
- View. scriptfile-Windows-Media Player
topic_type:
- apiref
api_name:
- VIEW.scriptFile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac7f447f1934c2589b7ae52b3a24e2dcb2b1ef7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371672"
---
# <a name="viewscriptfile"></a><span data-ttu-id="37a28-104">Scriptfile anzeigen</span><span class="sxs-lookup"><span data-stu-id="37a28-104">VIEW.scriptFile</span></span>

<span data-ttu-id="37a28-105">Das **scriptfile** -Attribut gibt die Dateinamen der begleitenden JScript-Dateien an.</span><span class="sxs-lookup"><span data-stu-id="37a28-105">The **scriptFile** attribute specifies the file names of accompanying JScript files.</span></span>

``` syntax
        elementID.scriptFile
```

## <a name="possible-values"></a><span data-ttu-id="37a28-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="37a28-106">Possible Values</span></span>

<span data-ttu-id="37a28-107">Bei diesem Attribut handelt es sich um eine schreibgeschützte **Zeichenfolge** ohne Standardwert.</span><span class="sxs-lookup"><span data-stu-id="37a28-107">This attribute is a write-only **String** with no default value.</span></span> <span data-ttu-id="37a28-108">Die Dateinamen mehrerer JScript-Dateien werden durch Semikolons getrennt.</span><span class="sxs-lookup"><span data-stu-id="37a28-108">The file names of multiple JScript files are delimited with semicolons.</span></span> <span data-ttu-id="37a28-109">Führende und folgende Leerzeichen und Semikolons sollten nicht vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="37a28-109">Leading and following spaces and semicolons should not be present.</span></span>

## <a name="remarks"></a><span data-ttu-id="37a28-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37a28-110">Remarks</span></span>

<span data-ttu-id="37a28-111">Der Code in den angegebenen Dateien kann von jedem Ereignishandler in der Ansicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37a28-111">The code in the specified files can be used by any event handler in the View.</span></span> <span data-ttu-id="37a28-112">Code, der von Ereignis Handlern in mehreren Ansichten verwendet wird, kann in einer Datei mit dem gleichen Namen wie die Skin-Definitionsdatei, jedoch mit der Erweiterung. js anstelle der Erweiterung. WMS abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="37a28-112">Code that is used by event handlers in multiple Views can be placed in a file with the same name as the skin definition file but with a .js extension instead of a .wms extension.</span></span> <span data-ttu-id="37a28-113">Diese Datei wird automatisch geladen und muss nicht in der Skin-Definitionsdatei angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="37a28-113">This file is loaded automatically and need not be specified in the skin definition file.</span></span>

## <a name="examples"></a><span data-ttu-id="37a28-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37a28-114">Examples</span></span>


```C++
<VIEW id="theView" scriptFile="theScript.js">
</VIEW>

```



## <a name="requirements"></a><span data-ttu-id="37a28-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37a28-115">Requirements</span></span>



| <span data-ttu-id="37a28-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37a28-116">Requirement</span></span> | <span data-ttu-id="37a28-117">Wert</span><span class="sxs-lookup"><span data-stu-id="37a28-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="37a28-118">Version</span><span class="sxs-lookup"><span data-stu-id="37a28-118">Version</span></span><br/> | <span data-ttu-id="37a28-119">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="37a28-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="37a28-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37a28-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37a28-121">**View-Element**</span><span class="sxs-lookup"><span data-stu-id="37a28-121">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





