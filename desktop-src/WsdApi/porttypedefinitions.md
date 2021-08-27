---
description: Generiert C-Konstanten für Porttypen.
ms.assetid: 6ad0d163-df51-48b6-aad7-a4b018688872
title: portTypeDefinitions-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9beb5b6697f53ecc3a9f7c805338c6ccebd9901d483607b100f5d1602ff4c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071390"
---
# <a name="porttypedefinitions-element"></a>portTypeDefinitions-Element

Generiert C-Konstanten für Porttypen.

## <a name="usage"></a>Verwendung

``` syntax
<portTypeDefinitions>
  child elements
</portTypeDefinitions>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                   | BESCHREIBUNG                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Codename**](codename.md)<br/>                   | Gibt den Namen an, der für den Porttyp im generierten Code verwendet werden soll. Standardmäßig wird der Codename aus dem qualifizierten Namen des Porttyps generiert.<br/> <br/>         |
| [**eventStubFunction**](eventstubfunction.md)<br/> | Gibt an, ob Stubfunktionsverweise in den Vorgangsstrukturen in den Porttypdefinitionen für Benachrichtigungsvorgänge enthalten sein sollen.<br/> <br/>        |
| [**Vorgang**](operation.md)<br/>                 | Gibt einen Vorgang an, für den Code generiert werden soll.<br/> <br/>                                                                                                  |
| [**Porttype**](porttype.md)<br/>                   | Gibt den Porttyp an, für den Code generiert werden soll.<br/> <br/>                                                                                                 |
| [**stubFunction**](stubfunction.md)<br/>           | Gibt an, ob Stubfunktionsverweise in den Vorgangsstrukturen in den Porttypdefinitionen für ein- und zweiseitige Vorgänge enthalten sein sollen.<br/> <br/> |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  portType?, 
  operation*, 
  stubFunction?, 
  eventStubFunction?, 
  codeName?
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | BESCHREIBUNG                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Codegenerator aus.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Dieses Element wird in der Regel in C-Quelldateien verwendet, um die von [**portTypeDeclarations deklarierten**](porttypedeclarations.md)Porttypkonstanten bereitzustellen.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




