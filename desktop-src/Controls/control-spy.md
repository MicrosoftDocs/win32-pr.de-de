---
title: Control Spy v 2.0
description: Control Spy ist ein Tool, mit dem Entwickler allgemeine Steuerelemente verstehen können, wie Sie Stile auf Sie anwenden und wie Sie auf Nachrichten und Benachrichtigungen reagieren.
ms.assetid: 27483100-debb-4d82-ac24-b97f933a6942
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3630953cb924f1fd416c56d4d58024b9aaf29421
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104039774"
---
# <a name="control-spy-v20"></a>Control Spy v 2.0

Control Spy ist ein Tool, mit dem Entwickler allgemeine Steuerelemente verstehen können: wie Sie Stile auf Sie anwenden und wie Sie auf Nachrichten und Benachrichtigungen reagieren. Mithilfe von Control Spy können Sie sofort sehen, wie sich unterschiedliche Stile auf das Verhalten und die Darstellung der einzelnen Steuerelemente auswirken, und wie Sie den Zustand der einzelnen Steuerelemente ändern können, indem Sie Nachrichten senden.

Es sind zwei Versionen von Control Spy verfügbar: eine für [Comctl32.dll Version 5. x](common-control-versions.md) und eine für Comctl32.dll Version 6,0 und höher. ControlSpyV6.exe verfügt über ein integriertes Anwendungs Manifest, das die neueren Steuerelemente mit dem Design "Design" verwendet. ControlSpyV5.exe nicht über dieses Manifest verfügt und somit standardmäßig die ältere Version verwendet.

Dieses Thema enthält folgende Abschnitte:

-   [Übersicht](#overview)
-   [Stile](#styles)
-   [Meldungen](#messages)
-   [Größe/Farbe](#sizecolor)
-   [Speicherort des Steuerungs Spy](#where-to-get-control-spy)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Control Spy hostet ein ausgewähltes gemeinsames Steuerelement in der Mitte des Anwendungsfensters. Sie können das angezeigte Steuerelement ändern, indem Sie im Listenfeld auf der linken Seite des Fensters verschiedene Steuerelemente auswählen. Nachrichten oder Benachrichtigungen, die vom Steuerelement empfangen werden, werden auf der rechten Seite des Fensters angezeigt, sobald sie eintreffen. Sie können diese Funktion aktivieren oder deaktivieren, indem Sie die Kontrollkästchen empfangene **Nachrichten** und **empfangene Benachrichtigungen** verwenden.

Die folgende Abbildung zeigt die Spy-Steuerungsanwendung.

![Spy-Fenster steuern](images/controlspy-main.png)

Am unteren Rand des Fensters stehen mehrere Registerkarten zur Verfügung, die mehr Funktionalität enthalten.

## <a name="styles"></a>Stile

Auf der Registerkarte **Stile** können Sie den aktuellen Fenster Stil des Steuer Elements ändern. Wählen Sie einen der aufgelisteten Stile aus bzw. deaktivieren Sie diese, und klicken Sie dann auf die Schaltfläche übernehmen, **um die Art** des angezeigten Steuer Elements zu ändern Alternativ können Sie die **Schaltfläche neu erstellen verwenden** , um ein neues Steuerelement mit den ausgewählten Stilen zu erstellen. Mit der Schaltfläche **Zurücksetzen** wird das Steuerelement an die Standard Stile zurückgegeben.

Die Schaltflächen zum **Kopieren** **und Kopieren der** Schaltflächen unterhalb der Registerkarte kopieren die ausgewählten Format Konstanten als bitweise oder ()-Trennzeichen in die Zwischenablage \| . Sie können diese Liste direkt in ihren aufzurufenden Befehl anfügen, um ein Steuerelement in ihrer eigenen Anwendung mit demselben Stil [**bereitzustellen.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)

Die folgende Abbildung zeigt die Registerkarte **Stile** für ein Schaltflächen-Steuerelement.

![Registerkarte "Spy Stile Steuern"](images/controlspy-styles.png)

## <a name="messages"></a>Meldungen

Auf der Registerkarte **Nachrichten** können Sie nahezu jede Nachricht an ein Steuerelement senden. Nachdem Sie eine Nachricht aus dem Listenfeld ausgewählt haben, können Sie Daten eingeben, die als *wParam* -Parameter und *LPARAM* -Parameter des Aufrufes [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)gesendet werden. Nachdem Sie auf **senden** klicken, wird die Meldung an das Steuerelement gesendet, und im Textfeld unten auf der Registerkarte wird ein beliebiges Ergebnis angezeigt.

In der folgenden Abbildung wird die Registerkarte Nachrichten angezeigt, wenn eine bestimmte Nachricht ausgewählt wird.

![Registerkarte "Spy Messages" Steuern](images/controlspy-messages.png)

## <a name="sizecolor"></a>Größe/Farbe

Die Registerkarte **Größe/Farbe** kann verwendet werden, um die Größe des Steuer Elements und die Farbe seines Hintergrunds zu ändern.

## <a name="where-to-get-control-spy"></a>Speicherort des Steuerungs Spy

Sie können [Control Spy 2,0](https://www.microsoft.com/download/details.aspx?id=4635) von MSDN herunterladen. Beide Versionen sind im Download enthalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Windows-Steuerelemente](window-controls.md)
</dt> <dt>

[Aktivieren von visuellen Stilen](cookbook-overview.md)
</dt> </dl>

 

 