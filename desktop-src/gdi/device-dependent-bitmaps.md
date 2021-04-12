---
description: Geräte abhängige Bitmaps (DDSB) werden mithilfe einer einzelnen Struktur, der Bitmap-Struktur, beschrieben.
ms.assetid: 63ff9cd6-cd07-4085-b166-268e4d9b7aad
title: Bitmaps Device-Dependent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a3de2c59509c71b38f9981df330b3b28effa26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130797"
---
# <a name="device-dependent-bitmaps"></a>Bitmaps Device-Dependent

Geräte abhängige Bitmaps (DDSB) werden mithilfe einer einzelnen Struktur, der [**Bitmap**](/windows/win32/api/wingdi/ns-wingdi-bitmap) -Struktur, beschrieben. Die Elemente dieser Struktur geben die Breite und Höhe eines rechteckigen Bereichs in Pixel an. die Breite des Arrays, das Einträge aus der Gerätepalette in Pixel zuordnet. und das Farb Format des Geräts in Bezug auf Farbflächen und Bits pro Pixel. Eine Anwendung kann das Farb Format eines Geräts abrufen, indem die [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) -Funktion aufgerufen und die entsprechenden Konstanten angegeben werden. Beachten Sie, dass eine DDB keine Farbwerte enthält. Stattdessen befinden sich die Farben in einem geräteabhängigen Format. Weitere Informationen finden Sie unter [Farbe in Bitmaps](color-in-bitmaps.md). Da jedes Gerät über einen eigenen Satz von Farben verfügen kann, wird eine für ein Gerät erstellte DDB möglicherweise nicht gut auf einem anderen Gerät angezeigt.

Damit eine DDB in einem Gerätekontext verwendet werden kann, muss Sie über die Farb Organisation dieses Geräte Kontexts verfügen. Daher wird eine DDB oft als *kompatible Bitmap* bezeichnet und weist in der Regel eine bessere GDI-Leistung als eine DIB auf. Um z. b. eine Bitmap für den Videospeicher zu erstellen, empfiehlt es sich, eine kompatible Bitmap mit dem gleichen Farb Format wie die primäre Anzeige zu verwenden. Im Videospeicher sind das Rendering in die Bitmap und die Anzeige auf dem Bildschirm deutlich schneller als von einer Systemspeicher Oberfläche oder direkt von einem DIB.

Zusätzlich zur Verbesserung der GDI-Leistung werden kompatible Bitmaps zum Erfassen von Bildern (siehe aufzeichnen [eines Images](capturing-an-image.md) ) und zum Erstellen von Bitmaps zur Laufzeit für Menüs verwendet. Weitere Informationen finden Sie unter "Erstellen der Bitmap" in (Weitere Informationen finden [Sie unter Verwenden von Menüs](../menurc/using-menus.md) ).

Um eine Bitmap zwischen Geräten mit einer anderen Farb Organisation zu übertragen, verwenden Sie [**GetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits) zum Konvertieren der kompatiblen Bitmap in ein DIB und zum Aufrufen von [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits) oder [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) , um das DIB dem zweiten Gerät anzuzeigen.

Es gibt zwei Arten von DDB-Typen: verwertbar und nicht verwerfbar. Eine verworfbare DDB ist eine Bitmap, die vom System verworfen wird, wenn die Bitmap nicht in einem Domänen Controller ausgewählt ist, und wenn der Systemspeicher gering ist. Die Funktion " [**kreateverwerdablebitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) " erstellt ververwerfbare Bitmaps. Die Funktionen "| [**atebitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap)", " [**kreatecompatiblebitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap)" und " [**kreatebitmapindirekte**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) " Erstellen nicht verwerfbare Bitmaps.

Eine Anwendung kann eine DDB aus einem DIB erstellen, indem Sie die erforderlichen Strukturen initialisiert und die [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) -Funktion aufruft. Das angeben \_ von "CBM init" im Aufruf von **CreateDIBitmap** entspricht dem Aufrufen der [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) -Funktion zum Erstellen einer DDB im Format des Geräts und dem anschließenden Aufrufen der [**SetDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits) -Funktion, um die DIB-Bits in die DDB zu übersetzen. Um zu ermitteln, ob ein Gerät die **SetDIBits** -Funktion unterstützt, können Sie die [**getdebug**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) -Funktion aufrufen und die RC \_ di- \_ Bitmap als RasterCaps-Flag angeben.

 

 
