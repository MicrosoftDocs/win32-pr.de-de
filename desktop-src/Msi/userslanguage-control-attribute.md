---
description: Wenn dieses Bitflag festgelegt ist, werden die Schriftarten mithilfe der standardmäßigen UI-Codepage des Benutzers erstellt. Wenn das Bitflag nicht festgelegt ist, werden die Schriftarten mithilfe der Daten Bank Codepage erstellt.
ms.assetid: 6a3dbabe-6a14-4401-b46c-e8a0bd0cbe63
title: Userslanguage-Steuerelement Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aff4109c5c0819b199343bb8ee38bfecc069ad4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357512"
---
# <a name="userslanguage-control-attribute"></a>Userslanguage-Steuerelement Attribut

Wenn dieses Bitflag festgelegt ist, werden die Schriftarten mithilfe der standardmäßigen UI-Codepage des Benutzers erstellt. Wenn das Bitflag nicht festgelegt ist, werden die Schriftarten mithilfe der Daten Bank Codepage erstellt.

## <a name="valid-controls"></a>Gültige Steuerelemente

[Text](text-control.md)

 

[ListBox](listbox-control.md)

 

[ComboBox](combobox-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                                |
|---------|-------------|-----------------------------------------|
| 1048576 | 0x00100000  | **msidbcontrolattributesuserslanguage** |



 

## <a name="remarks"></a>Bemerkungen

Dieses Steuerelement kann verwendet werden, um Text anzuzeigen, den der Benutzer in ein [Edit](edit-control.md) -oder [pathedit](pathedit-control.md) -Steuerelement eingegeben hat.

Das Bearbeitungs Steuerelement, das Steuerelement "pathedit", das [Director-Listen Steuer](directorylist-control.md) Element und das [directoriycombo-Steuer](directorycombo-control.md) Element verwenden immer die Schriftarten, die auf der Benutzeroberfläche der Standardbenutzer Oberfläche Dies kann Probleme verursachen, wenn zusätzliche Sprachen auf dem Betriebssystem installiert wurden. In diesem Fall sind die Schriftarten auf dem Computer möglicherweise nicht in der Lage, alle Zeichen in den hinzugefügten Sprachen darzustellen. Um zu ermitteln, welche Schriftarten verwendet werden können, suchen Sie nach den Werten in **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ fontlink \\ Systemlink**.

Weitere Informationen finden Sie unter [Steuerelement Attribute](control-attributes.md) und-Steuer [Elemente](controls.md).

 

 



