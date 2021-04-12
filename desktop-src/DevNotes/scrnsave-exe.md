---
description: Desktop der HKCU \\ -Systemsteuerung \\
ms.assetid: e18ea3c8-ddac-4214-83be-106c28c3c327
title: SCRNSAVE.EXE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d6a5d50b002299fe38508b387926b0eed11141
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393158"
---
# <a name="scrnsaveexe"></a>SCRNSAVE.EXE

**Desktop der HKCU \\ -Systemsteuerung \\**



| Datentyp | Range       | Standardwert |
|-----------|-------------|---------------|
| REG- \_ SZ   | *Dateiname* | (Keine)        |



 

## <a name="description"></a>BESCHREIBUNG

Gibt den Namen der ausführbaren Datei für den Bildschirmschoner an.

## <a name="change-method"></a>Methode ändern

Um den Wert dieses Eintrags zu ändern, doppelklicken Sie in der Systemsteuerung auf **Anzeige**, klicken Sie auf die Registerkarte **Bildschirmschoner** , und wählen Sie dann in der Liste **Bildschirmschoner** einen Bildschirmschoner aus.

Sie können diesen Eintrag auch mit der API-Funktion (Application Programming Interface, Anwendungsprogrammierschnittstelle) ändern, die von Desk.cpl **exportiert wird.** Sie können auf diese Funktion mit der Befehlszeile **rundll32.exe desk.cpl, installbildschirm** *Datei* zugreifen, wobei *File* der Name einer ausführbaren Datei für Bildschirmschoner ist.

## <a name="activation-method"></a>Aktivierungsmethoden

Änderungen, die an diesem Eintrag vorgenommen werden, werden wirksam, wenn das System den Bildschirmschoner das nächste Mal startet. Änderungen, die an diesem Eintrag vorgenommen werden, während ein Bildschirmschoner ausgeführt wird, wirken sich nicht auf die Ausführung des Bildschirmschoners aus.

## <a name="notes"></a>Notizen

-   Windows-Betriebssysteme fügen diesen Eintrag zur Registrierung hinzu, wenn Sie in der Systemsteuerung **anzeigen** verwenden, um einen Bildschirmschoner auszuwählen. Wenn Sie alle Bildschirmschoner deaktivieren, indem Sie in der Liste Bildschirmschoner den Eintrag **(keine)** auswählen, löscht das Betriebssystem diesen Eintrag aus der Registrierung und ruft die [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) -Funktion mit *uiaction* gleich SPI \_ setscreensaveactive und *uiparam* gleich **false** auf.
-   Dieser Eintrag kann durch eine Gruppenrichtlinie Einstellung auf Systemen ersetzt werden, die Gruppenrichtlinie unterstützen. Während der **Name der ausführbaren Datei für den Bildschirmschoner** Gruppenrichtlinie Einstellung aktiviert ist, wird dieser Eintrag vom System ignoriert. Die Konfiguration dieser Richtlinien Einstellung wird im **SCRNSAVE.EXE** Eintrag gespeichert, der sich im Unterschlüssel " **Richtlinien** " befindet.

 

 
