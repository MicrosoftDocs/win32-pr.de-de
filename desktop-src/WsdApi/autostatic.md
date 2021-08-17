---
description: Gibt an, ob WsdCodeGen versuchen soll, bestimmte generierte Felder automatisch als statisch zu kennzeichnen.
ms.assetid: 0c858567-e17a-46a0-b3ff-a0dc8089b0cd
title: autoStatic-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f6b9a447e964c90354c909fc0399276d8ed69e7d1dfb3a493d5590a6470d0cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738673"
---
# <a name="autostatic-element"></a>autoStatic-Element

Gibt an, ob WsdCodeGen versuchen soll, bestimmte generierte Felder automatisch als statisch zu kennzeichnen. Dieses Verhalten ist standardmäßig aktiviert.

## <a name="usage"></a>Verbrauch

``` syntax
<autoStatic/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                     | Beschreibung                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Das Stammelement einer XML-Skriptdatei des WSDAPI-Codegenerators.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Das **autoStatic-Element** ist nicht erforderlich und kann in der XML-Konfigurationsdatei ausgelassen werden. Das -Element kann verwendet werden, um das Kennzeichnen von generierten Feldern als statisch zu deaktivieren oder das Kennzeichnen bestimmter generierter Felder explizit als statisch zu erzwingen.

Mögliche Werte sind 1 (aktiviert, Standard) und 0 (deaktiviert). Die Aktivierung **von autoStatic** kann zu Kompilierungsproblemen führen, je nachdem, wie der Codegenerator an Ausgabedaten geleitet wird.

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




