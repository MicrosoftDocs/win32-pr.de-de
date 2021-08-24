---
description: Die FreeEventData-Methode gibt Speicherplatz frei, der der NMEVENTDATA-Struktur zugeordnet ist.
ms.assetid: f86dcfd8-5a3b-4ce3-9d45-04545b030a89
title: IMonitorEventer::FreeEventData-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer.FreeEventData
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: f2bf462ef63045c8c4e5822e3d28fc21b44dfeed5848da3ac89c8232dfacc062
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037440"
---
# <a name="imonitoreventerfreeeventdata-method"></a>IMonitorEventer::FreeEventData-Methode

Die **FreeEventData-Methode** gibt Speicherplatz frei, der der [**NMEVENTDATA-Struktur zugeordnet**](nmeventdata.md) ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT FreeEventData(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pNMEventData* \[ In\]
</dt> <dd>

Adresse der [**NMEVENTDATA-Struktur,**](nmeventdata.md) deren Arbeitsspeicher frei wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Monitore rufen diese Methode auf, um den Arbeitsspeicher frei zu geben, den sie für die Ereignisdatenstruktur zuordnen. Beachten Sie, dass der Monitor zwar noch über einen Zeiger auf Zeichenfolgen in einer zugeordneten [**NMEVENTDATA-Struktur**](nmeventdata.md) verfügt, der Arbeitsspeicher für diese Zeichenfolgen jedoch vor dem Aufrufen der **FreeEventData-Methode frei** werden muss.

Weitere Informationen zum Zuordnen von Arbeitsspeicher für eine [**NMEVENTDATA-Struktur**](nmeventdata.md) finden Sie unter [**IMonitorEventer::GetEventData**](imonitoreventer-geteventdata.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMonitorEventer**](imonitoreventer.md)
</dt> <dt>

[**IMonitorEventer::GetEventData**](imonitoreventer-geteventdata.md)
</dt> <dt>

[**NMEVENTDATA**](nmeventdata.md)
</dt> </dl>

 

 




