---
title: HKM_SETRULES Meldung (kommstrg. h)
description: Definiert die ungültigen Kombinationen und die standardmodifiziererkombination für ein Hot Key-Steuerelement.
ms.assetid: de3dd463-a534-4c7c-ae04-da80a3bff2ab
keywords:
- Windows-Steuerelemente für HKM_SETRULES Meldung
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
ms.openlocfilehash: c33c0918a7bb44fdac9a1f2c60fdde8e06b5e679
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477295"
---
# <a name="hkm_setrules-message"></a>HKM- \_ Nachricht

Definiert die ungültigen Kombinationen und die standardmodifiziererkombination für ein Hot Key-Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Array von-Flags, die ungültige Tastenkombinationen angeben. Dieser Parameter kann eine Kombination der folgenden Werte sein:



| Wert                                                                                                                                                   | Bedeutung                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="HKCOMB_A"></span><span id="hkcomb_a"></span><dl> <dt>**hkcomb \_ A**</dt> </dl>          | ALT<br/>             |
| <span id="HKCOMB_C"></span><span id="hkcomb_c"></span><dl> <dt>**hkcomb- \_ C**</dt> </dl>          | STRG<br/>            |
| <span id="HKCOMB_CA"></span><span id="hkcomb_ca"></span><dl> <dt>**hkcomb-Zertifizierungsstelle \_**</dt> </dl>       | STRG + ALT<br/>        |
| <span id="HKCOMB_NONE"></span><span id="hkcomb_none"></span><dl> <dt>**hkcomb \_ None**</dt> </dl> | Nicht geänderte Schlüssel<br/> |
| <span id="HKCOMB_S"></span><span id="hkcomb_s"></span><dl> <dt>**hkcomb \_ S**</dt> </dl>          | Schuss<br/>           |
| <span id="HKCOMB_SA"></span><span id="hkcomb_sa"></span><dl> <dt>**hkcomb- \_ sa**</dt> </dl>       | UMSCHALT+ALT<br/>       |
| <span id="HKCOMB_SC"></span><span id="hkcomb_sc"></span><dl> <dt>**hkcomb \_ SC**</dt> </dl>       | UMSCHALT + STRG<br/>      |
| <span id="HKCOMB_SCA"></span><span id="hkcomb_sca"></span><dl> <dt>**hkcomb \_ SCA**</dt> </dl>    | UMSCHALT + STRG + ALT<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Array von Flags, die die Tastenkombination angeben, die verwendet werden soll, wenn der Benutzer eine ungültige Kombination eingibt. Eine Liste der modifiziererflagwerte finden Sie in der Beschreibung der [**HKM \_ GetHotKey**](hkm-gethotkey.md) -Nachricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Wenn ein Benutzer eine ungültige Tastenkombination eingibt, die durch in *wParam* angegebene Flags definiert ist, verwendet das System den bitweisen OR-Operator, um die vom Benutzer eingegebenen Schlüssel mit den in *LPARAM* angegebenen Flags zu kombinieren. Die resultierende Tastenkombination wird in eine Zeichenfolge konvertiert und dann im Steuerelement "Hot Key" angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





