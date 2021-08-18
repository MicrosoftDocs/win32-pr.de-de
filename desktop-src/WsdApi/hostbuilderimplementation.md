---
description: Generiert eine Funktion, die einen typisierten Host erstellt.
ms.assetid: 2b4a4016-cc5d-4912-8e08-ce3a11ab0a06
title: hostBuilderImplementation-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042a288874a1829c36866c84ccb414db8c07233e199728006b4283920fe25ff0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856610"
---
# <a name="hostbuilderimplementation-element"></a>hostBuilderImplementation-Element

Generiert eine Funktion, die einen typisierten Host erstellt.

## <a name="usage"></a>Verbrauch

``` syntax
<hostBuilderImplementation>
  child elements
</hostBuilderImplementation>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                           | Beschreibung                                                      |
|---------------------------------------------------|------------------------------------------------------------------|
| [**hostedService**](hostedservice.md)<br/> | Der Dienst, der für den Host eingeschlossen werden soll. <br/> <br/> |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
hostedService+
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | Beschreibung                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Codegenerator aus.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




