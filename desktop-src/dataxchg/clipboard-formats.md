---
title: Zwischenablage Formate
description: Ein Fenster kann mehr als ein Objekt in der Zwischenablage platzieren, wobei jedes die gleichen Informationen in einem anderen Zwischenablage Format darstellt. Benutzer müssen die Zwischenablage Formate, die für ein Objekt in der Zwischenablage verwendet werden, nicht kennen.
ms.assetid: fe42baec-6b00-4816-b379-7f335da8a197
keywords:
- Zwischenablage, Formate
- Zwischenablage, Fenster
- Zwischenablage, Standardformate
- Zwischenablage, registrierte Formate
- Zwischenablage, synthetisierte Formate
- Standardformate für Zwischenablage
- Registrierte Zwischenablage Formate
- formatierte Zwischenablage Formate
- Cloud-Zwischenablage Formate
- Formate für Zwischenablage Verlauf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193ee4cc10c17846d974e50b17a464207026280b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341747"
---
# <a name="clipboard-formats"></a>Zwischenablage Formate

Ein Fenster kann mehr als ein Objekt in der Zwischenablage platzieren, wobei jedes die gleichen Informationen in einem anderen Zwischenablage Format darstellt. Benutzer müssen die Zwischenablage Formate, die für ein Objekt in der Zwischenablage verwendet werden, nicht kennen.

In den folgenden Themen werden die Zwischenablage Formate beschrieben.

