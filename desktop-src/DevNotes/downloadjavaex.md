---
description: Lädt die CAB-Datei Signatur herunter, überprüft die den Paketen zugeordneten Berechtigungen und führt Sie basierend auf der Authentifizierung aus.
ms.assetid: b86a8f39-73a1-4e17-ac83-9ed095de4922
title: Downloadjavaex-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownloadJavaEX
api_type:
- DllExport
api_location:
- Javacypt.dll
ms.openlocfilehash: 31371e91599d604db591ee3e921b42bc809aae21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370137"
---
# <a name="downloadjavaex-function"></a>Downloadjavaex-Funktion

Lädt die CAB-Datei Signatur herunter, überprüft die den Paketen zugeordneten Berechtigungen und führt Sie basierend auf der Authentifizierung aus.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI DownloadJavaEX(
  _In_ PALLOCATOR               Reserved,
  _In_ PCRYPT_PROVIDER_DATA     pProviderData,
  _In_ PJAVA_POLICY_PROVIDER    pJava,
  _In_ CRYPT_PROVIDER_FUNCTIONS *pFunctions,
  _In_ BOOL                     fCertificate,
  _In_ PJAVA_TRUST              pTrust
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Reserviert* \[ in\]
</dt> <dd>

Dieser Parameter ist reserviert.

</dd> <dt>

*pproviderdata* \[ in\]
</dt> <dd>

Eine [**\_ \_ Daten**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) Struktur des Crypt-Anbieters, die Zertifikat Daten wie z. b. Datei-und Zonen Berechtigungen enthält.

</dd> <dt>

*pjava* \[ in\]
</dt> <dd>

Eine [**Java- \_ Richtlinien \_ Anbieter**](/previous-versions//bb432350(v=vs.85)) Struktur, die Daten enthält, die sich auf den Richtlinien Anbieter beziehen.

</dd> <dt>

*pFunctions* \[ in\]
</dt> <dd>

Eine [**crypt- \_ Anbieter \_ Funktions**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions) Struktur, die eine Liste von Methoden zum Überprüfen von Zertifikat Objekten, Signaturen und abschließenden Richtlinien enthält.

</dd> <dt>

*Zertifikat* \[ in\]
</dt> <dd>

Wenn ein Zertifikat vorhanden ist, ist dieser Parameter **true**. Andernfalls ist Sie **false**.

</dd> <dt>

*ptrust* \[ in\]
</dt> <dd>

Eine [**Java- \_ Vertrauensstellungs**](/windows/desktop/api/Capi/ns-capi-java_trust) Struktur, die Vertrauensstellungs Informationen enthält, wie z. b. codierte Berechtigung, Codierungs Signatur und authentixes

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**. Andernfalls ist der Rückgabewert ein Fehlercode.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Javacypt.dll</dt> </dl> |



 

 
