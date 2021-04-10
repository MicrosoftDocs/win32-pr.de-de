---
description: Enthält einen Zeiger auf die imfsourceopenmonitor-Schnittstelle der Anwendungen.
ms.assetid: 5b94ae87-91fc-49d6-9355-83327cfdb3f3
title: MFPKEY_SourceOpenMonitor-Eigenschaft (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a49826ee16a733993b9052e12d9e6fcd5003410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131225"
---
# <a name="mfpkey_sourceopenmonitor-property"></a>Mfpkey \_ sourceopenmonitor (Eigenschaft)

Enthält einen Zeiger auf die [**imfsourceopenmonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) -Schnittstelle der Anwendung.



Datentyp

PROPVARIANT-Typ (VT)

PROPVARIANT-Member

**IUnknown** -Zeiger

VT \_ unbekannt

**punkVal**



## <a name="remarks"></a>Bemerkungen

Anwendungen können diese Eigenschaft an den quellresolver übergeben, um Ereignis Benachrichtigungen von der Netzwerkquelle zu erhalten.

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

 

 




