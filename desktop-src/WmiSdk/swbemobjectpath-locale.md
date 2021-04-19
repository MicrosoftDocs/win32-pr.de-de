---
description: Die Locale-Eigenschaft des "errbemubjectpath"-Objekts enthält das Gebiets Schema des Objekt Pfads.
ms.assetid: cde4ebac-b112-48b5-a274-802e6d3fbfbf
ms.tgt_platform: multiple
title: Errbemubjectpath. Locale-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Locale
- ISWbemObjectPath.Locale
- ISWbemObjectPath.get_Locale
- ISWbemObjectPath.put_Locale
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a046d3dabd21b9fc46f63764f9a5c7f3e8701d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358582"
---
# <a name="swbemobjectpathlocale-property"></a><span data-ttu-id="5f47d-103">Errbemubjectpath. Locale (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5f47d-103">SWbemObjectPath.Locale property</span></span>

<span data-ttu-id="5f47d-104">Die **locale** -Eigenschaft des " [**errbemubjectpath**](swbemobjectpath.md) "-Objekts enthält das Gebiets Schema des Objekt Pfads.</span><span class="sxs-lookup"><span data-stu-id="5f47d-104">The **Locale** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the locale of object path.</span></span>

<span data-ttu-id="5f47d-105">Wenn die Eigenschaft " **errbemubjectpath. locale** " Teil eines eigenständigen " [**errbemubjectpath**](swbemobjectpath.md) "-Objekts ist, ist Sie Lese-/Schreibzugriff und kann verwendet werden, um die Gebiets Schema Komponente des Monikers festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5f47d-105">When the **SWbemObjectPath.Locale** property is part of a standalone [**SWbemObjectPath**](swbemobjectpath.md) object, it is read/write and can be used to set the locale component of the moniker.</span></span>

<span data-ttu-id="5f47d-106">Wenn auf die Eigenschaft " **errbemubjectpath. locale** " als Teil einer " [**errbemubject. \_ path**](swbemobject-path-.md) "-Eigenschaft zugegriffen wird, ist sie schreibgeschützt und meldet den Wert des Gebiets Schemas, das bei der Bindung an den Namespace verwendet wird, aus dem das Objekt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="5f47d-106">When the **SWbemObjectPath.Locale** property is accessed as part of a [**SWbemObject.Path\_**](swbemobject-path-.md) property, it is read-only and reports the value of the locale used in binding to the namespace from which the object was obtained.</span></span>

<span data-ttu-id="5f47d-107">Für Microsoft-Gebiets Schema Bezeichner ist das Format der Zeichenfolge "MS \_ xxxx", wobei xxxx eine Zeichenfolge im hexadezimalen Format ist, die die LCID angibt.</span><span class="sxs-lookup"><span data-stu-id="5f47d-107">For Microsoft locale identifiers, the format of the string is "MS\_xxxx", where xxxx is a string in hexadecimal form that indicates the LCID.</span></span> <span data-ttu-id="5f47d-108">Der Gebiets Schema Bezeichner Deutschland ist beispielsweise "MS \_ 409".</span><span class="sxs-lookup"><span data-stu-id="5f47d-108">For example, the American English locale identifier is "MS\_409".</span></span>

<span data-ttu-id="5f47d-109">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5f47d-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="5f47d-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="5f47d-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f47d-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f47d-111">Syntax</span></span>


```VB
SWbemObjectPath.Locale As String
```



## <a name="property-value"></a><span data-ttu-id="5f47d-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5f47d-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="5f47d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f47d-113">Requirements</span></span>



| <span data-ttu-id="5f47d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f47d-114">Requirement</span></span> | <span data-ttu-id="5f47d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5f47d-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f47d-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f47d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5f47d-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f47d-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5f47d-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f47d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5f47d-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f47d-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5f47d-120">Header</span><span class="sxs-lookup"><span data-stu-id="5f47d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f47d-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f47d-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5f47d-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="5f47d-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="5f47d-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5f47d-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5f47d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5f47d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f47d-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f47d-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5f47d-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="5f47d-126">CLSID</span></span><br/>                    | <span data-ttu-id="5f47d-127">CLSID- \_ Swap-Austausch Pfad</span><span class="sxs-lookup"><span data-stu-id="5f47d-127">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="5f47d-128">IID</span><span class="sxs-lookup"><span data-stu-id="5f47d-128">IID</span></span><br/>                      | <span data-ttu-id="5f47d-129">IID \_ iswbemubjectpath</span><span class="sxs-lookup"><span data-stu-id="5f47d-129">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




