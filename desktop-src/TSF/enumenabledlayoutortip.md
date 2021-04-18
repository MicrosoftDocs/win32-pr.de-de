---
title: Enumenabledlayoutortip-Funktion
description: Listet alle aktivierten Tastaturlayouts oder Text Dienste der angegebenen Benutzereinstellung auf.
ms.assetid: b3c57e88-e04b-411b-9eba-83258da16773
keywords:
- Enumenabledlayoutortip-Funktion Text Dienst-Framework
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
ms.openlocfilehash: b192896dd95d5ab8f306158e33a8d248793bfc10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340786"
---
# <a name="enumenabledlayoutortip-function"></a>Enumenabledlayoutortip-Funktion

Listet alle aktivierten Tastaturlayouts oder Text Dienste der angegebenen Benutzereinstellung auf.

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

*playoutor-Profil* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den Puffer, der das layoutor profile-Array empfängt.

</dd> <dt>

*ubuflength* \[ in\]
</dt> <dd>

Die Länge des Puffers, auf den von *playoutor Tip profile* verwiesen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn " *playoutor tipprofile* " **null** ist, wird die Anzahl der in der Benutzereinstellung aktivierten Tastatur Elemente angezeigt. andernfalls die Anzahl der Tastatur Elemente, die in *playoutor profile* kopiert werden.

Für IME-Sprachen (Input Method Editor) werden alle IMEs zurückgegeben, auch wenn nur ein IME aktiviert ist. Wenn für einen Benutzer z. b. die Schnelleingabe Taste "cht New" aktiviert ist, gibt die **enumenabledlayoutortip** -Funktion alle fünf cht-IDs zurück.

## <a name="remarks"></a>Bemerkungen

Es ist keine Import Bibliothek verfügbar, die diese Funktion definiert. Daher ist es erforderlich, mithilfe von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)einen Zeiger auf diese Funktion zu erhalten.

> [!Note]  
> Die falsche Verwendung von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann die Sicherheit Ihrer Anwendung beeinträchtigen, indem die falsche DLL geladen wird. Informationen zum ordnungsgemäßen Laden von DLLs mit verschiedenen Versionen von Microsoft Windows finden Sie in der [Such Reihenfolge für die Dynamic Link Library](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 

Die Definition von layoutor profile lautet:

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

