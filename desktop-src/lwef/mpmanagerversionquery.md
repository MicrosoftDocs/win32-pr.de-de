---
title: MpManagerVersionQuery-Funktion (MpClient.h)
description: Gibt Versionsinformationen zu verschiedenen Komponenten des Schadsoftwareschutz-Managers zurück.
ms.assetid: 47DE12BF-D7A4-468B-B0E7-79B5C27E56F5
keywords:
- Legacy-Windows-Umgebungsfeatures der MpManagerVersionQuery-Funktion
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
ms.openlocfilehash: b6407f36650b699f6bcdc9cbdd832ff2db38f68e9db758411d42aa5e81564ea4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114540"
---
# <a name="mpmanagerversionquery-function"></a>MpManagerVersionQuery-Funktion

Gibt Versionsinformationen zu verschiedenen Komponenten des Schadsoftwareschutz-Managers zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI MpManagerVersionQuery(
  _In_  MPHANDLE        hMpHandle,
  _Out_ PMPVERSION_INFO pVersionInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hMpHandle* \[ In\]
</dt> <dd>

Typ: **MPHANDLE**

Behandeln Sie die Schnittstelle des Schadsoftwareschutz-Managers. Dieses Handle wird von der [**MpManagerOpen-Funktion**](mpmanageropen.md) zurückgegeben.

</dd> <dt>

*pVersionInfo* \[ out\]
</dt> <dd>

Typ: **PMPVERSION \_ INFO**

Zeiger auf eine Struktur, die Versionsinformationen zu verschiedenen Komponenten des Schadsoftwareschutz-Managers enthält. Weitere Informationen finden Sie unter [**MPVERSION \_ INFO**](mpversion-info.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert **S \_ OK.**

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

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**MPVERSION \_ INFO**](mpversion-info.md)
</dt> </dl>

 

 





