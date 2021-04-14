---
description: Ausstellen von unformatierten AV/C-Befehlen
ms.assetid: 18081652-962f-4605-84b7-1fa60f61ad05
title: Ausstellen von unformatierten AV/C-Befehlen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1cf1b25d45a0eb35ede7151941d0cd49d30db0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392513"
---
# <a name="issuing-raw-avc-commands"></a>Ausstellen von unformatierten AV/C-Befehlen

Die [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)-, [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)-und [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) -Schnittstellen funktionieren, indem Sie die Methodenaufrufe in Befehle für den Treiber übersetzen und dann die Antwort des Treibers interpretieren und Sie durch ein **HRESULT** oder einen Output-Parameter zurückgeben. Einige Gerätefunktionen sind jedoch möglicherweise über diese Methoden nicht zugänglich. Daher unterstützt msdv das Senden von unformatierten AV/C-Befehlen an das Gerät.

Beachten Sie bei der Verwendung dieses Features die folgenden Punkte:

-   Der Befehl wird ohne Fehlerüberprüfung oder Parameter Validierung direkt an das Gerät übergeben. Aus diesem Grund sollten Sie unformatierte AV/C-Befehle nur dann ausgeben, wenn die DirectShow-Schnittstellen die benötigte Funktionalität nicht implementieren.
-   Alle unformatierten AV/C-Befehle sind synchron. Der Thread, der den Befehl ausgibt, blockiert, bis der Befehl zurückgibt.
-   Es kann jeweils nur ein Befehl angegeben werden. Während der Befehl verarbeitet wird, lehnt das Gerät alle zusätzlichen Befehle ab.
-   Der UVC-Treiber unterstützt keine unformatierten AV/C-Befehle.

Um einen AV/C-Befehl zu senden, formatieren Sie den Befehl als Bytearray. Nennen Sie dann [**IAMExtTransport:: gettransportbasicparameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters). Übergeben Sie das ED \_ RAW \_ Ext \_ dev \_ cmd-Flag, die Array Größe und das Array. Sie müssen die Array Adresse in einen **lpolestr \** _-Typ umwandeln, da der ursprüngliche Zweck dieses Parameters darin besteht, einen Zeichen folgen Wert zurückzugeben.


```C++
BYTE AvcCmd[] = { ... }; // Contains the AV/C command (not shown)
long cbCmd = sizeof(AvcCmd);
hr = pTransport->GetTransportBasicParameters(
    ED_RAW_EXT_DEV_CMD, 
    &cbCmd,
    (LPOLESTR_) AvcCmd);
```



Der Inhalt des Arrays wird direkt an das Gerät übermittelt, sodass Sie darauf achten müssen, ihn ordnungsgemäß zu formatieren. Ein Befehl kann auf die Einheit (Camcorder) oder eine Untereinheit (Band oder Kamera) abzielen. Die relevanten Standards sind auf der [1394-Handels Assoziations Website](https://1394ta.org)verfügbar.

-   Allgemeine Spezifikation für den Befehl "AV/C Digital Interface"
-   Spezifikation für AV/C-Band Aufzeichnung/-Player-Untereinheit

Im ersten Thema wird beschrieben, wie Sie die AV/C-Befehle formatieren und die Unit-Befehle auflisten. In der zweiten Spezifikation werden die Untereinheiten Befehle aufgeführt.

Die **gettransportbasicparameters** -Methode gibt möglicherweise einen der folgenden Fehlercodes zurück:



| Fehlercode              | BESCHREIBUNG                                                                      |
|-------------------------|----------------------------------------------------------------------------------|
| Fehler \_ Timeout          | Timeout für den Befehl.                                                           |
| Fehler beim Zurücksetzen des Fehlers. \_ \_ \_  | Das Gerät hat den Befehl nicht akzeptiert.                                           |
| Fehler \_ nicht \_ unterstützt   | Der Befehl wird vom Gerät nicht unterstützt.                                         |
| Fehler \_ Anforderung \_ abgebrochen | Der Befehl wurde abgebrochen. Der Besitz des Geräts wurde entfernt, oder es ist ein Zurücksetzen des Busses aufgetreten. |



 

> [!Note]  
> Diese Fehler werden als Win32-Fehlercodes zurückgegeben, nicht als HRESULTs. Daher sollten Sie diese Werte direkt testen, anstatt die Makros " **erfolgreich** " und " **failed** " zu verwenden.

 

Wenn die Methode "S OK" zurückgibt \_ , wird die Antwort vom Gerät in das Array kopiert. Die Antwort Nutzlast ist möglicherweise größer als der Befehl, daher müssen Sie einen Puffer zuordnen, der groß genug ist, um Sie zu speichern. Die maximale Nutzlastgröße beträgt 512 Bytes. Beachten Sie, dass der Rückgabewert S \_ OK nicht immer bedeutet, dass das Gerät den Befehl erfolgreich ausgeführt hat. Die Anwendung muss die Antwort Nutzlast überprüfen, um den Status zu bestimmen.

Das folgende Beispiel zeigt den Befehl für die Suche nach einer absoluten Nachverfolgung der Nachverfolgung:


```C++
// Set up the ATN search command.
BYTE AvcCmd[] = 
{ 
    0x00,   // ctype = "control"
    0x20,   // subunit_type, subunit_id
    0x52,   // opcode (ATN)
    0x20,   // operand 0 = "search"
    0x00,   // operand 1 = ATN
    0x00,   // operand 2 = ATN
    0x00,   // operand 3 = ATN
    0xFF   //  operand 4 = D-VCR medium type.
};
// Specify a track number.
ULONG ulTrackNumber = track_number; // Specify the track number here.
// Shift over by 1 (LSB of operand 1 is a 1-bit blank flag)
ulTrackNumber = ulTrackNumber << 1; 
// Plug this number into operands 1 - 3.
AvcCmd[4] = (BYTE) (ulTrackNumber & 0x000000FF);
AvcCmd[5] = (BYTE)((ulTrackNumber & 0x0000FF00) >> 8);
AvcCmd[6] = (BYTE)((ulTrackNumber & 0x00FF0000) >> 16);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuern eines DV-Camcorder](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



