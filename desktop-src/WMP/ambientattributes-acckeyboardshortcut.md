---
title: Ambientattribute. accKeyboardShortcut
description: Das accKeyboardShortcut-Attribut gibt eine Tastenkombination für ein beliebiges Element an oder ruft diese ab.
ms.assetid: f97cffc9-4e7c-4226-9e02-0ea7f84b7450
keywords:
- Ambientattribute. accKeyboardShortcut-Fenster Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.accKeyboardShortcut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67d7259f0b32e3575d902a83b6508383361028d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368365"
---
# <a name="ambientattributesacckeyboardshortcut"></a>Ambientattribute. accKeyboardShortcut

Das **accKeyboardShortcut** -Attribut gibt eine Tastenkombination für ein beliebiges Element an oder ruft diese ab.

``` syntax
        elementID.accKeyboardShortcut
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** mit dem Standardwert "" (leere Zeichenfolge). Für das **Button** -Element hat dieses Attribut den Standardwert "Leertaste oder Eingabetaste". Der Standardwert für das **Slider** -Element ist "rechter/Pfeil nach oben, um zu vergrößern, nach-unten/Pfeil nach unten".

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird für Barrierefreiheits Zwecke verwendet. Sie ermöglicht es, dass eine Beschreibung der Tastenkombination für ein beliebiges Element von einem Reader-Programm gelesen wird. Dieses Attribut legt die Verknüpfung nicht fest. Das Skript muss dies tun.

Dieses Attribut gilt auch für Schaltflächen Elemente innerhalb des Steuer Elements der Schaltflächen Gruppe.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> </dl>

 

 





