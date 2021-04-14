---
title: PSM_QUERYSIBLINGS Meldung (prsht. h)
description: Wird an ein Eigenschaften Blatt gesendet, das die Nachricht dann an jede Ihrer Seiten weiterleitet. Sie können diese Nachricht explizit oder mithilfe des propsheet \_ querysiblings-Makros senden.
ms.assetid: 96f48847-b7b8-4d6f-8bde-ada915b7c962
keywords:
- Windows-Steuerelemente für PSM_QUERYSIBLINGS Meldung
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
ms.openlocfilehash: ea5943fefa906475e34d1cc7acc7f8a86cd99252
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517966"
---
# <a name="psm_querysiblings-message"></a>PSM- \_ querysiblings-Meldung

Wird an ein Eigenschaften Blatt gesendet, das die Nachricht dann an jede Ihrer Seiten weiterleitet. Sie können diese Nachricht explizit oder mithilfe des [**propsheet \_ querysiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der erste Anwendungs definierte Parameter.

</dd> <dt>

*lParam* 
</dt> <dd>

Der zweite Anwendungs definierte Parameter.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert ungleich 0 (null) von einer Seite im Eigenschaften Blatt zurück, oder NULL, wenn keine Seite einen Wert ungleich 0 (null) zurückgibt.

## <a name="remarks"></a>Bemerkungen

Wenn eine Seite einen Wert ungleich 0 (null) zurückgibt, sendet das Eigenschaften Blatt die Nachricht nicht an nachfolgende Seiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





