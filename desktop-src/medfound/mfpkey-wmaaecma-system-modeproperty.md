---
description: Legt den Verarbeitungsmodus für den sprach Erfassungs-DSP fest.
ms.assetid: 479b3525-5beb-4c6b-b1ad-8fa72c0d0fd0
title: MFPKEY_WMAAECMA_SYSTEM_MODE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfca745b83c8a73a2eb4c17c8a2206f90255088c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348910"
---
# <a name="mfpkey_wmaaecma_system_mode-property"></a>Mfpkey- \_ wmaaecma- \_ System \_ Modus (Eigenschaft)

Legt den Verarbeitungsmodus für den sprach Erfassungs-DSP fest.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="applies-to"></a>Gilt für

-   [Sprach Erfassungs-DSP](voicecapturedmo.md)

## <a name="remarks"></a>Bemerkungen

Der Wert dieser Eigenschaft ist ein Member der [AEC systemmodusenumeration \_ \_ ](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode) .

Die-Eigenschaft muss einen der folgenden Werte aufweisen.



| Wert | BESCHREIBUNG                                 |
|-------|---------------------------------------------|
| 0     | Nur der Modus für audioecho-Abbruch (AEC)     |
| 2     | Modus für die Verarbeitung von mikrofonarrays (nur Map) |
| 4     | AEC-und Zuordnungs Modus                            |
| 5     | Weder AEC noch Kartenmodus                    |



 

Sie müssen diese Eigenschaft festlegen, bevor Sie den sprach Erfassungs-DSP verwenden. Nachdem Sie diese Eigenschaft festgelegt haben, können Sie den DSP mit seinen Standardeinstellungen verwenden oder zusätzliche Eigenschaften festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Sprach Erfassungs-DSP](voicecapturedmo.md)
</dt> </dl>

 

 
