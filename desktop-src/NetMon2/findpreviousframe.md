---
description: Die findpreviousframe-Funktion findet den vorherigen Frame im aktuellen Aufzeichnungs Kontext, der mit dem Filter übereinstimmt.
ms.assetid: 16c5b981-a9f4-41e5-bb97-2caa3e9d8512
title: Findpreviousframe-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPreviousFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: deabf10702ca41c23101c5f60c9459e094e567fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958725"
---
# <a name="findpreviousframe-function"></a>Findpreviousframe-Funktion

Die **findpreviousframe** -Funktion findet den vorherigen Frame im aktuellen Aufzeichnungs Kontext, der mit dem Filter übereinstimmt.

## <a name="syntax"></a>Syntax


```C++
HFRAME WINAPI FindPreviousFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     LowestFrame
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hcurrentframe* 
</dt> <dd>

Handle für den Frame.

</dd> <dt>

*ProtocolName* 
</dt> <dd>

Der Protokoll Name, z. b. TCP.

</dd> <dt>

*DestinationAddress* 
</dt> <dd>

Die Zieladresse des Frame-, der gesucht wird.

</dd> <dt>

*SourceAddress* 
</dt> <dd>

Die Quelladresse des Frame-, der gesucht wird.

</dd> <dt>

*Protocoloffset* 
</dt> <dd>

Zeiger auf ein **Wort** , das den Protokoll Offset empfängt.

</dd> <dt>

*Originalframenum* 
</dt> <dd>

Startpunkt der Suche. Standardmäßig durchsucht diese Funktion nach dem Startpunkt " *originalframenum* " rückwärts 1.000 Frames. Sie können den suchbackweg ändern, indem Sie diese Zeile der Nmapi.ini-Datei hinzufügen, die sich im \\ Netzwerkmonitor Verzeichnis befindet.

Maxlookback =<new lookback distance>

</dd> <dt>

*Lowestframe* 
</dt> <dd>

Niedrigste Frame Nummer in der Erfassung, die durchsucht wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Handle für den vorherigen Frame.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.

## <a name="remarks"></a>Bemerkungen

Der Erfassungs Filter wird primär durch *ProtocolName* definiert. Dies ist die einzige erforderliche Filter Eingabe. Sie können *DestinationAddress* -und *SourceAddress* -Informationen hinzufügen, um die Erfassungs Geschwindigkeit zu erhöhen.

*Protocoloffset* wird an den aufrufenden Parser zurückgegeben, der dieses **DWORD** dem Zeiger hinzufügt, der durch Sperren des Frames (mit [parsertemporarylockframe](parsertemporarylockframe.md)) zurückgegeben wird, um das LPBYTE des gesuchten Protokolls abzurufen. Bei der Rückgabe wird dem Parser der hframe, der den Filter übergeben hat, übergeben. Wenn der Parser feststellt, dass es sich bei dem Frame nicht um den gesuchten Frame handelt, kann der Parser diesen hframe zurück an die **findpreviousframe** -Funktion übergeben, um den nächsten Frame abzurufen. Die Quell-und Zieladressen, die nicht erforderlich sind, können als **null**-Werte angegeben werden. Wenn diese Adressen verwendet werden, können Sie den Typ Address \_ Type \_ IP usw., nicht nur Mac-Typen aufweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




