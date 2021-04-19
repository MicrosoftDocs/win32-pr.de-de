---
description: Unterklassen alle Steuerelemente in einem Dialogfeld und im Dialogfenster selbst.
ms.assetid: 4d3c298b-07ba-4668-badd-dddecc389e70
title: Ctl3dSubclassDlgEx-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassDlgEx
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 6e29f65d5ddc3d0d9a7de05eef88b7a662e0e43f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370302"
---
# <a name="ctl3dsubclassdlgex-function"></a>Ctl3dSubclassDlgEx-Funktion

Unterklassen alle Steuerelemente in einem Dialogfeld und im Dialogfenster selbst.

## <a name="syntax"></a>Syntax


```C++
PUBLIC BOOL FAR PASCAL Ctl3dSubclassDlgEx(
   HWND  hwndDlg,
   DWORD grbit
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwnddlg* 
</dt> <dd>

Ein Handle für das Dialogfeld Fenster.

</dd> <dt>

*grbit* 
</dt> <dd>

Die Steuerelement Typen, die unter klassifiziert werden sollen. Dieser Wert kann einer der folgenden Werte sein:



| Wert                                                                                                                                                                                                                                     | Bedeutung                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="CTL3D_BUTTONS"></span><span id="ctl3d_buttons"></span><dl> <dt>**Ctl3d \_ Schalt**</dt> Flächen <dt>0x0001</dt> </dl>                 | Unterklassen Schaltflächen.<br/>                  |
| <span id="CTL3D_LISTBOXES"></span><span id="ctl3d_listboxes"></span><dl> <dt>**Ctl3d \_ ListBoxes**</dt> <dt>0x0002</dt> </dl>           | Listenfelder der Unterklasse.<br/>               |
| <span id="CTL3D_EDITS"></span><span id="ctl3d_edits"></span><dl> <dt>**Ctl3d \_ Bearbeitet**</dt> <dt>0x0004</dt> </dl>                       | Bearbeitungs Steuerelemente der Unterklasse.<br/>            |
| <span id="CTL3D_COMBOS"></span><span id="ctl3d_combos"></span><dl> <dt>**Ctl3d \_ Combos**</dt> <dt>0x0008</dt> </dl>                    | Kombinations Felder der Unterklasse.<br/>              |
| <span id="CTL3D_STATICTEXTS"></span><span id="ctl3d_statictexts"></span><dl> <dt>**Ctl3d \_ Statictexts**</dt> <dt>0x0010</dt> </dl>     | Statische Text Steuerelemente der Unterklasse.<br/>     |
| <span id="CTL3D_STATICFRAMES"></span><span id="ctl3d_staticframes"></span><dl> <dt>**Ctl3d \_ Staticframes**</dt> <dt>0x0020</dt> </dl>  | Statische Rahmen der Unterklasse.<br/>            |
| <span id="CTL3D_ALL"></span><span id="ctl3d_all"></span><dl> <dt>**Ctl3d \_ Alle**</dt> <dt>0xFFFF</dt> </dl>                             | Unterklasse alle-Steuerelemente.<br/>             |
| <span id="CTL3D_NODLGWINDOW"></span><span id="ctl3d_nodlgwindow"></span><dl> <dt>**Ctl3d \_ Nodlgwindow**</dt> <dt>0x00010000 bis</dt> </dl> | Die Unterklasse des Dialogfensters ist nicht.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn die Funktion erfolgreich ausgeführt wurde. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist besonders nützlich für Anwendungen, die auf C++ basieren.

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
