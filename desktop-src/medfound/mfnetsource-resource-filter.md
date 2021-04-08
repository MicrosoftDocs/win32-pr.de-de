---
description: Enthält einen Zeiger auf die imfnettresourcefilter-Rückruf Schnittstelle für den Microsoft Media Foundation http-Byte-Stream.
ms.assetid: C035B4AD-CF99-4A4F-9384-F80A3620BD27
title: MFNETSOURCE_RESOURCE_FILTER-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da94e8bc0bedba3e47dc2784119a5b30d2bffcb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754257"
---
# <a name="mfnetsource_resource_filter-property"></a>MF-Quell \_ Ressourcen \_ Filter (Eigenschaft)

Enthält einen Zeiger auf die [**imfnettresourcefilter**](/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter) -Rückruf Schnittstelle für den Microsoft Media Foundation http-Byte-Stream.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**IUnknown \** _

VT \_ unbekannt

_ *punkVal**



## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Eigenschaft, um den Media Foundation http-Bytestream zu konfigurieren. Um die-Eigenschaft festzulegen, übergeben Sie einen [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Zeiger an den quellresolver. Weitere Informationen finden Sie unter [Konfigurieren einer Medienquelle](configuring-a-media-source.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
