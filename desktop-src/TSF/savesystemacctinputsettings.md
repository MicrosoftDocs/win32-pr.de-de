---
title: SaveSystemAcctInputSettings-Funktion
description: Wendet das Benutzertastaturlayout und die Textdiensteinstellung auf die Systemkontenstruktur an.
ms.assetid: 73782637-3784-46d9-ba93-0527a2527412
keywords:
- SaveSystemAcctInputSettings-Textdienstframework
topic_type:
- apiref
api_name:
- SaveSystemAcctInputSettings
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c60b9743ebbf54ce7189499f7295d44377c272b6d7cfcf5693259f12657bf06c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118875294"
---
# <a name="savesystemacctinputsettings-function"></a>SaveSystemAcctInputSettings-Funktion

Wendet das Benutzertastaturlayout und die Textdiensteinstellung auf die Systemkontenstruktur an.

## <a name="syntax"></a>Syntax


```C++
BOOL CALLBACK SaveSystemAcctInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndParent* \[ In\]
</dt> <dd>

Das übergeordnete Fenster für das Warnungsdialogfeld. Das Warnungsdialogfeld wird nicht immer angezeigt und entsprechend angezeigt. Wenn dieser Parameter **NULL ist,** wird das Warnungsdialogfeld nicht angezeigt.

</dd> <dt>

*hSourceRegKey* \[ In\]
</dt> <dd>

Der Stammregistrierungsschlüssel der zu kopierenden Benutzereinstellung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert



| Rückgabecode                                                                          | Beschreibung                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**STIMMT**</dt> </dl>  | Die Funktion war erfolgreich.<br/>   |
| <dl> <dt>**FALSE**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Hinweise

Die Systemkontostruktur ist HKEY \_ USERS \\ . DEFAULT, HKEY \_ USERS \\ S-1-5-19 und HKEY \_ USERS \\ S-1-5-20.

## <a name="examples"></a>Beispiele

Es ist keine Importbibliothek verfügbar, die diese Funktion definiert. Daher ist es erforderlich, mit [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)einen Zeiger auf diese Funktion zu erhalten. Im folgenden Beispiel wird veranschaulicht, wie ein Zeiger auf diese Funktion erhalten wird.

> [!Note]  
> Die [**falsche Verwendung von LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann die Sicherheit Ihrer Anwendung gefährden, indem die falsche DLL geladen wird. Informationen zum [ordnungsgemäßen](/windows/desktop/Dlls/dynamic-link-library-search-order) Laden von DLLs mit verschiedenen Versionen von Microsoft Windows.

 


```C++
typedef HRESULT (WINAPI *PTF_ SAVESYSTEMACCTINPUTSETTINGS)(HWND hwndParent, HKEY hSourceRegKey);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SAVESYSTEMACCTINPUTSETTINGS pfnSaveSystemAcctInputSettings;
    
    pfnSaveSystemAcctInputSettings = (PTF_ SAVESYSTEMACCTINPUTSETTINGS)GetProcAddress(hInputDLL, "SaveSystemAcctInputSettings ");

    if(pfnSaveSystemAcctInputSettings)
    {
        bRet = (*pfnSaveSystemAcctInputSettings)( hwndParent, hSourceRegKey);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

