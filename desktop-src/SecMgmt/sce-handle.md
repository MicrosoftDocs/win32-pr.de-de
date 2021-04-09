---
description: Der SCE- \_ handle-Datentyp ist ein nicht transparentes Handle, das vom Sicherheitskonfigurations-Toolset bereitgestellt wird. Sie wird von pfsce \_ -Abfrage \_ Informationen und pfsce \_ Set \_ Info-Unterstützungsfunktionen verwendet, um Informationen zwischen der Anlage und der Sicherheitsdatenbank zu übergeben.
ms.assetid: 8db91e6f-b31e-40c6-a158-b4b3b00ba0c0
title: SCE_HANDLE (scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fef21dbe03d97dfa14537d5df132ba3cb222643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128773"
---
# <a name="sce_handle"></a>SCE- \_ handle

Der **SCE- \_ handle** -Datentyp ist ein nicht transparentes Handle, das vom Sicherheitskonfigurations-Toolset bereitgestellt wird. Sie wird von [**pfsce- \_ Abfrage \_ Informationen**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) und [**pfsce \_ Set \_ Info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) -Unterstützungsfunktionen verwendet, um Informationen zwischen der Anlage und der Sicherheitsdatenbank zu übergeben.


```C++
typedef PVOID SCE_HANDLE;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Scesvc. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**pfsce- \_ Abfrage \_ Informationen**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> <dt>

[**pfsce- \_ festgelegte \_ Informationen**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)
</dt> </dl>

 

