---
title: Querylayoutortipstring-Funktion
description: Fragt die angegebene Zeichenfolge ab, die das Format einer Liste von Tastaturlayouts oder Text Dienst Profilen darstellt.
ms.assetid: 92fd89b7-8b96-4709-8ee2-9814a908b4e4
keywords:
- Querylayoutortipstring-Funktion, Text Dienste-Framework
topic_type:
- apiref
api_name:
- QueryLayoutOrTipString
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11f4cead682a50897a74c60eeadf886e8b47456b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342465"
---
# <a name="querylayoutortipstring-function"></a>Querylayoutortipstring-Funktion

Fragt die angegebene Zeichenfolge ab, die das Format einer Liste von Tastaturlayouts oder Text Dienst Profilen darstellt.

## <a name="syntax"></a>Syntax


```C++
HRESULT CALLBACK QueryLayoutOrTipString(
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

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



| Rückgabecode                                                                                  | Beschreibung                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Alle in *PSZ* definierten Layouts oder Profile sind gültig.<br/>                  |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Mindestens eines der in *PSZ* definierten Layouts oder Profile ist ungültig.<br/> |



 

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



 

