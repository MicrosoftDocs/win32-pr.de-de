---
title: ISoftware. getsoft keyboardtextfont-Methode (Software-DC. h)
description: Die isoftkbd getsoftkeyboardtextfont-Methode ruft die von einer Soft Tastatur verwendete Text Schriftart ab.
ms.assetid: 73239359-70b4-47d6-abc5-9fee279ed3a6
keywords:
- Getsoft keyboardtextfont-Methode Text Services-Framework
- Getsoft keyboardtextfont-Methode Text Services-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services Framework, getsoft keyboardtextfont-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce939347042415a9060459102cd8a56665ac2de0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105249"
---
# <a name="isoftkbdgetsoftkeyboardtextfont-method"></a>Iweichkbd:: getsoft keyboardtextfont-Methode

Die **isoftkbd:: getsoftkeyboardtextfont** -Methode ruft die von einer Soft Tastatur verwendete Text Schriftart ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSoftKeyboardTextFont(
  [out] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*plogfont* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, in dem diese Methode eine [**logfontw**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur abruft, die die Text Schriftart für die weiche Tastatur definiert.

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

[**Icdkbd:: setsoftware keyboardtextfont**](isoftkbd-setsoftkeyboardtextfont.md)
</dt> </dl>

 

