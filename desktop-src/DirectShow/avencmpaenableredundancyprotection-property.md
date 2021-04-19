---
description: Gibt an, ob dem Frame Header eine zyklische Redundanz Überprüfung (CRC) hinzugefügt werden soll. Diese Eigenschaft gilt für MPEG-Audioencoder.
ms.assetid: 55f0de8b-26dd-4d48-b7ed-2ddcef630227
title: Avencmpenableredundancyprotection-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2028b5adaad55d46cc53c61f9d65a73819cc899
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106339664"
---
# <a name="avencmpaenableredundancyprotection-property"></a>Avencmpfenableredundancyprotection (Eigenschaft)

Gibt an, ob dem Frame Header eine zyklische Redundanz Überprüfung (CRC) hinzugefügt werden soll. Diese Eigenschaft gilt für MPEG-Audioencoder.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**Variant \_ bool** (**VT \_ bool**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencmpenableredundancyprotection**

## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft kann die folgenden Werte aufweisen.



| Wert          | BESCHREIBUNG                |
|----------------|----------------------------|
| Variant \_ false | Fügen Sie keine CRC-Prüfsumme hinzu. |
| Variant \_ true  | Fügen Sie eine CRC-Prüfsumme hinzu.        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[ Desktop Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften der Codec-API](codec-api-properties.md)
</dt> <dt>

[**Icodecapi-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




