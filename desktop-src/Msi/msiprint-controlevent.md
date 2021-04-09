---
description: Dieses Ereignis wird vom scrollabletext-Steuerelement veröffentlicht, damit der Benutzer den Inhalt des Steuer Elements drucken kann.
ms.assetid: 8cb91b21-f6db-4f49-827d-1ec739ff4f45
title: Msiprint ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0dd876f1a98e68c6ad61c7c122e1b51fa9c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868644"
---
# <a name="msiprint-controlevent"></a>Msiprint ControlEvent

Dieses Ereignis wird vom [scrollabletext-Steuer](scrollabletext-control.md) Element veröffentlicht, damit der Benutzer den Inhalt des Steuer Elements drucken kann.

**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt. Dieses ControlEvent ist ab Windows Installer 5,0 verfügbar.

Dieses Ereignis sollte von einem [PUSHBUTTON-Steuer](pushbutton-control.md) Element abonniert werden, das sich im gleichen Dialogfeld wie das [scrollabletext-Steuer](scrollabletext-control.md)Element befindet. In der [Tabelle "ControlEvent](controlevent-table.md)" sollte "themsiprint ControlEvent" erstellt werden.

## <a name="published-by"></a>Veröffentlicht von

[Scrollabletext](scrollabletext-control.md)

## <a name="argument"></a>Argument

Dieses ControlEvent verwendet kein Argument.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Diese ControlEvent führt keine Aktion für Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Ein [PUSHBUTTON](pushbutton-control.md) -Steuerelement im gleichen Dialogfeld wie das [scrollabletext-Steuer](scrollabletext-control.md) Element kann verwendet werden, um ein modales Dialogfeld anzuzeigen, das es dem Benutzer ermöglicht, den Inhalt des scrollabletext-Steuer Elements zu drucken.

 

 



