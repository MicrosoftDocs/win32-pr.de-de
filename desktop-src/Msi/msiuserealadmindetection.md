---
description: Legen Sie die MSIUSEREALADMINDETECTION-Eigenschaft auf 1 fest, um an fordern, dass das Installationsprogramm die tatsächlichen Benutzerinformationen verwendet, wenn die AdminUser-Eigenschaft festgelegt wird.
ms.assetid: eb0ed6e3-377b-40f4-afee-346a83e310cf
title: MSIUSEREALADMINDETECTION (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a177d320aff25cf21b932ca25e691f145f94ad3
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812937"
---
# <a name="msiuserealadmindetection-property"></a>MSIUSEREALADMINDETECTION (Eigenschaft)

Legen Sie die **MSIUSEREALADMINDETECTION-Eigenschaft** auf 1 fest, um an fordern, dass das Installationsprogramm die tatsächlichen Benutzerinformationen verwendet, wenn die [**AdminUser-Eigenschaft festgelegt**](adminuser.md) wird. Bei der Ausführung auf Windows Vista sind [**Privileged**](privileged.md) und **AdminUser** identisch. Autoren sollten die **Privileged-Eigenschaft** in neuen Paketen verwenden. Legacypakete, die unterschiedliche **Privileged-** und **AdminUser-Eigenschaften** erfordern, können den Unterschied wiederherstellen, indem Sie die **MSIUSEREALADMINDETECTION-Eigenschaft** festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 3.1 und früheren Versionen](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




