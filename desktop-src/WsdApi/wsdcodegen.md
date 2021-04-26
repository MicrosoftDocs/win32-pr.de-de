---
description: Das Stammelement einer WSDAPI-Codegenerator-XML-Skriptdatei.
ms.assetid: 3d40172b-6ba1-4e42-9a1a-519c8e88c2b1
title: wsdCodeGen-Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9861617854e0e75575f2993717f5b2a86515fb0f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994677"
---
# <a name="wsdcodegen-element"></a><span data-ttu-id="11a4f-103">wsdCodeGen-Element</span><span class="sxs-lookup"><span data-stu-id="11a4f-103">wsdCodeGen element</span></span>

<span data-ttu-id="11a4f-104">Das Stammelement einer WSDAPI-Codegenerator-XML-Skriptdatei.</span><span class="sxs-lookup"><span data-stu-id="11a4f-104">Is the root element of an WSDAPI code generator XML script file.</span></span>

## <a name="usage"></a><span data-ttu-id="11a4f-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="11a4f-105">Usage</span></span>

``` syntax
<wsdCodeGen
  ConfigFileVersion = "Any character string.">
  child elements
</wsdCodeGen>
```

## <a name="attributes"></a><span data-ttu-id="11a4f-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="11a4f-106">Attributes</span></span>



| <span data-ttu-id="11a4f-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="11a4f-107">Attribute</span></span>                        | <span data-ttu-id="11a4f-108">type</span><span class="sxs-lookup"><span data-stu-id="11a4f-108">Type</span></span>                             | <span data-ttu-id="11a4f-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="11a4f-109">Required</span></span>       | <span data-ttu-id="11a4f-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11a4f-110">Description</span></span>                                                                                  |
|----------------------------------|----------------------------------|----------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="11a4f-111">**ConfigFileVersion**</span><span class="sxs-lookup"><span data-stu-id="11a4f-111">**ConfigFileVersion**</span></span><br/> | <span data-ttu-id="11a4f-112">Eine beliebige Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="11a4f-112">Any character string.</span></span><br/> | <span data-ttu-id="11a4f-113">Ja</span><span class="sxs-lookup"><span data-stu-id="11a4f-113">Yes</span></span><br/> | <span data-ttu-id="11a4f-114">Die Version der Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="11a4f-114">The version of the configuration file.</span></span> <span data-ttu-id="11a4f-115">Der einzige gültige Wert ist "1.0".</span><span class="sxs-lookup"><span data-stu-id="11a4f-115">The only valid value is "1.0".</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="11a4f-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="11a4f-116">Child elements</span></span>



