---
description: Nicht implementiert und kann nicht verwendet werden.
ms.assetid: b41ba894-5cee-458d-935f-e89363925968
title: SslChangeNotify-Funktion (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslChangeNotify
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ff8bd1d23315894a3e858a536d10883f2fedcced792575157de824c02f3217ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907180"
---
# <a name="sslchangenotify-function"></a>SslChangeNotify-Funktion

Die **SslChangeNotify-Funktion** ist nicht implementiert und kann nicht verwendet werden.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslChangeNotify(
  _In_ HANDLE hEvent,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hEvent* \[ In\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **NTE NICHT \_ \_ UNTERSTÜTZT zurück.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

 




