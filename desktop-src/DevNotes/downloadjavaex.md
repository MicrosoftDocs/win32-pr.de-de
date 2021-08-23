---
description: Lädt .cab Dateisignatur herunter, überprüft die den Paketen zugeordneten Berechtigungen und führt sie basierend auf der Authentifizierung aus.
ms.assetid: b86a8f39-73a1-4e17-ac83-9ed095de4922
title: DownloadJavaEX-Funktion
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
ms.openlocfilehash: 628fdb1b8b0ec9979d844c8f48fb02fbf8f6a642a96c925f427c868160dd6b27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795260"
---
# <a name="downloadjavaex-function"></a>DownloadJavaEX-Funktion

Lädt .cab Dateisignatur herunter, überprüft die den Paketen zugeordneten Berechtigungen und führt sie basierend auf der Authentifizierung aus.

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

*Reserviert* \[ In\]
</dt> <dd>

Dieser Parameter ist reserviert.

</dd> <dt>

*pProviderData* \[ In\]
</dt> <dd>

Eine [**CRYPT \_ PROVIDER \_ DATA-Struktur,**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) die Zertifikatdaten wie Datei- und Zonenberechtigungen enthält.

</dd> <dt>

*pJava* \[ In\]
</dt> <dd>

Eine [**JAVA \_ POLICY \_ PROVIDER-Struktur,**](/previous-versions//bb432350(v=vs.85)) die Daten im Zusammenhang mit dem Richtlinienanbieter enthält.

</dd> <dt>

*pFunctions* \[ In\]
</dt> <dd>

Eine [**CRYPT \_ PROVIDER \_ FUNCTIONS-Struktur,**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions) die eine Liste von Methoden zum Überprüfen von Zertifikatobjekten, Signaturen und endgültigen Richtlinien enthält.

</dd> <dt>

*fCertificate* \[ In\]
</dt> <dd>

Wenn ein Zertifikat vorhanden ist, ist dieser Parameter **TRUE.** Andernfalls ist dies **FALSE.**

</dd> <dt>

*pTrust* \[ In\]
</dt> <dd>

Eine [**JAVA \_ TRUST-Struktur,**](/windows/desktop/api/Capi/ns-capi-java_trust) die Vertrauensinformationen wie codierte Berechtigung, Encodersignatur und authentic-Rückgaberichtliniencode enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert **S \_ OK.** Andernfalls ist der Rückgabewert ein Fehlercode.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Javacypt.dll</dt> </dl> |



 

 
