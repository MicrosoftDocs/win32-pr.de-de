---
description: Gibt den Speicherort und den Dateinamen einer WSDL-Datei an. Der Pfad kann ein absoluter oder relativer Pfad zur Datei sein, darf jedoch keine URL sein.
ms.assetid: 0664dcc6-1e71-46cf-9084-1adc84861b52
title: path-Element (Webdienste auf Geräten)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48df5a156149f00b8b153ccc0d46d6d2d34a1ce
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994307"
---
# <a name="path-element"></a><span data-ttu-id="7d301-104">path-Element</span><span class="sxs-lookup"><span data-stu-id="7d301-104">path element</span></span>

<span data-ttu-id="7d301-105">Gibt den Speicherort und den Dateinamen einer WSDL-Datei an.</span><span class="sxs-lookup"><span data-stu-id="7d301-105">Specifies the location and filename of a WSDL file.</span></span> <span data-ttu-id="7d301-106">Der Pfad kann ein absoluter oder relativer Pfad zur Datei sein, darf jedoch keine URL sein.</span><span class="sxs-lookup"><span data-stu-id="7d301-106">The path may be an absolute or relative path to the file, but must not be an URL.</span></span>

## <a name="usage"></a><span data-ttu-id="7d301-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="7d301-107">Usage</span></span>

``` syntax
<path/>
```

## <a name="attributes"></a><span data-ttu-id="7d301-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7d301-108">Attributes</span></span>

<span data-ttu-id="7d301-109">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="7d301-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="7d301-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7d301-110">Child elements</span></span>

<span data-ttu-id="7d301-111">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="7d301-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="7d301-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7d301-112">Parent elements</span></span>



| <span data-ttu-id="7d301-113">Element</span><span class="sxs-lookup"><span data-stu-id="7d301-113">Element</span></span>                         | <span data-ttu-id="7d301-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d301-114">Description</span></span>                                                             |
|---------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="7d301-115">**Wsdl**</span><span class="sxs-lookup"><span data-stu-id="7d301-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="7d301-116">Eine WSDL-Datei, die für Vertragsinformationen verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d301-116">A WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="examples"></a><span data-ttu-id="7d301-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7d301-117">Examples</span></span>

<span data-ttu-id="7d301-118">Der folgende XML-Code zeigt ein gültiges **Pfadelement.**</span><span class="sxs-lookup"><span data-stu-id="7d301-118">The following XML shows a valid **path** element.</span></span>

``` syntax
<path>"..\wsdls\example.wsdl"</path>
```

## <a name="element-information"></a><span data-ttu-id="7d301-119">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="7d301-119">Element information</span></span>



| <span data-ttu-id="7d301-120">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="7d301-120">Label</span></span> | <span data-ttu-id="7d301-121">Wert</span><span class="sxs-lookup"><span data-stu-id="7d301-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="7d301-122">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="7d301-122">Minimum supported system</span></span><br/> | <span data-ttu-id="7d301-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d301-123">Windows Vista</span></span> |
| <span data-ttu-id="7d301-124">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="7d301-124">Can be empty</span></span>                        | <span data-ttu-id="7d301-125">Ja</span><span class="sxs-lookup"><span data-stu-id="7d301-125">Yes</span></span>           |



 

 




