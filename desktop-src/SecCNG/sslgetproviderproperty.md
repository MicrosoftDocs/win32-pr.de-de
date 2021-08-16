---
description: Ruft den Wert einer angegebenen Anbietereigenschaft ab.
ms.assetid: 69235520-acaa-4ec4-9fd6-4b3297e14376
title: SslGetProviderProperty-Funktion (Sslprovider.h)
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
ms.openlocfilehash: bfe65fe4033397fd5885eceb3bf0d2ac9ce9aa9b487a84ab7611cb253d979220
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906108"
---
# <a name="sslgetproviderproperty-function"></a>SslGetProviderProperty-Funktion

Die **SslGetProviderProperty-Funktion** ruft den Wert einer angegebenen Anbietereigenschaft ab.

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

*hSslProvider* \[ In\]
</dt> <dd>

Das Handle des SSL-Anbieters [*(Secure Sockets Layer Protocol),*](/windows/desktop/SecGloss/s-gly) für den die Eigenschaft abgerufen werden soll.

</dd> <dt>

*pszProperty* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Unicode-Zeichenfolge, die den Namen der abzurufenden Eigenschaft enthält.

</dd> <dt>

*ppbOutput* \[ out\]
</dt> <dd>

Die Adresse eines Puffers, der den Eigenschaftswert empfängt.

Der Aufrufer der Funktion muss diesen Puffer freigeben, indem er die [**SslFreeBuffer-Funktion**](sslfreebuffer.md) aufruft.

</dd> <dt>

*pwOutput* \[ out\]
</dt> <dd>

Die Größe des *pbOutput-Puffers* in Bytes.

</dd> <dt>

*ppEnumState* \[ in, out\]
</dt> <dd>

Die Adresse eines **VOID-Zeigers,** der Enumerationszustandsinformationen empfängt, die in nachfolgenden Aufrufen dieser Funktion verwendet werden. Diese Informationen haben nur eine Bedeutung für den SSL-Anbieter und sind für den Aufrufer nicht transparent. Der SSL-Anbieter verwendet diese Informationen, um zu bestimmen, welches Element als Nächstes in der Enumeration enthalten ist. Wenn die Variable, auf die dieser Parameter zeigt, **NULL** enthält, wird die Enumeration von Anfang an gestartet.

Der Aufrufer der Funktion muss diesen Arbeitsspeicher freigeben, indem er die [**SslFreeBuffer-Funktion**](sslfreebuffer.md) aufruft.

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
| <dl> <dt>**NTE \_ UNGÜLTIGES \_ HANDLE**</dt> <dt>0x80090026L</dt> </dl>    | Das *hSslProvider-Handle* ist ungültig.<br/>                       |
| <dl> <dt>**NTE \_ INVALID \_ PARAMETER**</dt> <dt>0x80090027L</dt> </dl> | Einer der angegebenen Parameter ist ungültig.<br/>                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

