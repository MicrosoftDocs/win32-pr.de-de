---
title: AmbientAttributes.accKeyboardShortcut
description: Das attribut accKeyboardShortcut gibt eine Tastenkombinationsbeschreibung für jedes Element an oder ruft diese ab.
ms.assetid: f97cffc9-4e7c-4226-9e02-0ea7f84b7450
keywords:
- AmbientAttributes.accKeyboardShortcut-Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.accKeyboardShortcut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f467304bb9f38ab0683440d2a0ebc5fcc51adb92fbb1d50e8275eb36f256a159
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055209"
---
# <a name="ambientattributesacckeyboardshortcut"></a>AmbientAttributes.accKeyboardShortcut

Das **attribut accKeyboardShortcut** gibt eine Tastenkombinationsbeschreibung für jedes Element an oder ruft diese ab.

``` syntax
        elementID.accKeyboardShortcut
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine  Zeichenfolge mit Lese-/Schreibzugriff mit dem Standardwert "" (leere Zeichenfolge). Für das **BUTTON-Element** hat dieses Attribut den Standardwert "Spacebar or Enter". Für das **SLIDER-Element** ist der Standardwert "Nach rechts/nach oben pfeil to increase, Left/Down Arrow to decrease".

## <a name="remarks"></a>Hinweise

Dieses Attribut wird für Barrierefreiheitszwecke verwendet. Es ermöglicht eine Beschreibung der Tastenkombination für jedes Element, das von einem Readerprogramm laut vorgelesen werden kann. Mit diesem Attribut wird die Verknüpfung nicht festgelegt. Der Skripter muss diese Arbeit ausführen.

Dieses Attribut gilt auch für Schaltflächenelemente innerhalb des Schaltflächengruppen-Steuerelements.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> </dl>

 

 





