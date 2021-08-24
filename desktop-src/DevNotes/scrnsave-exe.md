---
description: HKCU \\ Systemsteuerung \\ Desktop.
ms.assetid: e18ea3c8-ddac-4214-83be-106c28c3c327
title: SCRNSAVE.EXE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e1ac7c0f2ee9d87911c0db195df89e2c27dcf1b19c0e9dac70d1517b0ad30ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571350"
---
# <a name="scrnsaveexe"></a>SCRNSAVE.EXE

**HKCU \\ Systemsteuerung \\ Desktop**



| Datentyp | Range       | Standardwert |
|-----------|-------------|---------------|
| REG \_ SZ   | *Dateiname* | (Keine)        |



 

## <a name="description"></a>Beschreibung

Gibt den Namen der ausführbaren Datei des Bildschirmschoners an.

## <a name="change-method"></a>Methode ändern

Um den Wert dieses Eintrags zu ändern, doppelklicken Sie  in Systemsteuerung auf **Anzeigen,** klicken Sie auf die Registerkarte Bildschirmschoner, und wählen Sie dann einen Bildschirmschoner aus der Liste Bildschirmschoner aus. 

Sie können diesen Eintrag auch mit der API-Funktion **InstallScreenSaver**(Anwendungsprogrammierschnittstelle) ändern, die von Desk.cpl. Sie können auf diese Funktion über die Befehlszeile **rundll32.exe desk.cpl,InstallScreenSaver-Datei** *zugreifen,* wobei file der Name einer ausführbaren Datei des Bildschirmschoners ist. 

## <a name="activation-method"></a>Aktivierungsmethoden

Änderungen an diesem Eintrag werden wirksam, wenn das System das nächste Mal einen Bildschirmschoner startet. Änderungen, die an diesem Eintrag vorgenommen werden, während ein Bildschirmschoner ausgeführt wird, haben keine Auswirkungen auf den ausgeführten Bildschirmschoner.

## <a name="notes"></a>Hinweise

-   Windows Betriebssystemen fügen Sie diesen Eintrag der Registrierung hinzu, wenn Sie **display** in Systemsteuerung verwenden, um einen Bildschirmschoner auszuwählen. Wenn Sie alle Bildschirmschoner deaktivieren, indem Sie **(Keine)** aus der Liste der Bildschirmschoner auswählen, löscht das Betriebssystem diesen Eintrag aus der Registrierung und ruft die [**SystemParametersInfo-Funktion**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) auf, bei der *uiAction* gleich SPI \_ SETSCREENSAVEACTIVE und *uiParam* gleich **FALSE** ist.
-   Dieser Eintrag kann durch eine Einstellung Gruppenrichtlinie auf Systemen ersetzt werden, die Gruppenrichtlinie. Während die **Einstellung Name der ausführbaren** Gruppenrichtlinie Bildschirmschoner aktiviert ist, ignoriert das System diesen Eintrag. Die Konfiguration dieser Richtlinieneinstellung wird  imSCRNSAVE.EXEgespeichert, der sich im Unterschlüssel **Richtlinien** befindet.

 

 