-   [Standard Formate für Zwischenablage](#standard-clipboard-formats)
-   [Registrierte Zwischenablage Formate](#registered-clipboard-formats)
-   [Private Zwischenablage Formate](#private-clipboard-formats)
-   [Mehrere Zwischenablage Formate](#multiple-clipboard-formats)
-   [Formatierte Zwischenablage Formate](#synthesized-clipboard-formats)
-   [Cloudzwischenablage-und Zwischenablage Formate](#cloud-clipboard-and-clipboard-history-formats)

## <a name="standard-clipboard-formats"></a>Standard Formate für Zwischenablage

Die vom System definierten Zwischenablage Formate werden als *Standardformate für die Zwischenablage* bezeichnet. Diese Zwischenablage Formate werden in [**Standard mäßigen Zwischenablage Formaten**](standard-clipboard-formats.md)beschrieben.

## <a name="registered-clipboard-formats"></a>Registrierte Zwischenablage Formate

Viele Anwendungen arbeiten mit Daten, die nicht in ein Standardmäßiges Zwischenablage Format übersetzt werden können, ohne dass Informationen verloren gehen. Diese Anwendungen können eigene Zwischenablage Formate erstellen. Ein Zwischenablage Format, das von einer Anwendung definiert wird, wird als [registriertes Zwischenablage Format](#registered-clipboard-formats)bezeichnet. Wenn beispielsweise eine Textverarbeitungsanwendung formatierten Text mit einem Standardtext Format in die Zwischenablage kopiert hat, gehen die Formatierungsinformationen verloren. Die Lösung wäre das Registrieren eines neuen Zwischenablage Formats, z. b. RTF (Rich Text Format).

Verwenden Sie die [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) -Funktion, um ein neues Zwischenablage Format zu registrieren. Diese Funktion nimmt den Namen des Formats an und gibt einen ganzzahligen Wert ohne Vorzeichen zurück, der das registrierte Zwischenablage Format darstellt. Wenn Sie den Namen des registrierten Zwischenablage Formats abrufen möchten, übergeben Sie den Wert einer Ganzzahl ohne Vorzeichen an die [**getclipboardformatname**](/windows/desktop/api/Winuser/nf-winuser-getclipboardformatnamea) -Funktion.

Wenn mehr als eine Anwendung ein Zwischenablage Format mit exakt demselben Namen registriert, wird das Zwischenablage Format nur einmal registriert. Beide Aufrufe der [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) -Funktion geben denselben Wert zurück. Auf diese Weise können zwei verschiedene Anwendungen Daten mithilfe eines registrierten Zwischenablage Formats freigeben.

## <a name="private-clipboard-formats"></a>Private Zwischenablage Formate

Eine Anwendung kann ein privates Zwischenablage Format identifizieren, indem Sie einen Wert im Bereich **CF \_ privatefirst** bis **CF \_ privatelast** definiert. Eine Anwendung kann ein privates Zwischenablage Format für ein Anwendungs definiertes Datenformat verwenden, das nicht beim System registriert werden muss.

Daten Handles, die privaten Zwischenablage Formaten zugeordnet sind, werden vom System nicht automatisch freigegeben. Wenn Ihr Windows private Zwischenablage Formate verwendet, können Sie die [**WM \_ destroyclipboard**](wm-destroyclipboard.md) -Nachricht verwenden, um alle zugehörigen Ressourcen freizugeben, die nicht mehr benötigt werden.

Weitere Informationen zur [**WM \_ destroyclipboard**](wm-destroyclipboard.md) -Nachricht finden Sie unter [Besitz der Zwischenablage](clipboard-operations.md).

Eine Anwendung kann Daten Handles in der Zwischenablage platzieren, indem ein privates Format im Bereich **CF \_ gdiobjfirst** bis **CF \_ gdiobjlast** definiert wird. Wenn Sie Werte in diesem Bereich verwenden, handelt es sich beim Daten Handle nicht um ein Handle für ein Windows Graphics Device Interface-Objekt (GDI), sondern um ein Handle, das von der [**globalzugewiesc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) -Funktion mit dem GMEM Verschieb \_ baren Flag zugeordnet wird. Wenn die Zwischenablage geleert wird, löscht das System das Objekt automatisch mithilfe der [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) -Funktion.

## <a name="multiple-clipboard-formats"></a>Mehrere Zwischenablage Formate

Ein Fenster kann mehrere Zwischenablage Objekte in der Zwischenablage platzieren, die jeweils die gleichen Informationen in einem anderen Zwischenablage Format darstellen. Beim Platzieren von Informationen in der Zwischenablage sollte das Fenster Daten in möglichst vielen Formaten bereitstellen. Um herauszufinden, wie viele Formate derzeit in der Zwischenablage verwendet werden, können Sie die Funktion " [**count-ClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-countclipboardformats) " abrufen.

Zwischenablage Formate mit den meisten Informationen sollten zuerst in der Zwischenablage platziert werden, gefolgt von weniger beschreibenden Formaten. Ein Fenster, das Informationen aus der Zwischenablage einfügt, ruft in der Regel ein Zwischenablage Objekt im ersten erkannten Format ab. Da Zwischenablage Formate in der Reihenfolge aufgelistet werden, in der Sie in der Zwischenablage platziert werden, ist das erste erkannte Format ebenfalls die beschreibende.

Nehmen wir beispielsweise an, ein Benutzer kopiert formatierten Text aus einem Textverarbeitungsdokument. Das Fenster, in dem das Dokument enthalten ist, kann die Daten in der Zwischenablage zuerst in einem registrierten Format wie RTF platzieren. Anschließend würde das Fenster Daten in der Zwischenablage in einem weniger beschreibenden Format platzieren, wie z. b. Text (**CF \_ Text**).

Wenn der Inhalt der Zwischenablage in ein anderes Fenster eingefügt wird, ruft das Fenster Daten in dem am häufigsten erkannten Format ab. Wenn das Fenster RTF erkennt, werden die entsprechenden Daten in das Dokument eingefügt. Andernfalls werden die Textdaten in das Dokument eingefügt, und die Formatierungsinformationen gehen verloren.

## <a name="synthesized-clipboard-formats"></a>Formatierte Zwischenablage Formate

Das System konvertiert Daten implizit zwischen bestimmten Zwischenablage Formaten: Wenn ein Fenster Daten in einem Format anfordert, das sich nicht in der Zwischenablage befindet, konvertiert das System ein verfügbares Format in das angeforderte Format. Das System kann Daten wie in der folgenden Tabelle angegeben konvertieren.



| Zwischenablageformat     | Konvertierungs Format    |
|----------------------|----------------------|
| **CF- \_ Bitmap**       | **CF- \_ DIB**          |
| **CF- \_ Bitmap**       | **CF \_ DIBV5**        |
| **CF- \_ DIB**          | **CF- \_ Bitmap**       |
| **CF- \_ DIB**          | **CF- \_ Palette**      |
| **CF- \_ DIB**          | **CF \_ DIBV5**        |
| **CF \_ DIBV5**        | **CF- \_ Bitmap**       |
| **CF \_ DIBV5**        | **CF- \_ DIB**          |
| **CF \_ DIBV5**        | **CF- \_ Palette**      |
| **CF \_ enhmetafile**  | **CF- \_ MetafilePict** |
| **CF- \_ MetafilePict** | **CF \_ enhmetafile**  |
| **CF- \_ OemText**      | **CF- \_ Text**         |
| **CF- \_ OemText**      | **CF \_ UnicodeText**  |
| **CF- \_ Text**         | **CF- \_ OemText**      |
| **CF- \_ Text**         | **CF \_ UnicodeText**  |
| **CF \_ UnicodeText**  | **CF- \_ OemText**      |
| **CF \_ UnicodeText**  | **CF- \_ Text**         |



 

Wenn das System eine automatische Typkonvertierung für ein bestimmtes Zwischenablage Format bereitstellt, ist es nicht vorteilhaft, die Konvertierungs Formate in der Zwischenablage zu platzieren.

Wenn das System eine automatische Typkonvertierung für ein bestimmtes Zwischenablage Format bereitstellt und Sie [**enumclipboardformats**](/windows/desktop/api/Winuser/nf-winuser-enumclipboardformats) zum Auflisten der Zwischenablage Datenformate aufzählen, listet das System zuerst das Format auf, das sich in der Zwischenablage befindet, gefolgt von den Formaten, in die es konvertiert werden kann.

Beim Kopieren von Bitmaps empfiehlt es sich, das **CF- \_ DIB** -oder **CF \_ DIBV5** -Format in der Zwischenablage zu platzieren. Dies liegt daran, dass die Farben in einer geräteabhängigen Bitmap (**CF- \_ Bitmap**) relativ zur Systempalette sind, die sich vor dem Einfügen der Bitmap ändern kann. Wenn sich das **CF \_ DIB** -oder **CF \_ DIBV5** -Format in der Zwischenablage befindet und ein Fenster das **CF- \_ Bitmap** -Format anfordert, rendert das System die geräteunabhängige Bitmap (DIB) mithilfe der aktuellen Palette zu diesem Zeitpunkt.

Wenn Sie das **CF- \_ Bitmapformat** in der Zwischenablage (und nicht in der **CF- \_ DIB**) platzieren, rendert das System das **CF \_ DIB** -oder **CF \_ DIBV5** -Zwischenablage Format, sobald die Zwischenablage geschlossen wird. Dadurch wird sichergestellt, dass die richtige Palette zum Generieren des DIB verwendet wird. Wenn Sie das **CF \_ DIBV5** -Format mit den bitmapfarbraum-Informationen in der Zwischenablage platzieren, konvertiert das System die Bitmapbits aus dem bitmapfarbraum in den sRGB-Farbraum, wenn **CF \_ DIB** oder **CF \_ DIBV5** angefordert wird. Wenn **CF \_ DIBV5** angefordert wird, wenn keine Farbraum-Informationen in der Zwischenablage vorhanden sind, gibt das System sRGB-Farbraum-Informationen in der [**BITMAPV5HEADER**](/windows/desktop/api/wingdi/ns-wingdi-bitmapv5header) -Struktur zurück. Konvertierungen zwischen anderen Zwischenablage Formaten werden bei Bedarf ausgeführt.

Wenn die Zwischenablage Daten im **CF- \_ Palettenformat** enthält, sollte die Anwendung die Funktionen " [**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette) " und " [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) " verwenden, um alle anderen Daten in der Zwischenablage für diese logische Palette zu erkennen.

Es gibt zwei Zwischenablage Formate für Metadateien: **CF \_ enhmetafile** und **CF \_ MetafilePict**. Geben Sie **CF \_ enhmetafile** für Erweiterte Metadateien und **CF \_ MetafilePict** für Windows-Metadateien an.

## <a name="cloud-clipboard-and-clipboard-history-formats"></a>Cloudzwischenablage-und Zwischenablage Formate

Einige Versionen von Windows enthalten die [cloudzwischenablage](/windows/whats-new/whats-new-windows-10-version-1809#cloud-clipboard), die den Verlauf der letzten Datenelemente der Zwischenablage beibehält und diese zwischen den Geräten des Benutzers synchronisieren kann.
Wenn Sie nicht möchten, dass die Daten, die Ihre Anwendung in der Zwischenablage platziert, in den Zwischenablage Verlauf aufgenommen oder mit anderen Geräten synchronisiert wird, kann die Anwendung dieses Verhalten steuern, indem Sie die Daten in bestimmten [registrierten Zwischenablage Formaten](#registered-clipboard-formats) platzieren, deren Namen dem Windows-System bekannt sind:

- **Excludeclipboardcontentfrommonitorprocessing** : Platzieren Sie alle Daten in der Zwischenablage in diesem Format, um zu verhindern, dass alle Zwischenablage Formate im Zwischenablage Verlauf eingeschlossen oder mit den anderen Geräten des Benutzers synchronisiert werden.
- **Canincludeinclipboardhistory** : Platzieren Sie einen serialisierten **[DWORD](../WinProg/windows-data-types.md)** -Wert von 0 (null) in der Zwischenablage in diesem Format, um zu verhindern, dass alle Zwischenablage Formate in den Zwischenablage Verlauf eingeschlossen werden, oder platzieren Sie den Wert 1, um explizit anzufordern, dass das Zwischenablage Element im Zwischenablage Element eingeschlossen wird. Dies hat keine Auswirkung auf die Synchronisierung der anderen Geräte des Benutzers.
- **Canuploadtocloudclipboard** : Platzieren Sie einen serialisierten **[DWORD](../WinProg/windows-data-types.md)** -Wert von 0 (null) in der Zwischenablage in diesem Format, um zu verhindern, dass alle Zwischenablage Formate mit den anderen Geräten des Benutzers synchronisiert werden, oder platzieren Sie den Wert 1, um explizit anzufordern, dass das Zwischenablage Element mit anderen Geräten synchronisiert werden soll. Dies wirkt sich nicht auf den Zwischenablage Verlauf des lokalen Geräts aus.

Wie bei anderen registrierten Zwischenablage Formaten müssen Sie die [**RegisterClipboardFormat**](
/windows/win32/api/winuser/nf-winuser-registerclipboardformata) -Funktion verwenden, um einen ganzzahligen Wert ohne Vorzeichen zu erhalten, der jedes der obigen drei Formate identifiziert.