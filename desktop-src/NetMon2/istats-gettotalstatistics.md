---
description: Die gettotalstatistics-Methode ruft die Gesamtstatistik für die aktuelle Erfassung ab.
ms.assetid: 494634f6-a9b3-4a50-8920-2387be9ba30f
title: 'IStats:: gettotalstatistics-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 51cdbfdcc796aa7d8091e8da5837809efaa63379
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353622"
---
# <a name="istatsgettotalstatistics-method"></a>IStats:: gettotalstatistics-Methode

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

Flag, mit dem Netzwerkmonitor wird, wie der interne Speicher der gesamten Statistik behandelt werden soll. Die Einstellung true weist Netzwerkmonitor an, den internen Speicher der gesamten Statistik zu löschen, nachdem die aktuellen Informationen abgerufen wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                            | Beschreibung                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl>   | Der npp ist nicht mit dem Netzwerk verbunden. Wenden Sie die [iStats:: Connect](istats-connect.md) -Methode an, um die NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**nmerr \_ nicht \_ \_ nur Statistiken**</dt> </dl> | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [iStats:: Connect](istats-connect.md) -Methode.<br/>                                |
| <dl> <dt>**nmerr wird \_ nicht \_ erfasst**</dt> </dl>   | Der NPP erfasst keine Daten. Um mit dem Erfassen von Daten zu beginnen, müssen Sie die [iStats:: Start](istats-start.md) -Methode<br/>                         |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt nur Daten zurück, während eine Erfassung ausgeführt wird, einschließlich der Pause, während die Erfassung angehalten wird.

Netzwerkmonitor speichert auch [*Konversations Statistiken*](c.md), die durch Aufrufen der [iStats:: getconversation ationstatistics](istats-getconversationstatistics.md) -Methode abgerufen werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats:: Connect](istats-connect.md)
</dt> <dt>

[IStats:: getconversation ationstatistics](istats-getconversationstatistics.md)
</dt> <dt>

[IStats:: Start,](istats-start.md)
</dt> <dt>

[Kam](statistics.md)
</dt> </dl>

 

 




