---
title: ISoftKbd CreateSoftKeyboardWindow-Methode (Softkbdc.h)
description: Die ISoftKbd CreateSoftKeyboardWindow-Methode erstellt ein softes Tastaturfenster.
ms.assetid: e9aa9d88-d0bb-407f-9b53-98c8747be5d3
keywords:
- CreateSoftKeyboardWindow-Methode Textdienstframework
- CreateSoftKeyboardWindow-Methode Textdienstframework , ISoftKbd-Schnittstelle
- ISoftKbd-Schnittstelle Textdienstframework , CreateSoftKeyboardWindow-Methode
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
ms.openlocfilehash: 7953ce70385585349ee905f83e999fb2fc4d71402d2baada413452c729032cc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952729"
---
# <a name="isoftkbdcreatesoftkeyboardwindow-method"></a>ISoftKbd::CreateSoftKeyboardWindow-Methode

Die **ISoftKbd::CreateSoftKeyboardWindow-Methode** erstellt ein softes Tastaturfenster.

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

*hOwner* \[ In\]
</dt> <dd>

Handle des Fensters, das die Softtastatur enthalten soll.

</dd> <dt>

Geben Sie in *die Titelleiste \_ ein.* \[\]
</dt> <dd>

Typ der Titelleiste für das Softtastaturfenster. Mögliche Typen werden durch die [**TITLEBAR \_ TYPE-Enumeration**](titlebar-type.md) definiert.

</dd> <dt>

*xPos* \[ In\]
</dt> <dd>

Die x-Position der oberen linken Ecke des soft-Tastaturfensters.

</dd> <dt>

*yPos* \[ In\]
</dt> <dd>

Die y-Position der oberen linken Ecke des soft-Tastaturfensters.

</dd> <dt>

*Breite* \[ In\]
</dt> <dd>

Die Breite des soften Tastaturfensters.

</dd> <dt>

*Höhe* \[ In\]
</dt> <dd>

Die Höhe des soft-Tastaturfensters.

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
| Verteilbare Komponente<br/>          | TSF 1.0 on Windows 2000 Professional<br/>                                        |
| Header<br/>                   | <dl> <dt>Softkbdc.h</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Softkbd.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::CreateSoftKeyboardLayoutFromResource**](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> <dt>

[**ISoftKbd::D estsoftKeyboardWindow**](isoftkbd-destroysoftkeyboardwindow.md)
</dt> <dt>

[**ISoftKbd::ShowSoftKeyboard**](isoftkbd-showsoftkeyboard.md)
</dt> <dt>

[**\_TITLEBAR-TYP**](titlebar-type.md)
</dt> </dl>

 

 





