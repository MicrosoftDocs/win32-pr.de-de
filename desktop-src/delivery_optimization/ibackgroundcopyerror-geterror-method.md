---
title: Ibackgroundcopyerror GetError-Methode (deliveryoptimization. h)
description: Ruft den Fehlercode ab und identifiziert den Kontext, in dem der Fehler aufgetreten ist.
ms.assetid: C87897CD-9648-4CEF-B963-68EE35356929
keywords:
- GetError-Methode
- GetError-Methode, ibackgroundcopyerror-Schnittstelle
- Ibackgroundcopyerror-Schnittstelle, GetError-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e14803c225ade6085658582e18b9ba2d52fc90c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949787"
---
# <a name="ibackgroundcopyerrorgeterror-method"></a>Ibackgroundcopyerror:: GetError-Methode

Ruft den Fehlercode ab und identifiziert den Kontext, in dem der Fehler aufgetreten ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetError(
  [out] BG_ERROR_CONTEXT *pContext,
  [out] HRESULT          *pErrorCode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pContext* \[ vorgenommen\]
</dt> <dd>

Der Kontext, in dem der Fehler aufgetreten ist. Eine Liste der Kontext Werte finden Sie in der [**BG_ERROR_CONTEXT**](bg-error-context.md) -Enumeration.

</dd> <dt>

*perrorcode* \[ vorgenommen\]
</dt> <dd>

Der Fehlercode des Fehlers, der aufgetreten ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt **S_OK** bei Erfolg oder einen der standardmäßigen com HRESULT-Werte bei einem Fehler zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError ist als 19c613a0-fcb8-4f 28-81ae-897c3d078-Datei definiert.<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ibackgroundcopyerror**](ibackgroundcopyerror.md)
</dt> <dt>

[**Ibackgroundcopyerror:: GetFile**](ibackgroundcopyerror-getfile-method.md)
</dt> </dl>

 

 





