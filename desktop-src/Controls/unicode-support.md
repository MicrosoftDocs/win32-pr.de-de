---
title: Unicode-Unterstützung für allgemeine Steuerelemente
description: In diesem Thema wird beschrieben, wie Unicode für allgemeine Steuerelementbenachrichtigungen unterstützt wird.
ms.assetid: 5020F638-261D-4D32-ACC4-F9572EDBE875
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01ab987516f1a91b47f8e5fd5f031631956d8c7bf59cd164edd83d414d5e72d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668892"
---
# <a name="unicode-support-for-common-controls"></a>Unicode-Unterstützung für allgemeine Steuerelemente

In diesem Thema wird beschrieben, wie Unicode für allgemeine Steuerelementbenachrichtigungen unterstützt wird.


Für Die Versionen 5.80 und höher von comctl32.dll unterstützen allgemeine Steuerungsbenachrichtigungen sowohl das ANSI- als auch das Unicode-Format auf Windows 95 Systemen oder höher. Das System bestimmt, welches Format verwendet werden soll, indem eine [**WM \_ NOTIFYFORMAT-Meldung**](wm-notifyformat.md) an Ihr Fenster gesendet wird. Um ein Format anzugeben, geben Sie \_ NFR-ANSI für ANSI-Benachrichtigungen oder NFR \_ UNICODE für Unicode-Benachrichtigungen zurück. Wenn Sie diese Meldung nicht verarbeiten, ruft das System [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) auf, um das Format zu bestimmen. Da Windows 95 und Windows 98 immer **FALSE** an diesen Funktionsaufruf zurückgeben, verwenden sie standardmäßig ANSI-Benachrichtigungen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu allgemeinen Steuerelementen](common-controls-intro.md)
</dt> </dl>

 

 