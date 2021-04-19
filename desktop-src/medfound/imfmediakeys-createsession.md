---
description: Erstellt mithilfe der angegebenen Initialisierungs Daten und benutzerdefinierten Daten ein Medien Schlüssel-Sitzungs Objekt. .
ms.assetid: 9f11433c-7cff-4a59-9d4a-7f4b56ba62cf
title: 'IMF Media Keys:: foratesession-Methode'
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
ms.openlocfilehash: 89d3abce0c1c15d472f7008fa0ef2c5f27bba6ad
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106366372"
---
# <a name="imfmediakeyscreatesession-method"></a>IMF Media Keys:: foratesession-Methode

Erstellt mithilfe der angegebenen Initialisierungs Daten und benutzerdefinierten Daten ein Medien Schlüssel-Sitzungs Objekt. .

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

Der MIME-Typ des Medien Containers, der für den Inhalt verwendet wird.

</dd> <dt>

*initData* 
</dt> <dd>

Die Initialisierungs Daten für das Schlüsselsystem.

</dd> <dt>

*betrieben* 
</dt> <dd>

Die Anzahl in Bytes von *initdata*.

</dd> <dt>

*CustomData* 
</dt> <dd>

Benutzerdefinierte Daten, die an das Schlüsselsystem gesendet werden.

</dd> <dt>

*cbcustomdata* 
</dt> <dd>

Die Anzahl in Bytes von *cbcustomdata*.

</dd> <dt>

*informiert* 
</dt> <dd>

informiert

</dd> <dt>

*ppSession* 
</dt> <dd>

Die Medien schlüsselsitzung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>MF mediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMF Media Keys**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




