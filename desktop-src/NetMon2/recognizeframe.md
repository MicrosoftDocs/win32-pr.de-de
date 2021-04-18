---
description: Die Funktion "erkenzeframe Export" gibt an, ob ein Datenelement als das vom Parser erkannte Protokoll erkannt wird. Die Funktion "erkenzeframe Export" muss für jeden Parser implementiert werden, der von der Parser-DLL unterstützt wird.
ms.assetid: 3f835f58-b011-4329-b9b2-ff865a1f0ae5
title: Erkenzeframe-Rückruffunktion (Netmon. h)
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
ms.openlocfilehash: e2660629cecfa279377794749714102077fb6979
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351585"
---
# <a name="recognizeframe-callback-function"></a>Erkenzeframe-Rückruffunktion

Die Funktion " **erkenzeframe** Export" gibt an, ob ein Datenelement als das vom Parser erkannte Protokoll erkannt wird. Die Funktion " **erkenzeframe** Export" muss für jeden Parser implementiert werden, der von der Parser-DLL unterstützt wird.

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

*hframe* \[ in\]
</dt> <dd>

Handle für den Frame, der die Daten enthält.

</dd> <dt>

*lpframe* \[ in\]
</dt> <dd>

Zeiger auf das erste Byte eines Frames. Der-Zeiger bietet eine Möglichkeit, Daten anzuzeigen, die von anderen-Parser erkannt werden.

</dd> <dt>

*lpprotocol* \[ in\]
</dt> <dd>

Zeiger auf den Anfang der nicht beanspruchten Daten. In der Regel befinden sich die nicht beanspruchten Daten in der Mitte eines Frames, da ein vorheriger Parser Daten vor diesem Parser beansprucht hat. Der Parser muss zuerst die nicht beanspruchten Daten testen.

</dd> <dt>

*MacType* \[ in\]
</dt> <dd>

Der Mac-Wert des ersten Protokolls in einem Frame. In der Regel wird der *MacType* -Wert verwendet, wenn der Parser das erste Protokoll in einem Frame identifizieren muss. Der *MacType* -Wert kann einer der folgenden Werte sein:



| Wert                                                                                                                                                                         | Bedeutung                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <dt>**Mac- \_ Typ \_ Ethernet**</dt> </dl>    | 802.3 <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <dt>**Mac- \_ Typ \_ TokenRing**</dt> </dl> | 802.5 <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <dt>**Mac- \_ Typ " \_ f"**</dt> </dl>                | ANSI x3t 9,5 <br/> |



 

</dd> <dt>

*Bytesleft* \[ in\]
</dt> <dd>

Die verbleibende Anzahl von Bytes von einer Position in einem Frame bis zum Ende des Frames.

</dd> <dt>

*hpreviousproycol* \[ in\]
</dt> <dd>

Handle des vorherigen Protokolls.

</dd> <dt>

*npreviousprotocoloffset* \[ in\]
</dt> <dd>

Offset des vorherigen Protokolls beginnend mit dem Frame.

</dd> <dt>

*Protocolstatus Code* \[ vorgenommen\]
</dt> <dd>

Protokoll Status Indikator. Die Parser-DLL muss einen der folgenden Statuscodes festlegen.



| Wert                                                                                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROTOCOL_STATUS_RECOGNIZED"></span><span id="protocol_status_recognized"></span><dl> <dt>**Protokoll \_ Status \_ erkannt**</dt> </dl>              | Der Parser erkennt die Daten, weiß aber nicht, welches Protokoll befolgt wird. Nachdem Sie den Code festgelegt haben, geben Sie einen Zeiger auf die verbleibenden nicht beanspruchten Daten zurück, die dem erkannten Protokoll folgen. Netzwerkmonitor verwendet den [*folgenden Protokoll Satz*](f.md) , um die Verarbeitung fortzusetzen. <br/> |
| <span id="PROTOCOL_STATUS_NOT_RECOGNIZED"></span><span id="protocol_status_not_recognized"></span><dl> <dt>**der Protokoll \_ Status wurde \_ nicht \_ erkannt.**</dt> </dl> | Der Parser erkennt die Daten nicht. Nachdem Sie diesen Code festgelegt haben, geben Sie den Zeiger auf den Anfang der Daten zurück, indem Sie den Zeiger verwenden, den der *lpprotocol* -Parameter an die Parser-DLL übergibt. Netzwerkmonitor verwendet den *folgenden Satz* des vorherigen Protokolls, um die Verarbeitung fortzusetzen. <br/>                |
| <span id="PROTOCOL_STATUS_CLAIMED"></span><span id="protocol_status_claimed"></span><dl> <dt>**Protokoll \_ Status \_ beansprucht**</dt> </dl>                       | Der Parser erkennt die Daten und beansprucht die verbleibenden Daten. Nachdem Sie den Code festgelegt haben, geben Sie **null** zurück, damit Netzwerkmonitor die Verarbeitung eines Frames beenden kann. <br/>                                                                                                                                           |
| <span id="PROTOCOL_STATUS_NEXT_PROTOCOL"></span><span id="protocol_status_next_protocol"></span><dl> <dt>**Protokoll \_ Status \_ nächstes \_ Protokoll**</dt> </dl>    | Der Parser erkennt die Daten und weiß, welches Protokoll befolgt wird. Nachdem Sie den Code festgelegt haben, legen Sie den Parameter *phnextprotocol* fest, und geben Sie einen Zeiger auf die verbleibenden nicht beanspruchten Daten zurück, die dem erkannten Protokoll folgen. Netzwerkmonitor die Verarbeitung des Frames fortsetzen. <br/>                               |



 

