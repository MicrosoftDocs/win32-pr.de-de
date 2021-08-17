---
description: Generiert einen Satz von SSL-Sitzungsschlüsseln (Secure Sockets Layer Protocol).
ms.assetid: 88465f30-8591-411e-8618-8a381d4c22e9
title: SslGenerateSessionKeys-Funktion (Sslprovider.h)
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
ms.openlocfilehash: 3a9d7a25e5dd2035bd0b060ae11904e351489309b3a5e3c65c0e1582dce77500
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906172"
---
# <a name="sslgeneratesessionkeys-function"></a>SslGenerateSessionKeys-Funktion

Die **SslGenerateSessionKeys-Funktion** generiert einen Satz von SSL-Sitzungsschlüsseln [*(Secure Sockets Layer Protocol).*](/windows/desktop/SecGloss/s-gly)

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

*hSslProvider* \[ In\]
</dt> <dd>

Das Handle für die SSL-Protokollanbieterinstanz.

</dd> <dt>

*hMasterKey* \[ In\]
</dt> <dd>

Das Handle für das [*Hauptschlüsselobjekt.*](/windows/desktop/SecGloss/m-gly)

</dd> <dt>

*phReadKey* \[ out\]
</dt> <dd>

Ein Zeiger auf das zurückgegebene Leseschlüsselhandle.

</dd> <dt>

*phWriteKey* \[ out\]
</dt> <dd>

Ein Zeiger auf das zurückgegebene Schreibschlüsselhandle.

</dd> <dt>

*pParameterList* \[ In\]
</dt> <dd>

Ein Zeiger auf ein Array von [**NCryptBuffer-Puffern,**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) die Informationen enthalten, die als Teil des Schlüsselaustauschvorgangs verwendet werden. Der genaue Satz von Puffern hängt vom verwendeten Protokoll und der verwendeten Verschlüsselungssammlung ab. Die Liste enthält mindestens Puffer, die die vom Client und server bereitgestellten Zufallswerte enthalten.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. folgende.



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**NTE \_ NO \_ MEMORY**</dt> <dt>0x8009000EL</dt> </dl>         | Es ist nicht genügend Arbeitsspeicher verfügbar, um die erforderlichen Puffer zuzuordnen.<br/> |
| <dl> <dt>**NTE \_ UNGÜLTIGES \_ HANDLE**</dt> <dt>0x80090026L</dt> </dl>    | Einer der bereitgestellten Handles ist ungültig.<br/>                     |
| <dl> <dt>**NTE \_ INVALID \_ PARAMETER**</dt> <dt>0x80090027L</dt> </dl> | Der *parameter phReadKey* oder *phWriteKey* ist NULL.<br/>            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

