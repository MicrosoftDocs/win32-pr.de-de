---
description: Übersicht über die Verwendung von Gesten.
ms.assetid: 5bc80086-7acf-4f86-a9fb-a663de489f8b
title: Verwenden von Gesten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132c4748dbf2638a57e005562fdec735ea6e87c27757d46549b7577f3bed7741
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449247"
---
# <a name="using-gestures"></a>Verwenden von Gesten

Die Tablet PC-Plattform stellt die Gestenerkennung von Microsoft zur Unterstützung von Anwendungsgesten zur Verfügung. Eine Liste der Gesten, die von der Gestenerkennung von Microsoft unterstützt werden, finden Sie in der Tabelle der Anwendungsgesten in der [**ApplicationGesture-Enumeration.**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) Der Tablet-PC unterstützt auch Systemgesten. Eine Liste der vom Tablet PC unterstützten Systemgesten finden Sie in der Tabelle der Systemgesten in der [**SystemGesture-Enumeration.**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)

## <a name="microsoft-gesture-recognizer"></a>Microsoft-Gestenerkennung

Sie können die Gestenerkennung von Microsoft verwenden, indem Sie die [**CollectionMode-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) des [**InkCollector-Objekts,**](inkcollector-class.md) des [**InkOverlay-Objekts**](inkoverlay-class.md) oder des [InkPicture-Steuerelements](inkpicture-control-reference.md) verwenden. Wenn Sie **die CollectionMode-Eigenschaft** auf den gemischten Modus (**InkAndGesture**) oder den gestenbasierten Modus (**GestureOnly**) festlegen, wird die Ink-Eigenschaft standardmäßig an die Microsoft-Gestenerkennung übergibt. Sie können die Microsoft-Gestenerkennung mit dem [InkEdit-Steuerelement](inkedit-control-reference.md) verwenden, indem Sie die [**InkMode-Eigenschaft**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) auf **InkAndGesture festlegen.** Sie können die Gestenerkennung auch mit dem [**RealTimeStylus-Objekt**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) verwenden, indem Sie einer seiner Plug-In-Auflistungen ein [**GestureRecognizer-Objekt**](gesturerecognizer-class.md) hinzufügen.

Wenn die gesten, die Sie verwenden möchten, jedoch nicht von der aktuellen Version der Microsoft-Gestenerkennung unterstützt werden, können Sie Eine eigene Erkennen erstellen und in Verbindung mit der Gestenerkennung von Microsoft verwenden. Dies ermöglicht vollständige Unterstützung für die Gesten in Ihrer Anwendung.

Der Tablet-PC verwendet einen Stift für einige oder alle Eingaben. Dies macht das Schreiben von Ink sehr einfach. Die Tablet PC-Plattform bietet eine Architektur für Stifteingaben, die eine mehrstufige Struktur von Gesten unterstützt. Gesten und Zuordnungen sind so definiert, dass der Benutzer erweiterte Gesten auf neuen Oberflächen schreiben und aufrufen kann, während Gesten, die herkömmliche Mausmeldungen anderer Windows-basierten Anwendungen aufrufen, reservieren.

Die Tablet PC-Plattform führt zwei Gestenebenen ein: Systemgesten, auch als Systemereignisse bezeichnet, und Anwendungsgesten. Die Stiftarchitektur unterstützt sowohl System- als auch Anwendungsgesten. Anwendungsgesten mit einem Strich und mehreren Strichen werden unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungsgesten](application-gestures.md)
</dt> <dt>

[Flicks-Gesten](flicks-gestures.md)
</dt> <dt>

[Systemgesten](system-gestures.md)
</dt> </dl>

 

 



