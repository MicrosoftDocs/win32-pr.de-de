---
description: Die \_ Bit-Flag-Konstanten von phonebuttonmode beschreiben die Schaltflächen Klassen.
ms.assetid: 7bf337ee-acda-42fe-b50b-370aad50dc03
title: PHONEBUTTONMODE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a4ee5e9835b7df06773bc1429641c91597c15e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365440"
---
# <a name="phonebuttonmode_-constants"></a>Phonebuttonmode- \_ Konstanten

Die Bit-Flag-Konstanten von **phonebuttonmode \_** beschreiben die Schaltflächen Klassen.

<dl> <dt>

<span id="PHONEBUTTONMODE_CALL"></span><span id="phonebuttonmode_call"></span>**phonebuttonmode \_ -Befehl**
</dt> <dd> <dl> <dt>



Die Schaltfläche wird einer aufrufdarstellung zugewiesen.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_DISPLAY"></span><span id="phonebuttonmode_display"></span>**phonebuttonmode- \_ Anzeige**
</dt> <dd> <dl> <dt>



Die Schaltfläche ist eine "weiche" Schaltfläche, die der Telefonanzeige zugeordnet ist. Ein Telefon Satz kann NULL oder mehr Anzeige Schaltflächen enthalten.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_DUMMY"></span><span id="phonebuttonmode_dummy"></span>**phonebuttonmode- \_ Dummy**
</dt> <dd> <dl> <dt>



Dieser Wert wird verwendet, um eine Schaltfläche/Lamp-Position zu beschreiben, die keine entsprechende Schaltfläche hat, aber nur über eine Lamp verfügt.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_FEATURE"></span><span id="phonebuttonmode_feature"></span>**phonebuttonmode- \_ Funktion**
</dt> <dd> <dl> <dt>



Die Schaltfläche wird den anfordernden Features des Schalters zugewiesen, z. b. Halt, Konferenz und Übertragung.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_KEYPAD"></span><span id="phonebuttonmode_keypad"></span>**phonebuttonmode- \_ Keypad**
</dt> <dd> <dl> <dt>



Die Schaltfläche ist eine der zwölf Tastatur-Schaltflächen, 0 bis 9, ' \* ' und ' \# '.


</dt> </dl> </dd> <dt>

<span id="PHONEBUTTONMODE_LOCAL"></span><span id="phonebuttonmode_local"></span>**phonebuttonmode \_ lokal**
</dt> <dd> <dl> <dt>



Die Schaltfläche ist eine lokale Funktions Schaltfläche, z. b. stumm-oder volumesteuerung.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Keine Erweiterbarkeit. Alle 32 Bits sind reserviert.

Dieser Enumerationstyp wird in der [**phonecaps**](/windows/desktop/api/Tapi/ns-tapi-phonecaps) -Datenstruktur verwendet, um die Bedeutung der Schaltflächen des Telefons zu beschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




