---
description: 'IRTC::GetTotalStatistics-Methode: Die GetTotalStatistics-Methode ruft die Gesamtstatistik für die aktuelle Erfassung ab.'
ms.assetid: e5098984-c69e-4cd5-9143-d85dfcbd7b92
title: IRTC::GetTotalStatistics-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: c2b5187ab0afb432e845c74d29144c02edf94cdb62f291ae69e88ea5a5fdf198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063870"
---
# <a name="irtcgettotalstatistics-method"></a>IRTC::GetTotalStatistics-Methode

Die **GetTotalStatistics-Methode** ruft die [*Gesamtstatistik für*](t.md) die aktuelle Erfassung [*ab.*](c.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpStats* \[ out\]
</dt> <dd>

Zeiger auf eine [STATISTICS-Struktur,](statistics.md) die die Gesamtstatistik für die Erfassung enthält. Es liegt in der Verantwortung der Aufrufer, den von der STATISTICS-Struktur verwendeten Arbeitsspeicher zu reservieren **und frei** zu geben.

</dd> <dt>

*fClearAfterReading* \[ In\]
</dt> <dd>

Flag, das verwendet wird, Netzwerkmonitor, wie der interne Speicher der Gesamtstatistik behandelt werden soll. Die Einstellung **TRUE weist** Netzwerkmonitor, den internen Speicher der Gesamtstatistik zu löschen, nachdem die aktuellen Informationen abgerufen wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                          | Beschreibung                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl> | Der NPP ist nicht mit dem Netzwerk verbunden. Rufen [Sie IRTC::Verbinden](irtc-connect.md) auf, um das NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**NMERR \_ NOT \_ REALTIME**</dt> </dl>  | Der NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IRTC::Verbinden-Methode.](irtc-connect.md)<br/>                     |
| <dl> <dt>**NMERR NOT CAPTURING (NMERR \_ WIRD NICHT \_ ERFASST)**</dt> </dl> | Der NPP erfasst keine Daten. Rufen Sie [IRTC::Start auf,](irtc-start.md) um mit dem Erfassen von Daten zu beginnen.<br/>                         |



 

## <a name="remarks"></a>Hinweise

Diese Methode gibt Daten nur zurück, während eine Erfassung in Bearbeitung ist, einschließlich, während die Erfassung angehalten wird.

Netzwerkmonitor speichert auch [*Konversationsstatistiken.*](c.md) Rufen Sie zum Abrufen von Konversationsstatistiken die [IRTC::GetConversationStatistics-Methode](irtc-getconversationstatistics.md) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Verbinden](irtc-connect.md)
</dt> <dt>

[IRTC::GetConversationStatistics](irtc-getconversationstatistics.md)
</dt> <dt>

[IRTC::Start](irtc-start.md)
</dt> <dt>

[Statistiken](statistics.md)
</dt> </dl>

 

 




