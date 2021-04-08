---
title: BCM_GETTEXTMARGIN Meldung (kommstrg. h)
description: Ruft die Ränder ab, mit denen Text in einem Schaltflächen-Steuerelement gezeichnet wird. Sie können diese Nachricht explizit senden oder das gettextmargin-Makro der Schaltfläche verwenden \_ .
ms.assetid: 6c141752-e636-41c4-9d05-df8b320ff59f
keywords:
- Windows-Steuerelemente für BCM_GETTEXTMARGIN Meldung
topic_type:
- apiref
api_name:
- BCM_GETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6a7d809207c21c74a36c796a9035ed0e3772481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949779"
---
# <a name="bcm_gettextmargin-message"></a>BCM \_ gettextmargin-Meldung

Ruft die Ränder ab, mit denen Text in einem Schaltflächen-Steuerelement gezeichnet wird. Sie können diese Nachricht explizit senden oder das [**\_ gettextmargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) -Makro der Schaltfläche verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die die Ränder enthält, die zum Zeichnen von Text verwendet werden sollen.

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



 

