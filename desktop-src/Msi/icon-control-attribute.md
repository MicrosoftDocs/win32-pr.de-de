---
description: Wenn dieses Bit festgelegt ist, wird Text durch ein Symbolbild ersetzt, und die Text -Spalte in der Control-Tabelle ist ein Fremdschlüssel in der Binärtabelle.
ms.assetid: 5eefdfcb-89a5-4885-bab0-6409ef3ce349
title: Symbolsteuerelementattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2caeb407b86b888a5dd3b1c08f16d0893233f82cec29b92519c267b286ea121
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315120"
---
# <a name="icon-control-attribute"></a>Symbolsteuerelementattribut

Wenn dieses Bit festgelegt ist, wird Text durch ein Symbolbild ersetzt, und die Text-Spalte in der [Control-Tabelle](control-table.md) ist ein Fremdschlüssel in der [Binärtabelle](binary-table.md).

Wenn dieses Bit nicht festgelegt ist, wird Text im -Steuerelement in der Text -Spalte der [Control-Tabelle](control-table.md)angegeben.

## <a name="valid-controls"></a>Gültige Steuerelemente

[CheckBox](checkbox-control.md)

[Pushbutton](pushbutton-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                       |
|---------|-------------|--------------------------------|
| 5242288 | 0x00080000  | **msidbControlAttributesIcon** |



 

## <a name="remarks"></a>Hinweise

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie die Symbolbits in die Spalte Attribute des Datensatzes des Steuerelements in die [Control-Tabelle ein.](control-table.md)

Die Text -Spalte in der Control-Tabelle wird als Fremdschlüssel für die [Binärtabelle](binary-table.md)verwendet, daher darf das Steuerelement weder ein Symbolbild noch Text enthalten.

Legen Sie nicht sowohl die Symbol- als auch die [Bitmapbits](bitmap-control-attribute.md) fest.

Weitere Informationen finden Sie unter [Steuerelementattribute](control-attributes.md) und das Steuerelement, das Sie unter [Steuerelemente](controls.md)erstellen müssen.

 

 



