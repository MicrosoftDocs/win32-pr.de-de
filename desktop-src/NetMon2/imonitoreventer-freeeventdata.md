---
description: Die Methode "freeventdata" gibt den zugeordneten Speicherplatz für die nmeventdata-Struktur frei.
ms.assetid: f86dcfd8-5a3b-4ce3-9d45-04545b030a89
title: 'Imonitoreventer:: freeventdata-Methode (Netmon. h)'
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
ms.openlocfilehash: c71b7563e00bfceb220ce1c2bf109339267fbabf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343642"
---
# <a name="imonitoreventerfreeeventdata-method"></a>Imonitoreventer:: freeventdata-Methode

Die Methode " **freeventdata** " gibt den zugeordneten Speicherplatz für die [**nmeventdata**](nmeventdata.md) -Struktur frei.

## <a name="syntax"></a>Syntax


```C++
HRESULT FreeEventData(
  [in] PNMEVENTDATA pNMEventData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pnmeventdata* \[ in\]
</dt> <dd>

Adresse der [**nmeventdata**](nmeventdata.md) -Struktur, deren Arbeitsspeicher freigegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt "S OK" zurück \_ .

## <a name="remarks"></a>Bemerkungen

Diese Methode wird von Monitoren aufgerufen, um den Arbeitsspeicher freizugeben, den Sie für die Ereignisdaten Struktur zuordnen. Beachten Sie, dass während des Monitors weiterhin ein Zeiger auf Zeichen folgen in einer zugeordneten [**nmeventdata**](nmeventdata.md) -Struktur vorhanden ist, muss der Arbeitsspeicher für diese Zeichen folgen freigegeben werden, bevor die Methode " **freieventdata** " aufgerufen wird.

Weitere Informationen zum Zuordnen von Arbeitsspeicher für eine [**nmeventdata**](nmeventdata.md) -Struktur finden Sie unter [**imonitoreventer:: geteventdata**](imonitoreventer-geteventdata.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imonitoreventer Enter**](imonitoreventer.md)
</dt> <dt>

[**Imonitoreventer:: geteventdata**](imonitoreventer-geteventdata.md)
</dt> <dt>

[**Nmeventdata**](nmeventdata.md)
</dt> </dl>

 

 




