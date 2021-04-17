---
description: Der Datentyp scesvc \_ handle ist ein nicht transparentes Handle, das vom Sicherheitskonfigurations-Toolset bereitgestellt wird.
ms.assetid: 478d7d4b-7983-4247-b8be-2e2cd3327533
title: SCESVC_HANDLE (scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09fbc115326361e4cbfe1152361a70a36007a302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525712"
---
# <a name="scesvc_handle"></a>scesvc- \_ handle

Der Datentyp **scesvc \_ handle** ist ein nicht transparentes Handle, das vom Sicherheitskonfigurations-Toolset bereitgestellt wird. Sie wird von Methoden der Schnittstellen [**iscesvplattachmentdata**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) und [**iscesvplattachmentpersistinfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) verwendet, um Informationen zwischen dem Snap-in "Sicherheitskonfiguration" und der Snap-in-Erweiterung zu übergeben.


```C++
typedef PVOID SCESVC_HANDLE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Scesvc. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscesvstreamtachmentdata**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)
</dt> <dt>

[**Iscesvplattachmentpersistinfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo)
</dt> </dl>

 

 




