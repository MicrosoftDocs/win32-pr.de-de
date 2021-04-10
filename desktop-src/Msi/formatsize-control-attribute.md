---
description: Wenn dieses Bit für ein statisches Text Steuerelement festgelegt ist, versucht das-Steuerelement automatisch, den angezeigten Text als Zahl zu formatieren, die die Anzahl von Bytes darstellt.
ms.assetid: acf76fff-b7a4-456b-91b9-eb3087879d7b
title: Formatsize-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7fa656b81272b8ac60985d3dac0416c0f81bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215121"
---
# <a name="formatsize-control-attribute"></a>Formatsize-Steuerelement Attribut

Wenn dieses Bit für ein statisches Text Steuerelement festgelegt ist, versucht das-Steuerelement automatisch, den angezeigten Text als Zahl zu formatieren, die die Anzahl von Bytes darstellt. Für eine ordnungsgemäße Formatierung muss der Text des Steuer Elements auf eine Zeichenfolge festgelegt werden, die eine Zahl darstellt, die in Einheiten von 512 Byte ausgedrückt wird. Der angezeigte Wert wird dann in Kilobyte (KB), Megabyte (MB) oder Gigabyte (GB) formatiert und mit der entsprechenden Zeichenfolge angezeigt, die die Einheiten darstellt. Weitere Informationen finden Sie unter [Text-Steuer](text-control.md)Element.



| Numerischer Wert von ursprünglichem Text | Verwendete Einheiten Zeichenfolge |
|----------------------------------|------------------|
| Kleiner als 20480                  | KB               |
| Kleiner als 20971520               | MB               |
| Kleiner als 10737418240            | GB               |



 

## <a name="valid-controls"></a>Gültige Steuerelemente



| Decimal | Hexadezimal | Control                          |
|---------|-------------|----------------------------------|
| 524288  | 0x00080000  | msidbcontrolattributesformatsize |



 

## <a name="remarks"></a>Bemerkungen

Um dieses Attribut für ein Steuerelement festzulegen, schließen Sie die formatsize-Bits in die Spalte Attribute des Datensatzes des Steuer Elements in der [Steuerelement Tabelle](control-table.md)ein. Der Text des Steuer Elements muss auf eine Zeichenfolge festgelegt werden, die eine Zahl darstellt, die in Einheiten von 512 Byte ausgedrückt wird. Der Text der Einheiten Zeichenfolgen wird in der [UIText-Tabelle](uitext-table.md)definiert. Die Positionierung der Einheiten Zeichenfolge wird von der [**leftunit**](leftunit.md) -Eigenschaft gesteuert. Wenn die Eigenschaft " **leftunit** " als beliebiger Wert definiert ist, wird die Einheiten Zeichenfolge vor dem numerischen Wert angezeigt. Wenn im Text, der dem Steuerelement zugeordnet ist, etwas anderes als numerische Zeichen angezeigt wird, ist der angezeigte Wert nicht definiert.

Zur Laufzeit löst das Installationsprogramm die Eigenschaft [**primaryvolumespacerequired**](primaryvolumespacerequired.md) auf die Gesamtanzahl der Bytes auf, die für die Installation in Einheiten von 512 benötigt wird. Ein statisches Text Steuerelement mit formatsize Bit kann verwendet werden, um die Gesamtanzahl von Bytes, die für die Installation erforderlich sind, nach Bedarf automatisch in KB, MB oder GB zu formatieren und zu bezeichnen. Nehmen Sie für die Zwecke dieses Beispiels an, dass die Gesamtzahl der Bytes 18.336.768 beträgt. Der Installer legt den Wert der Eigenschaft primaryvolumespacerequired auf 18.336.768 dividiert durch 512 oder 35.814 fest. Die vom Text-Steuerelement mit formatsize angezeigte Zahl beträgt 17 MB.

Die numerischen Werte des ursprünglichen Texts werden in den Einheiten 512 angegeben. In der obigen Tabelle entspricht die Zeichenfolge 20.480 der KB-Zeichenfolge, da 20.480 mal 512 das Ergebnis 10.485.760 Bytes oder 10.240 KB ergibt.

Die in der vorherigen Tabelle aufgeführten Einheiten Zeichenfolgen beziehen sich auf Schlüssel in der [UIText-Tabelle](uitext-table.md), in der der Text der Einheits Zeichenfolge definiert ist.

Die Positionierung der Einheiten Zeichenfolge wird von der [**leftunit**](leftunit.md) -Eigenschaft gesteuert. Wenn die Eigenschaft " **leftunit** " als beliebiger Wert definiert ist, wird die Einheiten Zeichenfolge vor dem numerischen Wert angezeigt.

Wenn im Text, der dem Steuerelement zugeordnet ist, etwas anderes als numerische Zeichen angezeigt wird, ist der angezeigte Wert nicht definiert.

Weitere Informationen finden Sie unter [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).

 

 



