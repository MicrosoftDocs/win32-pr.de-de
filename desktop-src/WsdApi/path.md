---
description: Gibt den Speicherort und den Dateinamen einer WSDL-Datei an. Der Pfad kann ein absoluter oder relativer Pfad zur Datei sein, darf jedoch keine URL sein.
ms.assetid: 0664dcc6-1e71-46cf-9084-1adc84861b52
title: Path-Element (Webdienste auf Geräten)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 763ad1479c20553fb7e62ab29e504d56bfa6d950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362254"
---
# <a name="path-element"></a><span data-ttu-id="da1db-104">Path-Element</span><span class="sxs-lookup"><span data-stu-id="da1db-104">path element</span></span>

<span data-ttu-id="da1db-105">Gibt den Speicherort und den Dateinamen einer WSDL-Datei an.</span><span class="sxs-lookup"><span data-stu-id="da1db-105">Specifies the location and filename of a WSDL file.</span></span> <span data-ttu-id="da1db-106">Der Pfad kann ein absoluter oder relativer Pfad zur Datei sein, darf jedoch keine URL sein.</span><span class="sxs-lookup"><span data-stu-id="da1db-106">The path may be an absolute or relative path to the file, but must not be an URL.</span></span>

## <a name="usage"></a><span data-ttu-id="da1db-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="da1db-107">Usage</span></span>

``` syntax
<path/>
```

## <a name="attributes"></a><span data-ttu-id="da1db-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="da1db-108">Attributes</span></span>

<span data-ttu-id="da1db-109">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="da1db-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="da1db-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="da1db-110">Child elements</span></span>

<span data-ttu-id="da1db-111">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="da1db-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="da1db-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="da1db-112">Parent elements</span></span>



| <span data-ttu-id="da1db-113">Element</span><span class="sxs-lookup"><span data-stu-id="da1db-113">Element</span></span>                         | <span data-ttu-id="da1db-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da1db-114">Description</span></span>                                                             |
|---------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="da1db-115">**WSDL**</span><span class="sxs-lookup"><span data-stu-id="da1db-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="da1db-116">Eine WSDL-Datei, die für Vertragsinformationen verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="da1db-116">A WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="examples"></a><span data-ttu-id="da1db-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="da1db-117">Examples</span></span>

<span data-ttu-id="da1db-118">Der folgende XML-Code zeigt ein gültiges **path** -Element.</span><span class="sxs-lookup"><span data-stu-id="da1db-118">The following XML shows a valid **path** element.</span></span>

``` syntax
<path>"..\wsdls\example.wsdl"</path>
```

## <a name="element-information"></a><span data-ttu-id="da1db-119">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="da1db-119">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="da1db-120">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="da1db-120">Minimum supported system</span></span><br/> | <span data-ttu-id="da1db-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da1db-121">Windows Vista</span></span> |
| <span data-ttu-id="da1db-122">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="da1db-122">Can be empty</span></span>                        | <span data-ttu-id="da1db-123">Ja</span><span class="sxs-lookup"><span data-stu-id="da1db-123">Yes</span></span>           |



 

 




