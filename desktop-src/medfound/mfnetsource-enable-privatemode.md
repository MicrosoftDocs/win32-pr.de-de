---
description: Aktiviert den privaten Downloadmodus in der Netzwerkquelle.
ms.assetid: 679661A7-1D31-43F3-A64E-16ADCB5414B0
title: MFNETSOURCE_ENABLE_PRIVATEMODE-Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e2ff972aa42753bb92be33fd6bf893d0578f28bf0ad29889a1b5986ba1a77c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113540"
---
# <a name="mfnetsource_enable_privatemode-property"></a>MFNETSOURCE \_ ENABLE \_ PRIVATEMODE-Eigenschaft

Aktiviert den privaten Downloadmodus in der Netzwerkquelle.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**Bool**

VT \_ I4

**lVal**



## <a name="remarks"></a>Hinweise

Wenn diese Eigenschaft **TRUE** ist, wird der Cache gelöscht, wenn die Sitzung beendet wird.

Die **MFNETSOURCE \_ CLIENTGUID-Konstante** definiert die GUID für den Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null). Um diese Eigenschaft für die Netzwerkquelle festzulegen, übergeben Sie einen **IPropertyStore-Zeiger** an den Quell resolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle.](configuring-a-media-source.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                          |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




