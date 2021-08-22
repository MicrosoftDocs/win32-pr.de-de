---
description: Wenn dieses Bit für ein Textsteuerelement festgelegt ist, wird das Vorkommen des Zeichens \# &0034;&&\# 0034; in einer Textzeichenfolge als sich selbst angezeigt. Wenn dieses Bit nicht festgelegt ist, wird das Zeichen nach &\# 0034;&&\# 0034; in der Textzeichenfolge als Unterstrich angezeigt.
ms.assetid: b958eecb-2f44-420f-8c93-7a4bd8b589da
title: NoPrefix-Steuerelementattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15345bb56ad85ec654cffe7a0bf2173973e032ac33aca633105d3a220647cf93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065880"
---
# <a name="noprefix-control-attribute"></a>NoPrefix-Steuerelementattribut

Wenn dieses Bit für ein Textsteuerelement festgelegt ist, wird das Vorkommen des Zeichens "&" in einer Textzeichenfolge als sich selbst angezeigt. Wenn dieses Bit nicht festgelegt ist, wird das Zeichen nach "&" in der Textzeichenfolge als Unterstrich angezeigt.

## <a name="valid-controls"></a>Gültige Steuerelemente

[Text](text-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                           |
|---------|-------------|------------------------------------|
| 131072  | 0x20000     | **msidbControlAttributesNoPrefix** |



 

## <a name="remarks"></a>Hinweise

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie das NoPrefix-Bit in die Attributes -Spalte des Datensatzes des Steuerelements in die [Control-Tabelle ein.](control-table.md)

Weitere Informationen finden Sie unter [Steuerelementattribute](control-attributes.md) und [Steuerelemente.](controls.md)

 

 



