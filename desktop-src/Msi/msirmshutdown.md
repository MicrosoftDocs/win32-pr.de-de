---
description: Die msirmshutdown-Eigenschaft bestimmt, wie Anwendungen oder Dienste, die derzeit von einem Update betroffene Dateien verwenden, heruntergefahren werden sollen, um die Installation des Updates zu ermöglichen.
ms.assetid: 6763a490-8d1a-42d2-a8cb-0743b7ba6866
title: Msirmshutdown (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4011e4fad980913271012dd86de44eec8c514f7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372655"
---
# <a name="msirmshutdown-property"></a>Msirmshutdown (Eigenschaft)

Die **msirmshutdown** -Eigenschaft bestimmt, wie Anwendungen oder Dienste, die derzeit von einem Update betroffene Dateien verwenden, heruntergefahren werden sollen, um die Installation des Updates zu ermöglichen.

## <a name="value"></a>Wert



| Wert                                                                        | Bedeutung                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Prozesse oder Dienste, die derzeit vom Update betroffene Dateien verwenden, werden heruntergefahren.<br/>                                                                                                                                                                   |
| <dl> <dt>1</dt> </dl> | Prozesse oder Dienste, die derzeit Dateien verwenden, die vom Update betroffen sind und die nicht auf den [Neustart-Manager](../rstmgr/restart-manager-portal.md)reagieren, müssen heruntergefahren werden.<br/>                                                                                       |
| <dl> <dt>2</dt> </dl> | Prozesse oder Dienste, die derzeit vom Update betroffene Dateien verwenden, werden nur heruntergefahren, wenn Sie für einen Neustart registriert wurden. Wenn ein Prozess oder Dienst nicht für einen Neustart registriert wurde, werden keine Prozesse oder Dienste heruntergefahren.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die **msirmshutdown** -Eigenschaft wird ignoriert, wenn der [Neustart-Manager](../rstmgr/restart-manager-portal.md) nicht verfügbar oder deaktiviert ist.

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

 

 
