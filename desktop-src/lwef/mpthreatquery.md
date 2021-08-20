---
title: MpThreatQuery-Funktion (MpClient.h)
description: Wird verwendet, um statische (z. B. Schweregrad und Kategorie) oder lokalisierte Informationen (z. B. Kategoriebeschreibung und Ratschläge) zu einer bestimmten Bedrohung abfragt.
ms.assetid: A06854B2-8444-46A4-A53F-FD5FEAFF47B7
keywords:
- MpThreatQuery-Funktion legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MpThreatQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 168f1ef4176db691576f31726eb8c8caab055df9a584b41c3195f7b5b4afeee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883014"
---
# <a name="mpthreatquery-function"></a>MpThreatQuery-Funktion

Wird verwendet, um statische (z. B. Schweregrad und Kategorie) oder lokalisierte Informationen (z. B. Kategoriebeschreibung und Ratschläge) zu einer bestimmten Bedrohung abfragt.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI MpThreatQuery(
  _In_      MPHANDLE                 hMpHandle,
  _In_      MPTHREAT_ID              ThreatID,
  _Out_     PMPTHREAT_INFO           *ppThreatInfo,
  _Out_opt_ PMPTHREAT_LOCALIZED_INFO *ppThreatLocalizedInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hMpHandle* \[ In\]
</dt> <dd>

Typ: **MPHANDLE**

Handle für die Benutzeroberfläche des Schadsoftwareschutz-Managers. Dieses Handle wird von der [**MpManagerOpen-Funktion**](mpmanageropen.md) zurückgegeben.

</dd> <dt>

*ThreatID* \[ In\]
</dt> <dd>

Typ: **MPTHREAT-ID \_**

Bedrohungs-ID, für die Informationen angefordert werden.

</dd> <dt>

*ppThreatInfo* \[ out\]
</dt> <dd>

Typ: **PMPTHREAT \_ \* INFO**

Gibt einen Zeiger auf eine Bedrohungsinformationsstruktur zurück, [**MPTHREAT \_ INFO.**](mpthreat-info.md) Die Struktur enthält Informationen wie Bedrohungs-ID, Name und Schweregrad.

</dd> <dt>

*ppThreatLocalizedInfo* \[ out, optional\]
</dt> <dd>

Typ: **PMPTHREAT \_ LOCALIZED \_ INFO \***

Gibt einen Zeiger auf eine -Struktur zurück, die lokalisierte Informationen zur Bedrohung enthält. Sie können NULL **übergeben,** wenn Sie nicht an lokalisierten Informationen zur Bedrohung interessiert sind. Siehe [**MPTHREAT \_ LOCALIZED \_ INFO**](mpthreat-localized-info.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert **S \_ OK.**

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT-Code.** Der Aufrufer kann die [**MpErrorMessageFormat-Funktion**](mperrormessageformat.md) verwenden, um eine generische Beschreibung der Fehlermeldung zu erhalten.

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

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**\_MPTHREAT-INFORMATIONEN**](mpthreat-info.md)
</dt> <dt>

[**LOKALISIERTE \_ MPTHREAT-INFORMATIONEN \_**](mpthreat-localized-info.md)
</dt> </dl>

 

 





