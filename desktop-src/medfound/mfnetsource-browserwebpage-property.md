---
description: Der Wert des Felds &\# 0034; CS (Referer) &\# 0034;, das die Netzwerkquelle für die Protokollierung verwendet.
ms.assetid: 328544b3-0d5f-4d1a-9ad1-ac38402d5898
title: MFNETSOURCE_BROWSERWEBPAGE-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e8222761299cad229b692ef400f69d0968ebd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959140"
---
# <a name="mfnetsource_browserwebpage-property"></a>Eigenschaft "browserwebseite" in MF NetSource \_

Der Wert des Felds "CS (Referer)", das die Netzwerkquelle für die Protokollierung verwendet. Anwendungen können diese Eigenschaft auf die URL der Webseite festlegen, in der die Anwendung eingebettet wurde.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

Breit Zeichen-Zeichenfolge (**WCHAR** \* )

VT \_ LPWSTR

**pwszval**



## <a name="remarks"></a>Bemerkungen

Die Konstante " **MF NetSource \_ browserwebseite** " definiert die GUID für diesen Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um die Netzwerkquelle zu konfigurieren. Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Client Protokollierung](client-logging.md)
</dt> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




