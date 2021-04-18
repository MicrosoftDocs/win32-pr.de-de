---
title: Enumlayoutortipforsetup-Funktion
description: Listet die installierten Tastaturlayouts und Text Dienste der Setup Benutzeroberfläche oder des OOBE-Werts auf.
ms.assetid: 3c6fc11c-36a5-4718-b584-b7f98f1b4180
keywords:
- Enumlayoutortipforsetup-Funktion Text Dienst-Framework
topic_type:
- apiref
api_name:
- EnumLayoutOrTipForSetup
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c9a65e0d966684329996e4f5d23370592250a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338528"
---
# <a name="enumlayoutortipforsetup-function"></a>Enumlayoutortipforsetup-Funktion

Listet die installierten Tastaturlayouts und Text Dienste der Setup Benutzeroberfläche oder des OOBE-Werts auf.

## <a name="syntax"></a>Syntax


```C++
UINT CALLBACK EnumLayoutOrTipForSetup(
  _In_  LANGID      langid,
  _Out_ LAYOUTORTIP *pLayoutOrTip,
  _In_  UINT        uBufLength,
  _In_  DWORD       dwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LangID* \[ in\]
</dt> <dd>

Die Sprach-ID des Elements, das aufgelistet werden soll.

</dd> <dt>

*playoutor Tip* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den Puffer, der das Array der layoutor Tip-Strukturen empfängt. Dies kann **null** sein, um die Anzahl der Elemente zu erhalten.

</dd> <dt>

*ubuflength* \[ in\]
</dt> <dd>

Die Länge des Puffers, auf den von *playoutor Tip* verwiesen wird. Dies wird ignoriert, wenn *playoutor Tip* den Wert **null** hat.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Nicht verwendet. Dieser Wert muss NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn *playoutor Tip* **null** ist, wird die Anzahl von Tastatur Elementen, die im System registriert sind, angezeigt. andernfalls die Anzahl der Tastatur Elemente, die in " *playoutor Tip*" kopiert werden.

## <a name="remarks"></a>Bemerkungen

Es ist keine Import Bibliothek verfügbar, die diese Funktion definiert. Daher ist es erforderlich, mithilfe von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)einen Zeiger auf diese Funktion zu erhalten.

> [!Note]  
> Die falsche Verwendung von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) kann die Sicherheit Ihrer Anwendung beeinträchtigen, indem die falsche DLL geladen wird. Informationen zum ordnungsgemäßen Laden von DLLs mit verschiedenen Versionen von Microsoft Windows finden Sie in der [Such Reihenfolge für die Dynamic Link Library](/windows/desktop/Dlls/dynamic-link-library-search-order) .

 

Die Definition von layoutor Tip lautet:

``` syntax
typedef struct tagLAYOUTORTIP {
    DWORD dwFlags;
#define LOT_DEFAULT    0x0001 // If this is on, this is a default item. 
#define LOT_DISABLED   0x0002 // if this is on, this is not enabled. 
    WCHAR szId[MAX_PATH]; // Id of the keyboard item in the string format. 
    WCHAR szName[MAX_PATH]; // The description of the keyboard item. 
} LAYOUTORTIP;
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

