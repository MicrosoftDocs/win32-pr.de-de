---
description: Gibt eine lokalisierte Version des Herstellernamens an.
ms.assetid: e87de50f-60ec-4c18-b21c-81f7b6928752
title: manufacturerLS-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d24950355c5439d9a99c4ef451f1330772f3459
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993677"
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



| Attribut               | type                                          | Erforderlich       | Beschreibung                                                             |
|-------------------------|-----------------------------------------------|----------------|-------------------------------------------------------------------------|
| **Data**<br/>     | Lokalisierte Name-Zeichenfolge des Herstellers<br/> | Ja<br/> | Der lokalisierte Herstellername.<br/> <br/>                 |
| **Sprache**<br/> | Sprachbezeichnerzeichenfolge<br/>         | Ja<br/> | Die Sprache des lokalisierten Herstellernamens.<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                   | BESCHREIBUNG                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**thisModelMetadata**](thismodelmetadata.md)<br/> | Definiert die Hersteller- und Modellmetadaten für das zu implementierte Gerät.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




