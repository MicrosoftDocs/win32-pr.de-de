---
description: Ausgeben von unformatierten AV/C-Befehlen
ms.assetid: 18081652-962f-4605-84b7-1fa60f61ad05
title: Ausgeben von unformatierten AV/C-Befehlen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729cad0be3a55a3f95592e54e8f91b9074892a8d111da9ad996b4e00a136cbe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153787"
---
# <a name="issuing-raw-avc-commands"></a>Ausgeben von unformatierten AV/C-Befehlen

Die Schnittstellen [**IAMExtDevice,**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice) [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)und [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) übersetzen die Methodenaufrufe in Befehle für den Treiber, interpretieren dann die Antwort des Treibers und geben sie über ein **HRESULT** oder einen Ausgabeparameter zurück. Auf einige Gerätefunktionen kann jedoch möglicherweise nicht über diese Methoden zugegriffen werden. Daher unterstützt MSDV das Senden von AV/C-Rohbefehlen an das Gerät.

Beachten Sie bei der Verwendung dieses Features die folgenden Punkte:

-   Der Befehl wird ohne Fehlerüberprüfung oder Parameterüberprüfung direkt an das Gerät übergeben. Aus diesem Grund sollten Sie unformatierte AV/C-Befehle nur dann ausstellen, wenn die DirectShow-Schnittstellen die benötigte Funktionalität nicht implementieren.
-   Alle unformatierten AV/C-Befehle sind synchron. Der Thread, der den Befehl ausgibt, wird blockiert, bis der Befehl zurückgegeben wird.
-   Es kann jeweils nur ein Befehl angegeben werden. Während der Verarbeitung des Befehls lehnt das Gerät alle zusätzlichen Befehle ab.
-   Der UVC-Treiber unterstützt keine unformatierten AV/C-Befehle.

Formatieren Sie den Befehl als Bytearray, um einen AV/C-Befehl zu senden. Rufen Sie dann [**IAMExtTransport::GetTransportBasicParameters auf.**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) Übergeben Sie das ED \_ RAW \_ EXT DEV \_ \_ CMD-Flag, die Arraygröße und das Array. Sie müssen die Arrayadresse in einen **\* LPOLESTR-Typ** umwandlungen, da der ursprüngliche Zweck dieses Parameters darin bestand, einen Zeichenfolgenwert zurückzugeben.


```C++
BYTE AvcCmd[] = { ... }; // Contains the AV/C command (not shown)
long cbCmd = sizeof(AvcCmd);
hr = pTransport->GetTransportBasicParameters(
    ED_RAW_EXT_DEV_CMD, 
    &cbCmd,
    (LPOLESTR*) AvcCmd);
```



Der Inhalt des Arrays wird direkt an das Gerät übergeben, daher müssen Sie darauf achten, es ordnungsgemäß zu formatieren. Ein Befehl kann auf die Einheit (DasEinband) oder eine Untereinheit (Band oder Kamera) abzielen. Die relevanten Standards sind auf der [Website 1394 Trade Association](https://1394ta.org)verfügbar.

-   Allgemeine Spezifikation des AV/C-Befehlssatzes für die digitale Schnittstelle
-   AV/C Tape Recorder/Player-Untereinheitsspezifikation

Erstere beschreibt das Formatieren von AV/C-Befehlen und listet die Komponentenbefehle auf. Die zweite Spezifikation listet die Untereinheitsbefehle auf.

Die **GetTransportBasicParameters-Methode** gibt möglicherweise einen der folgenden Fehlercodes zurück:



| Fehlercode              | BESCHREIBUNG                                                                      |
|-------------------------|----------------------------------------------------------------------------------|
| \_FEHLERTIMEOUT          | Für den Befehl ist ein Time out (Time-Out) für den Befehl erfolgt.                                                           |
| FEHLER \_ REQ \_ NOT \_ ACCEP  | Das Gerät hat den Befehl nicht akzeptiert.                                           |
| FEHLER \_ NICHT \_ UNTERSTÜTZT   | Das Gerät unterstützt den Befehl nicht.                                         |
| FEHLERANFORDERUNG \_ \_ ABGEBROCHEN | Der Befehl wurde abgebrochen. Stellen Sie sicher, dass das Gerät entfernt wurde oder ein Bus zurückgesetzt wurde. |



 

> [!Note]  
> Diese Fehler werden als Win32-Fehlercodes und nicht als HRESULTs zurückgegeben. Daher sollten Sie direkt auf diese Werte testen, anstatt die Makros **SUCCEEDED** und **FAILED** zu verwenden.

 

Wenn die Methode S \_ OK zurückgibt, wird die Antwort des Geräts in das Array kopiert. Da die Antwortnutzlast möglicherweise größer als der Befehl ist, müssen Sie einen Puffer zuordnen, der groß genug ist, um sie zu speichern. Die maximale Nutzlastgröße beträgt 512 Bytes. Beachten Sie, dass der Rückgabewert S \_ OK nicht immer bedeutet, dass das Gerät den Befehl erfolgreich ausgeführt hat. Die Anwendung muss die Antwortnutzlast untersuchen, um den Status zu ermitteln.

Das folgende Beispiel zeigt den Befehl zum Suchen nach einer absoluten Tracknummernsuche:


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

[Steuern eines DV-Dvds](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



