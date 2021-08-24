---
description: Das Installationsprogramm legt die RollbackDisabled-Eigenschaft fest, wenn der Rollback deaktiviert wurde.
ms.assetid: 72215b0f-2fc4-49aa-abf8-3206bdfc765f
title: RollbackDisabled-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1df5b392a69a04811853a449106858445969fed3b2c0598266ff3f8a1bcb51a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039870"
---
# <a name="rollbackdisabled-property"></a>RollbackDisabled-Eigenschaft

Das Installationsprogramm legt die **RollbackDisabled-Eigenschaft fest,** wenn der Rollback deaktiviert wurde. **RollbackDisabled wird** von Paketautoren verwendet, die sicherstellen müssen, dass das Installationsprogramm rollback nicht deaktiviert hat. Die **RollbackDisabled-Eigenschaft** kann in einem bedingten Ausdruck verwendet werden, der die Installation effektiv verweigert, wenn **die RollbackDisabled-Eigenschaft** festgelegt ist.

## <a name="default-value"></a>Standardwert

Standardmäßig ist ein Rollback aktiviert.

## <a name="remarks"></a>Hinweise

Da [Rollback](rollback-custom-actions.md) und [Commit](commit-custom-actions.md) nicht ausgeführt werden, während das Rollback deaktiviert ist, kann das Installationsprogramm während der Installation kein Paket ordnungsgemäß installieren, das diese Arten von benutzerdefinierten Aktionen in einer Transaktion verwendet. In diesem Fall sollte der Autor des Pakets eine Bedingung mit DisableRollback enthalten, die verhindert, dass die Installation fortgesetzt wird, wenn das Rollback deaktiviert ist.

Der DisableRollback-Richtlinienwert kann von einem Administrator als Teil der Zuweisung der Systemrichtlinie festgelegt werden. Administratoren wird empfohlen, den Rollback nur dann zu deaktivieren, wenn dies erforderlich ist. Weitere Informationen zum DisableRollback-Richtlinienwert finden Sie unter [Systemrichtlinie](system-policy.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Rollbackinstallation](rollback-installation.md)
</dt> <dt>

[Systemrichtlinie](system-policy.md)
</dt> <dt>

[Rollback benutzerdefinierter Aktionen](rollback-custom-actions.md)
</dt> <dt>

[Ausführen eines Commits für benutzerdefinierte Aktionen](commit-custom-actions.md)
</dt> </dl>

 

 




