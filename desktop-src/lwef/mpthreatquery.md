---
title: Mpbedrohlich Query-Funktion (mpclient. h)
description: Wird verwendet, um statische (z. b. Schweregrad und Kategorie) oder lokalisierte Informationen zu einer bestimmten Bedrohung (z. b. Kategorien Beschreibung und Ratschläge) abzufragen.
ms.assetid: A06854B2-8444-46A4-A53F-FD5FEAFF47B7
keywords:
- Mpbedrohlich Query-Funktion Legacy-Windows-Umgebungs Features
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
ms.openlocfilehash: 21d38a3734f9d98f3bd61143d4fe58bd606c7508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338721"
---
# <a name="mpthreatquery-function"></a>Mpbedrohlich Query-Funktion

Wird verwendet, um statische (z. b. Schweregrad und Kategorie) oder lokalisierte Informationen zu einer bestimmten Bedrohung (z. b. Kategorien Beschreibung und Ratschläge) abzufragen.

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

*hmphandle* \[ in\]
</dt> <dd>

Typ: **mphandle**

Handle für die Malware Protection Manager-Schnittstelle. Dieses Handle wird von der [**mpmanageropen**](mpmanageropen.md) -Funktion zurückgegeben.

</dd> <dt>

*Threatid* \[ in\]
</dt> <dd>

Typ: **mpthreat- \_ ID**

Der Bedrohungs Bezeichner, für den Informationen angefordert werden.

</dd> <dt>

*ppbedrohlich Info* \[ vorgenommen\]
</dt> <dd>

Typ: **pmpthreat \_ Info \** _

Gibt einen Zeiger auf eine Bedrohungs Informationsstruktur zurück, [_ *mpthreat \_ Info* *](mpthreat-info.md). Die Struktur enthält Informationen wie die Bedrohungs-ID, den Namen und den Schweregrad.

</dd> <dt>

*ppbedrohlich localizedinfo* \[ Out, optional\]
</dt> <dd>

Geben Sie Folgendes ein: **pmpthreat \_ lokalisierte \_ \* Info* _

Gibt einen Zeiger auf eine-Struktur zurück, die lokalisierte Informationen über die Bedrohung enthält. Sie können _ *null** übergeben, wenn Sie nicht an lokalisierten Informationen über die Bedrohung interessiert sind. Siehe " [**mpthreat \_ lokalisierte \_ Informationen**](mpthreat-localized-info.md)".

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**.

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

[**Mpmanageropen**](mpmanageropen.md)
</dt> <dt>

[**mpthreat- \_ Informationen**](mpthreat-info.md)
</dt> <dt>

[**lokalisierte mpthreat- \_ \_ Informationen**](mpthreat-localized-info.md)
</dt> </dl>

 

 





