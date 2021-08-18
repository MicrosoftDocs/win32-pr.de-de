---
description: Legt die Streamkonfiguration für die WTV-Medienquelle fest.
ms.assetid: 2181723A-C6E8-42BD-979C-5C26FE3986C4
title: MFPKEY_SBESourceMode -Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c6b4fc0b248000f0540fd47fd7bbf8bba907994d1351144521bf162d330340
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973369"
---
# <a name="mfpkey_sbesourcemode-property"></a>MFPKEY \_ SBESourceMode (Eigenschaft)

Legt die Streamkonfiguration für die WTV-Medienquelle fest.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**INT**

VT \_ INT

**intVal**



## <a name="remarks"></a>Hinweise

Verwenden Sie diese Eigenschaft, um die WTV-Medienquelle zu konfigurieren. Übergeben Sie zum Festlegen der -Eigenschaft einen [**IPropertyStore-Zeiger**](/windows/win32/api/propsys/nn-propsys-ipropertystore) an den Quellre resolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle.](configuring-a-media-source.md)

Die WTV-Medienquelle liest Windows Die aufgezeichneten TV Show-Dateien (WTV und MS-DRV).

Diese Eigenschaft muss einen der folgenden Werte haben.

-   1: Ordnen Sie verfügbare Audiostreams basierend auf dem lokalen System einer einzelnen Ausgabe zu. Dieser Modus ist für die Wiedergabe geeignet. (Standardeinstellung)
-   2. Alle Audiostreams und Unterstreams (z. B. Untertitel und Datenströme) werden ausgewählt. Dieser Modus ist für die Neu- oder Transcodierung geeignet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Desktop-Apps \| UWP-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Desktop-Apps \| UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
