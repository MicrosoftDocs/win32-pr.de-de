---
description: Beschreibt einen Namespace.
ms.assetid: 8e31526a-639f-481b-91f1-fcd376818cbf
title: Namespace-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a8747a25988b880d5287d959273fa0f4d144045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528580"
---
# <a name="namespace-element"></a>Namespace-Element

Beschreibt einen Namespace. Dieser Namespace kann für die Codegenerierung oder für die Behandlung von <WSDL: Import-> Direktiven verwendet werden.

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
| **uri**<br/> | Zeichen \_ Folge<br/> | Ja<br/> | Der eindeutige URI des Namespace.<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                               | BESCHREIBUNG                                                                                              |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**codeName**](codename.md)<br/>               | Der Name, der zum Identifizieren des Namespace in generiertem Code verwendet werden soll.<br/> <br/>                  |
| [**makroprefix**](macroprefix.md)<br/>         | Das Präfix, das im generierten Code für Namen von Makros im-Namespace verwendet werden soll.<br/> <br/> |
| [**Benennen**](name.md)<br/>                       | Ein qualifizierter Name im-Namespace.<br/> <br/>                                                |
| [**preferredprefix**](preferredprefix.md)<br/> | Das Präfix, dem der Namespace zugeordnet werden soll, um den XML-Code lesbarer zu machen.<br/> <br/> |



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
| [**wsdcodegen**](wsdcodegen.md)<br/> | Das Stamm Element einer XML-Skriptdatei des WSDAPI-Code-Generators.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Dieses Element kann verwendet werden, um dem Code Generator zusätzliche Informationen zu Namespaces, die in WSDL-und XSD-Dateien auftreten, oder zum Einführen neuer Namespaces bereitzustellen.

Namespaces, die durch eine Typreflektion oder in WSDL-und XSD-Dateien angegeben werden, werden automatisch vom Code-Generator analysiert und müssen nicht explizit im Skript definiert werden. In einigen Fällen kann dieses Element verwendet werden, um einem Namespace, auf den von der Typreflektion oder WSDL/XSD verwiesen wird, zusätzliche Eigenschaften oder Namen hinzuzufügen. Der Code-Generator berücksichtigt dies nicht als Konflikt.

Der folgende XML-Code zeigt ein Namespace-Element (mit untergeordneten Elementen, die ausgelassen werden).

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



 

 




