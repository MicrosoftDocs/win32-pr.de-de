---
description: Gibt ein Array von installierten SSL-Protokollanbietern (Secure Sockets Layer Protocol) zurück.
ms.assetid: a61ddcf5-b7e3-40b2-82fc-1cf87eb963ec
title: SslEnumProtocolProviders-Funktion (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumProtocolProviders
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: c0e20bd98f8f3e76d4185cf2a3aa52985d73f66ff1ea61ed50bf67552330290d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906682"
---
# <a name="sslenumprotocolproviders-function"></a>SslEnumProtocolProviders-Funktion

Die **SslEnumProtocolProviders-Funktion** gibt ein Array von installierten [*SSL-Protokollanbietern (Secure Sockets Layer Protocol)*](/windows/desktop/SecGloss/s-gly) zurück.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslEnumProtocolProviders(
  _Out_ DWORD              *pdwProviderCount,
  _Out_ NCryptProviderName **ppProviderList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdwProviderCount* \[ out\]
</dt> <dd>

Ein Zeiger auf einen **DWORD-Wert,** um die Anzahl der zurückgegebenen Protokollanbieter zu empfangen.

</dd> <dt>

*ppProviderList* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der das Array von [**NCryptProviderName-Strukturen**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) empfängt.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. folgende.



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ BAD \_ FLAGS**</dt> <dt>0x80090009L</dt> </dl>         | Der *dwFlags-Parameter* ist nicht 0 (null).<br/>                              |
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Es ist nicht genügend Arbeitsspeicher verfügbar, um die erforderlichen Puffer zuzuordnen.<br/>     |
| <dl> <dt>**NTE \_ INVALID \_ PARAMETER**</dt> <dt>0x80090027L</dt> </dl> | Der *parameter pdwProviderCount* oder *ppProviderList* ist **NULL.**<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn Sie das Array der [**NCryptProviderName-Strukturen**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) verwendet haben, rufen Sie die [**SslFreeBuffer-Funktion**](sslfreebuffer.md) auf, um das Array frei zu machen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

