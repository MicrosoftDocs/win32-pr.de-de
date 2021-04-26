---
description: Generiert eine Funktion, die einen typierten Host erstellt.
ms.assetid: 2b4a4016-cc5d-4912-8e08-ce3a11ab0a06
title: hostBuilderImplementation-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d333287acd199f4fe2aa8967a1b8d6458ff3ae
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994917"
---
# <a name="hostbuilderimplementation-element"></a>hostBuilderImplementation-Element

Generiert eine Funktion, die einen typierten Host erstellt.

## <a name="usage"></a>Verbrauch

``` syntax
<hostBuilderImplementation>
  child elements
</hostBuilderImplementation>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                           | BESCHREIBUNG                                                      |
|---------------------------------------------------|------------------------------------------------------------------|
| [**hostedService**](hostedservice.md)<br/> | Der Dienst, der für den Host eingeschlossen werden soll. <br/> <br/> |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
hostedService+
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | BESCHREIBUNG                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Codegenerator aus.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




