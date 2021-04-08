---
description: Ruft den Wert einer angegebenen Anbieter Eigenschaft ab.
ms.assetid: 69235520-acaa-4ec4-9fd6-4b3297e14376
title: Sslgetproviderproperty-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetProviderProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ced0f32d45531a1220f7aae9fe0e660648e5d1bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867667"
---
# <a name="sslgetproviderproperty-function"></a>Sslgetproviderproperty-Funktion

Die **sslgetproviderproperty** -Funktion Ruft den Wert einer angegebenen Anbieter Eigenschaft ab.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslGetProviderProperty(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _In_    LPCWSTR            pszProperty,
  _Out_   PBYTE              ppbOutput,
  _Out_   DWORD              *pcbOutput,
  _Inout_ PVOID              *ppEnumState,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hsslprovider* \[ in\]
</dt> <dd>

Das Handle des SSL-Anbieters ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ), für den die Eigenschaft abgerufen werden soll.

</dd> <dt>

*pszproperty* \[ in\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den Namen der abzurufenden Eigenschaft enthält.

</dd> <dt>

*ppboutput* \[ vorgenommen\]
</dt> <dd>

Die Adresse eines Puffers, der den Eigenschafts Wert empfängt.

Der Aufrufer der Funktion muss diesen Puffer durch Aufrufen der [**sslfreebuffer**](sslfreebuffer.md) -Funktion freigeben.

</dd> <dt>

*pcboutput* \[ vorgenommen\]
</dt> <dd>

Die Größe des *pboutput* -Puffers in Bytes.

</dd> <dt>

" *ppumschlag State* \[ " in, out\]
</dt> <dd>

Die Adresse eines **void** -Zeigers, der enumerationsstatusinformationen empfängt, die in nachfolgenden Aufrufen dieser Funktion verwendet werden. Diese Informationen sind nur für den SSL-Anbieter von Bedeutung und für den Aufrufer nicht transparent. Der SSL-Anbieter verwendet diese Informationen, um zu bestimmen, welches Element als nächstes in der-Enumeration verwendet wird. Wenn die Variable, auf die dieser Parameter verweist, **null** enthält, wird die Enumeration von Anfang an gestartet.

Der Aufrufer der Funktion muss diesen Arbeitsspeicher freigeben, indem er die [**sslfreebuffer**](sslfreebuffer.md) -Funktion aufruft.

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
| <dl> <dt>**Ernte \_ Ungültiges \_ handle**</dt> <dt>0x80090026l</dt> </dl>    | Das *hsslprovider* -Handle ist ungültig.<br/>                       |
| <dl> <dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt> </dl> | Einer der angegebenen Parameter ist ungültig.<br/>                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

