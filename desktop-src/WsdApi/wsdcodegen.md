---
description: Ist das Stamm Element einer XML-Skriptdatei des WSDAPI-Code-Generators.
ms.assetid: 3d40172b-6ba1-4e42-9a1a-519c8e88c2b1
title: wsdcodegen-Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656f2273926dc3420ec84d6b9f24759f8e3587e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353201"
---
# <a name="wsdcodegen-element"></a><span data-ttu-id="d403f-103">wsdcodegen-Element</span><span class="sxs-lookup"><span data-stu-id="d403f-103">wsdCodeGen element</span></span>

<span data-ttu-id="d403f-104">Ist das Stamm Element einer XML-Skriptdatei des WSDAPI-Code-Generators.</span><span class="sxs-lookup"><span data-stu-id="d403f-104">Is the root element of an WSDAPI code generator XML script file.</span></span>

## <a name="usage"></a><span data-ttu-id="d403f-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="d403f-105">Usage</span></span>

``` syntax
<wsdCodeGen
  ConfigFileVersion = "Any character string.">
  child elements
</wsdCodeGen>
```

## <a name="attributes"></a><span data-ttu-id="d403f-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="d403f-106">Attributes</span></span>



| <span data-ttu-id="d403f-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="d403f-107">Attribute</span></span>                        | <span data-ttu-id="d403f-108">type</span><span class="sxs-lookup"><span data-stu-id="d403f-108">Type</span></span>                             | <span data-ttu-id="d403f-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d403f-109">Required</span></span>       | <span data-ttu-id="d403f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d403f-110">Description</span></span>                                                                                  |
|----------------------------------|----------------------------------|----------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d403f-111">**Configfileversion**</span><span class="sxs-lookup"><span data-stu-id="d403f-111">**ConfigFileVersion**</span></span><br/> | <span data-ttu-id="d403f-112">Eine beliebige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d403f-112">Any character string.</span></span><br/> | <span data-ttu-id="d403f-113">Ja</span><span class="sxs-lookup"><span data-stu-id="d403f-113">Yes</span></span><br/> | <span data-ttu-id="d403f-114">Die Version der Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="d403f-114">The version of the configuration file.</span></span> <span data-ttu-id="d403f-115">Der einzige gültige Wert ist "1,0".</span><span class="sxs-lookup"><span data-stu-id="d403f-115">The only valid value is "1.0".</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="d403f-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d403f-116">Child elements</span></span>



