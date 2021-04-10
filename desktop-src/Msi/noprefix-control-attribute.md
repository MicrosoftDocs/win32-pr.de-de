---
description: Wenn dieses Bit für ein Text Steuerelement festgelegt ist, wird das Vorkommen des Zeichens &\# 0034; &&\# 0034; in einer Text Zeichenfolge als sich selbst angezeigt. Wenn dieses Bit nicht festgelegt ist, wird das Zeichen, das \# auf &0034; &&\# 0034; in der Text Zeichenfolge folgt, als unterstrichendes Zeichen angezeigt.
ms.assetid: b958eecb-2f44-420f-8c93-7a4bd8b589da
title: NoPrefix-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1e1a0c6da65605efca1aacc4582b34a8f673d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215118"
---
# <a name="noprefix-control-attribute"></a>NoPrefix-Steuerelement Attribut

Wenn dieses Bit für ein Text Steuerelement festgelegt ist, wird das Vorkommen des Zeichens "&" in einer Text Zeichenfolge als sich selbst angezeigt. Wenn dieses Bit nicht festgelegt ist, wird das Zeichen, das auf "&" in der Text Zeichenfolge folgt, als unterstrichendes Zeichen angezeigt.

## <a name="valid-controls"></a>Gültige Steuerelemente

[Text](text-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                           |
|---------|-------------|------------------------------------|
| 131072  | 0x20000     | **msidbcontrolattributesnoprefix** |



 

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das NoPrefix-Bit in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein.

Siehe [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).

 

 



