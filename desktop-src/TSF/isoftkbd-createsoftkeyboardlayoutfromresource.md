---
title: ISoftKbd CreateSoftKeyboardLayoutFromResource-Methode (Softkbdc.h)
description: Die ISoftKbd CreateSoftKeybboardLayoutFromResource-Methode erstellt ein weiches Tastaturlayout aus der angegebenen Ressource.
ms.assetid: c1b2f8bd-8065-426d-9c23-67fa46a33dc8
keywords:
- CreateSoftKeyboardLayoutFromResource-Textdienstframework
- CreateSoftKeyboardLayoutFromResource-Methode Textdienstframework , ISoftKbd-Schnittstelle
- ISoftKbd-Schnittstelle Textdienstframework , CreateSoftKeyboardLayoutFromResource-Methode
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
ms.openlocfilehash: 9bc76d54bc01f453559107576370bf1b1b4e1615c232cbb07599d6dafe56e8b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952895"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromresource-method"></a>ISoftKbd::CreateSoftKeyboardLayoutFromResource-Methode

Die **ISoftKbd::CreateSoftKeybboardLayoutFromResource-Methode** erstellt ein weiches Tastaturlayout aus der angegebenen Ressource.

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

*lpszResFile* \[ In\]
</dt> <dd>

Zeiger auf eine mit 0 (null) beendete Zeichenfolge, die den Namen der Ressourcendatei angibt.

</dd> <dt>

*lpszResType* \[ In\]
</dt> <dd>

Zeiger auf eine mit 0 (null) beendete Zeichenfolge, die den Typ der Ressource angibt.

</dd> <dt>

*lpszXMLResString* \[ In\]
</dt> <dd>

Zeiger auf eine auf 0 (null) beendete Zeichenfolge, die die Ressource identifiziert.

</dd> <dt>

*lpdwLayoutCookie* \[ out\]
</dt> <dd>

Zeiger auf den Puffer, in dem diese Methode ein Softtastaturlayoutcookie abruft.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                        | Beschreibung                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode war erfolgreich.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Mindestens ein Parameter ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Verteilbare Komponente<br/>          | TSF 1.0 auf Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile**](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)
</dt> <dt>

[**ISoftKbd::ShowSoftKeyboard**](isoftkbd-showsoftkeyboard.md)
</dt> </dl>

 

 





