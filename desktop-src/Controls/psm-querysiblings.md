---
title: PSM_QUERYSIBLINGS (Prsht.h)
description: Wird an ein Eigenschaftenblatt gesendet, das die Nachricht dann an jede seiner Seiten weitersandt. Sie können diese Nachricht explizit oder mithilfe des PropSheet \_ QuerySiblings-Makros senden.
ms.assetid: 96f48847-b7b8-4d6f-8bde-ada915b7c962
keywords:
- PSM_QUERYSIBLINGS von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- PSM_QUERYSIBLINGS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c270a3c7a667894f7821f6c0c169115846b6ddc2492648f5f9d75a0c85d21d04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088650"
---
# <a name="psm_querysiblings-message"></a>PSM \_ QUERYSIBLINGS-Meldung

Wird an ein Eigenschaftenblatt gesendet, das die Nachricht dann an jede seiner Seiten weitersandt. Sie können diese Nachricht explizit oder mithilfe des [**PropSheet \_ QuerySiblings-Makros**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Erster anwendungsdefinierter Parameter.

</dd> <dt>

*lParam* 
</dt> <dd>

Zweiter anwendungsdefinierter Parameter.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert ungleich 0 (null) von einer Seite im Eigenschaftenblatt zurück, oder 0 (null), wenn keine Seite einen Wert ungleich 0 (null) zurückgibt.

## <a name="remarks"></a>Hinweise

Wenn eine Seite einen Wert ungleich 0 (null) zurückgibt, sendet das Eigenschaftenblatt die Nachricht nicht an nachfolgende Seiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





