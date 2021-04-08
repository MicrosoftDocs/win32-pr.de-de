---
description: 'Verhindert die Generierung von Import-Anweisungen für angegebene Ziele, die in einem <WSDL: Import>-Element in einer WSDL-Datei genannt werden.'
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: excludeimport-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c08d8880029d9e03917e48b61561e3ab3eb2815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863999"
---
# <a name="excludeimport-element"></a>excludeimport-Element

Verhindert die Generierung von Import-Anweisungen für angegebene Ziele, die in einem <WSDL: Import>-Element in einer WSDL-Datei genannt werden. Dies kann verwendet werden, um zu verhindern, dass wsdcodegen bekannte Ziele importiert, wie z. b. die WS-Addressing-und WS-Eventing Spezifikationen, auch wenn in der WSDL auf diese Ziele verwiesen wird.

Der Wert dieses Elements muss auf den Namespace festgelegt werden, der im <WSDL: Import>-Elements benannt ist, das ausgeschlossen werden soll.

## <a name="usage"></a>Verbrauch

``` syntax
<excludeImport/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | BESCHREIBUNG                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [**WSDL**](wsdl.md)<br/> | Gibt eine WSDL-Datei an, die für Vertragsinformationen verarbeitet werden soll.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




