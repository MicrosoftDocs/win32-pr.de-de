---
description: Wenn das sichtbare Steuerelement Bit festgelegt ist, wird das Steuerelement im Dialogfeld angezeigt. Wenn dieses Bit nicht festgelegt ist, wird das-Steuerelement im Dialogfeld ausgeblendet. Der sichtbare oder verborgene Zustand des sichtbaren Steuerelement Attributs kann später durch ein Steuerelement Ereignis geändert werden.
ms.assetid: 77d3164c-ea8a-4dcf-afd5-02bb2c2568c6
title: Visible-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550513f6bd0e40e58694c2c15a9986b5b02f289c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346510"
---
# <a name="visible-control-attribute"></a>Visible-Steuerelement Attribut

Wenn das sichtbare Steuerelement Bit festgelegt ist, wird das Steuerelement im Dialogfeld angezeigt. Wenn dieses Bit nicht festgelegt ist, wird das-Steuerelement im Dialogfeld ausgeblendet. Der sichtbare oder verborgene Zustand des sichtbaren Steuerelement Attributs kann später durch ein [Steuerelement Ereignis](control-events.md)geändert werden.

## <a name="valid-controls"></a>Gültige Steuerelemente

Alle-Steuerelemente.

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                          |
|---------|-------------|-----------------------------------|
| 1       | 0x00000001  | **msidbcontrolattributesvisible** |



 

## <a name="remarks"></a>Bemerkungen

Sie können die [Tabelle "ControlCondition](controlcondition-table.md) " verwenden, um ein Steuerelement entsprechend dem Wert einer Eigenschaft oder Bedingungs Anweisung anzuzeigen oder auszublenden. Sie können ein Steuerelement auch ein-oder ausblenden, indem Sie das Steuerelement einem [ControlEvent](control-events.md)abonnieren. Geben Sie den Bezeichner des Attributs in der Spalte Attribut und den Bezeichner des Ereignisses in der Spalte Ereignis der [Tabelle EventMapping](eventmapping-table.md)ein.

Siehe [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).

 

 



