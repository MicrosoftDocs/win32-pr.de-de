---
description: Wird verwendet, um Arbeitsspeicher freizugeben, der von einer der Funktionen des Secure Sockets Layer-Protokolls (SSL) zugewiesen wurde.
ms.assetid: 75a85013-c745-43cb-85b5-e13a2778ec1d
title: Sslfrebuffer-Funktion (sslprovider. h)
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
ms.openlocfilehash: bced83b52ddf37266f64ae0c2b8919902f30fff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050562"
---
# <a name="sslfreebuffer-function"></a>Sslfrebuffer-Funktion

Die **sslfreebuffer** -Funktion wird verwendet, um Arbeitsspeicher freizugeben, der von einer der Funktionen des [*Secure Sockets Layer-Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL) zugewiesen wurde.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslFreeBuffer(
  _In_ PVOID pvInput
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pvinput* \[ in\]
</dt> <dd>

Ein Zeiger auf den Speicherpuffer, der freigegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. die folgenden:



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt> </dl> | Der Parameter " *pdwprovidercount* " oder " *ppproviderlist* " ist **null**.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

