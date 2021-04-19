---
description: Generiert einen Satz von SSL-Sitzungs Schlüsseln (Secure Sockets Layer Protocol).
ms.assetid: 88465f30-8591-411e-8618-8a381d4c22e9
title: Sslgeneratesessionkeys-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateSessionKeys
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cf8e20008d2a77cae3a47728f4e38fff8ae0b09b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366337"
---
# <a name="sslgeneratesessionkeys-function"></a>Sslgeneratesessionkeys-Funktion

Die **sslgeneratesessionkeys** -Funktion generiert einen Satz von SSL-Sitzungs Schlüsseln ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslGenerateSessionKeys(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _Out_ NCRYPT_KEY_HANDLE  *phReadKey,
  _Out_ NCRYPT_KEY_HANDLE  *phWriteKey,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hsslprovider* \[ in\]
</dt> <dd>

Das Handle für die SSL-Protokoll Anbieter Instanz.

</dd> <dt>

*hmasterkey* \[ in\]
</dt> <dd>

Das Handle für das [*Hauptschlüssel*](/windows/desktop/SecGloss/m-gly) Objekt.

</dd> <dt>

*Phread Key* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf das zurückgegebene Lese Schlüssel handle.

</dd> <dt>

*phschreitekey* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf das zurückgegebene Schreib Schlüssel handle.

</dd> <dt>

*pparameterlist* \[ in\]
</dt> <dd>

Ein Zeiger auf ein Array von [**ncryptbuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) -Puffern, die Informationen enthalten, die als Teil des Schlüsselaustausch Vorgangs verwendet werden. Der genaue Satz Puffer ist abhängig vom verwendeten Protokoll und der Verschlüsselungs Sammlung. Die Liste enthält mindestens Puffer, die den vom Client und vom Server bereitgestellten Zufallswert enthalten.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. die folgenden:



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**Ernte \_ Kein Arbeits \_ Speicher**</dt> <dt>0x8009000el</dt> </dl>         | Es ist nicht genügend Arbeitsspeicher verfügbar, um erforderliche Puffer zuzuordnen.<br/> |
| <dl> <dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt> </dl>    | Eines der bereitgestellten Handles ist ungültig.<br/>                     |
| <dl> <dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt> </dl> | Der Parameter " *Phread Key* " oder " *phschreitekey* " ist NULL.<br/>            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

