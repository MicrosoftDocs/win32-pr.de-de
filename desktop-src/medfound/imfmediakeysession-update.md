---
description: Übergibt einen Schlüsselwert an alle zugeordneten Daten, die vom Content Decryption Module für das angegebene Schlüsselsystem benötigt werden.
ms.assetid: 29e66037-5f18-4724-b6f2-d85555e6af69
title: WFMediaKeySession::Update-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.Update
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 12c9877990ed9601ccf6b2911504b720088fa956dc76d6db9b97bac518db2d49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062979"
---
# <a name="imfmediakeysessionupdate-method"></a>WFMediaKeySession::Update-Methode

Übergibt einen Schlüsselwert an alle zugeordneten Daten, die vom Content Decryption Module für das angegebene Schlüsselsystem benötigt werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Update(
   const BYTE  *key,
         DWORD cb
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*key* 
</dt> <dd></dd> <dt>

*Cb* 
</dt> <dd>

Die Anzahl des *Schlüssels* in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WFMEDIAKeySession**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




