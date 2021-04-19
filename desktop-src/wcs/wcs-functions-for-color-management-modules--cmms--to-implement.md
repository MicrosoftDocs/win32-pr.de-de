---
title: WCS-Funktionen für die zu implementierenden Farbverwaltungsmodule (CMMs)
description: Die folgenden Funktionen werden von den Farb Verwaltungs Modulen (CMMS) implementiert und für das Betriebssystem exportiert, um aufzurufen.
ms.assetid: e05129ec-9128-44f0-82c7-f4e01536d7a8
keywords:
- Windows Color System (WCS), Funktionen
- WCS (Windows Color System), Funktionen
- Bild Farbverwaltung, Funktionen
- Farbverwaltung, Funktionen
- Farben, Funktionen
- WCS-Referenz, Funktionen
- Referenz für WCs, Funktionen
- Windows Color System (WCS), Farb Verwaltungsmodul (CMM)
- WCS (Windows Color System), Farb Verwaltungsmodul (CMM)
- Bild Farbverwaltung, Farb Verwaltungsmodul (CMM)
- Farbverwaltung, Farb Verwaltungsmodul (CMM)
- Farben, Farb Verwaltungsmodul (CMM)
- WCS-Referenz, Farb Verwaltungsmodul (CMM)
- Referenz für WCs, Farb Verwaltungsmodul (CMM)
- Farb Verwaltungsmodul (CMM)
- CMM (Farb Verwaltungsmodul)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e9092c49077b1b4dda9e06829329194ec2e261
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106353266"
---
# <a name="wcs-functions-for-color-management-modules-cmms-to-implement"></a>WCS-Funktionen für die zu implementierenden Farbverwaltungsmodule (CMMs)

Die folgenden Funktionen werden von den Farb Verwaltungs Modulen (CMMS) implementiert und für das Betriebssystem exportiert, um aufzurufen.



