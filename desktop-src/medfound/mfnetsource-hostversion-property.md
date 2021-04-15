---
description: Der Wert des Felds &\# 0034; c-hostexever&\# 0034;, das die Netzwerkquelle für die Protokollierung verwendet.
ms.assetid: eee93457-483d-41dc-91c5-c12382d03152
title: MFNETSOURCE_HOSTVERSION-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f10c1a66bc2ab52455140733a6b60f25863c8f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485203"
---
# <a name="mfnetsource_hostversion-property"></a>Mbernetsource- \_ Hostversion (Eigenschaft)

Der Wert des Felds "c-hostexever", das von der Netzwerkquelle für die Protokollierung verwendet wird. Anwendungen können diese Eigenschaft auf die Versionsnummer der Host Anwendung festlegen. Die Host Anwendung ist die exe-Datei, die durch das Feld "c-hostexe" identifiziert wird.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**LONGLONG**

VT \_ I8

**Hval**



## <a name="remarks"></a>Bemerkungen

Die Konstante **mbernetsource- \_ Hostversion** definiert die GUID für diesen Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null).

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

 

 




