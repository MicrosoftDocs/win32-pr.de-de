---
title: MpThreatEnumerate-Funktion (MpClient.h)
description: Gibt Informationen zur nächsten Bedrohung in der Enumerationsliste zurück. Diese Funktion kann wiederholt aufgerufen werden, bis die Enumeration aller Bedrohungen abgeschlossen ist.
ms.assetid: 33244F4F-4FB7-4FA7-BC56-B9A30ABC3644
keywords:
- MpThreatEnumerate-Funktion Legacy-Windows-Umgebungsfeatures
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
ms.openlocfilehash: 9525ad44901bd62044721e634559e1c803b88b05e9250097d939b3a5a04d229a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943830"
---
# <a name="mpthreatenumerate-function"></a>MpThreatEnumerate-Funktion

Gibt Informationen zur nächsten Bedrohung in der Enumerationsliste zurück. Diese Funktion kann wiederholt aufgerufen werden, bis die Enumeration aller Bedrohungen abgeschlossen ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI MpThreatEnumerate(
  _In_  MPHANDLE       hThreatEnumHandle,
  _Out_ PMPTHREAT_INFO *ppThreatInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hThreatEnumHandle* \[ In\]
</dt> <dd>

Typ: **MPHANDLE**

Verarbeiten Sie einen von [**MpThreatOpen zurückgegebenen**](mpthreatopen.md)Bedrohungsenumerationskontext.

</dd> <dt>

*ppThreatInfo* \[ out\]
</dt> <dd>

Typ: **PMPTHREAT \_ \* INFO**

Gibt einen Zeiger auf eine Bedrohungsinformationsstruktur zurück, [**MPTHREAT \_ INFO.**](mpthreat-info.md) Die Struktur enthält Informationen wie Bedrohungs-ID, Name und Schweregrad.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert **S \_ OK.**

Wenn keine Elemente mehr vorhanden sind, die zurückgegeben werden sollen, lautet der Rückgabewert **S \_ FALSE**.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT-Code.** Der Aufrufer kann die [**MpErrorMessageFormat-Funktion**](mperrormessageformat.md) verwenden, um eine generische Beschreibung der Fehlermeldung abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpThreatOpen**](mpthreatopen.md)
</dt> <dt>

[**\_MPTHREAT-INFORMATIONEN**](mpthreat-info.md)
</dt> </dl>

 

 





