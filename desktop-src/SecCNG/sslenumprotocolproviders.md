---
description: Gibt ein Array installierter SSL-Protokoll Anbieter (Secure Sockets Layer Protocol) zurück.
ms.assetid: a61ddcf5-b7e3-40b2-82fc-1cf87eb963ec
title: Sslenenprotocolproviders-Funktion (sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumProtocolProviders
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 94c8648950af20a97bcc34b614aee0d0f716b043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218505"
---
# <a name="sslenumprotocolproviders-function"></a>Sslenenprotocolproviders-Funktion

Die **sslenenprotocolproviders** -Funktion gibt ein Array installierter SSL-Protokoll Anbieter ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ) zurück.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS WINAPI SslEnumProtocolProviders(
  _Out_ DWORD              *pdwProviderCount,
  _Out_ NCryptProviderName **ppProviderList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdwprovidercount* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen **DWORD** -Wert, der die Anzahl der zurückgegebenen Protokoll Anbieter empfängt.

</dd> <dt>

*ppproviderlist* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der das Array von [**ncryptprovidername**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) -Strukturen empfängt.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt Sie 0 (null) zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlerwert ungleich 0 (null) zurückgegeben.

Mögliche Rückgabecodes sind u. a. die folgenden:



| Rückgabecode/-wert                                                                                                                                                       | BESCHREIBUNG                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**Ernte \_ Ungültige \_ Flags**</dt> <dt>0x80090009l</dt> </dl>         | Der *dwFlags* -Parameter ist nicht 0 (null).<br/>                              |
| <dl> <dt>**Ernte \_ Kein Arbeits \_ Speicher**</dt> <dt>0x8009000el</dt> </dl>         | Es ist nicht genügend Arbeitsspeicher verfügbar, um erforderliche Puffer zuzuordnen.<br/>     |
| <dl> <dt>**Ernte \_ Ungültiger \_ Parameter**</dt> <dt>0x80090027l</dt> </dl> | Der Parameter " *pdwprovidercount* " oder " *ppproviderlist* " ist **null**.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie die Verwendung des Arrays von [**ncryptprovidername**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncryptprovidername) -Strukturen abgeschlossen haben, können Sie die [**sslfreebuffer**](sslfreebuffer.md) -Funktion aufrufen, um das Array freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

