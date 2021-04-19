---
description: Der Installer legt diese Eigenschaft fest, wenn der Benutzer über Administratorrechte verfügt.
ms.assetid: 2e7fd269-bd5f-40b7-b123-36b9c783a917
title: AdminUser (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11651f0d7103edabbcf7b40087db91f999b1a5b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367854"
---
# <a name="adminuser-property"></a>AdminUser (Eigenschaft)

Der Installer legt diese Eigenschaft fest, wenn der Benutzer über Administratorrechte verfügt.

**Windows Server 2008 und Windows Vista:** Die **AdminUser** -Eigenschaft ist identisch mit der Eigenschaft [**privilegiert**](privileged.md) . Autoren sollten die **privilegierte** Eigenschaft verwenden. Der Installer legt diese Eigenschaften fest, wenn der Benutzer über Administratorrechte verfügt, wenn die Anwendung von einem Systemadministrator zugewiesen wurde, oder wenn die Benutzer-und Computer Richtlinien alwaysinstallerhöhten auf true festgelegt sind.

## <a name="remarks"></a>Bemerkungen

Die Unterschiede zwischen diesen Eigenschaften können in einigen Legacy Paketen verwendet werden. Beispielsweise kann " **AdminUser** " anstelle von " [**privilegiert**](privileged.md) " in bedingten Anweisungen verwendet werden, da das Installationsprogramm nur die **AdminUser** -Eigenschaft festlegt, wenn der Benutzer ein Administrator ist. Der Installer legt die **privilegierte** Eigenschaft fest, wenn der Benutzer ein Administrator ist, oder wenn die Richtlinie dem Benutzer ermöglicht, mit erhöhten Rechten zu installieren.

**Windows Server 2008 und Windows Vista:** Nicht unterstützt. Die Berechtigungen " [**privilegiert**](privileged.md) " und " **AdminUser** " sind identisch. Pakete, die unterschiedliche **privilegierte** Eigenschaften und **AdminUser** -Eigenschaften erfordern, können den Unterschied wiederherstellen, indem Sie die Eigenschaft [**msiuserealadminerkennungs**](msiuserealadmindetection.md) festlegen.

Weitere Informationen finden Sie unter [Installieren eines Pakets mit erhöhten Rechten für eine nicht-Administrator-](installing-a-package-with-elevated-privileges-for-a-non-admin.md)und [**privilegierte**](privileged.md) Eigenschaft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Vista oder Windows Server 2008. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