| <span data-ttu-id="d403f-117">Element</span><span class="sxs-lookup"><span data-stu-id="d403f-117">Element</span></span>                                                         | <span data-ttu-id="d403f-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d403f-118">Description</span></span>                                                                                                                                                                                                                 |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d403f-119">**automatisch statisch**</span><span class="sxs-lookup"><span data-stu-id="d403f-119">**autoStatic**</span></span>](autostatic.md)<br/>                     | <span data-ttu-id="d403f-120">Gibt an, ob wsdcodegen versuchen soll, bestimmte generierte Felder automatisch als statisch zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="d403f-120">Indicates whether or not WsdCodeGen should try to automatically flag certain generated fields as static.</span></span> <span data-ttu-id="d403f-121">Diese Einstellung ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d403f-121">This is enabled by default.</span></span><br/> <br/>                                                                 |
| [<span data-ttu-id="d403f-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="d403f-122">**file**</span></span>](file.md)<br/>                                 | <span data-ttu-id="d403f-123">Weist den Code Generator an, eine Datei zu generieren.</span><span class="sxs-lookup"><span data-stu-id="d403f-123">Directs the code generator to generate a file.</span></span><br/> <br/>                                                                                                                                                       |
| [<span data-ttu-id="d403f-124">**hostmetadata**</span><span class="sxs-lookup"><span data-stu-id="d403f-124">**hostMetadata**</span></span>](hostmetadata.md)<br/>                 | <span data-ttu-id="d403f-125">Die hostingmetadaten für das Gerät, das implementiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d403f-125">The hosting metadata for the device to be implemented.</span></span> <span data-ttu-id="d403f-126">Dieses Element wird nur für Geräte Implementierungen (Hosts) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d403f-126">This element is used for device implementations (hosts) only.</span></span><br/> <br/>                                                                                 |
| [<span data-ttu-id="d403f-127">**layernumber**</span><span class="sxs-lookup"><span data-stu-id="d403f-127">**layerNumber**</span></span>](layernumber.md)<br/>                   | <span data-ttu-id="d403f-128">Die Anzahl der zu generierenden Code Schicht.</span><span class="sxs-lookup"><span data-stu-id="d403f-128">The number of the code layer to be generated.</span></span> <span data-ttu-id="d403f-129">Ebenennummern werden in Lauf Zeit Tabellen verwendet, um eine Codeebene für eine andere zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="d403f-129">Layer numbers are used in runtime tables to distinguish one layer of code for another.</span></span> <span data-ttu-id="d403f-130">WSDAPI selbst verwendet generierten Code mit einer Ebenennummer von 0.</span><span class="sxs-lookup"><span data-stu-id="d403f-130">WSDAPI itself uses generated code that has a layer number of 0.</span></span><br/> <br/> |
| [<span data-ttu-id="d403f-131">**layerprefix**</span><span class="sxs-lookup"><span data-stu-id="d403f-131">**layerPrefix**</span></span>](layerprefix.md)<br/>                   | <span data-ttu-id="d403f-132">Das Präfix, das im generierten Code verwendet werden soll, um die Eindeutigkeit generierter Symbole sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="d403f-132">The prefix to use in the generated code to assure uniqueness of generated symbols.</span></span> <span data-ttu-id="d403f-133">WSDAPI verwendet das Präfix "WSD".</span><span class="sxs-lookup"><span data-stu-id="d403f-133">WSDAPI uses the prefix "WSD".</span></span><br/> <br/>                                                                                     |
| [<span data-ttu-id="d403f-134">**Hilfen**</span><span class="sxs-lookup"><span data-stu-id="d403f-134">**macro**</span></span>](macro.md)<br/>                               | <span data-ttu-id="d403f-135">Definiert Text oder CDATA, der vom [**include**](include.md) -Element wieder verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d403f-135">Defines text or CDATA to be reused by the [**include**](include.md) element.</span></span><br/> <br/>                                                                                                                        |
| [<span data-ttu-id="d403f-136">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d403f-136">**nameSpace**</span></span>](namespace.md)<br/>                       | <span data-ttu-id="d403f-137">Beschreibt einen Namespace, der für die Codegenerierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d403f-137">Describes a namespace to be used for code generation.</span></span><br/> <br/>                                                                                                                                                |
| [<span data-ttu-id="d403f-138">**relationshipmetadata**</span><span class="sxs-lookup"><span data-stu-id="d403f-138">**relationshipMetadata**</span></span>](relationshipmetadata.md)<br/> | <span data-ttu-id="d403f-139">Beschreibt den Host und die gehosteten Metadaten für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="d403f-139">Describes the host and hosted metadata for the device.</span></span><br/> <br/>                                                                                                                                               |
| [<span data-ttu-id="d403f-140">**thismodelmetadata**</span><span class="sxs-lookup"><span data-stu-id="d403f-140">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/>       | <span data-ttu-id="d403f-141">Die Hersteller-und Modell Metadaten für das Gerät, das implementiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d403f-141">The manufacturer and model metadata for the device to be implemented.</span></span> <span data-ttu-id="d403f-142">Dieses Element wird nur für Geräte Implementierungen (Hosts) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d403f-142">This element is used for device implementations (hosts) only.</span></span><br/> <br/>                                                                  |
| [<span data-ttu-id="d403f-143">**WSDL**</span><span class="sxs-lookup"><span data-stu-id="d403f-143">**wsdl**</span></span>](wsdl.md)<br/>                                 | <span data-ttu-id="d403f-144">Gibt eine WSDL-Datei an, die für Vertragsinformationen verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d403f-144">Specifies a WSDL file to process for contract information.</span></span><br/> <br/>                                                                                                                                           |
| [<span data-ttu-id="d403f-145">**XSD**</span><span class="sxs-lookup"><span data-stu-id="d403f-145">**xsd**</span></span>](xsd.md)<br/>                                   | <span data-ttu-id="d403f-146">Gibt eine XSD-Datei an, die für Vertragsinformationen verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d403f-146">Specifies an XSD file to process for contract information.</span></span><br/> <br/>                                                                                                                                           |



### <a name="child-element-sequence"></a><span data-ttu-id="d403f-147">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="d403f-147">Child element sequence</span></span>

``` syntax
(
  layerNumber?, 
  layerPrefix?, 
  autoStatic?, 
  hostMetadata?, 
  thisModelMetadata?, 
  nameSpace*, 
  wsdl*, 
  xsd*, 
  file*, 
  macro*, 
  relationshipMetadata*
)
```

## <a name="parent-elements"></a><span data-ttu-id="d403f-148">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d403f-148">Parent elements</span></span>

<span data-ttu-id="d403f-149">Es gibt keine übergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="d403f-149">There are no parent elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="d403f-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d403f-150">Remarks</span></span>

<span data-ttu-id="d403f-151">Im Allgemeinen sollten [**Datei**](file.md) Elemente zuletzt auftreten, da Sie Code generieren, der die von den anderen Elementen angegebenen Daten verwendet.</span><span class="sxs-lookup"><span data-stu-id="d403f-151">In general, [**file**](file.md) elements should occur last because they generate code which uses data specified by the other elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="d403f-152">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="d403f-152">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="d403f-153">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="d403f-153">Minimum supported system</span></span><br/> | <span data-ttu-id="d403f-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d403f-154">Windows Vista</span></span> |
| <span data-ttu-id="d403f-155">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="d403f-155">Can be empty</span></span>                        | <span data-ttu-id="d403f-156">Ja</span><span class="sxs-lookup"><span data-stu-id="d403f-156">Yes</span></span>           |



 

 




