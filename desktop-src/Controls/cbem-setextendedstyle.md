---
title: CBEM_SETEXTENDEDSTYLE (Commctrl.h)
description: Legt erweiterte Stile innerhalb eines ComboBoxEx-Steuerelements fest.
ms.assetid: 00848bd0-5a2f-4bfb-ae1f-ee3aa88ac57a
keywords:
- CBEM_SETEXTENDEDSTYLE von Windows Steuerelementen
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
ms.openlocfilehash: efd1083e838d85f9cb659acb9a28b74a1d8605934be4c53fd72993e7470fad2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527970"
---
# <a name="cbem_setextendedstyle-message"></a>CBEM \_ SETEXTENDEDSTYLE-Meldung

Legt erweiterte Stile innerhalb eines ComboBoxEx-Steuerelements fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein **DWORD-Wert,** der angibt, welche Stile in *lParam* betroffen sein sollen. Nur die erweiterten Stile in *wParam* werden geändert. Wenn dieser Parameter 0 (null) ist, sind alle Stile in *lParam* betroffen.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein **DWORD-Wert,** der die [erweiterten Stile des ComboBoxEx-Steuerelements enthält,](comboboxex-control-extended-styles.md) die für das Steuerelement festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **DWORD-Wert** zurück, der die erweiterten Stile enthält, die zuvor für das -Steuerelement verwendet wurden.

## <a name="remarks"></a>Hinweise

*Mit wParam* können Sie einen oder mehrere erweiterte Stile ändern, ohne die vorhandenen Stile zuerst abrufen zu müssen. Wenn Sie z. B. [**CBES \_ EX \_ NOEDITIMAGE**](comboboxex-control-extended-styles.md) für *wParam* und 0 für *lParam* übergeben, wird der **CBES \_ EX \_ NOEDITIMAGE-Stil** nicht mehr angezeigt, aber alle anderen Stile bleiben unverändert.

Wenn Sie versuchen, einen erweiterten Stil für ein ComboBoxEx-Steuerelement, das mit dem [**CBS \_ SIMPLE-Stil**](combo-box-styles.md) erstellt wurde, zu setzen, wird es möglicherweise nicht ordnungsgemäß neu gepaint.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





