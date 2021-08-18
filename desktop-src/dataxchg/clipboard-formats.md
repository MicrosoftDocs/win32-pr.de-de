---
title: Zwischenablageformate
description: Ein Fenster kann mehrere Objekte in der Zwischenablage platzieren, die jeweils die gleichen Informationen in einem anderen Zwischenablageformat darstellen. Benutzer müssen die Zwischenablageformate, die für ein Objekt in der Zwischenablage verwendet werden, nicht kennen.
ms.assetid: fe42baec-6b00-4816-b379-7f335da8a197
keywords:
- Zwischenablage, Formate
- Zwischenablage, Fenster
- Zwischenablage, Standardformate
- Zwischenablage, registrierte Formate
- Zwischenablage, synthetisierte Formate
- Standardformate für die Zwischenablage
- Registrierte Zwischenablageformate
- synthetisierte Zwischenablageformate
- Cloud-Zwischenablageformate
- Zwischenablageverlaufsformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac6bd2dc9dda8c8ccecd164123af68865005d9d28d328ce5489abf23926113ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991340"
---
# <a name="clipboard-formats"></a>Zwischenablageformate

Ein Fenster kann mehrere Objekte in der Zwischenablage platzieren, die jeweils die gleichen Informationen in einem anderen Zwischenablageformat darstellen. Benutzer müssen die Zwischenablageformate, die für ein Objekt in der Zwischenablage verwendet werden, nicht kennen.

In den folgenden Themen werden die Zwischenablageformate beschrieben.

