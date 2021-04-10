---
title: TCM_SETEXTENDEDSTYLE Meldung (kommstrg. h)
description: Legt die erweiterten Stile fest, die vom Registerkarten-Steuerelement verwendet werden. Sie können diese Nachricht explizit oder mithilfe des tabstrg-Formats "tabctrl"/ \_ textendedstyle senden.
ms.assetid: 96ccebe1-2836-4198-8cd7-858401562c21
keywords:
- Windows-Steuerelemente für TCM_SETEXTENDEDSTYLE Meldung
topic_type:
- apiref
api_name:
- TCM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4c789b45eaae6cb3b1bc4fed6f216ec5010b463
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040630"
---
# <a name="tcm_setextendedstyle-message"></a>TCM-Nachricht "- \_ textendedstyle"

Legt die erweiterten Stile fest, die vom Registerkarten-Steuerelement verwendet werden. Sie können diese Nachricht explizit oder mithilfe des tabstrg-Formats " [**tabctrl"/ \_ textendedstyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein **DWORD** -Wert, der angibt, welche Stile in *LPARAM* betroffen sein sollen. Nur die erweiterten Stile in *wParam* werden geändert. Alle anderen Stile werden unverändert beibehalten. Wenn dieser Parameter 0 (null) ist, werden alle Stile in *LPARAM* beeinträchtigt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Wert, der die erweiterten Registerkarten-Steuerelement Stile Dieser Wert ist eine Kombination aus [erweiterten](tab-control-extended-styles.md)Formatvorlagen des Register Steuer Elements.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD** -Wert zurück, der das vorherige Registerkarten-Steuerelement erweiterte Stile enthält.

## <a name="remarks"></a>Bemerkungen

Mit dem *wParam* -Parameter können Sie einen oder mehrere erweiterte Stile ändern, ohne zuerst die vorhandenen Stile abrufen zu müssen. Wenn Sie z. b. [**TCS \_ Ex- \_ flatseparatoren**](tab-control-extended-styles.md) für *wParam* und 0 für *LPARAM* übergeben, wird der **TCS \_ Ex- \_ flatseparators** -Stil gelöscht, aber alle anderen Stile bleiben unverändert.

Aus Gründen der Abwärtskompatibilität wurde das [**tabstrg * \_ textendedstyle**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setextendedstyle) -Makro nicht so aktualisiert, dass *dwexmask* verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TCM \_ getextendecodstyle**](tcm-getextendedstyle.md)
</dt> </dl>

 

 





