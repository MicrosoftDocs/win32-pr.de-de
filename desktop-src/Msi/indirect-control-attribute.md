---
description: Das indirekte Steuerungs Attribut gibt an, ob indirekt auf den Wert verwiesen wird, der von diesem Steuerelement angezeigt oder geändert wird.
ms.assetid: dc9c0dd6-7e19-44ec-b1a5-3d51a1855adf
title: Indirektes Steuerungs Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d0c183f586c197b14810e7176bce607ac3adaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864223"
---
# <a name="indirect-control-attribute"></a>Indirektes Steuerungs Attribut

Das indirekte Steuerungs Attribut gibt an, ob indirekt auf den Wert verwiesen wird, der von diesem Steuerelement angezeigt oder geändert wird. Wenn dieses Bit festgelegt ist, zeigt das Steuerelement den Wert der Eigenschaft an oder ändert ihn, die den Bezeichner enthält, der in der Eigenschafts Spalte der [Steuerelement Tabelle](control-table.md)aufgeführt ist. Wenn dieses Bit nicht festgelegt ist, zeigt das Steuerelement den Wert der-Eigenschaft in der-Eigenschaften Spalte der Steuerelement Tabelle an oder ändert diesen.

## <a name="valid-controls"></a>Gültige Steuerelemente

Alle aktiven Steuerelemente.

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                           |
|---------|-------------|------------------------------------|
| 8       | 0x00000008  | **msidbcontrolattributesindirekte** |



 

## <a name="remarks"></a>Bemerkungen

Siehe [Steuerelement Attribute](control-attributes.md) und das Steuerelement, das Sie unter Steuer [Elementen](controls.md)erstellen müssen.

 

 



