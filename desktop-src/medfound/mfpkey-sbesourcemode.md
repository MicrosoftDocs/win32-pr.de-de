---
description: Legt die Datenstrom Konfiguration für die WTV-Medienquelle fest.
ms.assetid: 2181723A-C6E8-42BD-979C-5C26FE3986C4
title: MFPKEY_SBESourceMode-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82835a4cfc363e3ae2d054cce68f95c655447dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959412"
---
# <a name="mfpkey_sbesourcemode-property"></a>Mfpkey \_ sbesourcemode (Eigenschaft)

Legt die Datenstrom Konfiguration für die WTV-Medienquelle fest.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**INT**

VT \_ int

**intval**



## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Eigenschaft, um die WTV-Medienquelle zu konfigurieren. Um die-Eigenschaft festzulegen, übergeben Sie einen [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Zeiger an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

Die WTV-Medienquelle liest in Windows aufgezeichnete TV Show-Dateien (WTV und MS-drv).

Diese Eigenschaft muss einen der folgenden Werte aufweisen.

-   1: Ordnen Sie verfügbare Audiodatenströme einer einzelnen Ausgabe zu, basierend auf dem lokalen System. Dieser Modus eignet sich für die Wiedergabe. (Standardeinstellung)
-   2. Alle Audiostreams und unter Ströme (z. b. Beschriftung und Datenströme) werden ausgewählt. Dieser Modus eignet sich für die Umgestaltung oder die Transcodierung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
