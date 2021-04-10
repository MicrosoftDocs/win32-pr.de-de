---
title: EM_SHOWBALLOONTIP Meldung (kommstrg. h)
description: Die "em \_ ShowBalloonTip"-Meldung zeigt eine Sprechblase an, die einem Bearbeitungs Steuerelement zugeordnet ist.
ms.assetid: 1e6915b7-4b61-43b2-be13-b89c72378a1a
keywords:
- Windows-Steuerelemente für EM_SHOWBALLOONTIP Meldung
topic_type:
- apiref
api_name:
- EM_SHOWBALLOONTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8fc0174752ab8214873da9478a0af435be76427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104205"
---
# <a name="em_showballoontip-message"></a>EM \_ ShowBalloonTip-Meldung

Die " **EM \_ ShowBalloonTip** "-Meldung zeigt eine Sprechblase an, die einem Bearbeitungs Steuerelement zugeordnet ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**editballoontip**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip) -Struktur, die Informationen über die anzuzeigende Sprechblasen info enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, wird **true** zurückgegeben. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt. Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Editballoontip**](/windows/desktop/api/Commctrl/ns-commctrl-editballoontip)
</dt> <dt>

[**\_ShowBalloonTip bearbeiten**](/windows/desktop/api/Commctrl/nf-commctrl-edit_showballoontip)
</dt> </dl>

 

 





