---
description: Speichert einen privaten Schlüssel und den entsprechenden öffentlichen Schlüssel in einer angegebenen Datei.
ms.assetid: 491a128a-b4aa-4cca-a835-d0e8d7df6720
title: PvkPrivateKeySave-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeySave
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 3a2eed4b907f7c22414634a4b1ef49df6ca780181109a7396de2f8aa1776b7c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901209"
---
# <a name="pvkprivatekeysave-function"></a>PvkPrivateKeySave-Funktion

> [!IMPORTANT]
> Diese API ist veraltet. Microsoft kann diese API in zukünftigen Versionen entfernen.

 

Die **PvkPrivateKeySave-Funktion** speichert einen [*privaten Schlüssel*](../secgloss/p-gly.md) und den entsprechenden öffentlichen [*Schlüssel*](../secgloss/p-gly.md) in einer angegebenen Datei.

> [!Note]  
> Dieser Funktion ist keine Headerdatei oder Importbibliothek zugeordnet. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Headerdatei erstellen und die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um dynamisch eine Verknüpfung mit Mssign32.dll herzustellen.

 

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI PvkPrivateKeySave(
  _In_ HCRYPTPROV hCryptProv,
  _In_ HANDLE     hFile,
  _In_ DWORD      dwKeySpec,
  _In_ HWND       hwndOwner,
  _In_ LPCWSTR    pwszKeyName,
  _In_ DWORD      dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hCryptProv* \[ In\]
</dt> <dd>

Ein Handle für einen [*Kryptografiedienstanbieter (Cryptographic Service Provider,*](../secgloss/c-gly.md) CSP).

</dd> <dt>

*hFile* \[ In\]
</dt> <dd>

Ein Handle für eine Datei, die mit der anfänglichen Lese-/Schreibberechtigung und der nachfolgenden schreibgeschützten Berechtigung erstellt wurde.

</dd> <dt>

*dwKeySpec* \[ In\]
</dt> <dd>

Eine lange ganze Zahl für den Typ des Schlüssels. Mögliche Werte sind **AT \_ KEYEXCHANGE** oder **AT \_ SIGNATURE.**

</dd> <dt>

*hwndOwner* \[ In\]
</dt> <dd>

Wenn zum Verschlüsseln des privaten Schlüssels ein Kennwort erforderlich ist, ist dieser Parameter ein Handle für das übergeordnete Element des Dialogfelds. Andernfalls ist es **NULL.**

</dd> <dt>

*pwszKeyName* \[ In\]
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge für den Namen des zu speichernden Schlüssels.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Ein **DWORD-Wert,** der zusätzliche Optionen für die Funktion angibt. Weitere Informationen finden Sie im *dwFlags-Parameter* in [**CryptExportKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt diese Funktion **TRUE** zurück. Die **PvkPrivateKeySave-Funktion** gibt **FALSE** zurück, wenn sie fehlschlägt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
