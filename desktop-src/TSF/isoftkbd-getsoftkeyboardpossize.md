---
title: ISoftware. getsoft keyboardpossize-Methode (Software BDC. h)
description: Mit der isoftkbd getsoftkeyboardpossize-Methode werden die Anfangsposition und die Größe einer Soft Tastatur abgerufen.
ms.assetid: d4482e34-1723-4fe2-a488-e7c18eb3f68e
keywords:
- Getsoft keyboardpossize-Methode, Text Dienste-Framework
- Getsoft keyboardpossize-Methode, Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services-Framework, getsoft keyboardpossize-Methode
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9af445efd3e1b510280d20667862f2d95404597f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340908"
---
# <a name="isoftkbdgetsoftkeyboardpossize-method"></a>ISOFT kbd:: getsoft keyboardpossize-Methode

Mit der **isoftkbd:: getsoftkeyboardpossize** -Methode werden die Anfangsposition und die Größe einer Soft Tastatur abgerufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSoftKeyboardPosSize(
  [out] POINT *lpStartPoint,
  [out] WORD  *lpwidth,
  [out] WORD  *lpheight
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpstartpoint* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Puffer, in dem diese Methode eine [Punkt](/previous-versions//dd162805(v=vs.85)) Struktur abruft, die die Koordinaten der oberen linken Position der Soft Tastatur angibt.

</dd> <dt>

*lpwidth* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen Puffer, in dem diese Methode die Breite der Soft Tastatur abruft.

</dd> <dt>

*lpheight* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen Puffer, in dem diese Methode die Höhe der Soft Tastatur abruft.

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
</dt> <dt>

[**ISOFT kbd:: setsoftware keyboardpossize**](isoftkbd-setsoftkeyboardpossize.md)
</dt> </dl>

 

