---
description: Die gettotalstatistics-Methode ruft die Gesamtstatistik für die aktuelle Erfassung ab.
ms.assetid: 904c7496-5603-41b9-8481-06fa31f6f112
title: 'Idelta-DC:: gettotalstatistics-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0d194426933532fcf7a1965ed59b099489eefcb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393410"
---
# <a name="idelaydcgettotalstatistics-method"></a>Idelta aydc:: gettotalstatistics-Methode

Die **gettotalstatistics** -Methode ruft die [*Gesamtstatistik*](t.md) für die aktuelle [*Erfassung*](c.md)ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpstats* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine [Statistik](statistics.md)Struktur, die die Gesamtstatistik für die Erfassung bereitstellt. Es liegt in der Verantwortung des Aufrufers, den von der **Statistik** Struktur genutzten Arbeitsspeicher zuzuordnen und freizugeben.

</dd> <dt>

*f/oder Lese* \[ Vorgänge in\]
</dt> <dd>

Flag, mit dem Netzwerkmonitor wird, wie der interne Speicher der gesamten Statistik behandelt werden soll. Die Einstellung **true** weist Netzwerkmonitor an, den internen Speicher der gesamten Statistik zu löschen, nachdem die aktuellen Informationen abgerufen wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                          | Beschreibung                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl> | Der npp ist nicht mit dem Netzwerk verbunden. Wenden Sie [idelta-DC:: Connect](idelaydc-connect.md) an, um eine Verbindung mit dem Netzwerk herzustellen.<br/> |
| <dl> <dt>**nmerr \_ nicht \_ verzögert**</dt> </dl>   | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [idelta aydc:: Connect](idelaydc-connect.md) -Methode.<br/>             |
| <dl> <dt>**nmerr wird \_ nicht \_ erfasst**</dt> </dl> | Der NPP erfasst keine Daten. Nennen Sie [idelta aydc:: Start](idelaydc-start.md) , um mit dem Erfassen von Daten zu beginnen.<br/>                 |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt nur Daten zurück, während eine Erfassung ausgeführt wird. Wenn die Erfassung angehalten wird, werden Aufrufe dieser Methode nicht erfolgreich ausgeführt.

Netzwerkmonitor speichert auch [*Konversations Statistiken*](c.md), die durch Aufrufen der [idelta aydc:: getconversation ationstatistics](idelaydc-getconversationstatistics.md) -Methode abgerufen werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idelta-DC](idelaydc.md)
</dt> <dt>

[Idelta aydc:: Connect](idelaydc-connect.md)
</dt> <dt>

[Idelta aydc:: getconversation ationstatistics](idelaydc-getconversationstatistics.md)
</dt> <dt>

[Idelta aydc:: Start](idelaydc-start.md)
</dt> <dt>

[Kam](statistics.md)
</dt> </dl>

 

 




