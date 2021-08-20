---
title: Schlüsselenderfassung
description: Schlüsselenderfassung
ms.assetid: 932ed4ee-0928-41f7-a242-8b7435313647
keywords:
- WM_CAP_GET_SEQUENCE_SETUP Meldung
- capCaptureGetSetup-Makro
- CAPTUREPARMS-Struktur
- WM_CAP_SET_SEQUENCE_SETUP Meldung
- capCaptureSetSetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5764f6b1853e1b161501f3c8df22ff0b7387649c517a28e7e36e7a094f35b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140050"
---
# <a name="keys-ending-capture"></a>Schlüsselenderfassung

Sie können dem Benutzer erlauben, eine Aufzeichnungssitzung abzubricht, indem Sie eine Tastenkombination über die Tastatur drücken oder die rechte oder linke Maustaste drücken. Wenn der Benutzer eine Echtzeiterfassungssitzung abbricht, wird der Inhalt der Aufzeichnungsdatei verworfen. Wenn der Benutzer eine Schrittframe-Aufzeichnungssitzung abbricht, wird der Inhalt der Erfassungsdatei bis zum Abbruch der Erfassung gespeichert.

Sie können die Einstellungen zum Abbrechen einer Aufzeichnungssitzung mithilfe der [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP-Meldung**](wm-cap-get-sequence-setup.md) (oder des [**CapCaptureGetSetup-Makros)**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) abrufen. Die aktuelle Tastatureingabeeinstellung wird im **vKeyAbort-Member** der [**CAPTUREPARMS-Struktur**](/windows/win32/api/vfw/ns-vfw-captureparms) gespeichert. die aktuellen Mauseinstellungen werden in den **Membern fAbortLeftMouse** und **fAbortRightMouse** gespeichert. Sie können eine neue Tastenkombination oder Tastenkombination festlegen, indem Sie die Tastencode- oder Keycodekombination (wie bei einer Tastenkombination mit STRG- oder UMSCHALTTASTE) als Wert von **vKeyAbort** oder die linke oder rechte Maustaste als Abbruchtaste festlegen, indem Sie den Member **fAbortLeftMouse** oder **fAbortRightMouse** angeben. Nachdem Sie diese Member festgelegt haben, senden Sie die aktualisierte **CAPTUREPARMS-Struktur** mithilfe der [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP-Meldung**](wm-cap-set-sequence-setup.md) (oder des [**CapCaptureSetSetup-Makros)**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) an das Erfassungsfenster. Der Standardwert von **vKeyAbort** ist VK \_ ESCAPE. Sie müssen die [RegisterHotKey-Funktion](/windows/win32/api/winuser/nf-winuser-registerhotkey) aufrufen, bevor Sie eine Tastatureingabe angeben, die eine Aufzeichnungssitzung abbrechen kann. Die Standardwerte von **fAbortLeftMouse** und **fAbortRightMouse** sind **TRUE.**

 

 