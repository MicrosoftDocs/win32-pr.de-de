---
description: Array von Zeichen folgen mit den Parametern, die an den Protokollserver gesendet werden sollen.
ms.assetid: 36d711c7-a1ff-4ef2-b633-5f9f1662801e
title: MFNETSOURCE_LOGPARAMS-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec30f3f4d85f44905288601ba73ee6c246d8a9db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959284"
---
# <a name="mfnetsource_logparams-property"></a>Eigenschaft "MF NetSource \_ logparameams"

Array von Zeichen folgen mit den Parametern, die an den Protokollserver gesendet werden sollen.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**WCHAR \** _

VT \_ LPWSTR

_ *pwszval**



## <a name="remarks"></a>Bemerkungen

Die **MF NetSource \_ LogParser** -Konstante definiert die GUID für den Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null). Um diese Eigenschaft für die Netzwerkquelle festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




