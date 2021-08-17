---
description: Wenn dieses Bit für ein statisches Textsteuerfeld festgelegt ist, versucht das Steuerelement automatisch, den angezeigten Text als Zahl zu formatieren, die eine Anzahl von Bytes darstellt.
ms.assetid: acf76fff-b7a4-456b-91b9-eb3087879d7b
title: FormatSize-Steuerelementattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34df03c87ceb742b543f32b770c201646185ce02df6386e38c9c5af02c6a1a47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636038"
---
# <a name="formatsize-control-attribute"></a>FormatSize-Steuerelementattribut

Wenn dieses Bit für ein statisches Textsteuerfeld festgelegt ist, versucht das Steuerelement automatisch, den angezeigten Text als Zahl zu formatieren, die eine Anzahl von Bytes darstellt. Für die richtige Formatierung muss der Text des Steuerelements auf eine Zeichenfolge festgelegt werden, die eine Zahl darstellt, die in Einheiten von 512 Bytes ausgedrückt wird. Der angezeigte Wert wird dann in Kilobyte (KB), Megabyte (MB) oder Gigabyte (GB) formatiert und mit der entsprechenden Zeichenfolge angezeigt, die die Einheiten darstellt. Weitere Informationen finden Sie unter [Textsteuer.](text-control.md)



| Numerischer Wert des ursprünglichen Texts | Verwendete Einheitenzeichenfolge |
|----------------------------------|------------------|
| Kleiner als 20480                  | KB               |
| Kleiner als 20971520               | MB               |
| Kleiner als 10737418240            | GB               |



 

## <a name="valid-controls"></a>Gültige Steuerelemente



| Decimal | Hexadezimal | Control                          |
|---------|-------------|----------------------------------|
| 524288  | 0x00080000  | msidbControlAttributesFormatSize |



 

## <a name="remarks"></a>Hinweise

Um dieses Attribut für ein Steuerelement festlegen zu können, schließen Sie die FormatSize-Bits in die Spalte Attribute des Datensatzes des Steuerelements in die [Steuertabelle ein.](control-table.md) Der Text des Steuerelements muss auf eine Zeichenfolge festgelegt werden, die eine Zahl darstellt, die in Einheiten von 512 Bytes ausgedrückt wird. Der Text der Einheitenzeichenfolgen wird in der [UIText-Tabelle definiert.](uitext-table.md) Die Positionierung der Einheitenzeichenfolge wird durch die [**LeftUnit-Eigenschaft**](leftunit.md) gesteuert. Wenn die **LeftUnit-Eigenschaft** als ein beliebiger Wert definiert ist, wird die Einheitenzeichenfolge vor dem numerischen Wert angezeigt. Wenn etwas anderes als numerische Zeichen im text angezeigt wird, der dem Steuerelement zugeordnet ist, ist der angezeigte Wert nicht definiert.

Zur Laufzeit löst das Installationsprogramm die [**PrimaryVolumeSpaceRequired-Eigenschaft**](primaryvolumespacerequired.md) in die Gesamtanzahl von Bytes auf, die für die Installation in Einheiten von 512 erforderlich sind. Ein statisches Textsteuerfeld mit FormatSize-Bit kann verwendet werden, um die Gesamtanzahl von Bytes, die für die Installation in KB, MB oder GB erforderlich sind, automatisch zu formatieren und zu beschriften. Gehen Sie für dieses Beispiel davon aus, dass die Gesamtzahl der Bytes 18.336.768 beträgt. Das Installationsprogramm legt den Wert der PrimaryVolumeSpaceRequired-Eigenschaft auf 18.336.768 dividiert durch 512 oder 35.814 fest. Die vom Textsteuerfeld mit FormatSize angezeigte Zahl wäre 17 MB.

Die numerischen Werte des ursprünglichen Texts werden in Einheiten von 512 angegeben. In der obigen Tabelle entspricht die Zeichenfolge 20.480 der KB-Zeichenfolge, da 20.480 Mal 512 ein Ergebnis von 10.485.760 Byte oder 10.240 KB ergibt.

Die in der vorherigen Tabelle aufgeführten Einheitenzeichenfolgen verweisen auf Schlüssel in der [UIText-Tabelle,](uitext-table.md)in der der Text der Einheitenzeichenfolge definiert ist.

Die Positionierung der Einheitenzeichenfolge wird durch die [**LeftUnit-Eigenschaft**](leftunit.md) gesteuert. Wenn die **LeftUnit-Eigenschaft** als ein beliebiger Wert definiert ist, wird die Einheitenzeichenfolge vor dem numerischen Wert angezeigt.

Wenn etwas anderes als numerische Zeichen im text angezeigt wird, der dem Steuerelement zugeordnet ist, ist der angezeigte Wert nicht definiert.

Weitere Informationen finden Sie unter [Control Attributes](control-attributes.md) and [Controls](controls.md).

 

 



