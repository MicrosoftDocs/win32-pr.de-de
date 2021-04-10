---
title: Setdefaultlayoutortipuserreg-Funktion
description: Legt das angegebene Tastaturlayout oder einen Text Dienst als Standardeingabe Element der Benutzerregistrierung fest.
ms.assetid: 23ac67bb-b9dc-4f88-8fa0-a1d0534cbb84
keywords:
- Setdefaultlayoutortipuserreg Function-Framework für Text Dienste
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
ms.openlocfilehash: 48333b42b673cb6284e4b97001fa5ee88e0b3867
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103018"
---
# <a name="setdefaultlayoutortipuserreg-function"></a>Setdefaultlayoutortipuserreg-Funktion

Legt das angegebene Tastaturlayout oder einen Text Dienst als Standardeingabe Element der Benutzerregistrierung fest.

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

*pszuserreg* \[ in, optional\]
</dt> <dd>

Der Registrierungs Pfad des Benutzers. Wenn dieser Parameter **null** ist, wird der aktuelle HKEY- \_ \_ Benutzer verwendet.

</dd> <dt>

*pszsystemreg* \[ in, optional\]
</dt> <dd>

Der Registrierungs Pfad des Systems. Wenn dieser Parameter **null** ist, wird HKEY \_ local \_ Machine \\ System verwendet.

</dd> <dt>

*pszsoftwarerereg* \[ in, optional\]
</dt> <dd>

Der Registrierungs Pfad der Software. Wenn dieser Parameter **null** ist, wird die lokale HKEY- \_ \_ Computer \\ Software verwendet.

</dd> <dt>

*PSZ* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die die Liste der Tastaturlayout-oder Text Dienst profile darstellt.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Ein Bitfeld, das die folgenden Flags angibt:

> [!Note]  
> Die folgenden Bezeichner sind nicht in einer öffentlichen Header Datei definiert. Sie müssen entweder den Hexadezimalwert verwenden oder die Bezeichner \# definieren. Wenn Sie z. b. "sdlot \_ noapplydecurrentsession" verwenden möchten, müssen Sie " \# sdlot \_ noapplydecurrentsession 0x00000001" in Ihren Code einschließen.

 



| Wert                                                                                                                                                                                                                                                                         | Bedeutung                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <dt>**Sdlot \_ Noapplydecurrentsession**</dt> <dt>0x00000001</dt> </dl> | Speichert die Einstellung in der Registrierung, aber die Lauf Zeit Tastatur Einstellung der aktuellen Sitzung wird nicht aktualisiert. Wenn der Alternative Registrierungs Pfad in **setdefaultlayoutor tipuserreg** festgelegt wird, sollte dieses Flag festgelegt werden.<br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <dt>**Sdlot \_ Applyycurrentthread**</dt> <dt>0x00000002</dt> </dl>          | Wendet die Einstellung direkt auf den aktuellen Thread an.<br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert



| Rückgabecode                                                                          | Beschreibung                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**Fall**</dt> </dl>  | Die Funktion war erfolgreich.<br/>   |
| <dl> <dt>**Alarm**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das Zeichen folgen Format der Layoutliste lautet:

<langid 1>: <KLID 1>; \[ ...<LangID N>:<KLID N>

Das Zeichen folgen Format der Text Dienst Profil Liste lautet:

<langid 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};

Im folgenden finden Sie ein Beispiel für einen Wert für den *PSZ* -Parameter:


```
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a>Beispiele

Es ist keine Import Bibliothek verfügbar, die diese Funktion definiert. Daher ist es erforderlich, mithilfe von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)einen Zeiger auf diese Funktion zu erhalten. Im folgenden Beispiel wird veranschaulicht, wie ein Zeiger auf diese Funktion abgerufen wird.

> [!Note]  
> Die falsche Verwendung von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann die Sicherheit Ihrer Anwendung beeinträchtigen, indem die falsche DLL geladen wird. Informationen zum ordnungsgemäßen Laden von DLLs mit verschiedenen Versionen von Microsoft Windows finden Sie in der [Such Reihenfolge für die Dynamic Link Library](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

