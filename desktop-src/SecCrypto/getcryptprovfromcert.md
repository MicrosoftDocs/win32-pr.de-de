---
description: Ruft ein Handle für einen Kryptografiedienstanbieter (Cryptographic Service Provider, CSP) und eine Schlüsselspezifikation für einen Zertifikatkontext ab.
ms.assetid: ff72231f-e10f-49d2-b0e0-0008923803cc
title: GetCryptProvFromCert-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: c885c439014a26bafba3be8614981c67d200e9f87cd4e3c4f03e8cbcc1b77e38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006658"
---
# <a name="getcryptprovfromcert-function"></a>GetCryptProvFromCert-Funktion

> [!IMPORTANT]
> Diese API ist veraltet. Microsoft kann diese API in zukünftigen Versionen entfernen.

 

Die **GetCryptProvFromCert-Funktion** ruft ein Handle für einen [*Kryptografiedienstanbieter (Cryptographic Service Provider,*](../secgloss/c-gly.md) CSP) und eine Schlüsselspezifikation für einen [*Zertifikatkontext*](../secgloss/c-gly.md) ab. Verwenden Sie diese Funktion, um Zugriff auf den [*privaten Schlüssel*](../secgloss/p-gly.md) des Zertifikatausstellers zu erhalten.

> [!Note]  
> Dieser Funktion ist keine Headerdatei oder Importbibliothek zugeordnet. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Headerdatei erstellen und die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um dynamisch eine Verknüpfung mit Mssign32.dll herzustellen.

 

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI GetCryptProvFromCert(
  _In_      HWND           hwnd,
  _In_      PCCERT_CONTEXT pCert,
  _Out_     HCRYPTPROV     *phCryptProv,
  _Out_     DWORD          *pdwKeySpec,
  _In_      BOOL           *pfDidCryptAcquire,
  _Out_opt_ LPWSTR         *ppwszTmpContainer,
  _Out_opt_ LPWSTR         *ppwszProviderName,
  _Out_     DWORD          *pdwProviderType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwnd* \[ In\]
</dt> <dd>

Das Handle des Fensters, das als Besitzer aller angezeigten Dialogfelder verwendet werden soll. Dieser Member wird derzeit nicht verwendet und ignoriert. Es ist sicher, **NULL** für diesen Parameter zu übergeben.

</dd> <dt>

*pCert* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**CERT \_ CONTEXT-Struktur**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) für das Zertifikat.

</dd> <dt>

*phCryptProv* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [**HCRYPTPROV-Struktur,**](hcryptprov.md) die ein Handle für den CSP ist.

</dd> <dt>

*pdwKeySpec* \[ out\]
</dt> <dd>

Die Spezifikation des abzurufende privaten Schlüssels. Mögliche Werte sind **AT \_ KEYEXCHANGE** oder **AT \_ SIGNATURE.**

</dd> <dt>

*pfDidCryptAcquire* \[ In\]
</dt> <dd>

Ein -Wert, der angibt, ob die Funktion das Anbieterhandle basierend auf dem Zertifikat bezogen hat.

</dd> <dt>

*ppwszTmpContainer* \[ out, optional\]
</dt> <dd>

Die Adresse eines Zeigers auf eine auf NULL endende Zeichenfolge für den Namen des temporären Schlüsselcontainers. Die **GetCryptProvFromCert-Funktion** stellt den temporären Container bereit und initialisiert sie. Beim Aufrufen **von GetCryptProvFromCert** sollte die Adresse auf einen **NULL-Wert** verweisen.

</dd> <dt>

*ppwszProviderName* \[ out, optional\]
</dt> <dd>

Die Adresse eines Zeigers auf eine auf NULL endende Zeichenfolge für den Anbieternamen. Die **GetCryptProvFromCert-Funktion** gibt den Anbieternamen zurück. Beim Aufrufen **von GetCryptProvFromCert** sollte die Adresse auf einen **NULL-Wert** verweisen.

</dd> <dt>

*pdwProviderType* \[ out\]
</dt> <dd>

Gibt den CSP-Typ an. Dies kann 0 (null) oder einer der [Kryptografieanbietertypen sein.](cryptographic-provider-types.md) Wenn dieser Member 0 (null) ist, ist der Schlüsselcontainer einer der CNG-Schlüsselspeicheranbieter.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt diese Funktion **TRUE** zurück. Die **GetCryptProvFromCert-Funktion** gibt **FALSE** zurück, wenn sie fehlschlägt.

## <a name="remarks"></a>Hinweise

Das [MakeCert-Tool](makecert.md) ruft **GetCryptProvFromCert** auf, wenn Sie es mithilfe der Befehlszeilenoption **-is** aufrufen.

Wenn der *pfDidCryptAcquire-Parameter* auf **TRUE** festgelegt ist, legt die Funktion die Parameter *phCryptProv,* *pdwKeySpec* und *pdwProviderType* auf die Anbieterwerte fest.

Wenn Sie den CSP nicht mehr verwenden, können Sie ihn freigeben, indem Sie die [**FreeCryptProvFromCert-Funktion**](freecryptprovfromcert.md) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
