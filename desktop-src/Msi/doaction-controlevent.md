---
description: Das doaction ControlEvent benachrichtigt den Installer, eine benutzerdefinierte Aktion auszuführen. Dieses Ereignis kann durch ein PUSHBUTTON-Steuerelement, ein CheckBox-Steuerelement oder ein SelectionTree-Steuerelement veröffentlicht werden. Dieses Ereignis sollte in der Tabelle ControlEvent erstellt werden.
ms.assetid: 9a855330-8241-4912-84da-4fca43f1d240
title: Doaction ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74cc16c918522408e4cdf046e95d3d822ba3ac5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128388"
---
# <a name="doaction-controlevent"></a>Doaction ControlEvent

Das doaction ControlEvent benachrichtigt den Installer, eine benutzerdefinierte Aktion auszuführen. Dieses Ereignis kann durch ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement, ein [CheckBox](checkbox-control.md) -Steuerelement oder ein [SelectionTree](selectiontree-control.md) -Steuerelement veröffentlicht werden. Dieses Ereignis sollte in der Tabelle [ControlEvent](controlevent-table.md) erstellt werden.

Beachten Sie, dass benutzerdefinierte Aktionen, die von einem doaction ControlEvent gestartet werden, eine Nachricht mit der [**Message-Methode**](session-message.md)senden können, aber keine Nachricht mit [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)senden können. Auf Systemen vor Windows Server 2003 können benutzerdefinierte Aktionen, die von einem doaction ControlEvent gestartet werden, keine Nachrichten mit der **msiprocessmessage** oder der **Message-Methode** senden. Weitere Informationen finden Sie unter [Senden von Nachrichten an Windows Installer mithilfe von "msiprocessmessage](sending-messages-to-windows-installer-using-msiprocessmessage.md)".

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

## <a name="published-by"></a>Veröffentlicht von

Diese ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Eine Zeichenfolge, der Name der benutzerdefinierten Aktion, die ausgeführt werden soll.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Diese ControlEvent führt keine Aktion für Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement in einem Dialogfeld ist an dieses Ereignis in der Tabelle [ControlEvent](controlevent-table.md) gebunden, um eine benutzerdefinierte Aktion aufzurufen.

 

 



