---
title: EM_SETTARGETDEVICE Meldung (RichEdit. h)
description: Legt das Zielgerät und die für \ 0034 verwendete Linienbreite fest. was Sie sehen, ist das, was Sie erhalten \ 0034; (WYSIWYG) Formatierung in einem Rich-Edit-Steuerelement.
ms.assetid: dfc829f5-e711-419e-abb5-c1e8df994c4a
keywords:
- Windows-Steuerelemente für EM_SETTARGETDEVICE Meldung
topic_type:
- apiref
api_name:
- EM_SETTARGETDEVICE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f82d6ee5df86572564cffcf192395ccee1fbd05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104216"
---
# <a name="em_settargetdevice-message"></a>EM \_ SetTargetDevice-Meldung

Legt das Zielgerät und die Linienbreite fest, die für die Formatierung "was Sie sehen, was Sie erhalten" (WYSIWYG) in einem Rich-Edit-Steuerelement verwendet wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

HDC für das Zielgerät.

</dd> <dt>

*lParam* 
</dt> <dd>

Linienstärke, die für die Formatierung verwendet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist 0 (null), wenn der Vorgang fehlschlägt, oder ungleich NULL, wenn er erfolgreich ist.

## <a name="remarks"></a>Bemerkungen

Der HDC für den Standarddrucker kann wie folgt abgerufen werden.


```
PRINTDLG pd = { sizeof(pd) };
pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
if (PrintDlg(&pd))
{
    HDC hdc = pd.hDC;
    ...
}
```



Wenn *LPARAM* gleich 0 (null) ist, werden keine Zeilenumbrüche erstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





