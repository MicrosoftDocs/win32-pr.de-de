---
description: Gibt eine lokalisierte Version des Herstellernamens an.
ms.assetid: e87de50f-60ec-4c18-b21c-81f7b6928752
title: manufacturerLS-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5b6922e0d914048003b976ecf1f9a7b82febc2a9802334f1a125e357985e319
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794030"
---
# <a name="manufacturerls-element"></a>manufacturerLS-Element

Gibt eine lokalisierte Version des Herstellernamens an.

## <a name="usage"></a>Verbrauch

``` syntax
<manufacturerLS
  Language = "language identifier string"
  Data = "localized manufacturer name string"/>
```

## <a name="attributes"></a>Attribute



| attribute               | type                                          | Erforderlich       | Beschreibung                                                             |
|-------------------------|-----------------------------------------------|----------------|-------------------------------------------------------------------------|
| **Data**<br/>     | lokalisierte Herstellernamenszeichenfolge<br/> | Ja<br/> | Der lokalisierte Herstellername.<br/> <br/>                 |
| **Sprache**<br/> | Sprachenbezeichnerzeichenfolge<br/>         | Ja<br/> | Die Sprache des lokalisierten Herstellernamens.<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                   | BESCHREIBUNG                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**thisModelMetadata**](thismodelmetadata.md)<br/> | Definiert die Hersteller- und Modellmetadaten für das zu implementierende Gerät.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