-   [Standardformate der Zwischenablage](#standard-clipboard-formats)
-   [Registrierte Zwischenablageformate](#registered-clipboard-formats)
-   [Private Zwischenablageformate](#private-clipboard-formats)
-   [Mehrere Zwischenablageformate](#multiple-clipboard-formats)
-   [Synthetisierte Zwischenablageformate](#synthesized-clipboard-formats)
-   [Cloud-Zwischenablage- und Zwischenablageverlaufsformate](#cloud-clipboard-and-clipboard-history-formats)

## <a name="standard-clipboard-formats"></a>Standardformate der Zwischenablage

Die vom System definierten Zwischenablageformate werden als *Standardmäßige Zwischenablageformate* bezeichnet. Diese Zwischenablageformate werden unter [**Standard-Zwischenablageformate**](standard-clipboard-formats.md)beschrieben.

## <a name="registered-clipboard-formats"></a>Registrierte Zwischenablageformate

Viele Anwendungen arbeiten mit Daten, die nicht ohne Informationsverlust in ein Standardformat der Zwischenablage übersetzt werden können. Diese Anwendungen können eigene Zwischenablageformate erstellen. Ein von einer Anwendung definiertes Zwischenablageformat wird als [registriertes Zwischenablageformat](#registered-clipboard-formats)bezeichnet. Wenn eine Textverarbeitungsanwendung beispielsweise formatierten Text mit einem Standardtextformat in die Zwischenablage kopiert, geht die Formatierungsinformation verloren. Die Lösung wäre die Registrierung eines neuen Zwischenablageformats, z. B. Rich Text Format (RTF).

Verwenden Sie die [**RegisterClipboardFormat-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) um ein neues Zwischenablageformat zu registrieren. Diese Funktion akzeptiert den Namen des Formats und gibt einen ganzzahligen Wert ohne Vorzeichen zurück, der das registrierte Zwischenablageformat darstellt. Um den Namen des registrierten Zwischenablageformats abzurufen, übergeben Sie den Ganzzahlwert ohne Vorzeichen an die [**GetClipboardFormatName-Funktion.**](/windows/desktop/api/Winuser/nf-winuser-getclipboardformatnamea)

Wenn mehrere Anwendungen ein Zwischenablageformat mit genau demselben Namen registrieren, wird das Zwischenablageformat nur einmal registriert. Beide Aufrufe der [**RegisterClipboardFormat-Funktion**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) geben den gleichen Wert zurück. Auf diese Weise können zwei verschiedene Anwendungen Daten mithilfe eines registrierten Zwischenablageformats freigeben.

## <a name="private-clipboard-formats"></a>Private Zwischenablageformate

Eine Anwendung kann ein privates Zwischenablageformat identifizieren, indem sie einen Wert im Bereich **CF \_ PRIVATEFIRST** bis **CF \_ PRIVATELAST** definiert. Eine Anwendung kann ein privates Zwischenablageformat für ein anwendungsdefiniertes Datenformat verwenden, das nicht beim System registriert werden muss.

Datenhandles, die privaten Zwischenablageformaten zugeordnet sind, werden vom System nicht automatisch freigegeben. Wenn Ihre Fenster private Zwischenablageformate verwenden, können Sie die [**WM \_ DESTROYCLIPBOARD-Nachricht**](wm-destroyclipboard.md) verwenden, um alle zugehörigen Ressourcen freizugeben, die nicht mehr benötigt werden.

Weitere Informationen zur [**WM \_ DESTROYCLIPBOARD-Meldung**](wm-destroyclipboard.md) finden Sie unter Besitzer der [Zwischenablage.](clipboard-operations.md)

Eine Anwendung kann Datenhandles in der Zwischenablage platzieren, indem sie ein privates Format im Bereich **CF \_ GDIOBJFIRST** bis **CF \_ GDIOBJLAST** definiert. Bei Verwendung von Werten in diesem Bereich ist das Datenhandle kein Handle für ein GDI-Objekt (Windows Graphics Device Interface), sondern ein Handle, das von der [**GlobalAlloc-Funktion**](/windows/desktop/api/winbase/nf-winbase-globalalloc) mit dem GMEM \_ MOVEABLE-Flag zugeordnet wird. Wenn die Zwischenablage geleert wird, löscht das System das Objekt automatisch mithilfe der [**GlobalFree-Funktion.**](/windows/desktop/api/winbase/nf-winbase-globalfree)

## <a name="multiple-clipboard-formats"></a>Mehrere Zwischenablageformate

Ein Fenster kann mehrere Zwischenablageobjekte in der Zwischenablage platzieren, die jeweils die gleichen Informationen in einem anderen Zwischenablageformat darstellen. Beim Platzieren von Informationen in der Zwischenablage sollte das Fenster Daten in so vielen Formaten wie möglich bereitstellen. Um herauszufinden, wie viele Formate derzeit in der Zwischenablage verwendet werden, rufen Sie die [**CountClipboardFormats-Funktion**](/windows/desktop/api/Winuser/nf-winuser-countclipboardformats) auf.

Zwischenablageformate, die die meisten Informationen enthalten, sollten zuerst in der Zwischenablage platziert werden, gefolgt von weniger beschreibenden Formaten. Ein Fenster, in dem Informationen aus der Zwischenablage eingefügt werden, ruft in der Regel ein Zwischenablageobjekt im ersten format ab, das es erkennt. Da Zwischenablageformate in der Reihenfolge aufgeführt werden, in der sie in der Zwischenablage platziert werden, ist das erste erkannte Format auch das beschreibendste Format.

Angenommen, ein Benutzer kopiert formatierten Text aus einem Textverarbeitungsdokument. Das Fenster, das das Dokument enthält, kann daten zuerst in der Zwischenablage in einem registrierten Format platzieren, z. B. RTF. Anschließend würde das Fenster Daten in der Zwischenablage in einem weniger aussagekräftigen Format platzieren, z. B. Text (**CF \_ TEXT**).

Wenn der Inhalt der Zwischenablage in ein anderes Fenster eingefügt wird, ruft das Fenster Daten im beschreibendsten Format ab, das es erkennt. Wenn das Fenster RTF erkennt, werden die entsprechenden Daten in das Dokument eingefügt. Andernfalls werden die Textdaten in das Dokument eingefügt, und die Formatierungsinformationen verloren.

## <a name="synthesized-clipboard-formats"></a>Synthetisierte Zwischenablageformate

Das System konvertiert Daten implizit zwischen bestimmten Zwischenablageformaten: Wenn ein Fenster Daten in einem Format anfordert, das sich nicht in der Zwischenablage befindet, konvertiert das System ein verfügbares Format in das angeforderte Format. Das System kann Daten wie in der folgenden Tabelle angegeben konvertieren.



| Zwischenablageformat     | Konvertierungsformat    |
|----------------------|----------------------|
| **CF \_ BITMAP**       | **CF \_ DIB**          |
| **CF \_ BITMAP**       | **CF \_ DIBV5**        |
| **CF \_ DIB**          | **CF \_ BITMAP**       |
| **CF \_ DIB**          | **CF \_ PALETTE**      |
| **CF \_ DIB**          | **CF \_ DIBV5**        |
| **CF \_ DIBV5**        | **CF \_ BITMAP**       |
| **CF \_ DIBV5**        | **CF \_ DIB**          |
| **CF \_ DIBV5**        | **CF \_ PALETTE**      |
| **CF \_ ENHMETAFILE**  | **CF \_ METAFILEPICT** |
| **CF \_ METAFILEPICT** | **CF \_ ENHMETAFILE**  |
| **CF \_ OEMTEXT**      | **CF \_ TEXT**         |
| **CF \_ OEMTEXT**      | **CF \_ UNICODETEXT**  |
| **CF \_ TEXT**         | **CF \_ OEMTEXT**      |
| **CF \_ TEXT**         | **CF \_ UNICODETEXT**  |
| **CF \_ UNICODETEXT**  | **CF \_ OEMTEXT**      |
| **CF \_ UNICODETEXT**  | **CF \_ TEXT**         |



 

Wenn das System eine automatische Typkonvertierung für ein bestimmtes Zwischenablageformat bereitstellt, bietet es keinen Vorteil, die Konvertierungsformate in der Zwischenablage zu platzieren.

Wenn das System eine automatische Typkonvertierung für ein bestimmtes Zwischenablageformat bereitstellt und Sie [**EnumClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-enumclipboardformats) aufrufen, um die Zwischenablagedatenformate aufzulisten, listet das System zuerst das Format auf, das sich in der Zwischenablage befindet, gefolgt von den Formaten, in die es konvertiert werden kann.

Beim Kopieren von Bitmaps empfiehlt es sich, das **CF \_ DIB-** oder **CF \_ DIBV5-Format** in der Zwischenablage zu platzieren. Dies liegt daran, dass die Farben in einer geräteabhängigen Bitmap (**CF \_ BITMAP**) relativ zur Systempalette sind, die sich ändern kann, bevor die Bitmap eingefügt wird. Wenn sich das **CF \_ DIB-** oder **CF \_ DIBV5-Format** in der Zwischenablage befindet und ein Fenster das **CF \_ BITMAP-Format** anfordert, rendert das System die geräteunabhängige Bitmap (DIB) mithilfe der aktuellen Palette zu diesem Zeitpunkt.

Wenn Sie das **CF \_ BITMAP-Format** in der Zwischenablage platzieren (und nicht **CF \_ DIB),** rendert das System das **CF \_ DIB-** oder **CF \_ DIBV5-Zwischenablageformat,** sobald die Zwischenablage geschlossen wird. Dadurch wird sichergestellt, dass die richtige Palette zum Generieren des DIB verwendet wird. Wenn Sie das **CF \_ DIBV5-Format** mit den Bitmapfarbrauminformationen in der Zwischenablage platzieren, konvertiert das System die Bitmapbits aus dem Bitmapfarbraum in den sRGB-Farbraum, wenn **CF \_ DIB** oder **CF \_ DIBV5** angefordert wird. Wenn **CF \_ DIBV5** angefordert wird, wenn keine Farbrauminformationen in der Zwischenablage vorhanden sind, gibt das System sRGB-Farbrauminformationen in der [**BITMAPV5HEADER-Struktur**](/windows/desktop/api/wingdi/ns-wingdi-bitmapv5header) zurück. Konvertierungen zwischen anderen Zwischenablageformaten erfolgen bei Bedarf.

Wenn die Zwischenablage Daten im **CF \_ PALETTE-Format** enthält, sollte die Anwendung die Funktionen [**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette) und [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) verwenden, um alle anderen Daten in der Zwischenablage für diese logische Palette zu realisieren.

Es gibt zwei Zwischenablageformate für Metadateien: **CF \_ ENHMETAFILE** und **CF \_ METAFILEPICT**. Geben Sie **CF \_ ENHMETAFILE** für erweiterte Metadateien und **CF \_ METAFILEPICT** für Windows Metadateien an.

## <a name="cloud-clipboard-and-clipboard-history-formats"></a>Cloud-Zwischenablage- und Zwischenablageverlaufsformate

Einige Versionen von Windows enthalten [die Cloud-Zwischenablage,](/windows/whats-new/whats-new-windows-10-version-1809#cloud-clipboard)die einen Verlauf der letzten Datenelemente der Zwischenablage speichert und zwischen den Geräten des Benutzers synchronisieren kann.
Wenn Sie nicht möchten, dass die Daten, die Ihre Anwendung in der Zwischenablage platziert, in den Verlauf der Zwischenablage aufgenommen oder mit anderen Geräten synchronisiert werden, kann Ihre Anwendung dieses Verhalten steuern, indem Sie Daten in [bestimmten registrierten Zwischenablageformaten](#registered-clipboard-formats) platzieren, deren Namen dem Windows System bekannt sind:

- **ExcludeClipboardContentFromMonitorProcessing:** Platzieren Sie alle Daten in der Zwischenablage in diesem Format, um zu verhindern, dass alle Zwischenablageformate in den Zwischenablageverlauf aufgenommen oder mit den anderen Geräten des Benutzers synchronisiert werden.
- **CanIncludeInClipboardHistory:** Platzieren Sie einen serialisierten **[DWORD-Wert](../WinProg/windows-data-types.md)** von 0 (null) in der Zwischenablage in diesem Format, um zu verhindern, dass alle Zwischenablageformate in den Zwischenablageverlauf aufgenommen werden, oder platzieren Sie stattdessen einen Wert von 1, um explizit anzufordern, dass das Zwischenablageelement in den Zwischenablageverlauf aufgenommen werden soll. Dies wirkt sich nicht auf die Synchronisierung mit den anderen Geräten des Benutzers aus.
- **CanUploadToCloudClipboard:** Platzieren Sie einen serialisierten **[DWORD-Wert](../WinProg/windows-data-types.md)** von 0 (null) in der Zwischenablage in diesem Format, um zu verhindern, dass alle Zwischenablageformate mit den anderen Geräten des Benutzers synchronisiert werden, oder platzieren Sie stattdessen einen Wert von 1, um explizit anzufordern, dass das Zwischenablageelement mit anderen Geräten synchronisiert wird. Dies wirkt sich nicht auf den Verlauf der Zwischenablage des lokalen Geräts aus.

Wie bei anderen registrierten Zwischenablageformaten müssen Sie die [**RegisterClipboardFormat-Funktion**](
/windows/win32/api/winuser/nf-winuser-registerclipboardformata) verwenden, um einen ganzzahligen Wert ohne Vorzeichen abzurufen, der jedes der oben genannten drei Formate identifiziert.