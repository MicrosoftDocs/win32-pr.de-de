---
description: Die "attachproperties"-Exportfunktion ordnet die Eigenschaften einem Speicherort innerhalb einer erkannten Daten zu. Attachproperties müssen für jeden Parser implementiert werden, der von der Parser-DLL unterstützt wird.
ms.assetid: ef28f571-8364-47d0-841c-580e89333afd
title: Attachproperties-Rückruffunktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 3b3cb4be93b8d960b39f0f5c5cf2b5a4809573cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359020"
---
# <a name="attachproperties-callback-function"></a>Attachproperties-Rückruffunktion

Die " **attachproperties** "-Exportfunktion ordnet die Eigenschaften einem Speicherort innerhalb einer erkannten Daten zu. **Attachproperties** müssen für jeden Parser implementiert werden, der von der Parser-DLL unterstützt wird.

## <a name="syntax"></a>Syntax


```C++
DWORD AttachProperties(
  _In_ HFRAME    hFrame,
  _In_ LPBYTE    lpFrame,
  _In_ LPBYTE    lpProtocol,
  _In_ DWORD     MacType,
  _In_ DWORD     BytesLeft,
  _In_ HPROTOCOL hPreviousProtocol,
  _In_ DWORD     nPreviousProtocolOffset,
  _In_ DWORD     lpInstData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hframe* \[ in\]
</dt> <dd>

Handle des Frames, der analysiert wird.

</dd> <dt>

*lpframe* \[ in\]
</dt> <dd>

Zeiger auf das erste Byte in einem Frame.

</dd> <dt>

*lpprotocol* \[ in\]
</dt> <dd>

Zeiger auf den Anfang der erkannten Daten.

</dd> <dt>

*MacType* \[ in\]
</dt> <dd>

Der Mac-Wert des ersten Protokolls in einem Frame. *MacType* kann einen der folgenden Typen aufweisen:



| Wert                                                                                                                                                                         | Bedeutung                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <dt>**Mac- \_ Typ \_ Ethernet**</dt> </dl>    | 802.3 <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <dt>**Mac- \_ Typ \_ TokenRing**</dt> </dl> | 802.5 <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <dt>**Mac- \_ Typ " \_ f"**</dt> </dl>                | ANSI x3t 9,5 <br/> |



 

</dd> <dt>

*Bytesleft* \[ in\]
</dt> <dd>

Die verbleibende Anzahl von Bytes in einem Frame, beginnend am Anfang der erkannten Daten.

</dd> <dt>

*hpreviousproycol* \[ in\]
</dt> <dd>

Handle des vorherigen Protokolls.

</dd> <dt>

*npreviousprotocoloffset* \[ in\]
</dt> <dd>

Der Offset des vorherigen Protokolls ab dem Anfang des Frames.

</dd> <dt>

*lpinstdata* \[ in\]
</dt> <dd>

Zeiger auf die Instanzdaten, die das vorherige Protokoll bereitstellt. Instanzdaten dürfen nicht länger sein als eine Länge von DWORD \_ ptr.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf das erste Byte nach den erkannten Daten in einem Frame oder **null** , wenn es sich bei den erkannten Daten um das letzte Datenelement in einem Frame handelt.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Zeiger auf die erkannten Daten. Der *lpprotocol* -Parameter übergibt den Zeiger an die Parser-DLL.

## <a name="remarks"></a>Bemerkungen

Netzwerkmonitor Ruft die **attachproperties** -Funktion für jeden Parser auf, der ein Datenelement in einem Frame erkennt. Beachten Sie, dass der Parser bestimmt, welche Eigenschaften in den erkannten Daten vorhanden sind und wo sich die einzelnen Eigenschaften befinden.

Bei der Implementierung von **attachproperties** wird [attachpropertyinstance](attachpropertyinstance.md) aufgerufen, um die Daten zu verwenden, wie Sie in der Erfassung vorhanden sind. Sie können auch die [attachpropertyinstanceex](attachpropertyinstanceex.md) -Funktion aufrufen, um die Eigenschaften Daten zu ändern. Es wird jedoch empfohlen, dass Sie die Daten verwenden, wie Sie in der Erfassung vorhanden sind.

Die Funktionen " **attachpropertyinstanceex** " und " **attachpropertyinstance** " werden nur für die Eigenschaften aufgerufen, die in den erkannten Daten vorhanden sind. Beachten Sie, dass Netzwerkmonitor über eine Eigenschaften [*Datenbank*](p.md) für den Parser verfügt, der eine Beschreibung aller Eigenschaften enthält, die der Parser unterstützt.

**Instanzdaten**

Instanzdaten sind Informationen, die von einem Parser an einen anderen übergeben werden. Instanzdaten können beliebige Daten sein, die kleiner oder gleich einem DWORD- \_ ptr sind, oder ein Zeiger auf Daten, wie z. b. unformatierte Frame-Daten, die nicht vom Parser zugeordnet oder freigegeben werden müssen. Im *lpinstdata* -Parameter der **Eigenschaften attachproperties** und [erkennzeframe](recognizeframe.md) stellt Netzwerkmonitor einen Zeiger auf die Instanzdaten des vorherigen Protokolls bereit. Sie können die Instanzdaten für den Parser während der Implementierung von " **erkenzeframe**" festlegen.



| Für Informationen zu                                          | Siehe                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren.   | [Parser](parsers.md)                                             |
| Welche Einstiegspunkte in der Parser-DLL enthalten sind.           | [Architektur der Parser-DLL](parser-dll-architecture.md)             |
| Erkennen von Daten.                                      | [Implementieren von "erkenzeframe"](implementing-recognizeframe.md)     |
| So erstellen Sie eine Eigenschaften Datenbank                          | [Implementieren von Register](implementing-register.md)                 |
| Zum Implementieren von **attachproperties**  gehört ein Beispiel. | [Implementieren von attachproperties](implementing-attachproperties.md) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Attachpropertyinstance](attachpropertyinstance.md)
</dt> <dt>

[Attachpropertyinstanceex](attachpropertyinstanceex.md)
</dt> <dt>

[Erkenzeframe](recognizeframe.md)
</dt> </dl>

 

 




