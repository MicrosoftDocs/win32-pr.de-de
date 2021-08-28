---
title: Informationen zu Rebar-Steuerelementen
description: Ein Rebar-Steuerelement fungiert als Container für untergeordnete Fenster.
ms.assetid: vs|controls|~\controls\rebar\rebar.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55d34f76ca745f0807b849bd7c42c81944f11e4429fe2dc9670fa318cbd575ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434824"
---
# <a name="about-rebar-controls"></a>Informationen zu Rebar-Steuerelementen

Ein *Rebar-Steuerelement* fungiert als Container für untergeordnete Fenster. Sie kann ein oder mehrere *Bänder* enthalten, und jedes Band kann eine beliebige Kombination aus einem Klammerbalken, einer Bitmap, einer Textbezeichnung und einem untergeordneten Fenster aufweisen. Eine Anwendung weist einem Rebar-Steuerelementband ein untergeordnetes Fenster (in der Regel ein anderes Steuerelement) zu. Wenn Sie ein Rebar-Steuerelementband dynamisch neu positionieren, verwaltet das Steuerelement die Größe und Position des untergeordneten Fensters, das diesem Band zugewiesen ist. Außerdem kann eine Anwendung eine Hintergrundbitmap für ein Band angeben, und das Rebar-Steuerelement zeigt das untergeordnete Fenster des Bands über der Bitmap an.

Der folgende Screenshot zeigt ein Rebar-Steuerelement mit zwei Bändern. Eine enthält eine Symbolleiste und die andere ein Kombinationsfeld. Beide Bänder verfügen über einen Regler, mit dem sie verschoben und ihre Größe geändert werden können.

![Screenshot des Dialogfelds mit einem Rebar-Steuerelement mit einem Band, das eine Symbolleiste und ein Band mit einem Kombinationsfeld enthält](images/rb-rebar.png)

> [!Note]  
> Das Rebar-Steuerelement wird in Version 4.70 und höher von Comctl32.dll implementiert.

 

## <a name="rebar-bands-and-child-windows"></a>Leistenbänder und untergeordnete Windows

Eine Anwendung definiert die Merkmale eines Rebarbands mithilfe der [**RB \_ INSERTBAND-**](rb-insertband.md) und [**RB \_ SETBANDINFO-Meldungen.**](rb-setbandinfo.md) Diese Nachrichten akzeptieren die Adresse einer [**REBARBANDINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) als *lParam-Parameter.* Die **REBARBANDINFO-Strukturmember** definieren die Merkmale eines bestimmten Bands. Um die Merkmale eines Bands festzulegen, legen Sie den **cbsize-Member** so fest, dass er die Größe der Struktur in Bytes angibt. Legen Sie dann den **fMask-Member** fest, um anzugeben, welche Strukturmember ihre Anwendung füllt.

Um einem Band ein untergeordnetes Fenster zuzuweisen, schließen Sie das Flag RBBIM \_ CHILD in den **fMask-Member** der [**REBARBANDINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) ein, und legen Sie dann das **hwndChild-Element** auf das Handle des untergeordneten Fensters fest. Anwendungen können die minimal zulässige Breite und Höhe eines untergeordneten Fensters in den **CxMinChild-** und **cyMinChild-Membern** festlegen.

Wenn ein Rebar-Steuerelement zerstört wird, zerstört es alle untergeordneten Fenster, die den darin angezeigten Bändern zugewiesen sind. Um zu verhindern, dass das Steuerelement untergeordnete Fenster zerstört, die seinen Bändern zugewiesen sind, entfernen Sie die Bänder, indem Sie die [**RB \_ DELETEBAND-Nachricht**](rb-deleteband.md) senden, und verwenden Sie dann die [**RB \_ SETPARENT-Nachricht,**](rb-setparent.md) um das übergeordnete Fenster auf ein anderes Fenster zurückzusetzen, bevor das Steuerelement für die Neuleiste zerstört wird.

## <a name="the-rebar-control-user-interface"></a>Die Benutzeroberfläche des Steuerelements "Rebar"

Die Größe aller Rebar-Steuerelementbänder kann mit Ausnahme derjenigen geändert werden, die den RBBS \_ FIXEDSIZE-Stil verwenden. Um die Größe der Bänder innerhalb des Steuerelements zu ändern oder zu ändern, klicken Sie auf die Ziehleiste eines Bands, und ziehen Sie sie. Die Größe der untergeordneten Fenster, die den Bändern zugewiesen sind, wird vom Steuerelement für die Neuleiste automatisch geändert und neu positioniert. Darüber hinaus können Sie die Größe eines Bands umschalten, indem Sie ggf. auf den Bandtext klicken.

## <a name="the-rebar-controls-image-list"></a>Bildliste des Rebar-Steuerelements

Wenn eine Anwendung eine Bildliste mit einem Rebar-Steuerelement verwendet, muss sie die [**RB \_ SETBARINFO-Nachricht**](rb-setbarinfo.md) senden, bevor dem Steuerelement Bänder hinzugefügt werden. Diese Nachricht akzeptiert die Adresse einer [**REBARINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) als *lParam-Parameter.* Bereiten Sie vor dem Senden der Nachricht die **REBARINFO-Struktur** vor, indem Sie den **cbSize-Member** auf die Größe der -Struktur in Bytes festlegen. Wenn das Rebar-Steuerelement Bilder in den Bändern anzeigt, legen Sie das **fMask-Element** auf das RBIM \_ IMAGELIST-Flag fest, und weisen Sie dem **himl-Member** ein Bildlistenhandle zu. Wenn auf der Leiste keine Bandbilder verwendet werden, legen Sie **fMask** auf 0 (null) fest.

## <a name="rebar-control-message-forwarding"></a>Erneutes Steuern der Nachrichtenweiterleitung

Ein Rebar-Steuerelement leitet alle [**WM \_ NOTIFY-Fenstermeldungen**](wm-notify.md) an das übergeordnete Fenster weiter. Darüber hinaus leitet ein Rebar-Steuerelement alle Nachrichten weiter, die von Fenstern an das Steuerelement gesendet werden, die seinen Bändern zugewiesen sind, z. B. [**WM \_ CHARTOITEM,**](wm-chartoitem.md) [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command)und andere.

 

 