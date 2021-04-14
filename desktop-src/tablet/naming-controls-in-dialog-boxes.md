---
description: Wenn Sie Microsoft Windows-Dialogfelder verwenden, müssen Sie alle Steuerelemente bezeichnen, um die sprach Funktionalität zu vereinfachen. Im folgenden Dialogfeld Ausführen wird eine statische Text Steuerelement-Bezeichnung für ein Dropdown-Listenfeld angezeigt. Statischer Text endet mit einem Doppelpunkt.
ms.assetid: 3b01a4d2-9deb-413f-bab8-566df86b6af9
title: Benennen von Steuerelementen in Dialog Feldern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0f74ecb3737b422450388ee87ab4177e899aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565119"
---
# <a name="naming-controls-in-dialog-boxes"></a>Benennen von Steuerelementen in Dialog Feldern

Wenn Sie Microsoft Windows-Dialogfelder verwenden, müssen Sie alle Steuerelemente bezeichnen, um die sprach Funktionalität zu vereinfachen. Im folgenden Dialogfeld **Ausführen** wird eine statische Text Steuerelement-Bezeichnung für ein Dropdown-Listenfeld angezeigt. Statischer Text endet mit einem Doppelpunkt.

![Screenshot mit dem Dialogfeld "ausführen"](images/fb0bd076-e9f9-4260-a54a-9d7db93157da.jpg)

Es gibt zwei Arten von Kontrollen:

-   Steuerelemente, die über Beschriftungen als Eigenschaft dieses Steuer Elements verfügen, z. b. Befehls Schaltflächen und Kontrollkästchen. Barrierefreiheits Hilfen haben keine Probleme, diese Steuerelemente zu identifizieren, solange die Beschriftung ordnungsgemäß definiert ist.
-   Steuerelemente, die nicht über eigene Beschriftungen verfügen (z. b. Bearbeitungs Steuerelemente, Listenfelder und Listenansichten), müssen mithilfe separater statischer Text Steuerelemente beschriftet werden. Weitere Informationen zu Steuerelementen, die über keine eigenen Beschriftungen verfügen, finden Sie unter Steuer [Elemente ohne Beschriftungs Eigenschaften](controls-without-caption-properties.md).

Es können mehrere Techniken verwendet werden, um Situationen zu überwinden, in denen Steuerelemente nicht über eigene Beschriftungen verfügen, aber nur für Windows wirksam sind, die vom Standard Dialog-Manager (SDM) angezeigt werden. Alle anderen Fenster müssen die Namen und Beziehungen zwischen Steuerelementen verfügbar machen, indem Microsoft Active Accessibility explizit unterstützt wird. Weitere Informationen zu Active Accessibility finden Sie im Abschnitt zur [Barrierefreiheit](/windows/desktop/accessibility) in der MSDN Library.

 

 
