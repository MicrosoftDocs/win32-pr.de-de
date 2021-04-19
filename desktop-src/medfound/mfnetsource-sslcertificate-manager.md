---
description: Speichert den IUnknown-Zeiger der Klasse, die die IMF-Klasse "imssslcertifitoremanager" implementiert.
ms.assetid: 13e05bda-96c2-4095-a266-74185760f33a
title: MFNETSOURCE_SSLCERTIFICATE_MANAGER-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf6e21962e3d521e8c5781d59b2e0fe6fed04aa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346659"
---
# <a name="mfnetsource_sslcertificate_manager-property"></a>MF-Quelle \_ sslcertificate \_ Manager (Eigenschaft)

Speichert den **IUnknown** -Zeiger der Klasse, die die [**IMF-Klasse "imssslcertifitoremanager**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager) " implementiert. Die Client Implementierung stellt Methoden bereit, um das Client-SSL-Zertifikat zu erhalten, wenn es vom Server angefordert wird.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**IUnknown-Zeiger**

VT \_ unbekannt

**punkVal**



## <a name="remarks"></a>Bemerkungen

Die **MF-Quelle \_ sslcertificate \_ Manager** -Konstante definiert die GUID für den Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null). Um diese Eigenschaft für die Netzwerkquelle festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

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

 

 




