---
title: SetDefaultLayoutOrTipUserReg-Funktion
description: Legt das angegebene Tastaturlayout oder einen Textdienst als Standardeingabeelement der Benutzerregistrierung fest.
ms.assetid: 23ac67bb-b9dc-4f88-8fa0-a1d0534cbb84
keywords:
- SetDefaultLayoutOrTipUserReg-Funktion Textdienstframework
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 340e21d8d7416d72361a0e505029500b9a7dde3e53d3388c9311ae3351345c3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118875284"
---
# <a name="setdefaultlayoutortipuserreg-function"></a>SetDefaultLayoutOrTipUserReg-Funktion

Legt das angegebene Tastaturlayout oder einen Textdienst als Standardeingabeelement der Benutzerregistrierung fest.

## <a name="syntax"></a>Syntax


```C++
BOOL CALLBACK SetDefaultLayoutOrTipUserReg(
  _In_opt_ LPCWSTR pszUserReg,
  _In_opt_ LPCWSTR pszSystemReg,
  _In_opt_ LPCWSTR pszSoftwareReg,
  _In_     LPCWSTR psz,
  _In_     DWORD   dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszUserReg* \[ in, optional\]
</dt> <dd>

Der Registrierungspfad des Benutzers. Wenn dieser Parameter **NULL** ist, wird HKEY \_ CURRENT USER \_ verwendet.

</dd> <dt>

*pszSystemReg* \[ in, optional\]
</dt> <dd>

Der Registrierungspfad des Systems. Wenn dieser Parameter **NULL** ist, wird HKEY \_ LOCAL MACHINE System \_ \\ verwendet.

</dd> <dt>

*pszSoftwareReg* \[ in, optional\]
</dt> <dd>

Der Registrierungspfad der Software. Wenn dieser Parameter **NULL** ist, wird HKEY \_ LOCAL MACHINE Software \_ \\ verwendet.

</dd> <dt>

*psz* \[ In\]
</dt> <dd>

Eine Zeichenfolge, die die Tastaturlayoutliste oder die Profilliste der Textdienste darstellt.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Ein Bitfeld, das die folgenden Flags angibt:

> [!Note]  
> Die folgenden Bezeichner sind in einer öffentlichen Headerdatei nicht definiert. Sie müssen entweder den Hexadezimalwert verwenden oder \# die Bezeichner definieren. Um beispielsweise SDLOT \_ NOAPPLYTOCURRENTSESSION zu verwenden, müssen Sie \# SDLOT \_ NOAPPLYTOCURRENTSESSION 0x00000001 in Ihren Code einschließen.

 



| Wert                                                                                                                                                                                                                                                                         | Bedeutung                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <dt>**SDLOT \_ NOAPPLYTOCURRENTSESSION-0x00000001**</dt> <dt></dt> </dl> | Speichert die Einstellung in der Registrierung, aktualisiert jedoch nicht die Laufzeittastatureinstellung der aktuellen Sitzung. Wenn der alternative Registrierungspfad in **SetDefaultLayoutOrTipUserReg** festgelegt ist, sollte dieses Flag festgelegt werden.<br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <dt>**SDLOT \_ APPLYTOCURRENTTHREAD-0x00000002**</dt> <dt></dt> </dl>          | Wendet die Einstellung sofort auf den aktuellen Thread an.<br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert



| Rückgabecode                                                                          | Beschreibung                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**STIMMT**</dt> </dl>  | Die Funktion war erfolgreich.<br/>   |
| <dl> <dt>**FALSE**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Hinweise

Das Zeichenfolgenformat der Layoutliste lautet:

<LangID 1>:<SOLLD 1>; \[ ...<LangID N>:<KLID N>

Das Zeichenfolgenformat der Textdienstprofilliste lautet:

<LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxxxxxxxxxx};

Im Folgenden wird ein Beispiel für einen Wert für den *psz-Parameter* angezeigt:


```
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a>Beispiele

Es ist keine Importbibliothek verfügbar, die diese Funktion definiert. Daher ist es erforderlich, mit [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)einen Zeiger auf diese Funktion abzurufen. Im folgenden Beispiel wird veranschaulicht, wie sie einen Zeiger auf diese Funktion abrufen.

> [!Note]  
> Die falsche Verwendung von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann die Sicherheit Ihrer Anwendung beeinträchtigen, indem die falsche DLL geladen wird. Informationen zum ordnungsgemäßen Laden von DLLs mit verschiedenen Versionen von Microsoft Windows finden Sie unter [Suchreihenfolge](/windows/desktop/Dlls/dynamic-link-library-search-order) der Dynamic Link Library.

 


```C++
typedef HRESULT (
    WINAPI *PTF_ SETDEFAULTLAYOUTORTIPUSERREG)( LPCWSTR pszUserReg, 
    LPCWSTR pszSystemReg, 
    LPCWSTR pszSoftwareReg, 
    LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    //Error loading module -- fail as securely as possible 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIPUSERREG pfnSetDefaultLayoutOrTipUserReg;
    
    pfnSetDefaultLayoutOrTipUserReg = (PTF_ SETDEFAULTLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTipUserReg");

    if(pfnSetDefaultLayoutOrTipUserReg)
    {
        bRet = (*pfnSetDefaultLayoutOrTipUserReg)( pszUserReg, pszSystemReg, pszSoftwareReg, psz);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

