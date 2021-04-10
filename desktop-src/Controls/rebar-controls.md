---
title: Informationen über Grund leisten-Steuerelemente
description: Ein Grund leisten-Steuerelement fungiert als Container für untergeordnete Fenster.
ms.assetid: vs|controls|~\controls\rebar\rebar.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56bc68629db7387f4ba408a769f7d87a64256000
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039713"
---
# <a name="about-rebar-controls"></a>Informationen über Grund leisten-Steuerelemente

Ein Grund leisten- *Steuer* Element fungiert als Container für untergeordnete Fenster. Sie kann ein oder mehrere *Bänder* enthalten, und jedes Band kann eine beliebige Kombination aus einer Zieh Punkt Leiste, einer Bitmap, einer Text Bezeichnung und einem untergeordneten Fenster aufweisen. Eine Anwendung weist einem Grund leisten-Steuerelement ein untergeordnetes Fenster – normalerweise ein anderes Steuerelement – zu. Wenn Sie ein Grund leisten-Steuerelement dynamisch neu positionieren, verwaltet das Grund leisten-Steuerelement die Größe und Position des untergeordneten Fensters, das diesem Band zugewiesen ist. Außerdem kann eine Anwendung eine Hintergrund Bitmap für ein Band angeben, und das untergeordnete Fenster der untergeordneten Leiste zeigt das untergeordnete Fenster des Bands über der Bitmap an.

Der folgende Screenshot zeigt ein Grund leisten-Steuerelement mit zwei Bändern. Eine enthält eine Symbolleiste, die andere enthält ein Kombinations Feld. Beide Bänder verfügen über einen Zieh Punkt, der das Verschieben und Ändern der Größe ermöglicht.

![Screenshot des Dialog Felds mit einem Grund leisten-Steuerelement mit einem Band, das eine Symbolleiste und ein Band mit einem Kombinations Feld enthält](images/rb-rebar.png)

> [!Note]  
> Das Grund leisten-Steuerelement wird in Version 4,70 und höher von Comctl32.dll implementiert.

 

## <a name="rebar-bands-and-child-windows"></a>Grund leisten-und untergeordnete Fenster

Eine Anwendung definiert die Merkmale eines Grund leisten Bandes mithilfe der [**RB \_ InsertBand**](rb-insertband.md) -und [**RB- \_ SetBandInfo**](rb-setbandinfo.md) -Meldungen. Diese Nachrichten akzeptieren die Adresse einer [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) -Struktur als *LPARAM* -Parameter. Die **REBARBANDINFO** -Strukturmember definieren die Merkmale eines bestimmten Bands. Um die Merkmale eines Bands festzulegen, legen Sie den **CBSIZE** -Member fest, um die Größe der Struktur anzugeben (in Bytes). Legen Sie dann den **fmask** -Member fest, um anzugeben, welche Strukturmember Ihre Anwendung füllt.

Wenn Sie ein untergeordnetes Fenster einem Band zuweisen möchten, schließen Sie das untergeordnete rbbim \_ -Flag in den **fmask** -Member der [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) -Struktur ein, und legen Sie dann das **hwndchild** -Element auf das Handle des untergeordneten Fensters fest. Anwendungen können die minimale zulässige Breite und Höhe eines untergeordneten Fensters in den Membern **cxminchild** und **cyminchild** festlegen.

Wenn ein Grund leisten-Steuerelement zerstört wird, werden alle untergeordneten Fenster, die den darin enthaltenen Bändern zugewiesen sind, zerstört. Um zu verhindern, dass das Steuerelement die den Bändern zugewiesenen untergeordneten Fenster zerstört, entfernen Sie die Bänder, indem Sie die [**RB \_ DeleteBand**](rb-deleteband.md) -Nachricht senden, und verwenden Sie dann die [**RB- \_ SetParent**](rb-setparent.md) -Nachricht, um das übergeordnete Fenster auf ein anderes Fenster zurückzusetzen, bevor Sie das

## <a name="the-rebar-control-user-interface"></a>Die Benutzeroberfläche des Grund leisten-Steuer Elements

Für alle Grund leisten-Steuerelemente kann die Größe geändert werden, mit Ausnahme derjenigen, die den RBBS- \_ FixedSize-Stil verwenden. Wenn Sie die Größe der Bänder im Steuerelement ändern oder ändern möchten, klicken und ziehen Sie die Zieh Punkt Leiste eines Bands. Das Grund leisten-Steuerelement ändert die Größe und Position von untergeordneten Fenstern, die seinen Bändern zugewiesen sind, automatisch. Außerdem können Sie die Größe eines Bands umschalten, indem Sie ggf. auf den Text des Bands klicken.

## <a name="the-rebar-controls-image-list"></a>Bildliste des Grund leisten-Steuer Elements

Wenn eine Anwendung eine Bildliste mit einem Grund leisten-Steuerelement verwendet, muss Sie die [**RB- \_ setbarinfo**](rb-setbarinfo.md) -Nachricht senden, bevor dem Steuerelement Bänder hinzugefügt werden. Diese Nachricht akzeptiert die Adresse einer [**rebarinfo**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) -Struktur als *LPARAM* -Parameter. Bereiten Sie vor dem Senden der Nachricht die **rebarinfo** -Struktur vor, indem Sie das **CBSIZE** -Element auf die Größe der Struktur festlegen (in Bytes). Wenn das Grund leisten-Steuerelement Bilder auf den Bändern anzeigt, legen Sie den **fmask** -Member auf das rbim \_ -ImageList-Flag fest, und weisen Sie dem **HIML** -Member ein Bildlisten Handle zu. Wenn für die Info Leiste keine bandbilder verwendet werden, legen Sie **fmask** auf 0 (null) fest.

## <a name="rebar-control-message-forwarding"></a>Weiterleitungs Steuerung der Nachrichten Weiterleitung

Ein Grund leisten-Steuerelement leitet alle [**WM- \_ Benachrichtigungs**](wm-notify.md) Fenster Meldungen an das übergeordnete Fenster weiter. Außerdem leitet ein Grund leisten-Steuerelement alle gesendeten Nachrichten von Windows ab, das seinen Bändern zugewiesen ist, wie z. b. [**WM \_ chartoitem**](wm-chartoitem.md), [**WM \_ Command**](/windows/desktop/menurc/wm-command)und anderen.

 

 