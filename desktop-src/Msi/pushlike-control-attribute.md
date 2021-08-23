---
description: Wenn dieses Bit für ein Kontrollkästchen oder eine Optionsfeldgruppe festgelegt ist, wird die Schaltfläche mit der Darstellung einer Schaltfläche gezeichnet, die Logik bleibt jedoch gleich. Wenn das Bit nicht festgelegt ist, werden die Steuerelemente im üblichen Stil gezeichnet.
ms.assetid: c30b383a-7fae-413a-a6e6-8e958009f10c
title: PushLike-Steuerelementattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ab516038538849ac97d273d5fb3ede2be5be17417c48cf9a5624af98789867c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692479"
---
# <a name="pushlike-control-attribute"></a>PushLike-Steuerelementattribut

Wenn dieses Bit für ein Kontrollkästchen oder eine Optionsfeldgruppe festgelegt ist, wird die Schaltfläche mit der Darstellung einer Schaltfläche gezeichnet, die Logik bleibt jedoch gleich. Wenn das Bit nicht festgelegt ist, werden die Steuerelemente im üblichen Stil gezeichnet.

## <a name="valid-controls"></a>Gültige Steuerelemente

[CheckBox](checkbox-control.md)[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                           |
|---------|-------------|------------------------------------|
| 131072  | 0x00020000  | **msidbControlAttributesPushLike** |



 

## <a name="remarks"></a>Hinweise

Um dieses Attribut für ein Steuerelement festlegen zu können, schließen Sie das PushLike-Bit in die Spalte Attribute des Datensatzes des Steuerelements in die [Control-Tabelle ein.](control-table.md)

Weitere Informationen [finden Sie unter Steuerelementattribute](control-attributes.md) und [Steuerelemente.](controls.md)

 

 



