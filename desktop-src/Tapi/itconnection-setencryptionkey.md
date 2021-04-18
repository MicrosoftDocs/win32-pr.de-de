---
description: Die SetEncryptionKey-Methode legt den Verschlüsselungsschlüssel fest, der zum Entschlüsseln der Sitzung erforderlich ist, oder einen Indikator für einen Mechanismus, um einen verwendbaren Schlüssel auf externe Weise zu erhalten.
ms.assetid: 9efcf90e-3645-49f4-b27d-9a8246637310
title: 'Itconnection:: btencryptionkey-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91d0ce079d3815897c348e553df0af8dece8592b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357614"
---
# <a name="itconnectionsetencryptionkey-method"></a>Itconnection:: abtencryptionkey-Methode

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **SetEncryptionKey** -Methode legt den Verschlüsselungsschlüssel fest, der zum Entschlüsseln der Sitzung erforderlich ist, oder einen Indikator für einen Mechanismus, um einen verwendbaren Schlüssel auf externe Weise zu erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetEncryptionKey(
  [in] BSTR pKeyType,
  [in] BSTR *ppKeyData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pkeytype* \[ in\]
</dt> <dd>

Zeiger auf ein **BSTR** , das den Verschlüsselungs Schlüsseltyp enthält.

</dd> <dt>

*ppkeydata* \[ in\]
</dt> <dd>

Zeiger auf ein **BSTR** , das Informationen zum Verschlüsselungsschlüssel enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                          | Beschreibung                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Methode war erfolgreich.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die Anwendung muss " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Arbeitsspeicher für die Parameter " *pkeytype* " und " *ppkeydata* " zuzuweisen. Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den Arbeitsspeicher freizugeben, wenn die Variablen nicht mehr benötigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itconnection**](itconnection.md)
</dt> </dl>

 

