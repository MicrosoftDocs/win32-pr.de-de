---
description: Gibt an, ob dem Frameheader eine zyklische Redundanzprüfung (CRC) hinzugefügt werden soll. Diese Eigenschaft gilt für MPEG-Audioencoder.
ms.assetid: 55f0de8b-26dd-4d48-b7ed-2ddcef630227
title: AVEncMPAEnableRedundancyProtection-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b50e010b0b088e8817eca4dae1989cd6f623f55a9616c4449df62f115f98ff7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824110"
---
# <a name="avencmpaenableredundancyprotection-property"></a>AVEncMPAEnableRedundancyProtection-Eigenschaft

Gibt an, ob dem Frameheader eine zyklische Redundanzprüfung (CRC) hinzugefügt werden soll. Diese Eigenschaft gilt für MPEG-Audioencoder.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncMPAEnableRedundancyProtection**

## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft kann die folgenden Werte aufweisen.



| Wert          | BESCHREIBUNG                |
|----------------|----------------------------|
| VARIANT \_ FALSE | Fügen Sie keine CRC-Prüfsumme hinzu. |
| VARIANT \_ TRUE  | Fügen Sie eine CRC-Prüfsumme hinzu.        |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-API-Eigenschaften](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




