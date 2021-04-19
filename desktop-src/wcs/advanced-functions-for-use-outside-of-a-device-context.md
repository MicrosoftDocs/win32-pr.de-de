---
title: Erweiterte Funktionen zur Verwendung außerhalb eines Gerätekontexts
description: Diese Funktionen bieten erweiterte Funktionen für die Farbverwaltung außerhalb der Geräte Kontexte.
ms.assetid: 2f742743-094a-44b8-816b-24246607caeb
keywords:
- Windows Color System (WCS), Funktionen
- WCS (Windows Color System), Funktionen
- Bild Farbverwaltung, Funktionen
- Farbverwaltung, Funktionen
- Farben, Funktionen
- WCS-Referenz, Funktionen
- Referenz für WCs, Funktionen
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d04b7afe98f468fd3f580adf3eff145bce3aa1ac
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "106353237"
---
# <a name="advanced-functions-for-use-outside-of-a-device-context"></a>Erweiterte Funktionen zur Verwendung außerhalb eines Gerätekontexts

Diese Funktionen bieten erweiterte Funktionen für die Farbverwaltung außerhalb der Geräte Kontexte.



| Funktion                                                           | BESCHREIBUNG                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PCMSCALLBACKW**](/windows/win32/api/icm/nc-icm-pcmscallbackw) | \**PCMSCALLBACKW** (oder **applycallbackfunction**) ist eine Rückruffunktion, die Sie implementieren, um die WCS-Konfigurationsdaten zu aktualisieren, während das Dialogfeld, das von der [**setupcolormatchingw**](/windows/win32/api/icm/nf-icm-setupcolormatchingw) -Funktion angezeigt wird, ausgeführt wird. |
| [**Checkbitmapbits**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Überprüft, ob die Pixel in einer angegebenen Bitmap innerhalb des Ausgabe [gamches](g.md) einer angegebenen Transformation liegen. |
| [**Prüf Farben**](/windows/win32/api/icm/nf-icm-checkbitmapbits) | Bestimmt, ob die Farben in einem Array [im Ausgabe Spiel einer angegebenen](g.md) Transformation liegen. |
| [**Convertcolornametoindex**](/windows/win32/api/icm/nf-icm-convertcolornametoindex) | Konvertiert Farbnamen in einem benannten Farbraum in Indexnummern in einem International Color Consortium (ICC)-Farbprofil. |
| [**Convertindexycolorname**](/windows/win32/api/icm/nf-icm-convertindextocolorname) | Transformiert Indizes in einem Farbraum in ein Array von Namen in einem benannten Farbraum. |
| [**"Kreatecolortransformw"**](/windows/win32/api/icm/nf-icm-createcolortransformw) | Transformiert Indizes in einem Farbraum in ein Array von Namen in einem benannten Farbraum. |
| [**"Kreatemultiprofiletransform"**](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) | Akzeptiert ein Array von Profilen oder ein einzelnes [Geräte](d.md) Verknüpfungs Profil und erstellt eine Farb Transformation, mit der Anwendungen eine Farbzuordnung durchführen können. |
| [**Deletecolortransform**](/windows/win32/api/icm/nf-icm-deletecolortransform) | Löscht eine angegebene Farb Transformation. |
| [**Getcmminfo**](/windows/win32/api/icm/nf-icm-getcmminfo) | Ruft verschiedene Informationen über das Farb Verwaltungsmodul (Color Management Module, CMM) ab, das die angegebene Farb Transformation erstellt hat. |
| [**Getnamedprofilinfo**](/windows/win32/api/icm/nf-icm-getnamedprofileinfo) | Ruft Informationen über das im ersten Parameter angegebene benannte Farbprofil des International Color Consortium (ICC) ab. |
| [**Icmprogressproccallback**](icmprogressproccallback.md)         | Von der Anwendung bereitgestellte Rückruffunktion zum Melden des Status. Der Name dieser Funktion wird auch von der Anwendung definiert.                                                 |
| [**Selectcmm**](/windows/win32/api/icm/nf-icm-selectcmm) | Ermöglicht es Ihnen, das zu verwendende bevorzugte Farb Verwaltungsmodul (CMM) auszuwählen. |
| [**Setupcolormatchingw**](/windows/win32/api/icm/nf-icm-setupcolormatchingw)                   | Ermöglicht die Benutzersteuerung der Farbverwaltung über ein Dialogfeld.                                                                                                      |
| [**Translatebitmapbits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)                 | Konvertiert Bitmapfarben mithilfe einer Farb Transformation.                                                                                                                          |
| [**Translatecolors**](/windows/win32/api/icm/nf-icm-translatecolors) | Übersetzt ein Array von Farben aus dem [Quellfarbraum](c.md) in den Ziel Farbraum, wie durch eine Farb Transformation definiert. |
| [**Wcscheckcolors**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)                           | Bestimmt, ob die Farben in einem Array innerhalb des Ausgabe Farbskala einer angegebenen WCS-Farb Transformation liegen.                                                                |
| [**Wcstranslatecolors**](/windows/win32/api/icm/nf-icm-wcstranslatecolors) | Übersetzt ein Array von Farben aus dem Quellfarbraum in den Ziel Farbraum, wie durch eine Farb Transformation definiert.                                                |



 

 

 




