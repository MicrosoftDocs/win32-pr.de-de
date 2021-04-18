---
description: Speichert einen privaten Schlüssel und den zugehörigen öffentlichen Schlüssel in einer angegebenen Datei.
ms.assetid: 491a128a-b4aa-4cca-a835-d0e8d7df6720
title: Pvkprivatekeysave-Funktion
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
ms.openlocfilehash: ef60c3f615a704248fbcb8630322fa6b598141ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351815"
---
# <a name="pvkprivatekeysave-function"></a>Pvkprivatekeysave-Funktion

> [!IMPORTANT]
> Diese API ist veraltet. Microsoft kann diese API in zukünftigen Versionen entfernen.

 

Die **pvkprivatekeysave** -Funktion speichert einen [*privaten Schlüssel*](../secgloss/p-gly.md) und den zugehörigen [*öffentlichen Schlüssel*](../secgloss/p-gly.md) in einer angegebenen Datei.

> [!Note]  
> Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek. Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.

 

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

*hcryptprov* \[ in\]
</dt> <dd>

Ein Handle für einen [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSP).

</dd> <dt>

*hFile* \[ in\]
</dt> <dd>

Ein Handle für eine Datei, die mit der ersten Lese-/Schreibberechtigung und einer nachfolgenden schreibgeschützten Berechtigung erstellt wurde.

</dd> <dt>

*dwkeyspec* \[ in\]
</dt> <dd>

Eine lange ganze Zahl für den Schlüsseltyp. Mögliche Werte sind **bei \_ keyexchange** oder **bei \_ Signatur**.

</dd> <dt>

*hwndOwner* \[ in\]
</dt> <dd>

Wenn ein Kennwort zum Verschlüsseln des privaten Schlüssels erforderlich ist, ist dieser Parameter ein Handle für das übergeordnete Element des Dialog Felds. Andernfalls ist der Wert **null**.

</dd> <dt>

*pwszkeyname* \[ in\]
</dt> <dd>

Ein Zeiger auf eine mit NULL endende Zeichenfolge für den Namen des zu speichernden Schlüssels.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Ein **DWORD** -Wert, der zusätzliche Optionen für die Funktion angibt. Weitere Informationen finden Sie unter dem *dwFlags* -Parameter in [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt diese Funktion " **true**" zurück. Die **pvkprivatekeysave** -Funktion gibt **false** zurück, wenn Sie fehlschlägt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
