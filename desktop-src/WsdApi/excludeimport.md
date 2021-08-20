---
description: Verhindert die Generierung von Importanweisungen für angegebene Ziele, die in einem wsdl:import-Element in einer WSDL-Datei benannt sind.
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: excludeImport-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11ffc6c6ae6b0005de187afef7e8cbe7d36ca45a13350de1d4b59d40744ae980
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117920891"
---
# <a name="excludeimport-element"></a>excludeImport-Element

Verhindert die Generierung von Importanweisungen für angegebene Ziele, die in einem \<wsdl:import> -Element in einer WSDL-Datei benannt sind. Dadurch kann verhindert werden, dass WsdCodeGen bekannte Ziele importiert, z. B. die WS-Addressing und WS-Eventing Spezifikationen, obwohl auf diese Ziele in der WSDL verwiesen wird.

Der Wert dieses Elements muss auf den Namespace mit dem Namen im auszuschließenden Element festgelegt \<wsdl:import> werden.

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
| [**Wsdl**](wsdl.md)<br/> | Gibt eine WSDL-Datei an, die für Vertragsinformationen verarbeitet werden soll.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




