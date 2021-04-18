---
title: CBEM_SETEXTENDEDSTYLE Meldung (kommstrg. h)
description: Legt erweiterte Stile innerhalb eines ComboBoxEx-Steuer Elements fest.
ms.assetid: 00848bd0-5a2f-4bfb-ae1f-ee3aa88ac57a
keywords:
- Windows-Steuerelemente für CBEM_SETEXTENDEDSTYLE Meldung
topic_type:
- apiref
api_name:
- CBEM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a60518d2f6130c2c89e379125308fc2e647c6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339371"
---
# <a name="cbem_setextendedstyle-message"></a>CBEM- \_ textendedstyle-Meldung

Legt erweiterte Stile innerhalb eines ComboBoxEx-Steuer Elements fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein **DWORD** -Wert, der angibt, welche Stile in *LPARAM* betroffen sein sollen. Nur die erweiterten Stile in *wParam* werden geändert. Wenn dieser Parameter 0 (null) ist, werden alle Stile in *LPARAM* beeinträchtigt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein **DWORD** -Wert, der das [ComboBoxEx-Steuer](comboboxex-control-extended-styles.md) Element enthält, das für das Steuerelement festgelegt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD** -Wert zurück, der die erweiterten Stile enthält, die zuvor für das Steuerelement verwendet wurden.

## <a name="remarks"></a>Bemerkungen

mit *wParam* können Sie einen oder mehrere erweiterte Stile ändern, ohne zuerst die vorhandenen Stile abrufen zu müssen. Wenn Sie z. b. [**CBEs \_ Ex \_ noeditimage**](comboboxex-control-extended-styles.md) für *wParam* und 0 für *LPARAM* übergeben, wird der Stil **CBEs \_ Ex \_ noeditimage** gelöscht, aber alle anderen Stile bleiben unverändert.

Wenn Sie versuchen, einen erweiterten Stil für ein ComboBoxEx-Steuerelement festzulegen, das mit dem [**\_ einfachen CBS**](combo-box-styles.md) -Stil erstellt wurde, wird es möglicherweise nicht ordnungsgemäß neu gezeichnet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