| <span data-ttu-id="11a4f-117">Element</span><span class="sxs-lookup"><span data-stu-id="11a4f-117">Element</span></span>                                                         | <span data-ttu-id="11a4f-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11a4f-118">Description</span></span>                                                                                                                                                                                                                 |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11a4f-119">**autoStatic**</span><span class="sxs-lookup"><span data-stu-id="11a4f-119">**autoStatic**</span></span>](autostatic.md)<br/>                     | <span data-ttu-id="11a4f-120">Gibt an, ob WsdCodeGen versuchen soll, bestimmte generierte Felder automatisch als statisch zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="11a4f-120">Indicates whether or not WsdCodeGen should try to automatically flag certain generated fields as static.</span></span> <span data-ttu-id="11a4f-121">Diese Einstellung ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="11a4f-121">This is enabled by default.</span></span><br/> <br/>                                                                 |
| [<span data-ttu-id="11a4f-122">**Datei**</span><span class="sxs-lookup"><span data-stu-id="11a4f-122">**file**</span></span>](file.md)<br/>                                 | <span data-ttu-id="11a4f-123">Weist den Codegenerator an, eine Datei zu generieren.</span><span class="sxs-lookup"><span data-stu-id="11a4f-123">Directs the code generator to generate a file.</span></span><br/> <br/>                                                                                                                                                       |
| [<span data-ttu-id="11a4f-124">**hostMetadata**</span><span class="sxs-lookup"><span data-stu-id="11a4f-124">**hostMetadata**</span></span>](hostmetadata.md)<br/>                 | <span data-ttu-id="11a4f-125">Die Hostingmetadaten für das zu implementierende Gerät.</span><span class="sxs-lookup"><span data-stu-id="11a4f-125">The hosting metadata for the device to be implemented.</span></span> <span data-ttu-id="11a4f-126">Dieses Element wird nur für Geräteimplementierungen (Hosts) verwendet.</span><span class="sxs-lookup"><span data-stu-id="11a4f-126">This element is used for device implementations (hosts) only.</span></span><br/> <br/>                                                                                 |
| [<span data-ttu-id="11a4f-127">**layerNumber**</span><span class="sxs-lookup"><span data-stu-id="11a4f-127">**layerNumber**</span></span>](layernumber.md)<br/>                   | <span data-ttu-id="11a4f-128">Die Nummer der zu generierenden Codeebene.</span><span class="sxs-lookup"><span data-stu-id="11a4f-128">The number of the code layer to be generated.</span></span> <span data-ttu-id="11a4f-129">Ebenennummern werden in Laufzeittabellen verwendet, um eine Codeebene für eine andere zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="11a4f-129">Layer numbers are used in runtime tables to distinguish one layer of code for another.</span></span> <span data-ttu-id="11a4f-130">WSDAPI selbst verwendet generierten Code, der über eine Ebenennummer von 0 verfügt.</span><span class="sxs-lookup"><span data-stu-id="11a4f-130">WSDAPI itself uses generated code that has a layer number of 0.</span></span><br/> <br/> |
| [<span data-ttu-id="11a4f-131">**layerPrefix**</span><span class="sxs-lookup"><span data-stu-id="11a4f-131">**layerPrefix**</span></span>](layerprefix.md)<br/>                   | <span data-ttu-id="11a4f-132">Das Präfix, das im generierten Code verwendet werden soll, um die Eindeutigkeit generierter Symbole sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="11a4f-132">The prefix to use in the generated code to assure uniqueness of generated symbols.</span></span> <span data-ttu-id="11a4f-133">WSDAPI verwendet das Präfix "WSD".</span><span class="sxs-lookup"><span data-stu-id="11a4f-133">WSDAPI uses the prefix "WSD".</span></span><br/> <br/>                                                                                     |
| [<span data-ttu-id="11a4f-134">**Makro**</span><span class="sxs-lookup"><span data-stu-id="11a4f-134">**macro**</span></span>](macro.md)<br/>                               | <span data-ttu-id="11a4f-135">Definiert Text oder CDATA, der vom include-Element wiederverwendet [**werden**](include.md) soll.</span><span class="sxs-lookup"><span data-stu-id="11a4f-135">Defines text or CDATA to be reused by the [**include**](include.md) element.</span></span><br/> <br/>                                                                                                                        |
| [<span data-ttu-id="11a4f-136">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="11a4f-136">**nameSpace**</span></span>](namespace.md)<br/>                       | <span data-ttu-id="11a4f-137">Beschreibt einen Namespace, der für die Codegenerierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="11a4f-137">Describes a namespace to be used for code generation.</span></span><br/> <br/>                                                                                                                                                |
| [<span data-ttu-id="11a4f-138">**relationshipMetadata**</span><span class="sxs-lookup"><span data-stu-id="11a4f-138">**relationshipMetadata**</span></span>](relationshipmetadata.md)<br/> | <span data-ttu-id="11a4f-139">Beschreibt den Host und die gehosteten Metadaten für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="11a4f-139">Describes the host and hosted metadata for the device.</span></span><br/> <br/>                                                                                                                                               |
| [<span data-ttu-id="11a4f-140">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="11a4f-140">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/>       | <span data-ttu-id="11a4f-141">Die Hersteller- und Modellmetadaten für das zu implementierte Gerät.</span><span class="sxs-lookup"><span data-stu-id="11a4f-141">The manufacturer and model metadata for the device to be implemented.</span></span> <span data-ttu-id="11a4f-142">Dieses Element wird nur für Geräteimplementierungen (Hosts) verwendet.</span><span class="sxs-lookup"><span data-stu-id="11a4f-142">This element is used for device implementations (hosts) only.</span></span><br/> <br/>                                                                  |
| [<span data-ttu-id="11a4f-143">**Wsdl**</span><span class="sxs-lookup"><span data-stu-id="11a4f-143">**wsdl**</span></span>](wsdl.md)<br/>                                 | <span data-ttu-id="11a4f-144">Gibt eine WSDL-Datei an, die für Vertragsinformationen zu verarbeiten ist.</span><span class="sxs-lookup"><span data-stu-id="11a4f-144">Specifies a WSDL file to process for contract information.</span></span><br/> <br/>                                                                                                                                           |
| [<span data-ttu-id="11a4f-145">**Xsd**</span><span class="sxs-lookup"><span data-stu-id="11a4f-145">**xsd**</span></span>](xsd.md)<br/>                                   | <span data-ttu-id="11a4f-146">Gibt eine XSD-Datei an, die für Vertragsinformationen zu verarbeiten ist.</span><span class="sxs-lookup"><span data-stu-id="11a4f-146">Specifies an XSD file to process for contract information.</span></span><br/> <br/>                                                                                                                                           |



### <a name="child-element-sequence"></a><span data-ttu-id="11a4f-147">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="11a4f-147">Child element sequence</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="11a4f-148">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="11a4f-148">Parent elements</span></span>

<span data-ttu-id="11a4f-149">Es gibt keine übergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="11a4f-149">There are no parent elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="11a4f-150">Hinweise</span><span class="sxs-lookup"><span data-stu-id="11a4f-150">Remarks</span></span>

<span data-ttu-id="11a4f-151">Im Allgemeinen sollten [**Dateielemente**](file.md) zuletzt auftreten, da sie Code generieren, der die von den anderen Elementen angegebenen Daten verwendet.</span><span class="sxs-lookup"><span data-stu-id="11a4f-151">In general, [**file**](file.md) elements should occur last because they generate code which uses data specified by the other elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="11a4f-152">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="11a4f-152">Element information</span></span>



| <span data-ttu-id="11a4f-153">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="11a4f-153">Label</span></span> | <span data-ttu-id="11a4f-154">Wert</span><span class="sxs-lookup"><span data-stu-id="11a4f-154">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="11a4f-155">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="11a4f-155">Minimum supported system</span></span><br/> | <span data-ttu-id="11a4f-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11a4f-156">Windows Vista</span></span> |
| <span data-ttu-id="11a4f-157">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="11a4f-157">Can be empty</span></span>                        | <span data-ttu-id="11a4f-158">Ja</span><span class="sxs-lookup"><span data-stu-id="11a4f-158">Yes</span></span>           |



 

 




