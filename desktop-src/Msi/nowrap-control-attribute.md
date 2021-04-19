---
description: Wenn dieses Bit festgelegt ist, wird der Text im Steuerelement in einer einzelnen Zeile angezeigt. Wenn der Text die Ränder des Steuer Elements überschreitet, wird er abgeschnitten und ein Auslassungs Zeichen (&\# 0034;... &\# 0034;) wird am Ende eingefügt, um das Abschneiden anzugeben. Wenn dieses Bit nicht festgelegt ist, wird Text umschlossen.
ms.assetid: 0dec3d25-0da7-4054-8d5c-55e81be16489
title: NoWrap-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ee40b52fbec1c8add841f7055a7f42667eca94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360601"
---
# <a name="nowrap-control-attribute"></a>NoWrap-Steuerelement Attribut

Wenn dieses Bit festgelegt ist, wird der Text im Steuerelement in einer einzelnen Zeile angezeigt. Wenn der Text die Ränder des Steuer Elements überschreitet, wird er abgeschnitten, und am Ende wird ein Auslassungs Zeichen ("...") eingefügt, um das Abschneiden anzugeben. Wenn dieses Bit nicht festgelegt ist, wird Text umschlossen.

## <a name="valid-controls"></a>Gültige Steuerelemente

[Text](text-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                         |
|---------|-------------|----------------------------------|
| 262144  | 0x00040000  | **msidbcontrolattributesnowrap** |



 

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das nowrap-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.

Siehe [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).

 

 



