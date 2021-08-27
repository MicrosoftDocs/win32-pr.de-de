---
title: PSM_SETFINISHTEXT-Nachricht (Prsht.h)
description: Legt den Text der Schaltfläche Fertig stellen in einem Assistenten fest, zeigt die Schaltfläche an und aktiviert sie und blendet die Schaltflächen Weiter und Zurück aus. Sie können diese Nachricht explizit oder mithilfe des \_ PropSheet-Makros SetFinishText senden.
ms.assetid: fa89c6d7-9ab7-4e7c-ba08-d665420492a3
keywords:
- PSM_SETFINISHTEXT Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 5a08cafbeafeccb2235cb9b653f997aa8c60bd5fd21a3ccbc92e572fa5d3d0db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088560"
---
# <a name="psm_setfinishtext-message"></a>PSM \_ SETFINISHTEXT-Nachricht

Legt den Text der Schaltfläche **Fertig stellen** in einem Assistenten fest, zeigt die Schaltfläche an und aktiviert sie und blendet die Schaltflächen **Weiter** und **Zurück** aus. Sie können diese Nachricht explizit oder mithilfe des [**\_ PropSheet-Makros SetFinishText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf den neuen Text für die Schaltfläche **Fertig stellen.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Standardmäßig verfügt die Schaltfläche **Fertig stellen** nicht über eine Tastaturbeschleunigung. Sie können eine Tastaturbeschleunigung mit dieser Meldung erstellen, indem Sie ein ampersand (&) in die Textzeichenfolge einfügen, die Sie *lParam* zuweisen. Beispielsweise definiert "&Finish" F als Zugriffstaste.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **PSM \_ SETFINISHTEXTW** (Unicode) und **PSM \_ SETFINISHTEXTA** (ANSI)<br/>    |



 

 





