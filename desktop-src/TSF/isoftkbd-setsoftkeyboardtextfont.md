---
title: Icdkbd setsoft keyboardtextfont-Methode (Software-DC. h)
description: Die isoftkbd setsoftkeyboardtextfont-Methode legt die Text Schriftart fest, die von einer Soft Tastatur verwendet wird.
ms.assetid: 14705723-4592-40ef-9ebb-1c44c10c3cda
keywords:
- Setsoft keyboardtextfont-Methode Text Services-Framework
- Setsoft keyboardtextfont-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services-Framework, setsoft keyboardtextfont-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ff0a9adce61bc1a671d28c6e5d6ac5b6d329b42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342859"
---
# <a name="isoftkbdsetsoftkeyboardtextfont-method"></a>ISOFT kbd:: setsoft keyboardtextfont-Methode

Die **isoftkbd:: setsoftkeyboardtextfont** -Methode legt die Text Schriftart fest, die von einer Soft Tastatur verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSoftKeyboardTextFont(
  [in] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*plogfont* \[ in\]
</dt> <dd>

Zeiger auf eine [**logfontw**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur, die die Text Schriftart für die weiche Tastatur definiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                        | BESCHREIBUNG                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode war erfolgreich.<br/>           |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der *plogfont* -Parameter ist ungültig.<br/> |



 

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

[**Iweichkbd:: getsoftware keyboardtextfont**](isoftkbd-getsoftkeyboardtextfont.md)
</dt> </dl>

 

