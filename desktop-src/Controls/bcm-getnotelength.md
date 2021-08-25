---
title: BCM_GETNOTELENGTH Meldung (Commctrl.h)
description: Ruft die Länge des Hinweistexts ab, der in der Beschreibung für eine Befehlslinkschaltfläche angezeigt werden kann. Senden Sie diese Nachricht explizit oder mithilfe des \_ Schaltflächenmakros GetNoteLength.
ms.assetid: 62385485-b553-47e9-9f15-696cc4694752
keywords:
- BCM_GETNOTELENGTH Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- BCM_GETNOTELENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 385cb5d7694818a0e0e03ab74bcc31b76d13f5d304c7415b1f70a0fd43e1b31b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921660"
---
# <a name="bcm_getnotelength-message"></a>BCM \_ GETNOTELENGTH-Nachricht

Ruft die Länge des Hinweistexts ab, der in der Beschreibung für eine Befehlslinkschaltfläche angezeigt werden kann. Senden Sie diese Nachricht explizit oder mithilfe des [**\_ Schaltflächenmakros GetNoteLength.**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength)

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Muss Null sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Länge des Notiztexts in **WCHARs** zurück, einschließlich aller abschließenden NULL-Werte oder **0**(null), wenn kein Notiztext vorhanden ist.

## <a name="remarks"></a>Hinweise

Ab comctl32 DLL Version 6.01 können Befehlslinkschaltflächen einen Hinweis enthalten. Informationen zu DLL-Versionen finden Sie unter [Allgemeine Steuerungsversionen.](common-control-versions.md)

Die **BCM \_ GETNOTELENGTH-Nachricht** funktioniert nur mit den Schaltflächenstilen [**BS \_ COMMANDLINK**](button-styles.md) und [**BS \_ DEFCOMMANDLINK.**](button-styles.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[Schaltflächenstile](button-styles.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Schaltflächentypen](button-types-and-styles.md)
</dt> </dl>

 

 





