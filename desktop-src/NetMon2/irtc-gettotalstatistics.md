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
ms.openlocfilehash: 8ed659efe388f4eb9c9ac8afd6aa2c74fd0af7d3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110688"
---
# <a name="irtcgettotalstatistics-method"></a>IRTC::GetTotalStatistics-Methode

Die **GetTotalStatistics-Methode** ruft die [*Gesamtstatistik*](t.md) für die aktuelle [*Erfassung*](c.md)ab.

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

Zeiger auf eine [STATISTICS-Struktur,](statistics.md) die die Gesamtstatistik für die Erfassung bereitstellt. Es liegt in der Verantwortung der Aufrufer, den von der **STATISTICS-Struktur** verwendeten Arbeitsspeicher zuzuordnen und freizugeben.

</dd> <dt>

*fClearAfterReading* \[ In\]
</dt> <dd>

Flag, das verwendet wird, um Netzwerkmonitor zu informieren, wie der interne Speicher der Gesamtstatistik behandelt werden soll. Die Einstellung **TRUE** weist Netzwerkmonitor an, den internen Speicher der Gesamtstatistik zu löschen, nachdem die aktuellen Informationen abgerufen wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                          | Beschreibung                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl> | Das NPP ist nicht mit dem Netzwerk verbunden. Rufen Sie [IRTC::Connect](irtc-connect.md) auf, um das NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**NMERR \_ NOT \_ REALTIME**</dt> </dl>  | Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IRTC::Connect-Methode.](irtc-connect.md)<br/>                     |
| <dl> <dt>**NMERR \_ NICHT \_ ERFASSEN**</dt> </dl> | Das NPP erfasst keine Daten. Rufen Sie [IRTC::Start](irtc-start.md) auf, um mit der Erfassung von Daten zu beginnen.<br/>                         |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt Daten nur zurück, während eine Erfassung in Bearbeitung ist, einschließlich, während die Erfassung angehalten wird.

Netzwerkmonitor speichert auch [*Konversationsstatistiken.*](c.md) Rufen Sie zum Abrufen von Konversationsstatistiken die [IRTC::GetConversationStatistics-Methode](irtc-getconversationstatistics.md) auf.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Connect](irtc-connect.md)
</dt> <dt>

[IRTC::GetConversationStatistics](irtc-getconversationstatistics.md)
</dt> <dt>

[IRTC::Start](irtc-start.md)
</dt> <dt>

[Statistiken](statistics.md)
</dt> </dl>

 

 




