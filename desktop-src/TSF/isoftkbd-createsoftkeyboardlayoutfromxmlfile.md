---
title: ISOFT kbd-Methode für die Methode "deesoftkeyboardlayoutfromxmlfile" (Software-Domänen Controller. h)
description: Die Methode isoftkbd kreatesoftkeyboardlayoutfromxmlfile erstellt ein weiches Tastaturlayout aus der angegebenen XML-Datei.
ms.assetid: e665adab-1d75-4e41-87bf-c8ce0f7a0399
keywords:
- "\"Kreatesoftkeyboardlayoutfromxmlfile\"-Methode Text Dienst-Framework"
- "\"Kreatesoftkeyboardlayoutfromxmlfile\"-Methode Text Dienste-Framework, iSOFT kbd-Schnittstelle"
- ISOFT kbd Interface Text Services Framework, Methode "kreatesoftkeyboardlayoutfromxmlfile"
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromXMLFile
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9252db845c5e1cc732adc295e1989fee83d4ac6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346317"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromxmlfile-method"></a>ISOFT kbd:: kreatesoftkeyboardlayoutfromxmlfile-Methode

Die **isoftkbd:: deesoftkeyboardlayoutfromxmlfile** -Methode erstellt ein weiches Tastaturlayout aus der angegebenen XML-Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateSoftKeyboardLayoutFromXMLFile(
  [in]  WCHAR *lpszKeyboardDesFile,
  [in]  INT   szFileStrLen,
  [out] DWORD *pdwLayoutCookie
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpszkeyboarddesfile* \[ in\]
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen der XML-Datei angibt.

</dd> <dt>

*szfilestrinlen* \[ in\]
</dt> <dd>

Eine 0-terminierte Zeichenfolge, die die Länge der XML-Datei angibt.

</dd> <dt>

*pdwlayoutcookie* \[ vorgenommen\]
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

[**ISOFT kbd:: kreatesoftkeyboardlayoutfromresource**](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> </dl>

 

 





