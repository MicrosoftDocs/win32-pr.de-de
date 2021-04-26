---
description: Gibt an, ob WsdCodeGen versuchen soll, bestimmte generierte Felder automatisch als statisch zu kennzeichnen.
ms.assetid: 0c858567-e17a-46a0-b3ff-a0dc8089b0cd
title: autoStatic-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9414470f56021d475fb7cf52e570ac2793228445
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994927"
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



| Element                                     | BESCHREIBUNG                                                                          |
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



 

 




