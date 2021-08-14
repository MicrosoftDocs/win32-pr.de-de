---
description: Die \_ PHONEBUTTONMODE-Bitflagkonstanten beschreiben die Schaltflächenklassen.
ms.assetid: 7bf337ee-acda-42fe-b50b-370aad50dc03
title: PHONEBUTTONMODE_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9424c23a9fe6497c657081dd9e197526dc5eb897ad773b1e03fb33c9f08113df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761302"
---
# <a name="phonebuttonmode_-constants"></a>PHONEBUTTONMODE-Konstanten \_

Die **\_ PHONEBUTTONMODE-Bitflagkonstanten** beschreiben die Schaltflächenklassen.

<dl> <dt>

<span id="PHONEBUTTONMODE_CALL"></span><span id="phonebuttonmode_call"></span>**PHONEBUTTONMODE \_ CALL**
</dt> <dd> <dl> <dt>



Die Schaltfläche wird einer Aufrufdarstellung zugewiesen.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_DISPLAY"></span><span id="phonebuttonmode_display"></span>**\_PHONEBUTTONMODE-ANZEIGE**
</dt> <dd> <dl> <dt>



Die Schaltfläche ist eine "soft"-Schaltfläche, die der Anzeige des Telefons zugeordnet ist. Ein Smartphonesatz kann über 0 (null) oder mehr Anzeigeschaltflächen verfügen.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_DUMMY"></span><span id="phonebuttonmode_dummy"></span>**PHONEBUTTONMODE \_ DUMMY**
</dt> <dd> <dl> <dt>



Dieser Wert wird verwendet, um eine Schaltflächen-/Laternenposition zu beschreiben, die keine entsprechende Schaltfläche, sondern nur eine Lampe hat.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_FEATURE"></span><span id="phonebuttonmode_feature"></span>**\_PHONEBUTTONMODE-FEATURE**
</dt> <dd> <dl> <dt>



Die Schaltfläche wird zugewiesen, um Features vom Switch anzufordern, z. B. Halten, Konferenz und Übertragung.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_KEYPAD"></span><span id="phonebuttonmode_keypad"></span>**PHONEBUTTONMODE \_ KEYPAD**
</dt> <dd> <dl> <dt>



Die Schaltfläche ist eine der zwölf Tastendrucktasten 0 bis 9, \* ' ' und ' \# '.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_LOCAL"></span><span id="phonebuttonmode_local"></span>**PHONEBUTTONMODE \_ LOCAL**
</dt> <dd> <dl> <dt>



Die Schaltfläche ist eine lokale Funktionsschaltfläche, z. B. Stummschaltfläche oder Lautstärkeregler.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Dieser Enumerationstyp wird in der [**PHONECAPS-Datenstruktur**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) verwendet, um die Bedeutung zu beschreiben, die den Schaltflächen des Telefons zugeordnet ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




