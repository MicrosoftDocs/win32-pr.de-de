---
description: Es ist in der Regel wünschenswert, einen komplizierteren Satz von Informationen zu kopieren, als im frei Hand Format (Ink serialisiert Format, ISF) enthalten sein können.
ms.assetid: 1cef7f91-118c-4a16-802d-bd2ec5d15416
title: Speichern von frei Hand Eingaben in HTML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8372e6e77ea0284bc44fa70883964e53b3063bab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350363"
---
# <a name="storing-ink-in-html"></a>Speichern von frei Hand Eingaben in HTML

Es ist in der Regel wünschenswert, einen komplizierteren Satz von Informationen zu kopieren, als im frei Hand Format (Ink serialisiert Format, ISF) enthalten sein können. HTML ist aufgrund seiner starken Akzeptanz als Industriestandard und der Fähigkeit, heterogenen Inhalt darzustellen, besonders als Interoperabilitäts Format nützlich.

HTML ist weitgehend verständlich, gut dokumentiert und mit vielen Entwicklern vertraut. Es gibt viele Tools für die HTML-Produktion. Darüber hinaus enthält Microsoft Windows APIs (Application Programming Interfaces) zum Rendern und manipulieren von HTML. Zum Schluss bieten die Tablet PC Platform-APIs das befestigte GIF-Persistenzformat, das zum Einbetten in andere Formate geeignet ist. Dieses Format besteht aus einer GIF-Datei mit ISF (Ink Serialized Format), die in einen Anwendungs Erweiterungs Block eingebettet ist.

Diese GIF-Dateien sind Darstellungen von frei Hand Objekten, die:

-   Rendering in Anwendungen, die nicht frei Hand fähig sind, z. b. Browser oder ältere Word-Prozessoren.
-   Enthalten alle erforderlichen Informationen aus der ursprünglichen frei Hand Eingabe, die Sie für Zwecke wie z. b. Bearbeitung oder Erkennung beibehalten möchten.

Diese GIF-Dateien können mithilfe der persistenzmethoden der Tablet PC Platform-APIs erstellt werden. Dabei handelt es sich um GIFs, und Sie sollten die GIF-Erweiterung und für eine Anwendung verwenden, die nicht frei Hand Eingaben aktiviert ist, von einer normalen GIF. Für eine frei Hand aktivierte Anwendung gibt es jedoch einen umfangreichen Satz von Daten, die dem Bild zugrunde liegen.

Nachdem Sie von den Tablet PC Platform-APIs erstellt wurde, wird auf ein befestigtes GIF von einem IMG-Tag in HTML verwiesen. Der HTML-Code wird dann im standardmäßigen CF- \_ HTML-Zwischenablage Slot gespeichert. Dadurch kann der HTML-Code für andere Anwendungen sichtbar sein, unabhängig davon, ob Sie frei Hand Eingabe fähig sind. Das Image selbst kann im Windows-Internet Cache gespeichert werden und nach einem angemessenen Zeitraum auf "Age out" festgelegt werden.

Bestimmte Zusatzelemente für das img-Tag werden bereitgestellt oder sind erforderlich. Diese Zusatzelemente identifizieren den HTML-Code als enthaltende Freihand. Das folgende Beispiel verweist auf ein befestigtes GIF mithilfe von HTML-Tags:

`<img href="34372423432.gif" />`

Wenn es erforderlich ist, auf andere Weise auf das Image zu verweisen, z. b. Cascading Stylesheets oder Vector Markup Language (VML), sollte noch ein img-Tag vorhanden sein, das auf das Bild verweist. Dies ermöglicht das Auslagern und Einfügen in alle Anwendungen, die HTML-Darstellungen von frei Hand Eingaben akzeptieren.

Anwendungen, die Freihand in HTML unterstützen, sollten:

-   Generieren Sie CF \_ HTML, wenn der Benutzer eine Kopie ausführt. Wenn Sie CF- \_ HTML beim Kopieren generieren (oder als HTML speichern), verwenden Sie die [Microsoft. Ink. Ink. Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) -Methode, indem Sie den [Microsoft. Ink. PersistenceFormat](/previous-versions/ms827245(v=msdn.10)) -Wert im *p* -Parameter angeben, um ein befestigtes GIF-Bild zu generieren. Der alt-Text sollte auf das präzisere Erkennungs Ergebnis festgelegt werden. Sie können die Positionierung wie gewünscht auf absolut oder direkt festlegen.
-   Überprüfen Sie alle IMG-Tags, um zu bestimmen, ob Bilder, auf die Sie verweisen, frei Hand Eingaben enthalten, wenn der CF- \_ HTML-Slot für ein einfügen Wenn dies der Fall ist, behandeln Sie die Bilder [intern als frei](/previous-versions/aa515768(v=msdn.10)) Hand Objekte. Obwohl nur GIF-Dateien in dieser Version unterstützt werden, sollte Ihre Anwendung auch nicht-GIF-Images überprüfen, falls in Zukunft weitere Bildformate unterstützt werden.
-   Unterstützt das Kopieren und Einfügen von ISF. Anwendungen, die HTML unterstützen, sollten auch ISF unterstützen, um die Interoperabilität mit frei Hand fähigen Anwendungen zu verbessern, die HTML nicht erkennen. Dies ähnelt der Konvention, dass Anwendungen, die HTML in der Zwischenablage platzieren, auch Text platzieren.

Weitere Informationen zu den verstärkten-GIFs finden Sie unter [Bausteine](building-blocks.md).

 

 
