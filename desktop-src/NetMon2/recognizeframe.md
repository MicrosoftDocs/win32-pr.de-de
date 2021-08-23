---
description: Die RecognizeFrame-Exportfunktion gibt an, ob ein Datenteil als das Protokoll erkannt wird, das der Parser erkennt. Die RecognizeFrame-Exportfunktion muss für jeden Parser implementiert werden, der von der Parser-DLL unterstützt wird.
ms.assetid: 3f835f58-b011-4329-b9b2-ff865a1f0ae5
title: RecognizeFrame-Rückruffunktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizeFrame
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: b9f8fcbfccdb306038b7b654e947ff1a11654267012c7527799d8633ed8a9410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889700"
---
# <a name="recognizeframe-callback-function"></a>RecognizeFrame-Rückruffunktion

Die **RecognizeFrame-Exportfunktion** gibt an, ob ein Datenteil als das Protokoll erkannt wird, das der Parser erkennt. Die **RecognizeFrame-Exportfunktion** muss für jeden Parser implementiert werden, der von der Parser-DLL unterstützt wird.

## <a name="syntax"></a>Syntax


```C++
LPBYTE RecognizeFrame(
  _In_    HFRAME      hFrame,
  _In_    LPBYTE      lpFrame,
  _In_    LPBYTE      lpProtocol,
  _In_    DWORD       MacType,
  _In_    DWORD       BytesLeft,
  _In_    HPROTOCOL   hPreviousProtocol,
  _In_    DWORD       nPreviousProtocolOffset,
  _Out_   LPDWORD     ProtocolStatusCode,
  _Out_   LPHPROTOCOL phNextProtocol,
  _Inout_ PDWORD_PTR  lpInstData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hFrame* \[ In\]
</dt> <dd>

Handle für den Frame, der die Daten enthält.

</dd> <dt>

*lpFrame* \[ In\]
</dt> <dd>

Zeiger auf das erste Byte eines Frames. Der Zeiger bietet eine Möglichkeit, Daten anzuzeigen, die andere Parser erkennen.

</dd> <dt>

*lpProtocol* \[ In\]
</dt> <dd>

Zeiger auf den Anfang der nicht beanspruchten Daten. In der Regel befinden sich die nicht beanspruchten Daten in der Mitte eines Frames, da ein vorheriger Parser Daten vor diesem Parser beansprucht hat. Der Parser muss zuerst die nicht beanspruchten Daten testen.

</dd> <dt>

*MacType* \[ In\]
</dt> <dd>

MAC-Wert des ersten Protokolls in einem Frame. In der Regel wird der *MacType-Wert* verwendet, wenn der Parser das erste Protokoll in einem Frame identifizieren muss. Der *MacType-Wert* kann einer der folgenden Sein:



| Wert                                                                                                                                                                         | Bedeutung                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <dt>**\_ \_ MAC-TYP ETHERNET**</dt> </dl>    | 802.3 <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <dt>**MAC \_ TYPE \_ TOKENRING**</dt> </dl> | 802.5 <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <dt>**MAC \_ TYPE \_ FDDI**</dt> </dl>                | ANSI X3T9.5 <br/> |



 

</dd> <dt>

*BytesLeft* \[ In\]
</dt> <dd>

Die verbleibende Anzahl von Bytes von einer Position in einem Frame bis zum Ende des Frames.

</dd> <dt>

*hPreviousProtocol* \[ In\]
</dt> <dd>

Handle des vorherigen Protokolls.

</dd> <dt>

*nPreviousProtocolOffset* \[ In\]
</dt> <dd>

Offset des vorherigen Protokollanfangs des Frames.

</dd> <dt>

*ProtocolStatusCode* \[ out\]
</dt> <dd>

Protokollstatusanzeige. Die Parser-DLL muss einen der folgenden Statuscodes festlegen.



| Wert                                                                                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROTOCOL_STATUS_RECOGNIZED"></span><span id="protocol_status_recognized"></span><dl> <dt>**PROTOKOLLSTATUS \_ \_ ERKANNT**</dt> </dl>              | Der Parser erkennt die Daten, weiß aber nicht, welches Protokoll folgt. Geben Sie nach dem Festlegen des Codes einen Zeiger auf die verbleibenden nicht beanspruchten Daten zurück, die dem erkannten Protokoll folgen. Netzwerkmonitor verwendet den [*folgenden Satz*](f.md) des Protokolls, um die Analyse fortzusetzen. <br/> |
| <span id="PROTOCOL_STATUS_NOT_RECOGNIZED"></span><span id="protocol_status_not_recognized"></span><dl> <dt>**PROTOKOLLSTATUS \_ \_ NICHT \_ ERKANNT**</dt> </dl> | Der Parser erkennt die Daten nicht. Geben Sie nach dem Festlegen dieses Codes den Zeiger auf den Anfang der Daten zurück, indem Sie den Zeiger verwenden, den der *lpProtocol-Parameter* an die Parser-DLL übergibt. Netzwerkmonitor verwendet den *folgenden Satz* des vorherigen Protokolls, um die Analyse fortzusetzen. <br/>                |
| <span id="PROTOCOL_STATUS_CLAIMED"></span><span id="protocol_status_claimed"></span><dl> <dt>**\_BEANSPRUCHTER PROTOKOLLSTATUS \_**</dt> </dl>                       | Der Parser erkennt die Daten und beansprucht die verbleibenden Daten. Geben Sie nach dem Festlegen des Codes **NULL** für Netzwerkmonitor zurück, um die Analyse eines Frames zu beenden. <br/>                                                                                                                                           |
| <span id="PROTOCOL_STATUS_NEXT_PROTOCOL"></span><span id="protocol_status_next_protocol"></span><dl> <dt>**\_PROTOKOLLSTATUS \_ \_ NÄCHSTES PROTOKOLL**</dt> </dl>    | Der Parser erkennt die Daten und weiß, welches Protokoll folgt. Legen Sie nach dem Festlegen des Codes den *Parameter phNextProtocol* fest, und geben Sie einen Zeiger auf die verbleibenden nicht beanspruchten Daten zurück, die dem erkannten Protokoll folgen. Netzwerkmonitor setzt die Analyse des Frames fort. <br/>                               |



 

</dd> <dt>

*phNextProtocol* \[ out\]
</dt> <dd>

Zeiger auf das Handle des nächsten Protokolls. Dieser Parameter wird festgelegt, wenn ein Protokoll das Protokoll identifiziert, das einem Protokoll folgt. Rufen Sie die [GetProtocolFromTable-Funktion](getprotocolfromtable.md) auf, um das Handle des nächsten Protokolls abzurufen.

</dd> <dt>

*lpInstData* \[ in, out\]
</dt> <dd>

Bei der Eingabe ein Zeiger auf die Instanzdaten aus dem vorherigen Protokoll.

Bei der Ausgabe ein Zeiger auf die Instanzdaten für das aktuelle Protokoll. Instanzdaten dürfen nicht länger als eine DWORD \_ PTR-Länge sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf das erste Byte nach den erkannten Parserdaten. Wenn der Parser alle verbleibenden Daten beansprucht, ist der Rückgabewert **NULL.**

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein erster Zeiger, den der *lpProtocol-Parameter* übergibt.

## <a name="remarks"></a>Hinweise

Die **RecognizeFrame-Funktion** bestimmt, ob der Parser die Rohdaten ab dem *lpProtocol-Zeiger* erkennt.

-   Wenn das Protokoll die Daten erkennt, gibt die **RecognizeFrame-Funktion** einen Zeiger auf die verbleibenden Daten oder **NULL** zurück, wenn das aktuelle Protokoll das letzte Protokoll in einem Frame ist.
-   Wenn das Protokoll die Daten nicht erkennt, gibt die **RecognizeFrame-Funktion** den Zeiger zurück, der an die Parser-DLL im *lpProtocol-Parameter* übergeben wird.

> [!Note]  
> *RecognizeFrame* kann aufgerufen werden, bevor die [*Register-Funktion*](register-parser.md) aufgerufen wird, um die Protokolleigenschaften zu registrieren. Aus diesem Grund ist die Implementierung der *RecognizeFrame-Funktion* nicht von Eigenschaften oder Strukturen abhängig, die während der Implementierung der **Register-Protokollfunktion** erstellt oder initialisiert werden.

 

**Übergabesatz und Folgesatz**

Ein Parser kann einen Übergabesatz oder einen Folgesatz verwenden, um Netzwerkmonitor dem Protokoll zu identifizieren, das erkannten Daten folgt.

-   Wenn Informationen in erkannten Daten verfügbar sind, verwendet der Parser seinen Übergabesatz, um ein Handle für das nächste Protokoll abzurufen, und übergibt dieses Handle dann an Netzwerkmonitor.
-   Wenn keine Informationen verfügbar sind, übergibt der Parser kein Handle, und Netzwerkmonitor verwendet den Parser follow set, um zu bestimmen, welches Protokoll folgt.

**Übergeben von Informationen zwischen Protokollen**

Verwenden Sie den *lpInstData-Parameter,* um Informationen zwischen Protokollen zu übergeben. Bei der Eingabe können Sie die Informationen aus dem vorherigen Protokoll abrufen. Bei der Ausgabe können Sie Informationen an das nächste Protokoll übergeben.

Instanzdaten können alle Daten sein, die kleiner oder gleich einer DWORD \_ PTR-Länge sind, oder ein Zeiger auf Daten, z. B. Rohframedaten, die nicht vom Parser zugeordnet oder freigegeben werden müssen.



| Informationen zu                                        | Siehe                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Was Parser sind und wie sie mit Netzwerkmonitor arbeiten. | [Parser](parsers.md)                                                                                                    |
| Welche Einstiegspunkte in der Parser-DLL enthalten sind.        | [Parser-DLL-Architektur](parser-dll-architecture.md)                                                                    |
| Die Implementierung von **RecognizeFrame**  umfasst ein Beispiel. | [Implementieren von RecognizeFrame](implementing-recognizeframe.md)                                                            |
| Hier erfahren Sie, wie Sie einen Übergabesatz angeben und dem Satz folgen.              | [Angeben eines Übergabesatzes](specifying-a-handoff-set.md)[Angeben eines Folgesatzes](specifying-a-follow-set.md)<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[GetProtocolFromTable](getprotocolfromtable.md)
</dt> </dl>

 

 




