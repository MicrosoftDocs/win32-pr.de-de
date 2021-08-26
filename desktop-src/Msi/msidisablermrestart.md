---
description: Die MSIDISABLERMRESTART-Eigenschaft bestimmt, wie Anwendungen oder Dienste, die derzeit dateien verwenden, die von einem Update betroffen sind, heruntergefahren und neu gestartet werden sollen, um die Installation des Updates zu aktivieren.
ms.assetid: 45c804bf-6d15-416a-b106-d8bb3f4c547d
title: MSIDISABLERMRESTART(Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d46bdaee34b154ccaacddc36dcb08113fce9e3f749090eb80176080a60235e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042790"
---
# <a name="msidisablermrestart-property"></a>MSIDISABLERMRESTART(Eigenschaft)

Die **MSIDISABLERMRESTART-Eigenschaft** bestimmt, wie Anwendungen oder Dienste, die derzeit dateien verwenden, die von einem Update betroffen sind, heruntergefahren und neu gestartet werden sollen, um die Installation des Updates zu aktivieren.

## <a name="value"></a>Wert



| Wert                                                                        | Bedeutung                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Alle Systemdienste, die zum Installieren des Updates heruntergefahren wurden, werden neu gestartet. Alle Anwendungen, die sich selbst beim [Neustart-Manager registriert haben,](../rstmgr/restart-manager-portal.md) werden neu gestartet.<br/> |
| <dl> <dt>1</dt> </dl> | Prozesse, die während der Installation des Updates mithilfe des [Neustart-Managers](../rstmgr/restart-manager-portal.md) heruntergefahren wurden, werden nach dem Update nicht neu gestartet.<br/>                           |



 

## <a name="remarks"></a>Hinweise

Die **MSIDISABLERMRESTART-Eigenschaft** wird ignoriert, wenn der [Neustart-Manager](../rstmgr/restart-manager-portal.md) nicht verfügbar oder deaktiviert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Informationen zum [Windows Service Pack,](windows-installer-portal.md) das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 3.1 und früheren Versionen](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
