---
description: Verschlüsselt ein einzelnes Secure Sockets Layer Protocol (SSL)-Paket.
ms.assetid: 1002158b-1a4f-4461-978f-b221ef6332e0
title: Sslencryptpacket-Funktion (sslprovider. h)
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
ms.openlocfilehash: e839b37e839fd09d5df5f9902474b7ce7c4c74a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354000"
---
# <a name="sslencryptpacket-function"></a>Sslencryptpacket-Funktion

Die **sslencryptpacket** -Funktion verschlüsselt ein einzelnes [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) (SSL)-Paket.

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

*hsslprovider* \[ in\]
</dt> <dd>

Das Handle der SSL-Protokoll Anbieter Instanz.

</dd> <dt>

*HKEY* \[ in, out\]
</dt> <dd>

Das Handle für den Schlüssel, der zum Verschlüsseln des Pakets verwendet wird.

</dd> <dt>

*pbinput* \[ in\]
</dt> <dd>

Ein Zeiger auf den Puffer, der das Paket enthält, das verschlüsselt werden soll.

</dd> <dt>

*cbinput* \[ in\]
</dt> <dd>

Die Länge des *pbinput* -Puffers in Bytes.

</dd> <dt>

*pboutput* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, um das verschlüsselte Paket zu empfangen.

</dd> <dt>

*cboutput* \[ in\]
</dt> <dd>

Die Länge (Bytes) des *pboutput* -Puffers.

</dd> <dt>

*pcbresult* \[ vorgenommen\]
</dt> <dd>

Die Anzahl der in den *pboutput* -Puffer geschriebenen Bytes.

</dd> <dt>

*Sequencennummer* \[ in\]
</dt> <dd>

Die Sequenznummer, die diesem Paket entspricht.

</dd> <dt>

*dwcontenttype* \[ in\]
</dt> <dd>

Der Inhaltstyp, der diesem Paket entspricht, das das Protokoll der höheren Ebene angibt, das zum Verarbeiten des eingeschlossenen Pakets verwendet wird.



| Wert                                                                                                                                                                                                                                           | Bedeutung                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="CT_CHANGE_CIPHER_SPEC"></span><span id="ct_change_cipher_spec"></span><dl> <dt>**CT \_ \_Chiffre \_ Spezifikation ändern**</dt> <dt>20</dt> </dl> | Gibt eine Änderung in der Verschlüsselungs Strategie an.<br/>                         |
| <span id="CT_ALERT"></span><span id="ct_alert"></span><dl> <dt>**CT \_ Warnung**</dt> <dt>21</dt> </dl>                                          | Gibt an, dass das eingeschlossene Paket eine Warnung enthält.<br/>                 |
| <span id="CT_HANDSHAKE"></span><span id="ct_handshake"></span><dl> <dt>**CT \_ HANDSHAKE**</dt> <dt>22</dt> </dl>                              | Gibt an, dass das eingeschlossene Paket Teil des Handshake-Protokolls ist.<br/> |
| <span id="CT_APPLICATIONDATA"></span><span id="ct_applicationdata"></span><dl> <dt>**CT \_ ApplicationData**</dt> <dt>23</dt> </dl>            | Gibt an, dass das Paket Anwendungsdaten enthält.<br/>                  |



 

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. die folgenden:



| Rückgabecode/-wert                                                                                                                                                    | BESCHREIBUNG                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt> </dl> | Eines der bereitgestellten Handles ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

