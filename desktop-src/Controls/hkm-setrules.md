---
title: HKM_SETRULES (Commctrl.h)
description: Definiert die ungültigen Kombinationen und die Standardmodifiziererkombination für ein Hot Key-Steuerelement.
ms.assetid: de3dd463-a534-4c7c-ae04-da80a3bff2ab
keywords:
- HKM_SETRULES von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- HKM_SETRULES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ec47450ca0d67854d7be413d8a3eb3e5fec3eac49e18f6bcf96f86b563c8906
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958709"
---
# <a name="hkm_setrules-message"></a>HKM \_ SETRULES-Meldung

Definiert die ungültigen Kombinationen und die Standardmodifiziererkombination für ein Hot Key-Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Array von Flags, die ungültige Tastenkombinationen angeben. Dieser Parameter kann eine Kombination der folgenden Werte sein:



| Wert                                                                                                                                                   | Bedeutung                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="HKCOMB_A"></span><span id="hkcomb_a"></span><dl> <dt>**HKCOMB \_ A**</dt> </dl>          | ALT<br/>             |
| <span id="HKCOMB_C"></span><span id="hkcomb_c"></span><dl> <dt>**HKCOMB \_ C**</dt> </dl>          | STRG<br/>            |
| <span id="HKCOMB_CA"></span><span id="hkcomb_ca"></span><dl> <dt>**HKCOMB \_ CA**</dt> </dl>       | STRG+ALT<br/>        |
| <span id="HKCOMB_NONE"></span><span id="hkcomb_none"></span><dl> <dt>**HKCOMB \_ NONE**</dt> </dl> | Unveränderte Schlüssel<br/> |
| <span id="HKCOMB_S"></span><span id="hkcomb_s"></span><dl> <dt>**HKCOMB \_ S**</dt> </dl>          | Umschalten<br/>           |
| <span id="HKCOMB_SA"></span><span id="hkcomb_sa"></span><dl> <dt>**HKCOMB \_ SA**</dt> </dl>       | UMSCHALT+ALT<br/>       |
| <span id="HKCOMB_SC"></span><span id="hkcomb_sc"></span><dl> <dt>**HKCOMB \_ SC**</dt> </dl>       | UMSCHALT+STRG<br/>      |
| <span id="HKCOMB_SCA"></span><span id="hkcomb_sca"></span><dl> <dt>**HKCOMB \_ SCA**</dt> </dl>    | UMSCHALT+STRG+ALT<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Array von Flags, die die Schlüsselkombination angeben, die verwendet werden soll, wenn der Benutzer eine ungültige Kombination ein gibt. Eine Liste der Modifiziererflagwerte finden Sie in der Beschreibung der [**HKM \_ GETHOTKEY-Meldung.**](hkm-gethotkey.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Wenn ein Benutzer eine ungültige Schlüsselkombination ein gibt, wie durch in *wParam* angegebene Flags definiert, verwendet das System den bitweise OR-Operator, um die vom Benutzer eingegebenen Schlüssel mit den in *lParam* angegebenen Flags zu kombinieren. Die resultierende Tastenkombination wird in eine Zeichenfolge konvertiert und dann im Hot Key-Steuerelement angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





