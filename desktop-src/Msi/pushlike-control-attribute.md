---
description: Wenn dieses Bit in einem Kontrollkästchen oder einer Optionsfeld Gruppe festgelegt ist, wird die Schaltfläche mit der Darstellung einer Schaltfläche "Push" gezeichnet, aber die Logik bleibt unverändert. Wenn das-Bit nicht festgelegt ist, werden die Steuerelemente in Ihrem üblichen Stil gezeichnet.
ms.assetid: c30b383a-7fae-413a-a6e6-8e958009f10c
title: Pushlike-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839adfceb0484bc908b8c8c6d14616cfd03acdb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351664"
---
# <a name="pushlike-control-attribute"></a>Pushlike-Steuerelement Attribut

Wenn dieses Bit in einem Kontrollkästchen oder einer Optionsfeld Gruppe festgelegt ist, wird die Schaltfläche mit der Darstellung einer Schaltfläche "Push" gezeichnet, aber die Logik bleibt unverändert. Wenn das-Bit nicht festgelegt ist, werden die Steuerelemente in Ihrem üblichen Stil gezeichnet.

## <a name="valid-controls"></a>Gültige Steuerelemente

[CheckBox](checkbox-control.md)-[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                           |
|---------|-------------|------------------------------------|
| 131072  | 0x00020000  | **msidbcontrolattributespushlike** |



 

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das pushlike-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.

Siehe [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).

 

 



