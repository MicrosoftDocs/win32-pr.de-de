---
description: Das Line-Steuerelement ist eine horizontale Linie.
ms.assetid: 8b180b71-1e80-47c0-bb44-d5fcecabaed2
title: Liniensteuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb4dc02db9c701c0c5156a0e3f3e15a039893bae290fc7e8bee7dfce64f2eb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763490"
---
# <a name="line-control"></a>Liniensteuerelement

Das Line-Steuerelement ist eine horizontale Linie.

## <a name="control-attributes"></a>Steuerelementattribute

Sie können die folgenden Attribute mit diesem Steuerelement verwenden. Um den Wert eines Attributs mithilfe eines Ereignisses zu ändern, abonnieren Sie das Steuerelement für ein ControlEvent in der [EventMapping-Tabelle,](eventmapping-table.md) und listen Sie den Bezeichner des Attributs in der Spalte Attribute auf. Geben Sie den Bezeichner des ControlEvent in der Spalte Ereignis ein.



| Attributbezeichner                       | Hexadezimalbit                  | Beschreibung                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md) |                                  | Position des Steuerelements im Dialogfeld. Geben Sie die Breite, Höhe und Koordinaten der linken Ecke des Steuerelements in die Spalten Width, Height, X und Y der [Control-Tabelle](control-table.md) oder der [BBControl-Tabelle](bbcontrol-table.md)ein. Verwenden Sie [Installationseinheiten](installer-units.md) für Länge und Entfernung.<br/>                                         |
| [Visible](visible-control-attribute.md)   | 0x00000000 0x00000001<br/> | Ausgeblendetes Steuerelement. Sichtbares Steuerelement.<br/> Fügen Sie dieses Bit in das Bitwort der Spalte Attributes in die [Tabelle Control](control-table.md) oder [BBControl](bbcontrol-table.md) ein, um das Steuerelement bei der Erstellung sichtbar oder ausgeblendet zu machen.<br/> Sie können ein Steuerelement auch mithilfe der [ControlCondition-Tabelle](controlcondition-table.md)ausblenden oder anzeigen.<br/> |
| [Sunken](sunken-control-attribute.md)     | 0x00000000 0x00000004<br/> | Zeigt den standardmäßigen visuellen Stil an. Zeigt das Steuerelement mit einem eingesenkten 3D-Look an.<br/> Schließen Sie diese Bits in das Bitwort in die Attributes -Spalte der [Control-Tabelle](control-table.md)ein.<br/>                                                                                                                                                                   |



 

## <a name="remarks"></a>Hinweise

Dieses Steuerelement kann mithilfe der [**CreateWindowEx-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowexa) aus der STATIC-Klasse erstellt werden. Sie verfügt über die **Stile SS \_ ETCHEDHORZ** und **SS \_ SUNKEN.**

 

 
