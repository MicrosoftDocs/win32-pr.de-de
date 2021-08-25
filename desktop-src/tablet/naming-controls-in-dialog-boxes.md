---
description: Wenn Sie Microsoft Windows Dialogfelder verwenden, müssen Sie alle Steuerelemente beschriften, um die Sprachfunktionalität zu vereinfachen. Im folgenden Dialogfeld Ausführen wird eine statische Textsteuerzeichenbezeichnung für ein Dropdownlistenfeld angezeigt. Statischer Text endet mit einem Doppelpunkt.
ms.assetid: 3b01a4d2-9deb-413f-bab8-566df86b6af9
title: Benennen von Steuerelementen in Dialogfeldern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c33720c08a7f5454b54d7d982b14c091fe6e1df4c18a49cd649f54690f2eb11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449827"
---
# <a name="naming-controls-in-dialog-boxes"></a>Benennen von Steuerelementen in Dialogfeldern

Wenn Sie Microsoft Windows Dialogfelder verwenden, müssen Sie alle Steuerelemente beschriften, um die Sprachfunktionalität zu vereinfachen. Im folgenden **Dialogfeld** Ausführen wird eine statische Textsteuerzeichenbezeichnung für ein Dropdownlistenfeld angezeigt. Statischer Text endet mit einem Doppelpunkt.

![Screenshot des Dialogfelds "Ausführen"](images/fb0bd076-e9f9-4260-a54a-9d7db93157da.jpg)

Es gibt zwei Arten von Kontrollen:

-   Steuerelemente, deren Beschriftungen eine Eigenschaft dieses Steuerelements sind, z. B. Befehlsschaltflächen und Kontrollkästchen. Barrierefreiheitshilfen haben keine Probleme beim Identifizieren dieser Steuerelemente, solange die Beschriftung ordnungsgemäß definiert ist.
-   Steuerelemente, die nicht über eigene Beschriftungen verfügen, z. B. Bearbeitungssteuerelemente, Listenfelder und Listenansichten, müssen mithilfe separater statischer Textsteuerelemente bezeichnet werden. Weitere Informationen zu Steuerelementen, die nicht über eigene Beschriftungen verfügen, finden Sie unter [Steuerelemente ohne Beschriftungseigenschaften.](controls-without-caption-properties.md)

Verschiedene Techniken können verwendet werden, um Situationen zu überwinden, in denen Steuerelemente keine eigenen Untertitel haben, aber nur für Fenster wirksam sind, die vom Standarddialog-Manager (STANDARD Dialog Manager, SDM) angezeigt werden. Alle anderen Fenster müssen die Namen und die Beziehung zwischen Steuerelementen durch explizite Unterstützung Microsoft Active Accessibility. Weitere Informationen zu Active Accessibility finden Sie im [Abschnitt](/windows/desktop/accessibility) Barrierefreiheit der MSDN Library.

 

 
