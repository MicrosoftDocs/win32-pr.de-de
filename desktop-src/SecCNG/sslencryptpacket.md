---
description: Verschlüsselt ein einzelnes Secure Sockets Layer-Protokollpaket (SSL).
ms.assetid: 1002158b-1a4f-4461-978f-b221ef6332e0
title: SslEncryptPacket-Funktion (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEncryptPacket
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 74c489cae777b6ca7ac93020fb80ab198622fae97640c09cbd99544c2dafa4e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906662"
---
# <a name="sslencryptpacket-function"></a>SslEncryptPacket-Funktion

Die **SslEncryptPacket-Funktion** verschlüsselt ein einzelnes [*Secure Sockets Layer-Protokollpaket*](/windows/desktop/SecGloss/s-gly) (SSL).

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslEncryptPacket(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_KEY_HANDLE  hKey,
  _In_    PBYTE              *pbInput,
  _In_    DWORD              cbInput,
  _Out_   PBYTE              pbOutput,
  _In_    DWORD              cbOutput,
  _Out_   DWORD              *pcbResult,
  _In_    ULONGLONG          SequenceNumber,
  _In_    DWORD              dwContentType,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hSslProvider* \[ In\]
</dt> <dd>

Das Handle der SSL-Protokollanbieterinstanz.

</dd> <dt>

*hKey* \[ in, out\]
</dt> <dd>

Das Handle für den Schlüssel, der zum Verschlüsseln des Pakets verwendet wird.

</dd> <dt>

*pbInput* \[ In\]
</dt> <dd>

Ein Zeiger auf den Puffer, der das zu verschlüsselnde Paket enthält.

</dd> <dt>

*cbInput* \[ In\]
</dt> <dd>

Die Länge des *pbInput-Puffers in* Bytes.

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Puffer, um das verschlüsselte Paket zu empfangen.

</dd> <dt>

*cbOutput* \[ In\]
</dt> <dd>

Die Länge (Bytes) des *pbOutput-Puffers.*

</dd> <dt>

*beimResult* \[ out\]
</dt> <dd>

Die Anzahl von Bytes, die in den *pbOutput-Puffer geschrieben* werden.

</dd> <dt>

*SequenceNumber* \[ In\]
</dt> <dd>

Die Sequenznummer, die diesem Paket entspricht.

</dd> <dt>

*dwContentType* \[ In\]
</dt> <dd>

Der Inhaltstyp, der diesem Paket entspricht, der das Protokoll auf höherer Ebene angibt, das zum Verarbeiten des eingeschlossenen Pakets verwendet wird.



| Wert                                                                                                                                                                                                                                           | Bedeutung                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="CT_CHANGE_CIPHER_SPEC"></span><span id="ct_change_cipher_spec"></span><dl> <dt>**CT \_ ÄNDERN \_ DER \_ VERSCHLÜSSELUNGSSPEZIFIKATION**</dt> <dt>20</dt> </dl> | Gibt eine Änderung in der Verschlüsselungsstrategie an.<br/>                         |
| <span id="CT_ALERT"></span><span id="ct_alert"></span><dl> <dt>**CT \_ WARNUNG**</dt> <dt>21</dt> </dl>                                          | Gibt an, dass das eingeschlossene Paket eine Warnung enthält.<br/>                 |
| <span id="CT_HANDSHAKE"></span><span id="ct_handshake"></span><dl> <dt>**CT \_ HANDSHAKE**</dt> <dt>22</dt> </dl>                              | Gibt an, dass das eingeschlossene Paket Teil des Handshakeprotokolls ist.<br/> |
| <span id="CT_APPLICATIONDATA"></span><span id="ct_applicationdata"></span><dl> <dt>**CT \_ APPLICATIONDATA**</dt> <dt>23</dt> </dl>            | Gibt an, dass das Paket Anwendungsdaten enthält.<br/>                  |



 

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, gibt sie einen Fehlerwert ungleich 0 (null) zurück.

Mögliche Rückgabecodes sind u. a. folgende:



| Rückgabecode/-wert                                                                                                                                                    | BESCHREIBUNG                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ UNGÜLTIGES \_ HANDLE**</dt> <dt>0x80090026L</dt> </dl> | Eines der bereitgestellten Handles ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

