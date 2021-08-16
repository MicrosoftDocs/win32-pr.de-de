---
description: Wenn dieses Bit für ein ProgressBar-Steuerelement festgelegt ist, wird der Balken als eine Reihe kleiner Rechtecke gezeichnet. Wenn dieses Bit nicht festgelegt ist, wird die Statusanzeige als einzelnes kontinuierliches Rechteck gezeichnet.
ms.assetid: b2c43763-799c-4f09-b9f8-47a4a5f4faf3
title: Progress95-Steuerelementattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a0e6fa8f2c0cd0e1622db4bb406d3ada1b63229e92b60a35e915bf0dacc72fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627349"
---
# <a name="progress95-control-attribute"></a>Progress95-Steuerelementattribut

Wenn dieses Bit für ein [ProgressBar-Steuerelement festgelegt ist,](progressbar-control.md)wird der Balken als eine Reihe kleiner Rechtecke gezeichnet. Wenn dieses Bit nicht festgelegt ist, wird die Statusanzeige als einzelnes kontinuierliches Rechteck gezeichnet.

## <a name="valid-controls"></a>Gültige Steuerelemente

[Progressbar](progressbar-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                             |
|---------|-------------|--------------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesProgress95** |



 

## <a name="remarks"></a>Hinweise

Wenn Sie dieses Attribut für ein Steuerelement festlegen möchten, schließen Sie das Progress95-Bit in die Spalte Attribute des Datensatzes des Steuerelements in der [Control-Tabelle ein.](control-table.md)

Weitere [Informationen finden Sie unter Steuerelementattribute](control-attributes.md) und das Steuerelement, das Sie unter Steuerelemente erstellen [müssen.](controls.md)

 

 



