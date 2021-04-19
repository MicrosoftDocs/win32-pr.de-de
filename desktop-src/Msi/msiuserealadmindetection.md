---
description: Legen Sie die msiuserealadminerkennungs-Eigenschaft auf 1 fest, um anzufordern, dass das Installationsprogramm beim Festlegen der AdminUser-Eigenschaft tatsächliche Benutzerinformationen verwendet.
ms.assetid: eb0ed6e3-377b-40f4-afee-346a83e310cf
title: Msiuserealadminerkennungs (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0989174f41bc4b58f89e440dd9852dfde6249a5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369184"
---
# <a name="msiuserealadmindetection-property"></a>Msiuserealadminerkennungs (Eigenschaft)

Legen Sie die **msiuserealadminerkennungs** -Eigenschaft auf 1 fest, um anzufordern, dass das Installationsprogramm beim Festlegen der [**AdminUser**](adminuser.md) -Eigenschaft tatsächliche Benutzerinformationen verwendet. Bei der Ausführung unter Windows Vista sind die Berechtigungen " [**privilegiert**](privileged.md) " und " **AdminUser** " identisch. Autoren sollten die **privilegierte** Eigenschaft in neuen Paketen verwenden. Legacy Pakete, die unterschiedliche **privilegierte** Eigenschaften und **AdminUser** -Eigenschaften erfordern, können den Unterschied wiederherstellen, indem Sie die **msiuserealadminerkennungs** -Eigenschaft festlegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




