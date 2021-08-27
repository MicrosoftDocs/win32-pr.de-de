---
description: 'IDelaydC::GetTotalStatistics-Methode: Die GetTotalStatistics-Methode ruft die Gesamtstatistik für die aktuelle Erfassung ab.'
ms.assetid: 904c7496-5603-41b9-8481-06fa31f6f112
title: IDelaydC::GetTotalStatistics-Methode (Netmon.h)
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
ms.openlocfilehash: e6b4d76b3035e156da1f1d4decf7a5c59b28bf0ca13bc2bdaa33e319422509af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037550"
---
# <a name="idelaydcgettotalstatistics-method"></a>IDelaydC::GetTotalStatistics-Methode

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

Zeiger auf eine [STATISTICS-Struktur,](statistics.md)die die Gesamtstatistik für die Erfassung enthält. Der Aufrufer ist dafür verantwortlich, den von der STATISTICS-Struktur verwendeten Arbeitsspeicher zu reservieren **und frei** zu geben.

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
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl> | Der NPP ist nicht mit dem Netzwerk verbunden. Rufen [Sie IDelaydC::Verbinden](idelaydc-connect.md) auf, um eine Verbindung mit dem Netzwerk herzustellen.<br/> |
| <dl> <dt>**NMERR \_ NICHT \_ VERZÖGERT**</dt> </dl>   | Das NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IDelaydC::Verbinden-Methode.](idelaydc-connect.md)<br/>             |
| <dl> <dt>**NMERR NOT CAPTURING (NMERR \_ WIRD NICHT \_ ERFASST)**</dt> </dl> | Der NPP erfasst keine Daten. Rufen [Sie IDelaydC::Start auf, um](idelaydc-start.md) mit dem Erfassen von Daten zu beginnen.<br/>                 |



 

## <a name="remarks"></a>Hinweise

Diese Methode gibt Daten nur zurück, während eine Erfassung läuft. Wenn die Erfassung angehalten wird, sind Aufrufe dieser Methode nicht erfolgreich.

Netzwerkmonitor werden [*auch*](c.md)Konversationsstatistiken gespeichert, die durch Aufrufen der [IDelaydC::GetConversationStatistics-Methode abgerufen werden](idelaydc-getconversationstatistics.md) können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC::Verbinden](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> <dt>

[Statistiken](statistics.md)
</dt> </dl>

 

 




