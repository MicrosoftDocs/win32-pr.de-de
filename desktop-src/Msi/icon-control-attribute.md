---
description: Wenn dieses Bit festgelegt ist, wird Text durch ein Symbolbild ersetzt, und die Text-Spalte in der Steuerelement Tabelle ist ein Fremdschlüssel in die binäre Tabelle.
ms.assetid: 5eefdfcb-89a5-4885-bab0-6409ef3ce349
title: Symbol Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60c19674ac26f108109fad04e0836ed8dfeba6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356837"
---
# <a name="icon-control-attribute"></a>Symbol Steuerelement Attribut

Wenn dieses Bit festgelegt ist, wird Text durch ein Symbolbild ersetzt, und die Text-Spalte in der [Steuerelement Tabelle](control-table.md) ist ein Fremdschlüssel in die [binäre Tabelle](binary-table.md).

Wenn dieses Bit nicht festgelegt ist, wird der Text im-Steuerelement in der Text-Spalte der [Steuerelement Tabelle](control-table.md)angegeben.

## <a name="valid-controls"></a>Gültige Steuerelemente

[CheckBox](checkbox-control.md)

[PUSHBUTTON](pushbutton-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                       |
|---------|-------------|--------------------------------|
| 5242288 | 0x00080000  | **msidbcontrolattributesicon** |



 

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie die Symbol Bits in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.

Die Text-Spalte in der Steuerelement Tabelle wird als Fremdschlüssel für die [binäre Tabelle](binary-table.md)verwendet. Daher kann das Steuerelement kein Symbolbild und keinen Text enthalten.

Legen Sie nicht sowohl das Symbol als auch das [Bitmap](bitmap-control-attribute.md) -Bit fest.

Siehe [Steuerelement Attribute](control-attributes.md) und das Steuerelement, das Sie unter Steuer [Elementen](controls.md)erstellen müssen.

 

 



