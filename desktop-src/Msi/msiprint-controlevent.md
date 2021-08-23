---
description: Dieses Ereignis wird vom ScrollableText-Steuerelement veröffentlicht, damit der Benutzer den Inhalt dieses Steuerelements drucken kann.
ms.assetid: 8cb91b21-f6db-4f49-827d-1ec739ff4f45
title: MsiPrint ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbd2107e4930e7d2d410846f656f25143926f8675f354976d866b2ee5d547b0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519780"
---
# <a name="msiprint-controlevent"></a>MsiPrint ControlEvent

Dieses Ereignis wird vom [ScrollableText-Steuerelement veröffentlicht,](scrollabletext-control.md) damit der Benutzer den Inhalt dieses Steuerelements drucken kann.

**[Windows Installer 4.5 oder früher:](not-supported-in-windows-installer-4-5.md)** Nicht unterstützt. Dieses ControlEvent ist ab Windows Installer 5.0 verfügbar.

Dieses Ereignis sollte von einem [PushButton-Steuerelement](pushbutton-control.md) abonniert werden, das sich im gleichen Dialogfeld wie das [ScrollableText-Steuerelement befindet.](scrollabletext-control.md) TheMsiPrint ControlEvent sollte in der [ControlEvent-Tabelle verfasst werden.](controlevent-table.md)

## <a name="published-by"></a>Veröffentlicht von

[ScrollableText](scrollabletext-control.md)

## <a name="argument"></a>Argument

Dieses ControlEvent verwendet kein Argument.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Dieses ControlEvent führt keine Aktion auf Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Ein [PushButton-Steuerelement](pushbutton-control.md) im gleichen Dialogfeld wie das [ScrollableText-Steuerelement](scrollabletext-control.md) kann verwendet werden, um ein modales Dialogfeld anzuzeigen, in dem der Benutzer den Inhalt des ScrollableText-Steuerelements drucken kann.

 

 



