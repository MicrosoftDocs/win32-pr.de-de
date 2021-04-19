---
description: Legt die Anzahl von Arbeitsthreads fest, die von einem Video Decoder verwendet werden.
ms.assetid: A1570BB5-62BC-46C0-B9C9-61F99AA13BBE
title: CODECAPI_AVDecNumWorkerThreads-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d7c57d1b4176ad65313a5583a70f9ba4f7427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346669"
---
# <a name="codecapi_avdecnumworkerthreads-property"></a>Codecapi \_ avdecnumworkerthreads (Eigenschaft)

Legt die Anzahl von Arbeitsthreads fest, die von einem Video Decoder verwendet werden.

## <a name="data-type"></a>Datentyp

**Long** (**VT \_ I4**)

## <a name="property-guid"></a>Eigenschaften-GUID

Codecapi \_ avdecnumworkerthreads

## <a name="remarks"></a>Bemerkungen

Wenn der Wert 1 ist, wählt der Decoder die Anzahl der Threads aus.

Legen Sie diese Eigenschaft für die [**icodecapi**](/windows/desktop/api/strmif/nn-strmif-icodecapi) -Schnittstelle als **Long** -Wert fest (**VT \_ I4**). Legen Sie diese Eigenschaft für die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle als **UInt32** fest, obwohl der Wert signiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ -Desktop-Apps \| UWP-apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**Icodecapi**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

