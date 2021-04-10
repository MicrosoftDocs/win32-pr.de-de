---
description: Öffnet ein Handle für den angegebenen SSL-Protokoll Anbieter (Secure Sockets Layer Protocol).
ms.assetid: 0d5c4da3-12d6-4a53-a4d0-f0f174a4c8d8
title: Sslopenprovider-Funktion (sslprovider. h)
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
ms.openlocfilehash: 8a9ea6c97662d94fffef0c87a227d5e2ae052606
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214517"
---
# <a name="sslopenprovider-function"></a>Sslopenprovider-Funktion

Die **sslopenprovider** -Funktion öffnet ein Handle für den angegebenen SSL-Protokoll Anbieter ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).

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

*phsslprovider* \[ vorgenommen\]
</dt> <dd>

Die Adresse eines **NCrypt- \_ Prov- \_ Handles** , in dem das Anbieter handle geschrieben werden soll.

Wenn Sie die Verwendung des Handles abgeschlossen haben, sollten Sie es freigeben, indem Sie die [**sslfreeobject**](sslfreeobject.md) -Funktion aufrufen.

</dd> <dt>

*pszprovidername* \[ in\]
</dt> <dd>

Ein Zeiger auf eine Unicode-Zeichenfolge, die den Anbieter Namen enthält. Wenn der Wert dieses Parameters **null** ist, wird ein Handle für den **MS \_ SChannel- \_ Anbieter** zurückgegeben.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert und muss auf 0 (null) festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. die folgenden:



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt> </dl>    | Eines der bereitgestellten Handles ist ungültig.<br/>                      |
| <dl> <dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt> </dl> | Der Parameter " *phsslprovider* " oder " *ppproviderlist* " ist **null**.<br/> |
| <dl> <dt>**Status \_ Kein Arbeits \_ Speicher**</dt> <dt>0xc0000017l</dt> </dl>      | Es ist nicht genügend Arbeitsspeicher verfügbar, um erforderliche Puffer zuzuordnen.<br/>  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

