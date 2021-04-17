---
title: ISOFT kbd showkeysforkeyscanmode-Methode ("Soft kbdc. h")
description: Die isoftkbd showkeysforkeyscanmode-Methode zeigt die Schlüssel an, die für den Schlüssel Scan Modus für eine weiche Tastatur verwendet werden.
ms.assetid: bfa76e5b-6f6e-470a-ba3a-7ecff9f67f7b
keywords:
- Showkeysforkeyscanmode-Methode, Text Dienste-Framework
- Showkeysforkeyscanmode-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services Framework, showkeysforkeyscanmode-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.ShowKeysForKeyScanMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c46fbfc103c0ba40294e4c149d5fd427296765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478204"
---
# <a name="isoftkbdshowkeysforkeyscanmode-method"></a>ISOFT kbd:: showkeysforkeyscanmode-Methode

Die **isoftkbd:: showkeysforkeyscanmode** -Methode zeigt die Schlüssel an, die für den Schlüssel Scan Modus für eine weiche Tastatur verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT ShowKeysForKeyScanMode(
  [in] KEYID *lpKeyID,
  [in] INT   iKeyNum,
  [in] BOOL  fHighL
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpkeyid* \[ in\]
</dt> <dd>

Ein Zeiger auf ein Array von keyid-Elementen, die die Bezeichner von Schlüsseln angeben, die angezeigt werden sollen.

</dd> <dt>

*ikeynum* \[ in\]
</dt> <dd>

Die Anzahl der anzuzeigenden Schlüssel.

</dd> <dt>

vollständig  \[ in\]
</dt> <dd>

TRUE, wenn die-Methode die Schlüssel hervorheben soll, andernfalls **false** .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                        | BESCHREIBUNG                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode war erfolgreich.<br/>        |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Einer der Parameter ist ungültig.<br/> |



 

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

 

 





