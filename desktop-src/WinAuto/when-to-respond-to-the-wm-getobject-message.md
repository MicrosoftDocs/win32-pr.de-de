---
title: Wann auf die WM_GETOBJECT-Nachricht reagiert werden soll
description: Wenn eine Anwendung Microsoft Active Accessibility oder Benutzeroberflächenautomatisierung für ein Benutzeroberflächenelement unterstützt, darf die Anwendung nicht auf die WM \_ GETOBJECT-Nachricht reagieren, bevor das Objekt, das das Benutzeroberflächenelement darstellt, vollständig initialisiert wird oder nachdem die Anwendung mit dem Schließen begonnen hat.
ms.assetid: cc99f7ef-1eb6-40c4-9ec0-8fb18cb4a3e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdb12edde21b7906fdda91d1bc5d46e453696214b93a331e26034527e163a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114615"
---
# <a name="when-to-respond-to-the-wm_getobject-message"></a>Wann auf die WM GETOBJECT-Nachricht reagiert werden soll \_

Wenn eine Anwendung Microsoft Active Accessibility oder Benutzeroberflächenautomatisierung für ein Benutzeroberflächenelement unterstützt, darf die Anwendung nicht auf die [**WM \_ GETOBJECT-Nachricht**](wm-getobject.md) reagieren, bevor das Objekt, das das Benutzeroberflächenelement darstellt, vollständig initialisiert wurde oder nachdem die Anwendung mit dem Schließen begonnen hat. Wenn eine Anwendung ein neues Fenster erstellt, löst das System das [**EVENT \_ OBJECT \_ CREATE**](event-constants.md) WinEvent aus, um Clients zu benachrichtigen, bevor die [**WM \_ CREATE-Nachricht**](/windows/desktop/winmsg/wm-create) an die Fensterprozedur der Anwendung gesendet wird. Da viele Anwendungen **WM \_ CREATE** verwenden, um den Initialisierungsprozess zu starten, reagiert jede Barrierefreiheitsimplementierung eines Benutzeroberflächenelements erst auf die [**WM \_ GETOBJECT-Nachricht,**](wm-getobject.md) nachdem die Anwendung die Verarbeitung der **WM \_ CREATE-Nachricht** abgeschlossen hat.

 

 