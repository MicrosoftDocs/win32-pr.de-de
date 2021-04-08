---
description: Gibt an, wie die ASF-Medien Senke Windows Media DRM anwenden soll.
ms.assetid: 5f81294b-859a-4325-98dd-6267c736e1f1
title: MFPKEY_ASFMEDIASINK_DRMACTION-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80906a5ac6e5d12bd59dd57445d33b100fee1aef
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761478"
---
# <a name="mfpkey_asfmediasink_drmaction-property"></a>Mfpkey \_ asfmediasink \_ drmaction (Eigenschaft)

Gibt an, wie die ASF-Medien Senke Windows Media DRM anwenden soll.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**ULONG**

VT \_ UI4

**ulVal**



## <a name="remarks"></a>Bemerkungen

Der Wert dieser Eigenschaft ist ein Member der [**mfsink \_ wmdrmaction**](/windows/win32/api/wmcontainer/ne-wmcontainer-mfsink_wmdrmaction) -Enumeration.

Sie können dieses Attribut verwenden, um die ASF-Medien Senke zu konfigurieren. Die Verwendung hängt von der Funktion ab, die Sie zum Erstellen der ASF-Medien Senke aufzurufen:

-   [**Mfkreateasfmediasink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): fragt den abgerufenen [**imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) -Zeiger für die **IPropertyStore** -Schnittstelle ab.

-   [**Mfkreateasfmediasinkaktivierungs**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Aufrufen von [**imfasfcontentinfo:: getencodingconfigurationpropertystore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) für den [**imfasfcontentinfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) -Zeiger, der im *pcontentinfo* -Parameter angegeben ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
