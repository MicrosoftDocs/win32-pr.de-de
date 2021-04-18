---
description: Die gettotalstatistics-Methode ruft die Gesamtstatistik für die aktuelle Erfassung ab.
ms.assetid: e5098984-c69e-4cd5-9143-d85dfcbd7b92
title: 'Untc:: gettotalstatistics-Methode (Netmon. h)'
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
ms.openlocfilehash: 27128048b4326aae14ae6a2e2e6c0540b1105538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358826"
---
# <a name="irtcgettotalstatistics-method"></a>Untc:: gettotalstatistics-Methode

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

Zeiger auf eine [Statistik](statistics.md) Struktur, die die Gesamtstatistik für die Erfassung bereitstellt. Die Aufrufer sind dafür verantwortlich, den von der **Statistik** Struktur genutzten Arbeitsspeicher zuzuordnen und freizugeben.

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
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl> | Der npp ist nicht mit dem Netzwerk verbunden. Wenden [Sie](irtc-connect.md) sich an, um den NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**nmerr \_ nicht in \_ Echtzeit**</dt> </dl>  | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der Methode " [iritc:: Connect](irtc-connect.md) ".<br/>                     |
| <dl> <dt>**nmerr wird \_ nicht \_ erfasst**</dt> </dl> | Der NPP erfasst keine Daten. Nennen Sie " [untc:: Start](irtc-start.md) ", um die Datenerfassung zu starten<br/>                         |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt nur Daten zurück, während eine Erfassung ausgeführt wird, einschließlich der Pause, während die Erfassung angehalten wird.

Netzwerkmonitor speichert auch [*Konversations Statistiken*](c.md). Um Konversations Statistiken abzurufen, rufen Sie die Methode " [iritc:: getconversation ationstatistics](irtc-getconversationstatistics.md) " auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

["Iran"](irtc.md)
</dt> <dt>

[Iran:: Connect](irtc-connect.md)
</dt> <dt>

["Irren:: getconversation ationstatistics"](irtc-getconversationstatistics.md)
</dt> <dt>

["Iran:: Start"](irtc-start.md)
</dt> <dt>

[Kam](statistics.md)
</dt> </dl>

 

 




