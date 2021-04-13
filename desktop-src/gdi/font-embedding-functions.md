---
description: Die folgenden Funktionen werden mit eingebetteten Microsoft OpenType-Schriftarten verwendet.
ms.assetid: 8f47d7a5-db45-4a41-8af2-9fc6b373a531
title: Schriftart Einbettungs Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ece5b413be5489bf51df38fd92b6f3167823506
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994031"
---
# <a name="font-embedding-functions"></a>Schriftart Einbettungs Funktionen

Die folgenden Funktionen werden mit eingebetteten Microsoft OpenType-Schriftarten verwendet.



| Funktion                                                                   | BESCHREIBUNG                                                                                                                                              |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*cFP- \_ Zuweisung*](/windows/desktop/api/FontSub/nc-fontsub-cfp_allocproc)                                      | Von der Anwendung bereitgestellte Speicher Belegungs Funktion für "kreatefontpackage" und "mergefontpackage".                                                              |
| [*cFP- \_ freiproc*](/windows/desktop/api/FontSub/nc-fontsub-cfp_freeproc)                                        | Von der Anwendung bereitgestellte Speicher Belegungs Funktion für "", "" und "mergefontpackage".                                                            |
| [*cFP \_ rezuweisung*](/windows/desktop/api/FontSub/nc-fontsub-cfp_reallocproc)                                  | Von der Anwendung bereitgestellte Funktion zur erneuten Zuordnung von Speicher für "anatefontpackage" und "mergefontpackage".                                                            |
| [**"Kreatefontpackage"**](/windows/desktop/api/FontSub/nf-fontsub-createfontpackage)                             | Erstellt eine kompaktere Version einer angegebenen TrueType-Schriftart, um Sie an einen Drucker zu übergeben. Die resultierende Schriftart kann subsetted, komprimiert oder beides sein. |
| [**Mergefontpackage**](/windows/desktop/api/FontSub/nf-fontsub-mergefontpackage)                               | Führt die von "kreatefontpackage" erstellten Teilmenge von Schriftarten zusammen.                                                                                                        |
| [*Readembedproc*](/previous-versions//dd162894(v=vs.85))                                       | Vom Client bereitgestellte Rückruffunktion zum Lesen von streaminhalten aus einem Puffer.                                                                                 |
| [**Ttcharum Unicode**](/windows/desktop/api/T2embapi/nf-t2embapi-ttchartounicode)                                 | Konvertiert ein Array von 8-Bit-Zeichencode Werten in 16-Bit-Unicode-Werte.                                                                               |
| [**Ttdeleteembeddecodfont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttdeleteembeddedfont)                       | Gibt den von einer eingebetteten Schriftart verwendeten Arbeitsspeicher frei.                                                                                                                |
| [**Ttembedfont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfont)                                         | Erstellt eine Schriftart Struktur, die eine untergeordnete breit Zeichen Schriftart (16-Bit) enthält, wobei ein Gerätekontext als Quelle für die Schriftart Einbettungs Informationen verwendet wird.           |
| [**Ttembedfontex**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontex)                                     | Erstellt eine Schriftart Struktur, die die untergeordnete UCS-4-Zeichen Schriftart (32-Bit) enthält. dabei wird ein Gerätekontext als Quelle für die Schriftart Einbettungs Informationen verwendet.        |
| [**Ttembedfontfromflea**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontfromfilea)                       | Erstellt eine Schriftart Struktur, die eine untergeordnete breit Zeichen Schriftart (16-Bit) mit einer Datei als Quelle zum Einbetten von Informationen enthält.                     |
| [**Ttenableembeddingforename**](/windows/desktop/api/T2embapi/nf-t2embapi-ttenableembeddingforfacename)       | Fügt der Schriftart Ausschlussliste hinzu oder entfernt diese.                                                                                              |
| [**Ttgetembeddecodfontinfo**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetembeddedfontinfo)                     | Ruft Informationen zu einer eingebetteten Schriftart ab.                                                                                                            |
| [**TTGetEmbeddingType**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetembeddingtype)                           | Gibt Einbettungs Berechtigungen einer Schriftart zurück.                                                                                                                  |
| [**Ttgetnewfontname**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetnewfontname)                               | Erstellt einen neuen Namen für eine installierte eingebettete Schriftart.                                                                                                       |
| [**Ttisembeddingenabled**](/windows/desktop/api/T2embapi/nf-t2embapi-ttisembeddingenabled)                       | Bestimmt, ob die Schriftart Ausschlussliste eine angegebene Schriftart enthält.                                                                                     |
| [**Ttisembeddingenabledforfakename**](/windows/desktop/api/T2embapi/nf-t2embapi-ttisembeddingenabledforfacename) | Bestimmt, ob die Einbettung für eine angegebene Schriftart aktiviert ist.                                                                                            |
| [**Ttloadembeddecodfont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttloadembeddedfont)                           | Liest die eingebettete Schriftart aus dem Dokumentstream und installiert sie. Ermöglicht einem Client außerdem, die Einbettungs Berechtigungen der Schriftart weiter einzuschränken.             |
| [**Ttrunvalidationtests**](/windows/desktop/api/T2embapi/nf-t2embapi-ttrunvalidationtests)                       | Überprüft Teile oder alle Symbol Daten einer breit Zeichen Schriftart (16-Bit) im angegebenen Größenbereich.                                                         |
| [**Ttrunvalidationtestsex**](/windows/desktop/api/T2embapi/nf-t2embapi-ttrunvalidationtestsex)                   | UCS-4-Version von ttrunvalidationtests.                                                                                                                   |
| [*"Write-embedproc"*](/previous-versions//dd145225(v=vs.85))                                     | Vom Client bereitgestellte Rückruffunktion, um streaminhalte in einen Puffer zu schreiben.                                                                                  |



 

 

 
