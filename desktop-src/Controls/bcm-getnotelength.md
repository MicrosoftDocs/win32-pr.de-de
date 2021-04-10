---
title: BCM_GETNOTELENGTH Meldung (kommstrg. h)
description: Ruft die Länge des Notiz Texts ab, der in der Beschreibung für eine Befehls Link Schaltfläche angezeigt werden kann. Senden Sie diese Nachricht explizit oder mithilfe der Schaltfläche \_ getnotelength-Makro.
ms.assetid: 62385485-b553-47e9-9f15-696cc4694752
keywords:
- Windows-Steuerelemente für BCM_GETNOTELENGTH Meldung
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
ms.openlocfilehash: 1b33c5245778481033bd97326c3d66a40bf03210
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040511"
---
# <a name="bcm_getnotelength-message"></a>BCM \_ getnotelength-Meldung

Ruft die Länge des Notiz Texts ab, der in der Beschreibung für eine Befehls Link Schaltfläche angezeigt werden kann. Senden Sie diese Nachricht explizit oder mithilfe der [**Schaltfläche \_ getnotelength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) -Makro.

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

Gibt die Länge des Notiz Texts in **WCHARs** zurück, ohne abschließende **null**-Werte, oder 0 (null), wenn kein Hinweis Text vorhanden ist.

## <a name="remarks"></a>Bemerkungen

Ab ComCtl32 dll, Version 6,01, können Befehls Link Schaltflächen einen Hinweis enthalten. Weitere Informationen zu DLL-Versionen finden Sie unter [allgemeine Steuerelement Versionen](common-control-versions.md).

Die **BCM \_ getnotelength** -Nachricht funktioniert nur mit den Schaltflächen Stilen " [**SB \_ CommandLink**](button-styles.md) " und " [**SB \_ defcommandlink**](button-styles.md) ".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[Schaltflächenstile](button-styles.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Schaltflächentypen](button-types-and-styles.md)
</dt> </dl>

 

 





