---
description: Sucht den nächsten Frame im aktuellen Erfassungs Kontext, der mit dem Filter übereinstimmt.
ms.assetid: cc99b4a0-b6b0-43b4-8121-0e402d024009
title: Findnextframe-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2e303f7f9031ad451ad19be8bc8cbcd3abae3f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525151"
---
# <a name="findnextframe-function"></a>Findnextframe-Funktion

Die **findnextframe** -Funktion findet den nächsten Frame im aktuellen Aufzeichnungs Kontext, der mit dem Filter übereinstimmt.

## <a name="syntax"></a>Syntax


```C++
HFRAME WINAPI FindNextFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     HighestFrame
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hcurrentframe* 
</dt> <dd>

Ein Handle für den Frame.

</dd> <dt>

*ProtocolName* 
</dt> <dd>

Der Protokoll Name, z. b. TCP.

</dd> <dt>

*DestinationAddress* 
</dt> <dd>

Die Zieladresse.

</dd> <dt>

*SourceAddress* 
</dt> <dd>

Die Quelladresse.

</dd> <dt>

*Protocoloffset* 
</dt> <dd>

Ein Zeiger auf ein **Wort** , das den Protokoll Offset empfängt.

</dd> <dt>

*Originalframenum* 
</dt> <dd>

Der Ausgangspunkt der Suche. Diese Funktion durchsucht standardmäßig 1.000 Frames vom Ausgangspunkt *originalframenum* . Fügen Sie die folgende Zeile zur Nmapi.ini Datei hinzu, die sich im Netzwerkmonitor Verzeichnis befindet, um die Suche nach vorn zu ändern \\ .

Maxlookback =<new lookforward distance>

</dd> <dt>

*Highestframe* 
</dt> <dd>

Die höchste Frame Nummer in der Erfassung, die durchsucht wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Handle für den nächsten Frame.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.

## <a name="remarks"></a>Bemerkungen

Der Erfassungs Filter wird primär durch den *ProtocolName* -Parameter definiert, der die einzige erforderliche Filter Eingabe ist. Sie können *DestinationAddress* -und *SourceAddress* -Daten hinzufügen, um die Erfassungs Geschwindigkeit zu erhöhen.

Der *protocoloffset* -Zeiger wird an den aufrufenden Parser zurückgegeben, der das **Wort** dem Zeiger hinzufügt, der durch Sperren des Frames (mit [parsertemporarylockframe](parsertemporarylockframe.md)) zurückgegeben wird, um das **LPBYTE** des gesuchten Protokolls abzurufen. Bei der Rückgabe wird dem Parser der hframe, der den Filter übergeben hat, übergeben. Wenn der Parser feststellt, dass es sich bei diesem Frame nicht um den gesuchten Frame handelt, kann der Parser den hframe zurück an die **findnextframe** -Funktion übergeben, um den nächsten Frame zu erhalten. Die Quell-und Zieladressen sind nicht erforderlich und können als **null**-Werte übermittelt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




