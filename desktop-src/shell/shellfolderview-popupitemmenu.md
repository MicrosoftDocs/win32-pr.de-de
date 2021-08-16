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
ms.openlocfilehash: cf538a468e9664810e4a6869e47629adc585bea8ce81431cf3c0de3c583f5285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968439"
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



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 
