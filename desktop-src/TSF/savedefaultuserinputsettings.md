---
title: Savedefaultuserinputsettings-Funktion
description: Wendet die Benutzer Tastaturlayout-und Text Dienst Einstellung auf die Standardbenutzer Struktur an.
ms.assetid: ab3ec13f-fc5b-4c4d-ba11-679f97624651
keywords:
- Savedefaultuserinputsettings-Funktion, Text Dienste-Framework
topic_type:
- apiref
api_name:
- SaveDefaultUserInputSettings
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66eb789a88f1a1a0c25fa26b95b3dda758f1ea1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391700"
---
# <a name="savedefaultuserinputsettings-function"></a>Savedefaultuserinputsettings-Funktion

Wendet die Benutzer Tastaturlayout-und Text Dienst Einstellung auf die Standardbenutzer Struktur an.

## <a name="syntax"></a>Syntax


```C++
BOOL CALLBACK SaveDefaultUserInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Das übergeordnete Fenster für das Dialogfeld "Warnung". Das Dialogfeld "Warnung" wird nicht immer angezeigt und wird entsprechend angezeigt. Wenn dieser Parameter NULL ist, wird das Dialogfeld Warnung nicht angezeigt.

</dd> <dt>

*hsourceregkey* \[ in\]
</dt> <dd>

Der Stamm Registrierungsschlüssel der zu kopierenden Benutzereinstellung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert



| Rückgabecode                                                                          | Beschreibung                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**Fall**</dt> </dl>  | Die Funktion war erfolgreich.<br/>   |
| <dl> <dt>**Alarm**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="examples"></a>Beispiele

Es ist keine Import Bibliothek verfügbar, die diese Funktion definiert. Daher ist es erforderlich, mithilfe von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)einen Zeiger auf diese Funktion zu erhalten. Im folgenden Beispiel wird veranschaulicht, wie ein Zeiger auf diese Funktion abgerufen wird.

> [!Note]  
> Die falsche Verwendung von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann die Sicherheit Ihrer Anwendung beeinträchtigen, indem die falsche DLL geladen wird. Informationen zum ordnungsgemäßen Laden von DLLs mit verschiedenen Versionen von Microsoft Windows finden Sie in der [Such Reihenfolge für die Dynamic Link Library](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 


```C++
typedef HRESULT (WINAPI *PTF_ SAVEDEFAULTUSERINPUTSETTINGS)(HWND hwndParent, HKEY hSourceRegKey);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SAVEDEFAULTUSERINPUTSETTINGS pfnSaveDefaultUserInputSettings;
    
    pfnSaveDefaultUserInputSettings = (PTF_ SAVEDEFAULTUSERINPUTSETTINGS)GetProcAddress(hInputDLL, "SaveDefaultUserInputSettings ");

    if(pfnSaveDefaultUserInputSettings)
    {
        bRet = (*pfnSaveDefaultUserInputSettings)( hwndParent, hSourceRegKey);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

