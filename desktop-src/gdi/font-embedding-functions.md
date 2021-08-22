---
description: Die folgenden Funktionen werden mit eingebetteten Microsoft OpenType-Schriftarten verwendet.
ms.assetid: 8f47d7a5-db45-4a41-8af2-9fc6b373a531
title: Funktionen zum Einbetten von Schriftarten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fe820c8b9e6a17f148705599d77ea08bbc4b3f8d52821c171c9e86ca13e2ad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761183"
---
# <a name="font-embedding-functions"></a>Funktionen zum Einbetten von Schriftarten

Die folgenden Funktionen werden mit eingebetteten Microsoft OpenType-Schriftarten verwendet.



| Funktion                                                                   | BESCHREIBUNG                                                                                                                                              |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*CFP \_ ALLOCPROC*](/windows/desktop/api/FontSub/nc-fontsub-cfp_allocproc)                                      | Von der Anwendung bereitgestellte Speicherbelegungsfunktion für CreateFontPackage und MergeFontPackage.                                                              |
| [*CFP \_ FREEPROC*](/windows/desktop/api/FontSub/nc-fontsub-cfp_freeproc)                                        | Von der Anwendung bereitgestellte Speicheraufbelegungsfunktion für CreateFontPackage und MergeFontPackage.                                                            |
| [*CFP \_ REALLOCPROC*](/windows/desktop/api/FontSub/nc-fontsub-cfp_reallocproc)                                  | Von der Anwendung bereitgestellte Speicherzuteilungsfunktion für CreateFontPackage und MergeFontPackage.                                                            |
| [**CreateFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-createfontpackage)                             | Erstellt eine kompaktere Version einer angegebenen TrueType-Schriftart, um sie an einen Drucker zu übergeben. Die resultierende Schriftart kann eine Teilmenge, eine Komprimierung oder beides sein. |
| [**MergeFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-mergefontpackage)                               | Führt Teilmengenschriftarten zusammen, die von CreateFontPackage erstellt wurden.                                                                                                        |
| [*READEMBEDPROC*](/previous-versions//dd162894(v=vs.85))                                       | Vom Client bereitgestellte Rückruffunktion zum Lesen von Streaminhalten aus einem Puffer.                                                                                 |
| [**TTCharToUnicode**](/windows/desktop/api/T2embapi/nf-t2embapi-ttchartounicode)                                 | Konvertiert ein Array von 8-Bit-Zeichencodewerten in 16-Bit-Unicode-Werte.                                                                               |
| [**TTDeleteEmbeddedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttdeleteembeddedfont)                       | Gibt von einer eingebetteten Schriftart verwendeten Arbeitsspeicher frei.                                                                                                                |
| [**TTEmbedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfont)                                         | Erstellt eine Schriftstruktur, die eine teilteilige Breitzeichenschriftart (16-Bit) enthält, wobei ein Gerätekontext als Quelle für Schriftarteinbettungsinformationen verwendet wird.           |
| [**TTEmbedFontEx**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontex)                                     | Erstellt eine Schriftstruktur, die die UCS-4-Schriftart (32-Bit) mit Teilmengen enthält, wobei ein Gerätekontext als Quelle für die Schriftarteinbettungsinformationen verwendet wird.        |
| [**TTEmbedFontFromFileA**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontfromfilea)                       | Erstellt eine Schriftartstruktur, die eine teilteilige Breitzeichenschriftart (16-Bit) enthält, wobei eine Datei als Quelle für Schriftarteinbettungsinformationen verwendet wird.                     |
| [**TTEnableEmbeddingForFacename**](/windows/desktop/api/T2embapi/nf-t2embapi-ttenableembeddingforfacename)       | Fügt Facenames der Schriftartausschlussliste hinzu oder entfernt sie aus dieser.                                                                                              |
| [**TTGetEmbeddedFontInfo**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetembeddedfontinfo)                     | Ruft Informationen zu einer eingebetteten Schriftart ab.                                                                                                            |
| [**TTGetEmbeddingType**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetembeddingtype)                           | Gibt einbettende Berechtigungen einer Schriftart zurück.                                                                                                                  |
| [**TTGetNewFontName**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetnewfontname)                               | Erstellt einen neuen Namen für eine installierte eingebettete Schriftart.                                                                                                       |
| [**TTIsEmbeddingEnabled**](/windows/desktop/api/T2embapi/nf-t2embapi-ttisembeddingenabled)                       | Bestimmt, ob die Schriftartausschlussliste eine angegebene Schriftart enthält.                                                                                     |
| [**TTIsEmbeddingEnabledForFacename**](/windows/desktop/api/T2embapi/nf-t2embapi-ttisembeddingenabledforfacename) | Bestimmt, ob das Einbetten für eine angegebene Schriftart aktiviert ist.                                                                                            |
| [**TTLoadEmbeddedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttloadembeddedfont)                           | Liest die eingebettete Schriftart aus dem Dokumentstream und installiert sie. Ermöglicht es einem Client auch, die Einbettungsberechtigungen der Schriftart weiter einzuschränken.             |
| [**TTRunValidationTests**](/windows/desktop/api/T2embapi/nf-t2embapi-ttrunvalidationtests)                       | Überprüft teile oder alle Glyphendaten einer Breitzeichenschriftart (16-Bit) im angegebenen Größenbereich.                                                         |
| [**TTRunValidationTestsEx**](/windows/desktop/api/T2embapi/nf-t2embapi-ttrunvalidationtestsex)                   | UCS-4-Version von TTRunValidationTests.                                                                                                                   |
| [*WRITEEMBEDPROC*](/previous-versions//dd145225(v=vs.85))                                     | Vom Client bereitgestellte Rückruffunktion zum Schreiben von Streaminhalten in einen Puffer.                                                                                  |



 

 

 