</dd> <dt>

*phnextprotocol* \[ vorgenommen\]
</dt> <dd>

Zeiger auf das Handle des nächsten Protokolls. Dieser Parameter wird festgelegt, wenn ein Protokoll das Protokoll identifiziert, das einem Protokoll folgt. Um das Handle des nächsten Protokolls zu erhalten, rufen Sie die [getprotocolfromtable](getprotocolfromtable.md) -Funktion auf.

</dd> <dt>

*lpinstdata* \[ in, out\]
</dt> <dd>

Bei Eingabe ein Zeiger auf die Instanzdaten aus dem vorherigen Protokoll.

Bei der Ausgabe ein Zeiger auf die Instanzdaten für das aktuelle Protokoll. Instanzdaten dürfen nicht länger sein als eine Länge von DWORD \_ ptr.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf das erste Byte nach den erkannten Parserdaten. Wenn der Parser alle verbleibenden Daten beansprucht, ist der Rückgabewert **null**.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein anfänglicher Zeiger, den der *lpprotocol* -Parameter übergibt.

## <a name="remarks"></a>Bemerkungen

Die Funktion " **erkenzeframe** " bestimmt, ob der Parser die Rohdaten erkennt, beginnend beim *lpprotocol* -Zeiger.

-   Wenn das Protokoll die Daten erkennt, gibt die Funktion " **erkenzeframe** " einen Zeiger auf die restlichen Daten zurück oder gibt **null** zurück, wenn das aktuelle Protokoll das letzte Protokoll in einem Frame ist.
-   Wenn das Protokoll die Daten nicht erkennt, gibt die Funktion " **erkennzeframe** " den Zeiger zurück, der an die Parser-DLL im *lpprotocol* -Parameter übergeben wurde.

> [!Note]  
> " *Erkenzeframe* " kann aufgerufen werden, bevor die [*Register*](register-parser.md) -Funktion aufgerufen wird, um die Protokoll Eigenschaften zu registrieren. Aus diesem Grund ist die Implementierung der Funktion " *erkennzeframe* " nicht auf Eigenschaften oder Strukturen angewiesen, die während der Implementierung der Protokoll **Registrierungs** Funktion erstellt oder initialisiert werden.

 

**Handoff festgelegtes und Resultset**

Ein Parser kann einen Handzettel Satz oder einen nachfolgenden Satz verwenden, um zu ermitteln, ob das Protokoll auf erkannte Daten folgt Netzwerkmonitor.

-   Wenn Informationen in erkannten Daten verfügbar sind, verwendet der Parser seine handsemenge, um ein Handle für das nächste Protokoll abzurufen, und übergibt dieses Handle dann an Netzwerkmonitor.
-   Wenn keine Informationen verfügbar sind, übergibt der Parser kein Handle, und Netzwerkmonitor verwendet die parserfolgenmenge, um zu bestimmen, welches Protokoll befolgt wird.

**Übergeben von Informationen zwischen Protokollen**

Verwenden Sie den *lpinstdata* -Parameter, um Informationen zwischen Protokollen zu übergeben. Bei der Eingabe können Sie die Informationen aus dem vorherigen Protokoll abrufen. Bei der Ausgabe können Sie Informationen an das nächste Protokoll übergeben.

Instanzdaten können beliebige Daten sein, die kleiner oder gleich einem DWORD- \_ ptr sind, oder ein Zeiger auf Daten, wie z. b. unformatierte Frame-Daten, die nicht vom Parser zugeordnet oder freigegeben werden müssen.



| Informationen zu                                        | Siehe                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren. | [Parser](parsers.md)                                                                                                    |
| Welche Einstiegspunkte in der Parser-DLL enthalten sind.        | [Architektur der Parser-DLL](parser-dll-architecture.md)                                                                    |
| Zum Implementieren von " **erkenzeframe**  " gehört ein Beispiel. | [Implementieren von "erkenzeframe"](implementing-recognizeframe.md)                                                            |
| Gibt an, wie ein Übergabe festgelegt und der Satz befolgt wird.              | [Angeben eines handsesets](specifying-a-handoff-set.md)mit[Angabe eines folgenden](specifying-a-follow-set.md) Satzes<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Getprotocolfromtable](getprotocolfromtable.md)
</dt> </dl>

 

 




