---
title: Unicode-Unterstützung für allgemeine Steuerelemente
description: In diesem Thema wird beschrieben, wie Unicode für allgemeine Steuerelement Benachrichtigungen unterstützt wird.
ms.assetid: 5020F638-261D-4D32-ACC4-F9572EDBE875
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb029d6e1c018f1793c749aefb2f88104559cae
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949238"
---
# <a name="unicode-support-for-common-controls"></a>Unicode-Unterstützung für allgemeine Steuerelemente

In diesem Thema wird beschrieben, wie Unicode für allgemeine Steuerelement Benachrichtigungen unterstützt wird.


Bei den Versionen 5,80 und höher von comctl32.dll unterstützen allgemeine Steuerelement Benachrichtigungen sowohl ANSI-als auch Unicode-Formate auf Windows 95-Systemen oder höher. Das System bestimmt, welches Format verwendet werden soll, indem das Fenster eine [**WM \_ notifyformat**](wm-notifyformat.md) -Meldung gesendet wird. Wenn Sie ein Format angeben möchten, geben Sie NFR \_ ANSI für ANSI-Benachrichtigungen oder NFR \_ Unicode für Unicode-Benachrichtigungen zurück. Wenn Sie diese Meldung nicht verarbeiten, ruft das System [**iswindowunicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) auf, um das Format zu bestimmen. Da Windows 95 und Windows 98 bei diesem Funktions aufrufimmer **false** zurückgeben, werden standardmäßig ANSI-Benachrichtigungen verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu allgemeinen Steuerelementen](common-controls-intro.md)
</dt> </dl>

 

 