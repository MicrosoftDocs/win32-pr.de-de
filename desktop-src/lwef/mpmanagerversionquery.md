---
title: Mpmanagerversionquery-Funktion (mpclient. h)
description: Gibt Versionsinformationen zu verschiedenen Komponenten des Malware Schutz-Managers zurück.
ms.assetid: 47DE12BF-D7A4-468B-B0E7-79B5C27E56F5
keywords:
- Mpmanagerversionquery-Funktion Legacy Funktionen der Windows-Umgebung
topic_type:
- apiref
api_name:
- MpManagerVersionQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a841a83d8ceb828de0a5a9cd80f5f5bdc7f5c914
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341409"
---
# <a name="mpmanagerversionquery-function"></a>Mpmanagerversionquery-Funktion

Gibt Versionsinformationen zu verschiedenen Komponenten des Malware Schutz-Managers zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI MpManagerVersionQuery(
  _In_  MPHANDLE        hMpHandle,
  _Out_ PMPVERSION_INFO pVersionInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hmphandle* \[ in\]
</dt> <dd>

Typ: **mphandle**

Handle für die Malware Protection Manager-Schnittstelle. Dieses Handle wird von der [**mpmanageropen**](mpmanageropen.md) -Funktion zurückgegeben.

</dd> <dt>

*pversioninfo* \[ vorgenommen\]
</dt> <dd>

Typ: **pmpversion \_ Info**

Zeiger auf eine-Struktur, die Versionsinformationen zu verschiedenen Komponenten des Malware Schutz-Managers enthält. Siehe [**mpversion \_ Info**](mpversion-info.md).

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

[**mpversion- \_ Informationen**](mpversion-info.md)
</dt> </dl>

 

 





