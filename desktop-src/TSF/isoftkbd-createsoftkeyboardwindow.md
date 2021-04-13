---
title: ISOFT kbd-Methode von "samatesoftkeyboardwindow" ("Soft-BDC. h")
description: Mit der isoftkbd-Methode "kreatesoftkeyboardwindow" wird ein vorläufiges Tastatur Fenster erstellt.
ms.assetid: e9aa9d88-d0bb-407f-9b53-98c8747be5d3
keywords:
- "\"Kreatesoftkeyboardwindow\"-Methode, Text Dienste-Framework"
- Kreatesoftkeyboardwindow-Methode Text Dienste-Framework, iSOFT kbd-Schnittstelle
- ISOFT kbd Interface Text Services-Framework, Methode "kreatesoftkeyboardwindow"
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0ed6f9f91f335945d40dd0b995226a400965ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518407"
---
# <a name="isoftkbdcreatesoftkeyboardwindow-method"></a>ISOFT kbd:: kreatesoftkeyboardwindow-Methode

Die **isoftkbd:: kreatesoftkeyboardwindow** -Methode erstellt ein weiches Tastatur Fenster.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateSoftKeyboardWindow(
  [in] HWND          hOwner,
  [in] TITLEBAR_TYPE Titlebar_type,
  [in] INT           xPos,
  [in] INT           yPos,
  [in] INT           width,
  [in] INT           height
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*howner* \[ in\]
</dt> <dd>

Handle des Fensters, das die weiche Tastatur enthalten soll.

</dd> <dt>

*TitleBar- \_ Typ* \[ in\]
</dt> <dd>

Der Typ der Titelleiste für das weiche Tastatur Fenster. Mögliche Typen werden durch die [**TitleBar- \_ Typenumeration**](titlebar-type.md) definiert.

</dd> <dt>

*xPos* \[ in\]
</dt> <dd>

Die x-Position der oberen linken Ecke des Soft Tastatur Fensters.

</dd> <dt>

*yPos* \[ in\]
</dt> <dd>

Die y-Position der oberen linken Ecke des Soft Tastatur Fensters.

</dd> <dt>

*Breite* \[ in\]
</dt> <dd>

Die Breite des Soft Tastatur Fensters.

</dd> <dt>

*Höhe* \[ in\]
</dt> <dd>

Die Höhe des Soft Tastatur Fensters.

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
</dt> <dt>

[**ISOFT kbd::D estroysoft keyboardwindow**](isoftkbd-destroysoftkeyboardwindow.md)
</dt> <dt>

[**Iweichkbd:: ShowSoft Keyboard**](isoftkbd-showsoftkeyboard.md)
</dt> <dt>

[**TitleBar- \_ Typ**](titlebar-type.md)
</dt> </dl>

 

 





