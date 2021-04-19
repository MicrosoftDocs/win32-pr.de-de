---
description: Verhindert die Generierung von Import-Anweisungen für angegebene Ziele, die in einem wsdl:import-Element in einer WSDL-Datei benannt sind.
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: excludeImport-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf511a24ad4007deb886900843991364fcf03a5a
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380774"
---
# <a name="excludeimport-element"></a>excludeImport-Element

Verhindert die Generierung von Import-Anweisungen für angegebene Ziele, die in einem \<wsdl:import> -Element in einer WSDL-Datei benannt sind. Dies kann verwendet werden, um zu halten, dass WsdCodeGen bekannte Ziele wie die WS-Addressing- und WS-Eventing-Spezifikationen importiert, obwohl in der WSDL auf diese Ziele verwiesen wird.

Der Wert dieses Elements muss auf den Namespace mit dem Namen im \<wsdl:import> auszuschließenden Element festgelegt werden.

## <a name="usage"></a>Verwendung

``` syntax
<excludeImport/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | Beschreibung                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [**Wsdl**](wsdl.md)<br/> | Gibt eine WSDL-Datei an, die für Vertragsinformationen zu verarbeiten ist.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




