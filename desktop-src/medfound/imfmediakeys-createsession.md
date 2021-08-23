---
description: Erstellt ein Medienschlüsselsitzungsobjekt unter Verwendung der angegebenen Initialisierungsdaten und benutzerdefinierten Daten. .
ms.assetid: 9f11433c-7cff-4a59-9d4a-7f4b56ba62cf
title: WFMediaKeys::CreateSession-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.CreateSession
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 2dd9bcc7a1151b042d275917e8bd8106eb079de3315137ca41fa7faecaf5c957
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942040"
---
# <a name="imfmediakeyscreatesession-method"></a>WFMediaKeys::CreateSession-Methode

Erstellt ein Medienschlüsselsitzungsobjekt unter Verwendung der angegebenen Initialisierungsdaten und benutzerdefinierten Daten. .

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateSession(
         BSTR                     mimeType,
   const BYTE                     *initData,
         DWORD                    cb,
   const BYTE                     *customData,
         DWORD                    cbCustomData,
         IMFMediaKeySessionNotify *notify,
         IMFMediaKeySession       **ppSession
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mimeType* 
</dt> <dd>

Der MIME-Typ des Mediencontainers, der für den Inhalt verwendet wird.

</dd> <dt>

*initData* 
</dt> <dd>

Die Initialisierungsdaten für das Schlüsselsystem.

</dd> <dt>

*Cb* 
</dt> <dd>

Die Anzahl von *initData in* Bytes.

</dd> <dt>

*Customdata* 
</dt> <dd>

Benutzerdefinierte Daten, die an das Schlüsselsystem gesendet werden.

</dd> <dt>

*cbCustomData* 
</dt> <dd>

Die Anzahl von *cbCustomData* in Bytes.

</dd> <dt>

*Benachrichtigen* 
</dt> <dd>

Benachrichtigen

</dd> <dt>

*ppSession* 
</dt> <dd>

Die Medienschlüsselsitzung.

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

[**WFMediaKeys**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




