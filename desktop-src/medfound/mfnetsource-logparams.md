---
description: Array von Zeichenfolgen mit den Parametern, die an den Protokollserver gesendet werden.
ms.assetid: 36d711c7-a1ff-4ef2-b633-5f9f1662801e
title: MFNETSOURCE_LOGPARAMS -Eigenschaft (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba557c4fb0bf77693669e8cb46af269ec3a4f2ed72c536e4bdab53a0778dc038
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113520"
---
# <a name="mfnetsource_logparams-property"></a>MFNETSOURCE \_ LOGPARAMS-Eigenschaft

Array von Zeichenfolgen mit den Parametern, die an den Protokollserver gesendet werden.



Datentyp

PROPVARIANT-Typ (vt)

PROPVARIANT-Member

**Wchar\***

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Hinweise

Die **MFNETSOURCE \_ LOGPARAMS-Konstante** definiert die GUID für den Eigenschaftsschlüssel. Der Eigenschaftenbezeichner (PID) ist 0 (null). Um diese Eigenschaft für die Netzwerkquelle festlegen zu können, übergeben Sie einen **IPropertyStore-Zeiger** an den Quellre resolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle.](configuring-a-media-source.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




