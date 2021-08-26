---
description: Die GetEventData-Methode ordnet Speicherplatz für die NMEVENTDATA- und NMCOLUMNINFO-Strukturen zu.
ms.assetid: b24a2a30-4543-4311-87ec-66872463aed7
title: IMonitorEventer::GetEventData-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.GetEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 3a089e57ac5f66187f97dfa6ae7533aeda620632bdbf35c7b5bf3a34d4654b0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037370"
---
# <a name="imonitoreventergeteventdata-method"></a>IMonitorEventer::GetEventData-Methode

Die **GetEventData-Methode** ordnet Speicherplatz für die [NMEVENTDATA-](nmeventdata.md) und [NMCOLUMNINFO-Strukturen](nmcolumninfo.md) zu.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetEventData(
  [in]  BYTE         bNumColumns,
  [out] PNMEVENTDATA *ppNMEventData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bNumColumns* \[ In\]
</dt> <dd>

Anzahl der erforderlichen **NMCOLUMNINFO-Strukturen.**

</dd> <dt>

*ppNMEventData* \[ out\]
</dt> <dd>

Adresse der **NMEVENTDATA-Struktur,** die zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK.

Wenn die Methode nicht erfolgreich ist, lautet der Rückgabewert NMERR \_ OUT \_ OF \_ MEMORY.

## <a name="remarks"></a>Hinweise

Monitore rufen diese Methode auf, um Speicher für die Ereignisdaten- und Spalteninformationsstrukturen zuzuordnen. Informationen zum Freigeben von Arbeitsspeicher für eine **NMEVENTDATA-Struktur** finden Sie unter [IMonitorEventer::FreeEventData.](imonitoreventer-freeeventdata.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IMonitorEventer](imonitoreventer.md)
</dt> <dt>

[IMonitorEventer::FreeEventData](imonitoreventer-freeeventdata.md)
</dt> <dt>

[NMEVENTDATA](nmeventdata.md)
</dt> <dt>

[NMCOLUMNINFO](nmcolumninfo.md)
</dt> </dl>

 

 




