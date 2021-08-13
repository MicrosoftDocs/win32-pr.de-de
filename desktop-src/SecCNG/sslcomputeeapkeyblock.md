---
description: Berechnet den Schlüsselblock, der vom Extensible Authentication Protocol (EAP) verwendet wird.
ms.assetid: 0f382668-6fc6-440f-ba61-70b1db0f3987
title: SslComputeEapKeyBlock-Funktion (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeEapKeyBlock
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 48f657f565c239f797fd67b108ce3b18b692dfabc0248e1005465e9123ac492d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907171"
---
# <a name="sslcomputeeapkeyblock-function"></a>SslComputeEapKeyBlock-Funktion

Die **SslComputeEapKeyBlock-Funktion** berechnet den Schlüsselblock, der vom Extensible Authentication Protocol (EAP) verwendet wird.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslComputeEapKeyBlock(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hMasterKey,
  _In_      PBYTE              pbRandoms,
  _In_      DWORD              cbRandoms,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSslProvider* \[ In\]
</dt> <dd>

Das Handle der SSL-Protokollanbieterinstanz [*(Secure Sockets Layer Protocol).*](/windows/desktop/SecGloss/s-gly)

</dd> <dt>

*hMasterKey* \[ In\]
</dt> <dd>

Das Handle des [*Hauptschlüsselobjekts.*](/windows/desktop/SecGloss/m-gly)

</dd> <dt>

*pbRandoms* \[ In\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine Verkettung der zufälligen Client- \_ und \_ Serverzufallswerte der SSL-Sitzung enthält.

</dd> <dt>

*cbRandoms* \[ In\]
</dt> <dd>

Die Länge des *pbRandoms-Puffers* in Bytes.

</dd> <dt>

*pbOutput* \[ out, optional\]
</dt> <dd>

Die Adresse eines Puffers, der das Schlüsselblob empfängt. Der *cbOutput-Parameter* enthält die Größe dieses Puffers. Wenn dieser Parameter **NULL** ist, wird von dieser Funktion die erforderliche Größe in Bytes in das **DWORD-Objekt** gesetzt, auf das der *parameter "pwResult"* zeigt.

</dd> <dt>

*cbOutput* \[ In\]
</dt> <dd>

Die Länge des *pbOutput-Puffers* in Bytes.

</dd> <dt>

*resultsResult* \[ out\]
</dt> <dd>

Ein Zeiger auf einen **DWORD-Wert,** der die Länge des in den *pbOutput-Puffer* geschriebenen Hashs in Bytes angibt.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Legen Sie auf **NCRYPT \_ SSL \_ SERVER \_ FLAG** fest, um anzugeben, dass es sich um einen Serveraufruf handelt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.



| Rückgabecode/-wert                                                                                                                                                    | BESCHREIBUNG                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ UNGÜLTIGES \_ HANDLE**</dt> <dt>0x80090026L</dt> </dl> | Einer der angegebenen Handles ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

