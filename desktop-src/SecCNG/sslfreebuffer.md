---
description: Wird verwendet, um Arbeitsspeicher freizugeben, der von einer der SSL-Anbieterfunktionen (Secure Sockets Layer Protocol) belegt wurde.
ms.assetid: 75a85013-c745-43cb-85b5-e13a2778ec1d
title: SslFreeBuffer-Funktion (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslFreeBuffer
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 6121802b8815a2e13fab0f4336420b763fe931a6e022fcce73080adfb01197c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906479"
---
# <a name="sslfreebuffer-function"></a>SslFreeBuffer-Funktion

Die **SslFreeBuffer-Funktion** wird verwendet, um Arbeitsspeicher freizugeben, der von einer der SSL-Anbieterfunktionen [*(Secure Sockets Layer Protocol)*](/windows/desktop/SecGloss/s-gly) belegt wurde.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslFreeBuffer(
  _In_ PVOID pvInput
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvInput* \[ In\]
</dt> <dd>

Ein Zeiger auf den freizugebenden Speicherpuffer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. folgende.



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ INVALID \_ PARAMETER**</dt> <dt>0x80090027L</dt> </dl> | Der *parameter pdwProviderCount* oder *ppProviderList* ist **NULL.**<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

