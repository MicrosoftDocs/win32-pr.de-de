---
description: Das Installationsprogramm legt diese Eigenschaft fest, wenn der Benutzer über Administratorrechte verfügt.
ms.assetid: 2e7fd269-bd5f-40b7-b123-36b9c783a917
title: AdminUser-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1b765aa4ece1bc19b5ed59e97a98ca4579042d52d65c0024ae018c794f9aaa3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581910"
---
# <a name="adminuser-property"></a>AdminUser-Eigenschaft

Das Installationsprogramm legt diese Eigenschaft fest, wenn der Benutzer über Administratorrechte verfügt.

**Windows Server 2008 und Windows Vista:** Die **AdminUser-Eigenschaft** ist identisch mit der [**Privileged-Eigenschaft.**](privileged.md) Autoren sollten die **Privileged-Eigenschaft** verwenden. Das Installationsprogramm legt diese Eigenschaften fest, wenn der Benutzer über Administratorrechte verfügt, wenn die Anwendung von einem Systemadministrator zugewiesen wurde oder wenn sowohl die Benutzer- als auch die Computerrichtlinien AlwaysInstallElevated auf TRUE festgelegt sind.

## <a name="remarks"></a>Hinweise

Die Unterschiede zwischen diesen Eigenschaften wurden möglicherweise in einigen Legacypaketen verwendet. Beispielsweise wurde **AdminUser** möglicherweise anstelle von [**Privileged**](privileged.md) in bedingten Anweisungen verwendet, da das Installationsprogramm die **AdminUser-Eigenschaft** nur festlegt, wenn der Benutzer administrator ist. Das Installationsprogramm legt die **Privileged-Eigenschaft** fest, wenn der Benutzer Administrator ist oder wenn die Richtlinie es dem Benutzer ermöglicht, mit erhöhten Rechten zu installieren.

**Windows Server 2008 und Windows Vista:** Wird nicht unterstützt. [**Privileged**](privileged.md) und **AdminUser** sind identisch. Pakete, die eindeutige **Privileged-** und **AdminUser-Eigenschaften** erfordern, können den Unterschied wiederherstellen, indem sie die [**MSIUSEREALADMINDETECTION-Eigenschaft**](msiuserealadmindetection.md) festlegen.

Weitere Informationen finden Sie unter [Installing a Package with Elevated Privileges for a Non-Admin ( Installieren eines Pakets mit erhöhten Rechten)](installing-a-package-with-elevated-privileges-for-a-non-admin.md)und Privileged property [**(Privilegierte**](privileged.md) Eigenschaft).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 unter Windows Vista oder Windows Server 2008. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den mindestens erforderlichen Windows Service Packs, die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time [Anforderungen](windows-installer-portal.md) für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




