---
title: EnumEnabledLayoutOrTip-Funktion
description: Enumeriert alle aktivierten Tastaturlayouts oder Textdienste der angegebenen Benutzereinstellung.
ms.assetid: b3c57e88-e04b-411b-9eba-83258da16773
keywords:
- EnumEnabledLayoutOrTip-Textdienstframework
topic_type:
- apiref
api_name:
- EnumEnabledLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45b7f6ee6876042f2660e9430f096a96f3fa5ec40d78828041c6787f1e18bcd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117953462"
---
# <a name="enumenabledlayoutortip-function"></a>EnumEnabledLayoutOrTip-Funktion

Enumeriert alle aktivierten Tastaturlayouts oder Textdienste der angegebenen Benutzereinstellung.

## <a name="syntax"></a>Syntax


```C++
UINT EnumEnabledLayoutOrTip(
  _In_opt_ LPCWSTR            pszUserReg,
  _In_opt_ LPCWSTR            pszSystemReg,
  _In_opt_ LPCWSTR            pszSoftwareReg,
  _Out_    LAYOUTORTIPPROFILE *pLayoutOrTipProfile,
  _In_     UINT               uBufLength
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszUserReg* \[ in, optional\]
</dt> <dd>

Der Registrierungspfad des Benutzers. Wenn dieser Parameter NULL **ist,** wird HKEY \_ CURRENT USER \_ verwendet.

</dd> <dt>

*pszSystemReg* \[ in, optional\]
</dt> <dd>

Der Registrierungspfad des Systems. Wenn dieser Parameter NULL **ist,** wird HKEY \_ LOCAL MACHINE System \_ \\ verwendet.

</dd> <dt>

*pszSoftwareReg* \[ in, optional\]
</dt> <dd>

Der Registrierungspfad der Software. Wenn dieser Parameter NULL **ist,** wird HKEY \_ LOCAL MACHINE Software \_ \\ verwendet.

</dd> <dt>

*pLayoutOrTipProfile* \[ out\]
</dt> <dd>

Zeiger auf den Puffer, der das LAYOUTORTIPPROFILE-Array empfängt.

</dd> <dt>

*uBufLength* \[ In\]
</dt> <dd>

Die Länge des Puffers, auf den *pLayoutOrTipProfile zeigt.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn *pLayoutOrTipProfile* **NULL ist,** die Anzahl der Tastaturelemente, die in der Benutzereinstellung aktiviert sind; andernfalls die Anzahl der Tastaturelemente, die in *pLayoutOrTipProfile kopiert werden.*

Für IME-Sprachen (Input Method Editor) werden alle IMEs zurückgegeben, auch wenn nur ein IME aktiviert ist. Wenn beispielsweise für einen Benutzer die CHT New Quick IME aktiviert ist, gibt die **EnumEnabledLayoutOrTip-Funktion** alle fünf CHT-IMEs zurück.

## <a name="remarks"></a>Hinweise

Es ist keine Importbibliothek verfügbar, die diese Funktion definiert. Daher ist es erforderlich, mit [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)einen Zeiger auf diese Funktion zu erhalten.

> [!Note]  
> Die [**falsche Verwendung von LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann die Sicherheit Ihrer Anwendung gefährden, indem die falsche DLL geladen wird. Informationen zum [ordnungsgemäßen](/windows/desktop/Dlls/dynamic-link-library-search-order) Laden von DLLs mit verschiedenen Versionen von Microsoft Windows.

 

Die Definition von LAYOUTORTIPPROFILE ist:

``` syntax
typedef struct tagLAYOUTORTIPPROFILE {
    DWORD  dwProfileType;       // InputProcessor or HKL 
#define LOTP_INPUTPROCESSOR 1
#define LOTP_KEYBOARDLAYOUT 2
    LANGID langid;              // language id 
    CLSID  clsid;               // CLSID of tip 
    GUID   guidProfile;         // profile description 
    GUID   catid;               // category of tip 
    DWORD  dwSubstituteLayout;  // substitute hkl 
    DWORD  dwFlags;             // Flags 
    WCHAR  szId[MAX_PATH];      // KLID or TIP profile for string 
} LAYOUTORTIPPROFILE;
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

