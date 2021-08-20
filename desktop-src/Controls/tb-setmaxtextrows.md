---
title: TB_SETMAXTEXTROWS (Commctrl.h)
description: Legt die maximale Anzahl von Textzeilen fest, die auf einer Symbolleistenschaltfläche angezeigt werden.
ms.assetid: a14d74e8-cc21-482d-9bca-38dc7c0528ec
keywords:
- TB_SETMAXTEXTROWS von Windows Steuerelementen
topic_type:
- apiref
api_name:
- TB_SETMAXTEXTROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d6a1e1a2cda7b3dced4cf538623578d48b41d38925629f2985a35974baed229
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167480"
---
# <a name="tb_setmaxtextrows-message"></a>TB \_ SETMAXTEXTROWS-Meldung

Legt die maximale Anzahl von Textzeilen fest, die auf einer Symbolleistenschaltfläche angezeigt werden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Maximale Anzahl von Textzeilen, die angezeigt werden können.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) oder andernfalls 0 (null) zurück.

## <a name="remarks"></a>Hinweise

Damit Text umbrechen kann, müssen Sie die maximale Schaltflächenbreite festlegen, indem Sie eine [**TB \_ SETBUTTONWIDTH-Nachricht**](tb-setbuttonwidth.md) senden. Der Text wird bei einem Zeilenumbruch umbruchgeumbruchen. Zeilenumbrüche (" \\ n") im Text werden ignoriert. Text in TBSTYLE \_ LIST-Symbolleisten wird immer in einer einzelnen Zeile angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





