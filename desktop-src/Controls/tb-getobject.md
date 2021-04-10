---
title: TB_GETOBJECT Meldung (kommstrg. h)
description: Ruft das IDropTarget-Element für ein ToolBar-Steuerelement ab.
ms.assetid: b26394ea-6f0f-4084-956d-f9166cc54b76
keywords:
- Windows-Steuerelemente für TB_GETOBJECT Meldung
topic_type:
- apiref
api_name:
- TB_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce923feaec893e6f4304eb0b993de33dc1fe2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105056"
---
# <a name="tb_getobject-message"></a>TB- \_ GetObject-Nachricht

Ruft das [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) -Element für ein ToolBar-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Bezeichner der angeforderten Schnittstelle. Dieser Wert muss auf **IID \_ IDropTarget** zeigen.

</dd> <dt>

*lParam* 
</dt> <dd>

Adresse, die den Schnittstellen Zeiger empfängt. Wenn ein Fehler auftritt, wird ein **null** -Zeiger in diese Adresse eingefügt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück, der den Erfolg oder das Fehlschlagen des Vorgangs angibt.

## <a name="remarks"></a>Bemerkungen

Das [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) der Symbolleiste wird von der Symbolleiste verwendet, wenn Objekte gezogen oder darauf abgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

