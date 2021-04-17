---
title: Image-Data Komprimierung
description: Image-Data Komprimierung
ms.assetid: 689cf403-cbb5-4ccb-a05b-0caa617430ed
keywords:
- Videokomprimierungs-Manager (VCM), Image-Datenkomprimierung
- VCM (Videokomprimierungs-Manager), Image-Datenkomprimierung
- Iccompress-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8f59a163a9b5a74d2d2fe984417069985fa86a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390199"
---
# <a name="image-data-compression"></a>Image-Data Komprimierung

Die Anwendung kann eine Reihe von [**iccompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) -Funktionen und-Makros verwenden, um Daten zu komprimieren. Mithilfe der Funktionen und Makros können Sie die folgenden Aufgaben ausführen:

-   Bestimmen Sie das zu verwendende Komprimierungs Format für ein angegebenes Eingabeformat.
-   Bereiten Sie den-Kompressor vor.
-   Komprimieren Sie die Daten.
-   Ende der Komprimierung.

Die Anwendung kann die Kontrolle über den Komprimierungs Prozess mithilfe der [**iccompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) -Funktionen und-Makros erhöhen. Diese Gruppe von Funktionen und Makros verarbeitet einzelne Frames anstelle der gesamten Sequenz. Die Anwendung kann z. b. die Frames identifizieren, die mithilfe der **iccompress** -Funktion als Keyframes komprimiert werden.

Ein-Kompressor empfängt Daten in einem Format, komprimiert die Daten und gibt eine komprimierte Version der Daten mit einem angegebenen Format zurück. Das typische Eingabeformat gibt Disb mithilfe der [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur an. Das typische Ausgabeformat gibt komprimierte Disb an, wobei auch die **BitmapInfo** -Struktur verwendet wird.

> [!Note]  
> Um die Abbild-und audioabnahme während der Wiedergabe zu minimieren, sollten Sie eine AVI-Datei nicht mehrmals komprimieren. Kombinieren Sie unkomprimierte Video Teile in Ihrem Bearbeitungssystem, und komprimieren Sie dann das endgültige Produkt.

 

## <a name="compressor-and-compression-format-selection"></a>Auswahl des Kompressors und Komprimierungs Formats

Wenn Sie Daten komprimieren möchten und die Anwendung ein bestimmtes Ausgabeformat erfordert, senden Sie die [**ICM- \_ Komprimierungs \_ Abfrage**](icm-compress-query.md) Nachricht (oder verwenden Sie das [**iccompressquery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) -Makro), um den-Kompressor abzufragen und zu ermitteln, ob die Eingabe-und Ausgabeformate unterstützt werden.

Wenn das Ausgabeformat für die Anwendung nicht wichtig ist, müssen Sie nur einen Kompressor finden, der das Eingabeformat verarbeiten kann. Um zu ermitteln, ob ein-Kompressor das Eingabeformat verarbeiten kann, können Sie die **ICM- \_ Komprimierungs \_ Abfrage** senden und **null** für den *LPARAM* -Parameter angeben. Diese Meldung gibt das Ausgabeformat nicht an die Anwendung zurück. Die Anwendung kann die erforderliche Puffergröße für die Daten bestimmen, die das Komprimierungs Format angeben, indem Sie die [**ICM \_ Compress \_ get- \_ Format**](icm-compress-get-format.md) Meldung sendet (oder das Makro [**iccompressgetformatsize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) verwenden). Sie können die Format Daten auch abrufen, indem Sie ICM \_ Compress \_ get \_ Format (oder das Makro [**iccompressgetformat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) ) senden.

Wenn Sie den größten Puffer ermitteln möchten, den der-Kompressor für die Komprimierung benötigen könnte, senden Sie die [**ICM \_ Compress \_ get \_ size**](icm-compress-get-size.md) -Nachricht (oder verwenden Sie das [**iccompressgetsize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) -Makro). Sie können die Anzahl von Bytes, die von der [**icsendmessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) -Funktion zurückgegeben werden, verwenden, um einen Puffer für nachfolgende Bild Komprimierungen zuzuordnen.

## <a name="compressor-initialization"></a>Initialisierung des Kompressors

Nachdem die Anwendung einen Kompressor ausgewählt hat, mit dem die Eingabe-und Ausgabeformate verarbeitet werden können, die Sie benötigt, können Sie den-Kompressor mithilfe der [**ICM- \_ Komprimierungs \_ Begin**](icm-compress-begin.md) -Nachricht initialisieren (oder das-Makro von [**iccompressbegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) verwenden). Diese Nachricht erfordert das-Kompressor-Handle und die Eingabe-und Ausgabeformate.

## <a name="data-compression"></a>Datenkomprimierung

Sie können die [**iccompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) -Funktion verwenden, um einen Frame zu komprimieren. Die Anwendung muss diese Funktion wiederholt verwenden, bis alle Frames in einer Sequenz komprimiert sind. Die Anwendung muss außerdem die Anzahl der einzelnen mit **iccompress** komprimierten Frames nachverfolgen und inkrementalisieren. Der-Kompressor verwendet diesen Wert, um zu überprüfen, ob Frames während der schnellen temporalen Komprimierung außerhalb der Reihenfolge gesendet werden (Unterschiede zwischen aufeinander folgenden Frames werden Wenn die Anwendung einen Frame erneut komprimiert, sollte Sie dieselbe Frame Nummer wie beim ersten Komprimieren des Frames verwenden. Wenn Ihre Anwendung ein Bild mit einem anderen Frame komprimiert, kann Sie eine Frame Nummer von NULL angeben.

Die Anwendung kann das **iccompress- \_ Keyframe** -Flag verwenden, um den Frame durch [**iccompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) als Keyframe komprimiert zu gestalten.

Wenn VCM die Steuerung an die Anwendung zurückgibt, nachdem ein Frame komprimiert wurde, speichert VCM die komprimierten Daten in den Strukturen, auf die von den Parametern *lpbioutput* und *lpdata* verwiesen wird. Wenn die Anwendung die komprimierten Daten verschieben muss, kann Sie Ihre Größe im *bisizeimage* -Member der [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur ermitteln, die in *lpbioutput* angegeben ist.

> [!Note]  
> Die Anwendung muss die Strukturen und Puffer zuordnen, in denen die nicht komprimierten und komprimierten Daten gespeichert werden. Wenn der-Kompressor Temporale Komprimierung unterstützt, muss die Anwendung auch eine Struktur und einen Puffer zuordnen, um das Format und die Daten für den vorherigen Frame von Informationen zu speichern.

 

## <a name="ending-compression"></a>Komprimierung wird beendet

Nachdem die Anwendung die Daten komprimiert hat, kann Sie das [**iccompressend**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) -Makro verwenden, um den Kompressor zu benachrichtigen, dass der Vorgang abgeschlossen wurde. Wenn Sie die Komprimierung nach der Verwendung dieser Funktion neu starten möchten, muss die Anwendung den-Kompressor erneut initialisieren, indem Sie die [**ICM \_ Compress \_ Begin**](icm-compress-begin.md) -Nachricht sendet (oder das [**iccompressbegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) -Makro verwenden).

 

 