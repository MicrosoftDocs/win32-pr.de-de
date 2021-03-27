---
description: Erstellt ein Kontextmenü für das angegebene Element und gibt die ausgewählte Befehls Zeichenfolge zurück.
title: Shellfolderview. popupitemmenu-Methode (Shldisp. h)
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
ms.openlocfilehash: 513f654442361da840cb02089810c814275c5867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217692"
---
# <a name="shellfolderviewpopupitemmenu-method"></a>Shellfolderview. popupitemmenu-Methode

Erstellt ein Kontextmenü für das angegebene Element und gibt die ausgewählte Befehls Zeichenfolge zurück.

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

*vitem* \[ in\]
</dt> <dd>

Typ: **Variant**

Das [**folderItem**](folderitem.md) -Objekt, für das das Kontextmenü erstellt wird.

</dd> <dt>

*VX* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Die horizontale Position des Menüs in Bildschirm Koordinaten.

</dd> <dt>

*Vy* \[ in, optional\]
</dt> <dd>

Typ: **Variant**

Die vertikale Position des Menüs in Bildschirm Koordinaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie Folgendes ein: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _

Die _ *String**, die die Befehls Zeichenfolge empfängt.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |



 

 
