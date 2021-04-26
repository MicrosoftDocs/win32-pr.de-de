---
description: Generiert eine Deklaration für eine Funktion, die einen typisierten Host erstellt.
ms.assetid: 3c08e913-b47e-4ca7-b8bc-7b036e57db01
title: hostBuilderDeclaration-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf3ddd474b4000b053b49157f1fc4b2eb399d34
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994907"
---
# <a name="hostbuilderdeclaration-element"></a>hostBuilderDeclaration-Element

Generiert eine Deklaration für eine Funktion, die einen typisierten Host erstellt.

## <a name="usage"></a>Verbrauch

``` syntax
<hostBuilderDeclaration>
  child elements
</hostBuilderDeclaration>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                   | BESCHREIBUNG                                                                                                                                                                                                                  |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Schnittstelle**](interface.md)<br/> | Der Name der Dienstschnittstelle, die für den Host eingeschlossen werden soll. Der Wert dieses Elements muss mit dem Wert des [**untergeordneten Schnittstellenelements**](interface.md) von [**hostedService**](hostedservice.md)übereinstimmen. <br/> <br/> |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
interface+
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



 

 




