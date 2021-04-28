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
ms.openlocfilehash: b3a0ce4f230236e276fede528a5e778ecafd51fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113528"
---
# <a name="idelaydcgettotalstatistics-method"></a>IDelaydC::GetTotalStatistics-Methode

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

Zeiger auf eine [STATISTICS-Struktur,](statistics.md)die die Gesamtstatistik für die Erfassung bereitstellt. Der Aufrufer ist dafür verantwortlich, den von der **STATISTICS-Struktur** verwendeten Arbeitsspeicher zuzuordnen und freizugeben.

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
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl> | Das NPP ist nicht mit dem Netzwerk verbunden. Rufen Sie [IDelaydC::Connect](idelaydc-connect.md) auf, um eine Verbindung mit dem Netzwerk herzustellen.<br/> |
| <dl> <dt>**NMERR \_ NICHT \_ VERZÖGERT**</dt> </dl>   | Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IDelaydC::Connect-Methode.](idelaydc-connect.md)<br/>             |
| <dl> <dt>**NMERR \_ NICHT \_ ERFASSEN**</dt> </dl> | Das NPP erfasst keine Daten. Rufen Sie [IDelaydC::Start](idelaydc-start.md) auf, um mit der Erfassung von Daten zu beginnen.<br/>                 |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt Daten nur zurück, während eine Erfassung ausgeführt wird. Wenn die Erfassung angehalten wird, sind Aufrufe dieser Methode nicht erfolgreich.

Netzwerkmonitor speichert auch [*Konversationsstatistiken,*](c.md)die durch Aufrufen der [IDelaydC::GetConversationStatistics-Methode](idelaydc-getconversationstatistics.md) abgerufen werden können.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC::Connect](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> <dt>

[Statistiken](statistics.md)
</dt> </dl>

 

 




