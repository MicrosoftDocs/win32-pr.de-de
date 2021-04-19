---
description: Berechnet den Schlüssel Block, der vom EAP (Extensible Authentication Protocol) verwendet wird.
ms.assetid: 0f382668-6fc6-440f-ba61-70b1db0f3987
title: Sslcomputeeapkeyblock-Funktion (sslprovider. h)
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
ms.openlocfilehash: d46c1284b208975126067ff295507b51def9133b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367877"
---
# <a name="sslcomputeeapkeyblock-function"></a>Sslcomputeeapkeyblock-Funktion

Die **sslcomputeeapkeyblock** -Funktion berechnet den Schlüssel Block, der vom Extensible Authentication Protocol (EAP) verwendet wird.

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

*hsslprovider* \[ in\]
</dt> <dd>

Das Handle der Protokoll Anbieter Instanz des [*Secure Sockets Layer Protokolls*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*hmasterkey* \[ in\]
</dt> <dd>

Das Handle des [*Hauptschlüssel*](/windows/desktop/SecGloss/m-gly) Objekts.

</dd> <dt>

*pbrandoms* \[ in\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine Verkettung der zufälligen Zufallswerte des Clients \_ und \_ des Servers der SSL-Sitzung enthält.

</dd> <dt>

*cbrandoms* \[ in\]
</dt> <dd>

Die Länge des *pbrandoms* -Puffers in Bytes.

</dd> <dt>

*pboutput* \[ Out, optional\]
</dt> <dd>

Die Adresse eines Puffers, der das Schlüsselblob empfängt. Der *cboutput* -Parameter enthält die Größe dieses Puffers. Wenn dieser Parameter **null** ist, fügt diese Funktion die erforderliche Größe (in Bytes) in das **DWORD** ein, auf das durch den *pcbresult* -Parameter verwiesen wird.

</dd> <dt>

*cboutput* \[ in\]
</dt> <dd>

Die Länge des *pboutput* -Puffers in Bytes.

</dd> <dt>

*pcbresult* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen **DWORD** -Wert, der die Länge des in den *pboutput* -Puffer geschriebenen Hashs in Bytes angibt.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Legen Sie auf **NCrypt \_ SSL \_ Server \_ Flag** fest, um anzugeben, dass es sich um einen Server-Befehl handelt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.



| Rückgabecode/-wert                                                                                                                                                    | BESCHREIBUNG                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt> </dl> | Eines der angegebenen Handles ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

