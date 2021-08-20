---
title: InstallLayoutOrTipUserReg-Funktion
description: Aktiviert die angegebenen Tastaturlayouts oder Textdienste für den angegebenen Benutzer.
ms.assetid: f9b7a77e-5e82-41a6-8deb-be13bb96e85f
keywords:
- InstallLayoutOrTipUserReg-Funktion Textdienstframework
topic_type:
- apiref
api_name:
- InstallLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8af476cc18d788c0fe732e45ddfdc9f22748e595058d6f7feb1660f61963bf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952922"
---
# <a name="installlayoutortipuserreg-function"></a>InstallLayoutOrTipUserReg-Funktion

Aktiviert die angegebenen Tastaturlayouts oder Textdienste für den angegebenen Benutzer.

## <a name="syntax"></a>Syntax


```C++
BOOL CALLBACK InstallLayoutOrTipUserReg(
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

Ein Bitfeld, das die folgenden Flags angibt.

> [!Note]  
> Die folgenden Bezeichner sind in einer öffentlichen Headerdatei nicht definiert. Sie müssen entweder den Hexadezimalwert verwenden oder \# die Bezeichner definieren. Um beispielsweise **ILOT \_ UNINSTALL** verwenden zu können, müssen Sie `#define ILOT_UNINSTALL 0x00000001` in Ihren Code einschließen.

 



| Wert                                                                                                                                                                                                                                                                      | Bedeutung                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="ILOT_UNINSTALL"></span><span id="ilot_uninstall"></span><dl> <dt>**ILOT \_ DEINSTALLIEREN**</dt> <dt>0x00000001</dt> </dl>                                           | Identisch mit **ILOT \_ DISABLED**.<br/>                                     |
| <span id="ILOT_DEFPROFILE"></span><span id="ilot_defprofile"></span><dl> <dt>**ILOT \_ DEFPROFILE**</dt> <dt>0x00000002</dt> </dl>                                        | Legt das angegebene Layout oder den angegebenen Tipp als Standardelement fest.<br/>             |
| <span id="ILOT_NOAPPLYTOCURRENTSESSION"></span><span id="ilot_noapplytocurrentsession"></span><dl> <dt>**ILOT \_ NOAPPLYTOCURRENTSESSION-0x00000020**</dt> <dt></dt> </dl> | Die Einstellung wird gespeichert, aber nicht auf die aktuelle Sitzung angewendet.<br/> |
| <span id="ILOT_CLEANINSTALL"></span><span id="ilot_cleaninstall"></span><dl> <dt>**ILOT \_ CLEANINSTALL**</dt> <dt>0x00000040</dt> </dl>                                  | Deaktiviert alle aktuellen Tastaturlayouts und Textdienste.<br/> |
| <span id="ILOT_DISABLED"></span><span id="ilot_disabled"></span><dl> <dt>**ILOT \_ DISABLED**</dt> <dt>0x00000080</dt> </dl>                                              | Deaktiviert das angegebene Tastaturlayout und den Textdienst.<br/>        |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert



| Rückgabecode                                                                         | Beschreibung                               |
|-------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**STIMMT**</dt> </dl> | Die Funktion war erfolgreich.<br/>   |
| <dl> <dt>**FASE**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Hinweise

Das Zeichenfolgenformat der Layoutliste lautet:

<LangID 1>:<SOLLD 1>; \[ ...<LangID N>:<KLID N>

Das Zeichenfolgenformat der Textdienstprofilliste lautet:

<LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxxxxxxxxxx};

Im Folgenden wird ein Beispiel für einen Wert für den *psz-Parameter* angezeigt:


```C++
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
  WINAPI *PTF_ INSTALLLAYOUTORTIPUSERREG)(LPCWSTR pszUserReg, 
  LPCWSTR pszSystemReg, 
  LPCWSTR pszSoftwareReg, 
  LPCWSTR psz, 
  DWORD dwFlasg);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ INSTALLLAYOUTORTIPUSERREG pfnInputLayoutOrTipUserReg;
    
    pfnInputLayoutOrTipUserReg = (PTF_ INSTALLLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "InputLayoutOrTipUserReg");

    if(pfnInputLayoutOrTipUserReg)
    {
        bRet = (*pfnInputLayoutOrTipUserReg)(pszUserReg, pszSystemReg, pszSoftwareReg, psz, dwFlags);
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



 

