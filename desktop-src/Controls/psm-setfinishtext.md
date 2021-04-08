---
title: PSM_SETFINISHTEXT Meldung (prsht. h)
description: Legt den Text der Schaltfläche Fertigstellen in einem Assistenten fest, zeigt die Schaltfläche an und aktiviert Sie und blendet die Schaltflächen weiter und zurück aus. Sie können diese Nachricht explizit oder mithilfe des propsheet- \_ Makros setfinishtext senden.
ms.assetid: fa89c6d7-9ab7-4e7c-ba08-d665420492a3
keywords:
- Windows-Steuerelemente für PSM_SETFINISHTEXT Meldung
topic_type:
- apiref
api_name:
- PSM_SETFINISHTEXT
- PSM_SETFINISHTEXTA
- PSM_SETFINISHTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08195cddc96c8b92f403be6940f31099e21151f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740097"
---
# <a name="psm_setfinishtext-message"></a>PSM \_ setfinishtext-Nachricht

Legt den Text der Schaltfläche **Fertig** stellen in einem Assistenten fest, zeigt die Schaltfläche an und aktiviert Sie und blendet die Schaltflächen **weiter** und **zurück** aus. Sie können diese Nachricht explizit oder mithilfe des [**propsheet-Makros \_ setfinishtext**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf den neuen Text für die Schaltfläche **Fertig** stellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Standardmäßig verfügt die Schaltfläche **Fertig** stellen nicht über eine Tastatur Beschleunigung. Sie können eine Zugriffstaste mit dieser Meldung erstellen, indem Sie in die Text Zeichenfolge, die Sie *LPARAM* zuweisen, ein kaufmännisches und-Zeichen (&) einschließen. Beispielsweise definiert "&Finish" F als Zugriffstaste.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **PSM \_ Setfinishtextw** (Unicode) und **PSM \_ setfinishtexta** (ANSI)<br/>    |



 

 





