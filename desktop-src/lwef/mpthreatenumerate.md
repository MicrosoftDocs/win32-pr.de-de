---
title: Mperate Enumerate-Funktion (mpclient. h)
description: Gibt Informationen über die nächste Bedrohung in der Enumerationsliste zurück. Diese Funktion kann wiederholt aufgerufen werden, bis die Enumeration aller Bedrohungen vollständig ist.
ms.assetid: 33244F4F-4FB7-4FA7-BC56-B9A30ABC3644
keywords:
- Mpenenumerate-Funktion Legacy Funktionen der Windows-Umgebung
topic_type:
- apiref
api_name:
- MpThreatEnumerate
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acdbb7971371015a401c1a951ace8c55869fd405
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956835"
---
# <a name="mpthreatenumerate-function"></a>Mpbedrohlich Enumerate-Funktion

Gibt Informationen über die nächste Bedrohung in der Enumerationsliste zurück. Diese Funktion kann wiederholt aufgerufen werden, bis die Enumeration aller Bedrohungen vollständig ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI MpThreatEnumerate(
  _In_  MPHANDLE       hThreatEnumHandle,
  _Out_ PMPTHREAT_INFO *ppThreatInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hbedrohlich-enumhandle* \[ in\]
</dt> <dd>

Typ: **mphandle**

Handle für einen Bedrohungs enumerationskontext, der von [**mpbedrohlich Open**](mpthreatopen.md)zurückgegeben wird.

</dd> <dt>

*ppbedrohlich Info* \[ vorgenommen\]
</dt> <dd>

Typ: **pmpthreat \_ Info \** _

Gibt einen Zeiger auf eine Bedrohungs Informationsstruktur zurück, [_ *mpthreat \_ Info* *](mpthreat-info.md). Die Struktur enthält Informationen wie die Bedrohungs-ID, den Namen und den Schweregrad.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**.

Wenn keine weiteren Elemente vorhanden sind, die zurückgegeben werden sollen, ist der Rückgabewert **S \_ false**.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT** -Code. Der Aufrufer kann die [**mperrormessageformat**](mperrormessageformat.md) -Funktion verwenden, um eine generische Beschreibung der Fehlermeldung zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mperrormessageformat**](mperrormessageformat.md)
</dt> <dt>

[**Mpbedrohlich öffnen**](mpthreatopen.md)
</dt> <dt>

[**mpthreat- \_ Informationen**](mpthreat-info.md)
</dt> </dl>

 

 





