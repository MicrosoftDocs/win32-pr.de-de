---
description: Öffnet ein Handle für den angegebenen SSL-Protokollanbieter (Secure Sockets Layer Protocol).
ms.assetid: 0d5c4da3-12d6-4a53-a4d0-f0f174a4c8d8
title: SslOpenProvider-Funktion (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenProvider
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 2bd24183fd96fd177e5ec958d84e7c4751af4226bb3d76de8bea2dba4b170b4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905639"
---
# <a name="sslopenprovider-function"></a>SslOpenProvider-Funktion

Die **SslOpenProvider-Funktion** öffnet ein Handle für den angegebenen SSL-Protokollanbieter [*(Secure Sockets Layer Protocol).*](/windows/desktop/SecGloss/s-gly)

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslOpenProvider(
  _Out_ NCRYPT_PROV_HANDLE *phSslProvider,
  _In_  LPCWSTR            pszProviderName,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*phSslProvider* \[ out\]
</dt> <dd>

Die Adresse eines **NCRYPT \_ \_ PROV-HANDLES,** in das das Anbieterhandle geschrieben werden soll.

Wenn Sie das Handle nicht mehr verwenden, sollten Sie es freigeben, indem Sie die [**SslFreeObject-Funktion**](sslfreeobject.md) aufrufen.

</dd> <dt>

*pszProviderName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine Unicode-Zeichenfolge, die den Anbieternamen enthält. Wenn der Wert dieses Parameters **NULL** ist, wird ein Handle für den **MS \_ SCHANNEL \_ PROVIDER** zurückgegeben.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert und muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. folgende.



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ UNGÜLTIGES \_ HANDLE**</dt> <dt>0x80090026L</dt> </dl>    | Einer der bereitgestellten Handles ist ungültig.<br/>                      |
| <dl> <dt>**NTE \_ INVALID \_ PARAMETER**</dt> <dt>0x80090027L</dt> </dl> | Der *parameter phSslProvider* oder *ppProviderList* ist **NULL.**<br/> |
| <dl> <dt>**STATUS \_ NO \_ MEMORY**</dt> <dt>0xC0000017L</dt> </dl>      | Es ist nicht genügend Arbeitsspeicher verfügbar, um die erforderlichen Puffer zuzuordnen.<br/>  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

