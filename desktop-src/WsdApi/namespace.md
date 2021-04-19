---
description: Beschreibt einen Namespace.
ms.assetid: 8e31526a-639f-481b-91f1-fcd376818cbf
title: nameSpace-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2414919f699bb60c2cf1e48bc52030c36cf67a0
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380844"
---
# <a name="namespace-element"></a>nameSpace-Element

Beschreibt einen Namespace. Dieser Namespace kann für die Codegenerierung oder für die Verarbeitung von Direktiven \<wsdl:import> verwendet werden.

## <a name="usage"></a>Verwendung

``` syntax
<nameSpace
  uri = "character_string">
  child elements
</nameSpace>
```

## <a name="attributes"></a>Attribute



| Attribut          | type                         | Erforderlich       | Beschreibung                                             |
|--------------------|------------------------------|----------------|---------------------------------------------------------|
| **uri**<br/> | \_Zeichenfolge<br/> | Ja<br/> | Der eindeutige URI des Namespace.<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                               | Beschreibung                                                                                              |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**Codename**](codename.md)<br/>               | Der Name, der verwendet werden soll, um den Namespace im generierten Code zu identifizieren.<br/> <br/>                  |
| [**macroPrefix**](macroprefix.md)<br/>         | Das Präfix, das im generierten Code für Die Namen von Makros im Namespace verwendet werden soll.<br/> <br/> |
| [**Namen**](name.md)<br/>                       | Ein qualifizierter Name im Namespace.<br/> <br/>                                                |
| [**preferredPrefix**](preferredprefix.md)<br/> | Das Präfix, dem der Namespace zugeordnet werden soll, damit der XML-Code besser lesbar ist.<br/> <br/> |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  preferredPrefix?, 
  macroPrefix?, 
  codeName?, 
  name*
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                     | Beschreibung                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Das Stammelement einer XML-Skriptdatei des WSDAPI-Codegenerators.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Dieses Element kann verwendet werden, um dem Codegenerator zusätzliche Informationen zu Namespaces zur Verfügung zu stellen, auf die es in WSDL- und XSD-Dateien trifft, oder um neue Namespaces einzuführen.

Namespaces, die durch Typlektion impliziert oder in WSDL- und XSD-Dateien angegeben werden, werden automatisch vom Codegenerator analysiert und müssen nicht explizit im Skript definiert werden. In einigen Fällen kann dieses Element verwendet werden, um zusätzliche Eigenschaften oder Namen zu einem Namespace hinzuzufügen, auf den durch Typlektion oder WSDL/XSD verwiesen wird. Der Codegenerator betrachtet dies nicht als Konflikt.

Der folgende XML-Code zeigt ein nameSpace-Element (mit untergeordneten Elementen, die aus Gründen der Kürze ausgelassen werden).

``` syntax
<nameSpace uri="https://www.example.com/namespace">
  ...
</nameSpace>
```

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




