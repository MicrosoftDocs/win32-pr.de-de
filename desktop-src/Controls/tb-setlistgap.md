---
title: TB_SETLISTGAP Meldung (kommstrg. h)
description: Legt den Abstand zwischen den Symbolleisten-Schaltflächen auf einer bestimmten Symbolleiste fest.
ms.assetid: ca8ba6e4-cf70-41ca-ac61-cd13671d4010
keywords:
- Windows-Steuerelemente für TB_SETLISTGAP Meldung
topic_type:
- apiref
api_name:
- TB_SETLISTGAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 224a709b7beefcfdf49ea7838f905977487aca8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858634"
---
# <a name="tb_setlistgap-message"></a>TB \_ setlistgap-Nachricht

Legt den Abstand zwischen den Symbolleisten-Schaltflächen auf einer bestimmten Symbolleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Lücke zwischen den Schaltflächen auf der Symbolleiste in Pixel.

</dd> <dt>

*lParam* 
</dt> <dd>

Ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Die Lücke zwischen Schaltflächen gilt nur für das Symbolleisten-Steuerelement, das diese Nachricht empfängt. Der Empfang dieser Nachricht löst eine neupaint der Symbolleiste aus, wenn die Symbolleiste momentan sichtbar ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





