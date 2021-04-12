---
description: Enthält einen Zeiger auf die imfnetproxyloerfactory-Schnittstelle.
ms.assetid: 455325c0-5116-4e81-9729-fab9c6a367c7
title: MFNETSOURCE_PROXYLOCATORFACTORY-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1199333e9eb343ab9d8f96864372b2dc385ab7d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130712"
---
# <a name="mfnetsource_proxylocatorfactory-property"></a>Eigenschaft "MF NetSource \_ proxylo. Factory"

Enthält einen Zeiger auf die [**imfnetproxyloerfactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) -Schnittstelle.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**IUnknown** -Zeiger

VT \_ unbekannt

**punkVal**



## <a name="remarks"></a>Bemerkungen

Die Konstante " **MF NetSource \_ proxyloskiorfactory** " definiert die GUID für diesen Eigenschafts Schlüssel. Der Eigenschaften Bezeichner (PID) ist 0 (null).

Anwendungen können diese Eigenschaft verwenden, um einen benutzerdefinierten proxylocator für die Netzwerkquelle bereitzustellen. Um die-Eigenschaft festzulegen, übergeben Sie einen **IPropertyStore** -Zeiger an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> <dt>

[Proxy Unterstützung für Netzwerk Quellen](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




