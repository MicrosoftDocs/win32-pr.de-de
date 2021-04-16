---
title: ISOFT kbd enumsoft Keyboard-Methode (Software-Domänen Controller. h)
description: Die isoftkbd enumsoftkeyboard-Methode listet die möglichen weichen Tastaturen auf, die die angegebene Sprache unterstützen.
ms.assetid: c71f99e5-c4c2-4b09-a58f-d3f4348d0c5d
keywords:
- Enumsoft Keyboard-Methode, Text Dienste-Framework
- Enumsoft Keyboard-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services Framework, enumsoft Keyboard-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.EnumSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ecdb083684163798a68674628a8b1abc2460268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478000"
---
# <a name="isoftkbdenumsoftkeyboard-method"></a>Iweichkbd:: enumsoft Keyboard-Methode

Die **isoftkbd:: enumsoftkeyboard** -Methode listet die möglichen weichen Tastaturen auf, die die angegebene Sprache unterstützen.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnumSoftKeyboard(
  [in]  LANGID langid,
  [out] DWORD  *lpdwKeyboard
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*LangID* \[ in\]
</dt> <dd>

Der Sprachen Bezeichner.

</dd> <dt>

*lpdwkeyboard* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen Puffer, in dem diese Methode Bezeichner der verfügbaren Soft Tastaturen abruft.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                        | BESCHREIBUNG                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode war erfolgreich.<br/>         |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Der *LangID* -Parameter ist ungültig.<br/> |



 

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
</dt> </dl>

 

 





