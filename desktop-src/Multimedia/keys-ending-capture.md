---
title: Schlüssel zum Beenden der Erfassung
description: Schlüssel zum Beenden der Erfassung
ms.assetid: 932ed4ee-0928-41f7-a242-8b7435313647
keywords:
- WM_CAP_GET_SEQUENCE_SETUP Meldung
- capcapturegetsetup-Makro
- Captuprojektms-Struktur
- WM_CAP_SET_SEQUENCE_SETUP Meldung
- capcapturesetsetup-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a91d6ee7d07ed36c11cce7e888c9a9710f403cf9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725113"
---
# <a name="keys-ending-capture"></a>Schlüssel zum Beenden der Erfassung

Sie können es Benutzern ermöglichen, eine Erfassungs Sitzung abzubrechen, indem Sie eine Tastenkombination oder Tastenkombination aus der Tastatur drücken, oder indem Sie die Rechte oder die linke Maustaste drücken. Wenn der Benutzer eine echt Zeit Erfassungs Sitzung abbricht, wird der Inhalt der Erfassungs Datei verworfen. Wenn der Benutzer eine Schritt-Frame-Erfassungs Sitzung abbricht, wird der Inhalt der Erfassungs Datei bis zum Zeitpunkt der Abbruch Erfassung gespeichert.

Sie können die Einstellungen für das Abbrechen einer Erfassungs Sitzung abrufen, indem Sie die " [**WM \_ Cap \_ get \_ Sequence \_**](wm-cap-get-sequence-setup.md) "-Setup Nachricht (oder das " [**capcapturegetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) "-Makro) verwenden. Die aktuelle Tastatureingabe-Einstellung wird im **vkeyabort** -Member der [**captumamams**](/windows/win32/api/vfw/ns-vfw-captureparms) -Struktur gespeichert. die aktuellen Mauseinstellungen werden in den Elementen **fabortleftmouse** und **faborzghtmouse** gespeichert. Sie können eine neue Tastenkombination oder Tastenkombination festlegen, indem Sie die Kombination aus Keycode oder Keycode (wie in einer Tastenkombination STRG oder UMSCHALT) als Wert von **vkeyabort** angeben oder die linke oder Rechte Maustaste als Abbruch Taste festlegen, indem Sie den **fabortleftmouse** -Member oder den **faborzghtmouse** -Member angeben. Nachdem Sie diese Member festgelegt haben, senden Sie die aktualisierte **captuadapms** -Struktur mithilfe der " [**WM \_ Cap \_ Set \_ Sequence \_**](wm-cap-set-sequence-setup.md) "-Setup Nachricht (oder dem " [**capcapturesetsetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) "-Makro) an das Aufzeichnungs Fenster. Der Standardwert von **vkeyabort** ist "VK \_ Escape". Sie müssen die [RegisterHotKey](/windows/win32/api/winuser/nf-winuser-registerhotkey) -Funktion aufrufen, bevor Sie eine Tastenkombination angeben, mit der eine Aufzeichnungs Sitzung abgebrochen werden kann. Die Standardwerte von **fabortleftmouse** und **faborseleghtmouse** sind **true**.

 

 