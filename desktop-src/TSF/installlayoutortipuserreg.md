---
title: Installlayoutortipuserreg-Funktion
description: Aktiviert die angegebenen Tastaturlayouts oder Text Dienste für den angegebenen Benutzer.
ms.assetid: f9b7a77e-5e82-41a6-8deb-be13bb96e85f
keywords:
- Installlayoutortipuserreg-Funktion Text Dienst-Framework
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
ms.openlocfilehash: b0484aeb16990467edd6e9f56a8a0cb6ca27b9ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741625"
---
# <a name="installlayoutortipuserreg-function"></a>Installlayoutortipuserreg-Funktion

Aktiviert die angegebenen Tastaturlayouts oder Text Dienste für den angegebenen Benutzer.

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

Ein Bitfeld, das die folgenden Flags angibt.

> [!Note]  
> Die folgenden Bezeichner sind nicht in einer öffentlichen Header Datei definiert. Sie müssen entweder den Hexadezimalwert verwenden oder die Bezeichner \# definieren. Wenn Sie z. b. " **Ilot \_ Uninstall** " verwenden möchten, müssen Sie `#define ILOT_UNINSTALL 0x00000001` in Ihren Code einschließen.

 



| Wert                                                                                                                                                                                                                                                                      | Bedeutung                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="ILOT_UNINSTALL"></span><span id="ilot_uninstall"></span><dl> <dt>**Ilot \_**</dt> <dt>0x00000001</dt> deinstallieren </dl>                                           | Identisch mit " **Ilot \_ deaktiviert**".<br/>                                     |
| <span id="ILOT_DEFPROFILE"></span><span id="ilot_defprofile"></span><dl> <dt>**Ilot \_ Defprofile**</dt> <dt>0x00000002</dt> </dl>                                        | Legt das angegebene Layout oder den Tipp als Standardelement fest.<br/>             |
| <span id="ILOT_NOAPPLYTOCURRENTSESSION"></span><span id="ilot_noapplytocurrentsession"></span><dl> <dt>**Ilot \_ Noapplydecurrentsession**</dt> <dt>0x00000020</dt> </dl> | Die Einstellung wird gespeichert, aber nicht auf die aktuelle Sitzung angewendet.<br/> |
| <span id="ILOT_CLEANINSTALL"></span><span id="ilot_cleaninstall"></span><dl> <dt>**Ilot \_ Cleaninstall**</dt> <dt>0x00000040</dt> </dl>                                  | Deaktiviert alle aktuellen Tastaturlayouts und Text Dienste.<br/> |
| <span id="ILOT_DISABLED"></span><span id="ilot_disabled"></span><dl> <dt>**Ilot \_**</dt> <dt>0x00000080</dt> deaktiviert </dl>                                              | Deaktiviert das angegebene Tastaturlayout und den angegebenen Text Dienst.<br/>        |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert



| Rückgabecode                                                                         | Beschreibung                               |
|-------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**Fall**</dt> </dl> | Die Funktion war erfolgreich.<br/>   |
| <dl> <dt>**-Sicherung**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das Zeichen folgen Format der Layoutliste lautet:

<langid 1>: <KLID 1>; \[ ...<LangID N>:<KLID N>

Das Zeichen folgen Format der Text Dienst Profil Liste lautet:

<langid 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};

Im folgenden finden Sie ein Beispiel für einen Wert für den *PSZ* -Parameter:


```C++
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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

