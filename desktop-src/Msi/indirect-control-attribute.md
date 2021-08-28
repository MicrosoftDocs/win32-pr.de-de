---
description: Das Attribut Indirekte Steuerung gibt an, ob indirekt auf den von diesem Steuerelement angezeigten oder geänderten Wert verwiesen wird.
ms.assetid: dc9c0dd6-7e19-44ec-b1a5-3d51a1855adf
title: Attribut der indirekten Steuerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c679938a818fb8393958c35694f3c2b7f782c91fc2dfcf1ac04777553ec629c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996688"
---
# <a name="indirect-control-attribute"></a>Attribut der indirekten Steuerung

Das Attribut Indirekte Steuerung gibt an, ob indirekt auf den von diesem Steuerelement angezeigten oder geänderten Wert verwiesen wird. Wenn dieses Bit festgelegt ist, zeigt das Steuerelement den Wert der Eigenschaft an, deren Bezeichner in der Spalte Eigenschaft der [Control-Tabelle aufgeführt ist, oder ändert diesen.](control-table.md) Wenn dieses Bit nicht festgelegt ist, zeigt das -Steuerelement den Wert der -Eigenschaft in der Property -Spalte der Control-Tabelle an oder ändert diesen.

## <a name="valid-controls"></a>Gültige Steuerelemente

Alle aktiven Steuerelemente.

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                           |
|---------|-------------|------------------------------------|
| 8       | 0x00000008  | **msidbControlAttributesIndirect** |



 

## <a name="remarks"></a>Hinweise

Weitere [Informationen finden Sie unter Steuerelementattribute](control-attributes.md) und das Steuerelement, das Sie unter Steuerelemente erstellen [müssen.](controls.md)

 

 



