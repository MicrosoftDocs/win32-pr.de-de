---
description: Wenn dieses Bit in einem Bearbeitungs Steuerelement festgelegt ist, erstellt das Installationsprogramm ein Bearbeitungs Steuerelement mit mehreren Zeilen mit einer vertikalen Scrollleiste.
ms.assetid: cbdbe088-9cf1-4af8-a5f7-072faee7f34e
title: Multiline-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936bc4b3901293e950690e878a0f86229bb03b4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215477"
---
# <a name="multiline-control-attribute"></a>Multiline-Steuerelement Attribut

Wenn dieses Bit in einem [Bearbeitungs Steuer](edit-control.md)Element festgelegt ist, erstellt das Installationsprogramm ein Bearbeitungs Steuerelement mit mehreren Zeilen mit einer vertikalen Scrollleiste.

Wenn dieses Bit nicht festgelegt ist, gibt es an, dass ein normales Bearbeitungs Steuerelement angezeigt wird.

## <a name="valid-controls"></a>Gültige Steuerelemente

[Bearbeitungs Steuer](edit-control.md)Element.



| Decimal | Hexadezimal | Konstante                            |
|---------|-------------|-------------------------------------|
| 65536   | 0x00010000  | **msidbcontrolattributesmultiline** |



 

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das mehrzeilige Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.

Siehe [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).

 

 



