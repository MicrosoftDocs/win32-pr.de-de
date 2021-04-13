---
description: Ruft ein Handle für einen Kryptografiedienstanbieter (CSP) und eine Schlüssel Spezifikation für einen Zertifikat Kontext ab.
ms.assetid: ff72231f-e10f-49d2-b0e0-0008923803cc
title: Getcryptprovfromcert-Funktion
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
ms.openlocfilehash: bcd396c45333dee42bae4cb8bdfdd52792f1bdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350128"
---
# <a name="getcryptprovfromcert-function"></a>Getcryptprovfromcert-Funktion

> [!IMPORTANT]
> Diese API ist veraltet. Microsoft kann diese API in zukünftigen Versionen entfernen.

 

Die **getcryptprovfromcert** -Funktion Ruft ein Handle für einen [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP) und eine Schlüssel Spezifikation für einen [*Zertifikat*](../secgloss/c-gly.md) Kontext ab. Verwenden Sie diese Funktion, um Zugriff auf den [*privaten Schlüssel*](../secgloss/p-gly.md) des Zertifikat Ausstellers zu erhalten.

> [!Note]  
> Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.

 

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

*HWND* \[ in\]
</dt> <dd>

Das Handle des Fensters, das als Besitzer beliebiger Dialogfelder verwendet werden soll, die angezeigt werden. Dieser Member wird derzeit nicht verwendet und wird ignoriert. Es ist sicher, **null** für diesen Parameter zu übergeben.

</dd> <dt>

*pcert* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**CERT- \_ Kontext**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) Struktur für das Zertifikat.

</dd> <dt>

*phcryptprov* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**hcryptprov**](hcryptprov.md) -Struktur, die ein Handle für den CSP ist.

</dd> <dt>

*pdwkeyspec* \[ vorgenommen\]
</dt> <dd>

Die Spezifikation des abzurufenden privaten Schlüssels. Mögliche Werte sind **bei \_ keyexchange** oder **bei \_ Signatur**.

</dd> <dt>

*pfdidcryptacquire* \[ in\]
</dt> <dd>

Ein-Wert, der angibt, ob die Funktion das Anbieter handle basierend auf dem Zertifikat abgerufen hat.

</dd> <dt>

*ppwsztmpcontainer* \[ Out, optional\]
</dt> <dd>

Die Adresse eines Zeigers auf eine NULL-terminierte Zeichenfolge für den temporären Schlüssel Container Namen. Mit der **getcryptprovfromcert** -Funktion wird der temporäre Container bereitstellt und initialisiert. Beim Aufrufen von **getcryptprovfromcert** sollte die Adresse auf einen **null** -Wert zeigen.

</dd> <dt>

*ppwszprovidername* \[ Out, optional\]
</dt> <dd>

Die Adresse eines Zeigers auf eine NULL-terminierte Zeichenfolge für den Anbieter Namen. Die **getcryptprovfromcert** -Funktion gibt den Anbieter Namen zurück. Beim Aufrufen von **getcryptprovfromcert** sollte die Adresse auf einen **null** -Wert zeigen.

</dd> <dt>

*pdwprovidertype* \[ vorgenommen\]
</dt> <dd>

Gibt den CSP-Typ an. Dies kann NULL oder einer der [kryptografieanbiettypen](cryptographic-provider-types.md)sein. Wenn dieser Member 0 (null) ist, ist der Schlüssel Container einer der CNG-Schlüsselspeicher Anbieter.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt diese Funktion " **true**" zurück. Die **getcryptprovfromcert** -Funktion gibt **false** zurück, wenn Sie fehlschlägt.

## <a name="remarks"></a>Bemerkungen

Das [Makecert](makecert.md) -Tool ruft **getcryptprovfromcert** auf, wenn Sie es mithilfe der Befehlszeilenoption **-is** aufrufen.

Wenn der Parameter " *pfdidcryptacquire* " auf " **true**" festgelegt ist, legt die Funktion die Parameter " *phcryptprov*", " *pdwkeyspec*" und " *pdwprovidertype* " auf die Anbieter Werte fest.

Wenn Sie die Verwendung des CSP abgeschlossen haben, können Sie es durch Aufrufen der [**freecryptprovfromcert**](freecryptprovfromcert.md) -Funktion freigeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
