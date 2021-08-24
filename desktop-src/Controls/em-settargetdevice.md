---
title: EM_SETTARGETDEVICE Nachricht (Richedit.h)
description: Legt das Zielgerät und die Linienbreite fest, die für \ 0034 verwendet werden. Sie sehen, was Sie erhalten \ 0034; (WYSIWYG)-Formatierung in einem Rich-Edit-Steuerelement.
ms.assetid: dfc829f5-e711-419e-abb5-c1e8df994c4a
keywords:
- EM_SETTARGETDEVICE Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 2d9a3cd4e59f3800b91fedee446e927ab0ec39988474752561a04dace5572ef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697590"
---
# <a name="em_settargetdevice-message"></a>EM \_ SETTARGETDEVICE-Meldung

Legt die Zielgeräte- und Linienbreite fest, die für die Formatierung "Was Sie sehen, was Sie erhalten" (WYSIWYG) in einem Rich-Edit-Steuerelement verwendet wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

HDC für das Zielgerät.

</dd> <dt>

*lParam* 
</dt> <dd>

Linienbreite, die für die Formatierung verwendet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist 0 (null), wenn der Vorgang fehlschlägt, oder ungleich 0 (null), wenn er erfolgreich ist.

## <a name="remarks"></a>Hinweise

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



Wenn *lParam 0* (null) ist, werden keine Zeilenumbrüche erstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





