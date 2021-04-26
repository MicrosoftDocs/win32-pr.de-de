---
description: Beschreibt einen Namespace.
ms.assetid: 8e31526a-639f-481b-91f1-fcd376818cbf
title: nameSpace-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c3e2735efbb99fbe404f2531336c2e2bd0f89d7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994277"
---
# <a name="namespace-element"></a>nameSpace-Element

Beschreibt einen Namespace. Dieser Namespace kann für die Codegenerierung oder für die Behandlung von -Anweisungen verwendet \<wsdl:import> werden.

## <a name="usage"></a>Verbrauch

``` syntax
<nameSpace
  uri = "character_string">
  child elements
</nameSpace>
```

## <a name="attributes"></a>Attribute



| Attribut          | type                         | Erforderlich       | BESCHREIBUNG                                             |
|--------------------|------------------------------|----------------|---------------------------------------------------------|
| **uri**<br/> | Zeichenfolge \_<br/> | Ja<br/> | Der eindeutige URI des Namespace.<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                               | BESCHREIBUNG                                                                                              |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**Codename**](codename.md)<br/>               | Der Name, der verwendet werden soll, um den Namespace im generierten Code zu identifizieren.<br/> <br/>                  |
| [**macroPrefix**](macroprefix.md)<br/>         | Das Präfix, das im generierten Code für Namen von Makros im Namespace verwendet werden soll.<br/> <br/> |
| [**Namen**](name.md)<br/>                       | Ein qualifizierter Name im Namespace.<br/> <br/>                                                |
| [**preferredPrefix**](preferredprefix.md)<br/> | Das Präfix, dem der Namespace zugeordnet werden soll, um den XML-Code lesbarer zu machen.<br/> <br/> |



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



| Element                                     | BESCHREIBUNG                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Das Stammelement einer WSDAPI-Codegenerator-XML-Skriptdatei.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Dieses Element kann verwendet werden, um dem Codegenerator zusätzliche Informationen zu Namespaces bereitzustellen, die in WSDL- und XSD-Dateien auftreten, oder um neue Namespaces einzuführen.

Namespaces, die durch Typreflektion impliziert oder in WSDL- und XSD-Dateien angegeben sind, werden automatisch vom Codegenerator analysiert und müssen nicht explizit im Skript definiert werden. In einigen Fällen kann dieses Element verwendet werden, um einem Namespace, auf den durch Typreflektion oder WSDL/XSD verwiesen wird, zusätzliche Eigenschaften oder Namen hinzuzufügen. Der Codegenerator betrachtet dies nicht als Konflikt.

Der folgende XML-Code zeigt ein nameSpace-Element (bei dem aus Kürze die unteren Elemente weggelassen werden).

``` syntax
<nameSpace uri="https://www.example.com/namespace">
  ...
</nameSpace>
```

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




