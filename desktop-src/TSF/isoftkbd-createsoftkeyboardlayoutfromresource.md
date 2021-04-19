---
title: ISOFT kbd-Methode für die Methode "deesoftkeyboardlayoutfromresource" ("Soft-BDC. h")
description: Die Methode isoftkbd kreatesoftkeybboardlayoutfromresource erstellt ein weiches Tastaturlayout aus der angegebenen Ressource.
ms.assetid: c1b2f8bd-8065-426d-9c23-67fa46a33dc8
keywords:
- Kreatesoftkeyboardlayoutfromresource-Methode Text Dienst-Framework
- Kreatesoftkeyboardlayoutfromresource-Methode Text Dienst Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services Framework, Methode "kreatesoftkeyboardlayoutfromresource"
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromResource
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f454b5d8f3366517d91170d6a92d6a9dbed5764
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342641"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromresource-method"></a>ISOFT kbd:: kreatesoftkeyboardlayoutfromresource-Methode

Die **isoftkbd:: deesoftkeybboardlayoutfromresource** -Methode erstellt ein weiches Tastaturlayout aus der angegebenen Ressource.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateSoftKeyboardLayoutFromResource(
  [in]  WCHAR *lpszResFile,
  [in]  WCHAR *lpszResType,
  [in]  WCHAR *lpszXMLResString,
  [out] DWORD *lpdwLayoutCookie
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszresfile* \[ in\]
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen der Ressourcen Datei angibt.

</dd> <dt>

*lpszrestype* \[ in\]
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Typ der Ressource angibt.

</dd> <dt>

*lpszxmlresstring* \[ in\]
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die die Ressource identifiziert.

</dd> <dt>

*lpdwlayoutcookie* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf den Puffer, in dem diese Methode ein weiches Tastaturlayout-Cookie abruft.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                        | BESCHREIBUNG                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode war erfolgreich.<br/>          |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Mindestens ein Parameter ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Software-Domänen Controller. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Software. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iweichkbd**](isoftkbd.md)
</dt> <dt>

[**Iweichkbd:: erkreatesoftkeyboardlayoutfromxmlfile**](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)
</dt> <dt>

[**Iweichkbd:: ShowSoft Keyboard**](isoftkbd-showsoftkeyboard.md)
</dt> </dl>

 

 





