---
description: Wenn das Bit des Bitmap-Steuerelements festgelegt ist, wird der Text im -Steuerelement durch ein Bitmapbild ersetzt. Die Text -Spalte in der Control-Tabelle ist ein Fremdschlüssel in der Binärtabelle.
ms.assetid: ec774f31-7712-4a70-8c69-1cc731009049
title: Bitmap-Steuerelementattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2cd7ea8186d1ed16de71ae9974bb67a082142ed3e921d023ad905d4f47bbc98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638739"
---
# <a name="bitmap-control-attribute"></a>Bitmap-Steuerelementattribut

Wenn das Bit des Bitmap-Steuerelements festgelegt ist, wird der Text im -Steuerelement durch ein Bitmapbild ersetzt. Die Text -Spalte in der [Control-Tabelle](control-table.md) ist ein Fremdschlüssel in der [Binärtabelle](binary-table.md).

Wenn dieses Bit nicht festgelegt ist, wird der Text im -Steuerelement in der Text -Spalte der [Control-Tabelle angegeben.](control-table.md)

## <a name="valid-controls"></a>Gültige Steuerelemente

[CheckBox](checkbox-control.md)

 

[Pushbutton](pushbutton-control.md)

 

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                         |
|---------|-------------|----------------------------------|
| 262144  | 0x00040000  | **msidbControlAttributesBitmap** |



 

## <a name="remarks"></a>Hinweise

Um dieses Attribut für ein Steuerelement zu festlegen, schließen Sie das Bitmap-Bit in die Spalte Attribute des Datensatzes des Steuerelements in die [Control-Tabelle ein.](control-table.md)

Die Text -Spalte in der Control-Tabelle wird als Fremdschlüssel für die [Binärtabelle](binary-table.md)verwendet, daher darf das Steuerelement nicht sowohl ein Symbolbild als auch Text enthalten.

Legen Sie nicht sowohl das Symbol- [als auch](icon-control-attribute.md) das Bitmap-Bits fest.

Weitere [Informationen finden Sie unter Steuerelementattribute](control-attributes.md) und das Steuerelement, das Sie unter Steuerelemente erstellen [müssen.](controls.md)

 

 



