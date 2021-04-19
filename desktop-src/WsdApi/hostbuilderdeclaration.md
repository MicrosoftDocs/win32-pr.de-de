---
description: Generiert eine Deklaration für eine Funktion, mit der ein typisierter Host erstellt wird.
ms.assetid: 3c08e913-b47e-4ca7-b8bc-7b036e57db01
title: hostbuilderdeclaration-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16576050efc76264f42dff6a19549f69933185b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352503"
---
# <a name="hostbuilderdeclaration-element"></a>hostbuilderdeclaration-Element

Generiert eine Deklaration für eine Funktion, mit der ein typisierter Host erstellt wird.

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
| [**Schnittstelle**](interface.md)<br/> | Der Name der Dienst Schnittstelle, die für den Host eingeschlossen werden soll. Der Wert dieses Elements muss mit dem Wert des untergeordneten [**Schnitt**](interface.md) stellen-Elements von " [**hustedservice**](hostedservice.md)" identisch sein. <br/> <br/> |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
interface+
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | BESCHREIBUNG                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Code-Generator aus.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




