---
description: Das DoAction ControlEvent benachrichtigt das Installationsprogramm, eine benutzerdefinierte Aktion auszuführen. Dieses Ereignis kann von einem PushButton-Steuerelement, einem CheckBox-Steuerelement oder einem SelectionTree-Steuerelement veröffentlicht werden. Dieses Ereignis sollte in der ControlEvent-Tabelle verfasst werden.
ms.assetid: 9a855330-8241-4912-84da-4fca43f1d240
title: DoAction ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc4133c9b9fb0b312423952ee72d1e9e38defc2713345e1a7ed106fb141f0a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692620"
---
# <a name="doaction-controlevent"></a>DoAction ControlEvent

Das DoAction ControlEvent benachrichtigt das Installationsprogramm, eine benutzerdefinierte Aktion auszuführen. Dieses Ereignis kann von einem [PushButton-Steuerelement,](pushbutton-control.md) [einem CheckBox-Steuerelement](checkbox-control.md) oder einem [SelectionTree-Steuerelement veröffentlicht](selectiontree-control.md) werden. Dieses Ereignis sollte in der [ControlEvent-Tabelle verfasst](controlevent-table.md) werden.

Beachten Sie, dass benutzerdefinierte Aktionen, die von einem DoAction ControlEvent gestartet werden, eine Nachricht mit der [**Message-Methode**](session-message.md)senden können, aber keine Nachricht mit [**MsiProcessMessage senden können.**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) Auf Systemen vor Windows Server 2003 können benutzerdefinierte Aktionen, die von einem DoAction ControlEvent gestartet werden, keine Nachrichten mit **MsiProcessMessage oder** **Message Method senden.** Weitere Informationen finden Sie unter [Senden von Nachrichten an Windows Installer mit msiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).

Für dieses ControlEvent muss die Benutzeroberfläche auf der vollständigen [*Benutzeroberflächenebene ausgeführt*](f-gly.md) werden. Dieses Ereignis funktioniert nicht mit einer reduzierten [*Benutzeroberfläche oder*](r-gly.md) einer [*einfachen Benutzeroberfläche.*](b-gly.md) Weitere Informationen finden Sie unter [Benutzeroberfläche Levels](user-interface-levels.md).

## <a name="published-by"></a>Veröffentlicht von

Dieses ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Eine Zeichenfolge, der Name der auszuführenden benutzerdefinierten Aktion.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Dieses ControlEvent führt keine Aktion auf Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Ein [PushButton-Steuerelement](pushbutton-control.md) in einem Dialogfeld ist an dieses Ereignis in der [ControlEvent-Tabelle](controlevent-table.md) gebunden, um eine benutzerdefinierte Aktion auf aufruft.

 

 



