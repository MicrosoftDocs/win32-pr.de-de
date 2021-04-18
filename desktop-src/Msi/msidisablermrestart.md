---
description: Die msidisablermrestart-Eigenschaft bestimmt, wie Anwendungen oder Dienste, die derzeit von einem Update betroffene Dateien verwenden, heruntergefahren und neu gestartet werden müssen, um die Installation des Updates zu ermöglichen.
ms.assetid: 45c804bf-6d15-416a-b106-d8bb3f4c547d
title: Msidisablermrestart (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1215822b26bb9bd48fa52ee46806bc288a2986b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368483"
---
# <a name="msidisablermrestart-property"></a>Msidisablermrestart (Eigenschaft)

Die **msidisablermrestart** -Eigenschaft bestimmt, wie Anwendungen oder Dienste, die derzeit von einem Update betroffene Dateien verwenden, heruntergefahren und neu gestartet werden müssen, um die Installation des Updates zu ermöglichen.

## <a name="value"></a>Wert



| Wert                                                                        | Bedeutung                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Alle Systemdienste, die zur Installation des Updates heruntergefahren wurden, werden neu gestartet. Alle Anwendungen, die sich mit dem [Neustart-Manager](../rstmgr/restart-manager-portal.md) registriert haben, werden neu gestartet.<br/> |
| <dl> <dt>1</dt> </dl> | Prozesse, die mit dem Neustart- [Manager](../rstmgr/restart-manager-portal.md) während der Installation des Updates heruntergefahren wurden, werden nach dem Anwenden des Updates nicht neu gestartet.<br/>                           |



 

## <a name="remarks"></a>Bemerkungen

Die **msidisablermrestart** -Eigenschaft wird ignoriert, wenn der [Neustart-Manager](../rstmgr/restart-manager-portal.md) nicht verfügbar oder deaktiviert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Informationen zu den minimalen Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
