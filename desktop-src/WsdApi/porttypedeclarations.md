---
description: Generiert C-Konstantendeklarationen für Porttypen.
ms.assetid: 05a06206-3cc4-428d-b9f2-b7945e63922c
title: portTypeDeclarations-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e19780d4a48c95cd47872b0428b368e6b7e99887
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996557"
---
# <a name="porttypedeclarations-element"></a>portTypeDeclarations-Element

Generiert C-Konstantendeklarationen für Porttypen.

## <a name="usage"></a>Verbrauch

``` syntax
<portTypeDeclarations>
  child elements
</portTypeDeclarations>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                   | BESCHREIBUNG                                                                                                                                                               |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Codename**](codename.md)<br/>   | Gibt den Namen an, der für den Porttyp im generierten Code verwendet werden soll. Standardmäßig wird der Codename aus dem qualifizierten Namen des Porttyps generiert.<br/> <br/> |
| [**Vorgang**](operation.md)<br/> | Gibt einen Vorgang an, für den Code generiert werden soll.<br/> <br/>                                                                                          |
| [**Porttype**](porttype.md)<br/>   | Gibt den Porttyp an, für den Code generiert werden soll.<br/> <br/>                                                                                         |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  portType?, 
  operation*, 
  codeName?
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | BESCHREIBUNG                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Codegenerator aus.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Auf Porttypdeklarationen wird von der Anwendung und einem großen Teil des generierten Codes verwiesen. Dieses Element wird verwendet, um Includedateien zu generieren.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




