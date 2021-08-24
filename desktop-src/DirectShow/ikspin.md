---
description: Die IKsPin-Schnittstelle stellt eine Methode zum Abrufen der Medien bereit, die von einem Pin in einem Kernelmodusfilter unterstützt werden. IKsPin verfügt über zusätzliche Methoden neben der hier gezeigten, aber sie werden für DirectShow nicht unterstützt.
ms.assetid: 14d9bef2-e8f0-49d5-bd89-69a95814cf8c
title: IKsPin-Schnittstelle (Ksproxy.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 8855378544bcc2ea7357af220b5d80d32edde74a50c304e973c9821aa8e9a41c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792330"
---
# <a name="ikspin-interface"></a>IKsPin-Schnittstelle

Die `IKsPin` -Schnittstelle stellt eine Methode zum Abrufen der Von einem Pin unterstützten Medien für einen Kernelmodusfilter bereit. `IKsPin` verfügt über zusätzliche Methoden neben der hier gezeigten, aber sie werden für DirectShow nicht unterstützt.

## <a name="members"></a>Member

Die **IKsPin-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IKsPin** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IKsPin-Schnittstelle** verfügt über diese Methoden.



| Methode                                          | Beschreibung                                          |
|:------------------------------------------------|:-----------------------------------------------------|
| [**KsQueryMediums**](ikspin-ksquerymediums.md) | Ruft die von einem Pin unterstützten Medien ab.<br/> |



 

## <a name="remarks"></a>Hinweise

Sie müssen Ks.h vor Ksproxy.h einschließen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Ksproxy.h</dt> </dl>    |
| Bibliothek<br/>                  | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
