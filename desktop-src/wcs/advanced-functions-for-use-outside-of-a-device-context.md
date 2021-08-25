---
title: Erweiterte Funktionen zur Verwendung außerhalb eines Gerätekontexts
description: Diese Funktionen bieten erweiterte Farbverwaltungsfunktionen außerhalb von Gerätekontexten.
ms.assetid: 2f742743-094a-44b8-816b-24246607caeb
keywords:
- Windows Color System (WCS), Funktionen
- WCS (Windows Color System), Funktionen
- Bildfarbverwaltung, Funktionen
- Farbverwaltung, Funktionen
- Farben, Funktionen
- WCS-Referenz, Funktionen
- Referenz für WCS,Functions
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685b9fe1c7139be1c54e1b158a03c1de54d01b2b80ec4cab4b86603680c6d957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814614"
---
# <a name="advanced-functions-for-use-outside-of-a-device-context"></a>Erweiterte Funktionen zur Verwendung außerhalb eines Gerätekontexts

Diese Funktionen bieten erweiterte Farbverwaltungsfunktionen außerhalb von Gerätekontexten.



| Funktion                                                           | Beschreibung                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PCMSCALLBACKW**](/windows/win32/api/icm/nc-icm-pcmscallbackw) | \**PCMSCALLBACKW** (oder **ApplyCallbackFunction**) ist eine Rückruffunktion, die Sie implementieren, die die WCS-Konfigurationsdaten aktualisiert, während das von der [**SetupColorMatchingW-Funktion**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) angezeigte Dialogfeld ausgeführt wird. |
| [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Überprüft, ob die Pixel in einer angegebenen Bitmap innerhalb der Ausgabe [gamut](g.md) einer angegebenen Transformation liegen. |
| [**CheckColors**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Bestimmt, ob die Farben in einem Array innerhalb des [Ausgabeumfangs](g.md) einer angegebenen Transformation liegen. |
| [**ConvertColorNameToIndex**](/windows/win32/api/icm/nf-icm-convertcolornametoindex) | Konvertiert Farbnamen in einem benannten Farbraum in Indexnummern in einem COLOR-Farbprofil (International Color Consortium). |
| [**ConvertIndexToColorName**](/windows/win32/api/icm/nf-icm-convertindextocolorname) | Transformiert Indizes in einem Farbraum in ein Array von Namen in einem benannten Farbraum. |
| [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) | Transformiert Indizes in einem Farbraum in ein Array von Namen in einem benannten Farbraum. |
| [**CreateMultiProfileTransform**](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) | Akzeptiert ein Array von Profilen oder ein einzelnes [Gerätelinkprofil](d.md) und erstellt eine Farbtransformation, die Anwendungen zum Durchführen der Farbzuordnung verwenden können. |
| [**DeleteColorTransform**](/windows/win32/api/icm/nf-icm-deletecolortransform) | Löscht eine angegebene Farbtransformation. |
| [**GetCMMInfo**](/windows/win32/api/icm/nf-icm-getcmminfo) | Ruft verschiedene Informationen zum Farbverwaltungsmodul (Color Management Module, CMM) ab, das die angegebene Farbtransformation erstellt hat. |
| [**GetNamedProfileInfo**](/windows/win32/api/icm/nf-icm-getnamedprofileinfo) | Ruft Informationen zum benannten Farbprofil des International Color Consortium (INTERNATIONAL) ab, das im ersten Parameter angegeben ist. |
| [**ICMProgressProcCallback**](icmprogressproccallback.md)         | Von der Anwendung bereitgestellte Rückruffunktion zum Melden des Fortschritts. Der Name dieser Funktion wird auch von der Anwendung definiert.                                                 |
| [**Wählen SieCMM aus.**](/windows/win32/api/icm/nf-icm-selectcmm) | Ermöglicht ihnen die Auswahl des bevorzugten Farbverwaltungsmoduls (CMM), das verwendet werden soll. |
| [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw)                   | Stellt die Benutzersteuerung über die Farbverwaltung über ein Dialogfeld bereit.                                                                                                      |
| [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)                 | Konvertiert Bitmapfarben mithilfe einer Farbtransformation.                                                                                                                          |
| [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) | Übersetzt ein Array von Farben aus dem [Quellfarbraum](c.md) in den Zielfarbraum, wie durch eine Farbtransformation definiert. |
| [**WcsCheckColors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)                           | Bestimmt, ob sich die Farben in einem Array innerhalb des Ausgabeumfangs einer angegebenen WCS-Farbtransformation befinden.                                                                |
| [**WcsTranslateColors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors) | Übersetzt ein Array von Farben aus dem Quellfarbraum in den Zielfarbraum, wie durch eine Farbtransformation definiert.                                                |



 

 

 




