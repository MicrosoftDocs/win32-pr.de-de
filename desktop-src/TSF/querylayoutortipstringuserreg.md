---
title: Querylayoutortipstringuserreg-Funktion
description: Fragt die angegebene Zeichenfolge ab, die das Format einer Liste von Tastaturlayouts oder Text Dienst Profilen mit dem angegebenen Registrierungs Pfad darstellt.
ms.assetid: b7b42fda-5a65-483a-b3f3-85157bb1a667
keywords:
- Querylayoutortipstringuserreg-Funktion Text Dienst-Framework
topic_type:
- apiref
api_name:
- QueryLayoutOrTipStringUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7f3e4979318b44e8c6be876af5301ad31e544d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342464"
---
# <a name="querylayoutortipstringuserreg-function"></a>Querylayoutortipstringuserreg-Funktion

Fragt die angegebene Zeichenfolge ab, die das Format einer Liste von Tastaturlayouts oder Text Dienst Profilen mit dem angegebenen Registrierungs Pfad darstellt.

## <a name="syntax"></a>Syntax


```C++
HRESULT CALLBACK QueryLayoutOrTipStringUserReg(
  _In_ LPCWSTR pszUserReg,
  _In_ LPCWSTR pszSystemReg,
  _In_ LPCWSTR pszSoftwareReg,
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszuserreg* \[ in\]
</dt> <dd>

Der Registrierungs Pfad des Benutzers. Wenn dieser Parameter **null** ist, wird der aktuelle HKEY- \_ \_ Benutzer verwendet.

</dd> <dt>

*pszsystemreg* \[ in\]
</dt> <dd>

Der Registrierungs Pfad des Systems. Wenn dieser Parameter **null** ist, wird HKEY \_ local \_ Machine \\ System verwendet.

</dd> <dt>

*pszsoftwarerereg* \[ in\]
</dt> <dd>

Der Registrierungs Pfad der Software. Wenn dieser Parameter **null** ist, wird die lokale HKEY- \_ \_ Computer \\ Software verwendet.

</dd> <dt>

*PSZ* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die eine Liste von Tastaturlayouts oder Text Dienst Profilen darstellt.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Diese Angabe muss 0 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                  | Beschreibung                                                                       |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Alle in **PSZ** definierten Layouts oder Profile sind gültig.<br/>                  |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Mindestens eines der in **PSZ** definierten Layouts oder Profile ist ungültig.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Es ist keine Import Bibliothek verfügbar, die diese Funktion definiert. Daher ist es erforderlich, mithilfe von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)einen Zeiger auf diese Funktion zu erhalten.

> [!Note]  
> Die falsche Verwendung von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann die Sicherheit Ihrer Anwendung beeinträchtigen, indem die falsche DLL geladen wird. Informationen zum ordnungsgemäßen Laden von DLLs mit verschiedenen Versionen von Microsoft Windows finden Sie in der [Such Reihenfolge für die Dynamic Link Library](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 

Das Zeichen folgen Format der Layoutliste lautet:

<langid 1>: <KLID 1>; \[ ...<LangID N>:<KLID N>

Das Zeichen folgen Format der Text Dienst Profil Liste lautet:

<langid 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};

Im folgenden finden Sie ein Beispiel für einen Wert für den *PSZ* -Parameter:

``` syntax
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

