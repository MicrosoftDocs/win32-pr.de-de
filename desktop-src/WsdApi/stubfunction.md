---
description: Gibt an, ob Stubfunktionsverweise in die Vorgangsstrukturen in den Porttypdefinitionen für ein- und zweigefinge Vorgänge eingeschlossen werden sollen.
ms.assetid: 2547f71d-8a30-4df8-ba38-6707c415708e
title: stubFunction-Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9304aa33bd193edc631949a93e1d770a1fade3d0c5726a9f2d897ea1862476
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118552411"
---
# <a name="stubfunction-element"></a>stubFunction-Element

Gibt an, ob Stubfunktionsverweise in die Vorgangsstrukturen in den Porttypdefinitionen für ein- und zweigefinge Vorgänge eingeschlossen werden sollen.

## <a name="usage"></a>Verbrauch

``` syntax
<stubFunction/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                       | Beschreibung                                                  |
|---------------------------------------------------------------|--------------------------------------------------------------|
| [**portTypeDefinitions**](porttypedefinitions.md)<br/> | Generiert C-Konstanten für Porttypen.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Stubfunktionsverweise werden in Hostingszenarien für one-way- und two-way-Vorgänge verwendet.

Gültige Werte für dieses Element sind 1 (TRUE/Stubfunktionsverweise eingeschlossen) und 0 (FALSE/keine Stubfunktionsverweise enthalten).

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




