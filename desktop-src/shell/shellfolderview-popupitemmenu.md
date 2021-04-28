---
description: 'ShellFolderView.PopupItemMenu-Methode: Erstellt ein Kontextmenü für das angegebene Element und gibt die ausgewählte Befehlszeichenfolge zurück.'
title: ShellFolderView.PopupItemMenu-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.PopupItemMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 1610d91e-87c3-4ba5-9147-1595eddb2c3a
ms.openlocfilehash: cb862ba159f55d3ab82495ddeb32a87f3ce1901b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083388"
---
# <a name="shellfolderviewpopupitemmenu-method"></a>ShellFolderView.PopupItemMenu-Methode

Erstellt ein Kontextmenü für das angegebene Element und gibt die ausgewählte Befehlszeichenfolge zurück.

## <a name="syntax"></a>Syntax


```JScript
retVal = ShellFolderView.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vItem* \[ In\]
</dt> <dd>

Typ: **Variant**

Das [**FolderItem-Objekt,**](folderitem.md) für das das Kontextmenü erstellt wird.

</dd> <dt>

*vx* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Die horizontale Position des Menüs in Bildschirmkoordinaten.

</dd> <dt>

*vy* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Die vertikale Position des Menüs in Bildschirmkoordinaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)\***

Die **Zeichenfolge,** die die Befehlszeichenfolge empfängt.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 
