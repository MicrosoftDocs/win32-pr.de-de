---
description: Der Installer legt die rollbackdeaktiviert-Eigenschaft fest, wenn das Rollback deaktiviert wurde.
ms.assetid: 72215b0f-2fc4-49aa-abf8-3206bdfc765f
title: Rollbackdeaktiviert (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f50c8e344ed4291210afb1714ce97d90b590999
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369465"
---
# <a name="rollbackdisabled-property"></a>Rollbackdeaktiviert (Eigenschaft)

Der Installer legt die **rollbackdeaktiviert** -Eigenschaft fest, wenn das Rollback deaktiviert wurde. **Rollbackdeaktiviert** wird von Paket Autoren verwendet, die sicherstellen müssen, dass das Rollback vom Installationsprogramm nicht deaktiviert wurde. Die **rollbackdeaktiviert** -Eigenschaft kann in einem bedingten Ausdruck verwendet werden, der die Fortsetzung mit der Installation verweigert, wenn die **rollbackdeaktiviert** -Eigenschaft festgelegt ist.

## <a name="default-value"></a>Standardwert

Standardmäßig ist das Rollback aktiviert.

## <a name="remarks"></a>Bemerkungen

Da [Rollback](rollback-custom-actions.md) und [Commit](commit-custom-actions.md) nicht ausgeführt werden, während ein Rollback deaktiviert ist, kann das Installationsprogramm ein Paket, das diese Typen von benutzerdefinierten Aktionen in einer Transaktion verwendet, während der Installation nicht ordnungsgemäß installieren. In diesem Fall sollte der Autor des Pakets eine Bedingung mithilfe von DISABLEROLLBACK einschließen, mit der verhindert wird, dass die Installation fortgesetzt wird, wenn das Rollback deaktiviert ist.

Der Wert der DISABLEROLLBACK-Richtlinie kann von einem Administrator als Teil der Zuweisung von Systemrichtlinien festgelegt werden. Administratoren wird empfohlen, Rollbacks nur dann zu deaktivieren, wenn dies erforderlich ist. Weitere Informationen zum Wert der DISABLEROLLBACK-Richtlinie finden Sie unter [System Richtlinie](system-policy.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Rollback-Installation](rollback-installation.md)
</dt> <dt>

[Systemrichtlinie](system-policy.md)
</dt> <dt>

[Zurücksetzen von benutzerdefinierten Aktionen](rollback-custom-actions.md)
</dt> <dt>

[Commit für benutzerdefinierte Aktionen](commit-custom-actions.md)
</dt> </dl>

 

 




