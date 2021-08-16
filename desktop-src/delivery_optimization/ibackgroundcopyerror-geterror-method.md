---
title: IBackgroundCopyError GetError-Methode (Deliveryoptimization.h)
description: Ruft den Fehlercode ab und identifiziert den Kontext, in dem der Fehler aufgetreten ist.
ms.assetid: C87897CD-9648-4CEF-B963-68EE35356929
keywords:
- GetError-Methode
- GetError-Methode, IBackgroundCopyError-Schnittstelle
- IBackgroundCopyError-Schnittstelle, GetError-Methode
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
ms.openlocfilehash: d147bc877f9694617ec94651f53f4cf438c00de8d752710c3659f24ba4ffe21c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118810326"
---
# <a name="ibackgroundcopyerrorgeterror-method"></a>IBackgroundCopyError::GetError-Methode

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

*pContext* \[ out\]
</dt> <dd>

Kontext, in dem der Fehler aufgetreten ist. Eine Liste der Kontextwerte finden Sie in [**der**](bg-error-context.md) BG_ERROR_CONTEXT Enumeration.

</dd> <dt>

*pErrorCode* \[ out\]
</dt> <dd>

Fehlercode des aufgetretenen Fehlers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt **S_OK** bei Erfolg oder einen der STANDARDMÄßIGEN COM HRESULT-Werte bei einem Fehler zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur Desktop-Apps der Version 1709) \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError ist als 19C613A0-FCB8-4F28-81AE-897C3D078F81 definiert.<br/>             |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyError::GetFile**](ibackgroundcopyerror-getfile-method.md)
</dt> </dl>

 

 





