---
description: Wenn das Bit Visible Control festgelegt ist, wird das Steuerelement im Dialogfeld angezeigt. Wenn dieses Bit nicht festgelegt ist, wird das Steuerelement im Dialogfeld ausgeblendet. Der sichtbare oder ausgeblendete Zustand des Visible-Steuerelementattributs kann später durch ein Steuerelementereignis geändert werden.
ms.assetid: 77d3164c-ea8a-4dcf-afd5-02bb2c2568c6
title: Sichtbares Steuerelementattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78abdecdc46f179b7639a6ecaa627d92b643ed781ade242a152262d38c46f7eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498800"
---
# <a name="visible-control-attribute"></a>Sichtbares Steuerelementattribut

Wenn das Bit Visible Control festgelegt ist, wird das Steuerelement im Dialogfeld angezeigt. Wenn dieses Bit nicht festgelegt ist, wird das Steuerelement im Dialogfeld ausgeblendet. Der sichtbare oder ausgeblendete Zustand des Visible-Steuerelementattributs kann später durch ein [Steuerelementereignis](control-events.md)geändert werden.

## <a name="valid-controls"></a>Gültige Steuerelemente

Alle Steuerelemente.

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                          |
|---------|-------------|-----------------------------------|
| 1       | 0x00000001  | **msidbControlAttributesVisible** |



 

## <a name="remarks"></a>Hinweise

Sie können die [Tabelle ControlCondition](controlcondition-table.md) verwenden, um ein Steuerelement entsprechend dem Wert einer Eigenschaft oder bedingten Anweisung anzuzeigen oder auszublenden. Sie können ein Steuerelement auch ein- oder ausblenden, indem Sie das Steuerelement einem [ControlEvent](control-events.md)abonnieren. Geben Sie den Bezeichner des Attributs in der Spalte Attribute und den Bezeichner des Ereignisses in der Spalte Ereignis der [EventMapping-Tabelle](eventmapping-table.md)ein.

Weitere Informationen finden Sie unter [Steuerelementattribute](control-attributes.md) und [Steuerelemente.](controls.md)

 

 