| Funktion                                                                     | BESCHREIBUNG                                                                               |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**Cmcheckcolors**](/windows/win32/api/icm/nf-icm-cmcheckcolors) | Bestimmt, ob angegebene Farben [im Ausgabe Spiel einer angegebenen](./g.md) Transformation liegen. |
| [**Cmcheckcolorsingamut**](/windows/win32/api/icm/nf-icm-cmcheckcolorsingamut) | Bestimmt, ob die angegebenen RGB-drei [im Ausgabe Spiel einer angegebenen](./g.md) Transformation liegen. |
| [**Cmcheckrgsb**](/windows/desktop/api/Wingdi/)                                           | Überprüft Bitmap-Farben anhand eines Ausgabe gamches.                                             |
| [**Cmconvertcolornametoindex**](/windows/win32/api/icm/nf-icm-cmconvertcolornametoindex) | Konvertiert Farbnamen in einem benannten Farbraum in Indexnummern in einem Farbprofil |
| [**Cmconvertindexycolorname**](/windows/win32/api/icm/nf-icm-cmconvertindextocolorname) | Transformiert Indizes in einem Farbraum in ein Array von Namen in einem benannten Farbraum. |
| [**Cmkreatedevicelinkprofile**](/windows/win32/api/icm/nf-icm-cmcreatedevicelinkprofile) | Erstellt ein [Geräte](./d.md) Verknüpfungs Profil in dem Format, das vom International Color Consortium in seiner Spezifikation für das ICC-Profil Format angegeben wird. |
| [**Cmkreatemultiprofiletransform**](/windows/win32/api/icm/nf-icm-cmcreatemultiprofiletransform) | Akzeptiert ein Array von Profilen oder ein einzelnes [Geräte](./d.md) Verknüpfungs Profil und erstellt eine Farb Transformation. Diese Transformation ist eine Zuordnung von dem Farbraum, der durch das erste Profil angegeben wird, zu dem des zweiten Profils usw. |
| [**Cmkreateprofile**](/windows/win32/api/icm/nf-icm-cmcreateprofile) | Erstellt ein Anzeige Farbprofil aus einer [**logcolorspacea**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) -Struktur. |
| [**Cmkreateprofilew**](/windows/win32/api/icm/nf-icm-cmcreateprofilew) | Erstellt ein Anzeige Farbprofil aus einer [**logcolorspacew**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) -Struktur. |
| [**Cmkreatetransform**](/windows/win32/api/icm/nf-icm-cmcreatetransform) | Veraltet. Es gibt keine Ersatz-API, da diese nicht mehr verwendet wird. Entwickler alternativer CMM-Module müssen diese nicht implementieren. |
| [**Cmkreatetransformext**](/windows/win32/api/icm/nf-icm-cmcreatetransformext) | Erstellt eine Farb Transformation, die von einer Eingabe [**logcolorspacea**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacea) zu einem optionalen Ziel Raum und dann zu einem Ausgabegerät zugeordnet wird. dabei wird ein Satz von Flags verwendet, die definieren, wie die Transformation erstellt werden soll. |
| [**Cmkreatetransformextw**](/windows/win32/api/icm/nf-icm-cmcreatetransformextw) | Erstellt eine Farb Transformation, die von einer Eingabe [**logcolorspacew**](/windows/win32/api/wingdi/ns-wingdi-logcolorspacew) zu einem optionalen Ziel Raum und dann zu einem Ausgabegerät zugeordnet wird. dabei wird ein Satz von Flags verwendet, die definieren, wie die Transformation erstellt werden soll. |
| [**Cmkreatetransformw**](/windows/win32/api/icm/nf-icm-cmcreatetransformw) | Veraltet. Es gibt keine Ersatz-API, da diese nicht mehr verwendet wird. Entwickler alternativer CMM-Module müssen diese nicht implementieren. |
| [**Cmdeletetransform**](/windows/win32/api/icm/nf-icm-cmdeletetransform) | Löscht eine angegebene Farb Transformation und gibt den zugeordneten Arbeitsspeicher frei. |
| [**Cmgetinfo**](/windows/win32/api/icm/nf-icm-cmgetinfo) | Ruft verschiedene Informationen über das Farb Verwaltungsmodul (Color Management Module, CMM) ab. |
| [**Cmgetnamedprofileingefo**](/windows/win32/api/icm/nf-icm-cmgetnamedprofileinfo) | Ruft Informationen über das angegebene benannte Farbprofil ab. |
| [**CMGetPS2ColorRenderingDictionary**](/windows/desktop/api/Wingdi/) | Ruft ein PostScript-Farb Rendering-Wörterbuch ab.                                             |
| [**CMGetPS2ColorRenderingIntent**](/windows/win32/api/icm/nf-icm-cmgetps2colorrenderingintent) | Ruft das [textrenderingziel](rendering-intents.md) der PostScript-Ebene 2 aus einem Profil ab. |
| [**CMGetPS2ColorSpaceArray**](/windows/desktop/api/Wingdi/)                   | Ruft ein Zeichen für ein PostScript-Farbraum ab.                                                      |
| [**Cmispromelevalid**](/windows/win32/api/icm/nf-icm-cmisprofilevalid) | Meldet, ob das angegebene Profil ein gültiges ICC-Profil ist, das für die Farbverwaltung verwendet werden kann. |
| [**Cmtranslatecolors**](/windows/win32/api/icm/nf-icm-cmtranslatecolors) | Übersetzt ein Array von Farben aus einem Quell [Farbraum](rendering-intents.md) mithilfe einer Farb Transformation in einen Ziel Farbraum. |
| [**Cmtranslatergb**](/windows/win32/api/icm/nf-icm-cmtranslatergb) | Übersetzt ein von der Anwendung bereitgestelltes rgbquad in den Geräte [Farbraum](color-spaces.md). |
| [**Cmtranslatergsb**](/windows/win32/api/icm/nf-icm-cmtranslatergbs) | Übersetzt eine Bitmap mithilfe einer Farb Transformation von einem [Farb Raum](color-spaces.md) in einen anderen. |
| [**Cmtranslatergbsegxt**](/windows/win32/api/icm/nf-icm-cmtranslatergbsext) | Übersetzt eine Bitmap aus einem definierten Format in ein anderes definiertes Format und ruft in regelmäßigen Abständen eine Rückruffunktion auf, wenn eine angegeben wird, um den Fortschritt zu melden und zuzulassen, dass die aufrufenden Anwendung die Übersetzung beendet. |



 

 

 