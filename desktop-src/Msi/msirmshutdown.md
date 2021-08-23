---
description: Die MSIRMSHUTDOWN-Eigenschaft bestimmt, wie Anwendungen oder Dienste, die derzeit dateien verwenden, die von einem Update betroffen sind, heruntergefahren werden sollen, um die Installation des Updates zu aktivieren.
ms.assetid: 6763a490-8d1a-42d2-a8cb-0743b7ba6866
title: MSIRMSHUTDOWN-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac31a924727217ac86937f4f7ac553717138461e0668a7e79916ffab796f8bd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012878"
---
# <a name="msirmshutdown-property"></a>MSIRMSHUTDOWN-Eigenschaft

Die **MSIRMSHUTDOWN-Eigenschaft** bestimmt, wie Anwendungen oder Dienste, die derzeit dateien verwenden, die von einem Update betroffen sind, heruntergefahren werden sollen, um die Installation des Updates zu aktivieren.

## <a name="value"></a>Wert



| Wert                                                                        | Bedeutung                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Prozesse oder Dienste, die derzeit dateien verwenden, die vom Update betroffen sind, werden heruntergefahren.<br/>                                                                                                                                                                   |
| <dl> <dt>1</dt> </dl> | Prozesse oder Dienste, die derzeit dateien verwenden, die vom Update betroffen sind und nicht auf den [Neustart-Manager](../rstmgr/restart-manager-portal.md)reagieren, werden zum Herunterfahren gezwungen.<br/>                                                                                       |
| <dl> <dt>2</dt> </dl> | Prozesse oder Dienste, die derzeit dateien verwenden, die vom Update betroffen sind, werden nur heruntergefahren, wenn sie alle für einen Neustart registriert wurden. Wenn kein Prozess oder Dienst für einen Neustart registriert wurde, werden keine Prozesse oder Dienste heruntergefahren.<br/> |



 

## <a name="remarks"></a>Hinweise

Die **MSIRMSHUTDOWN-Eigenschaft** wird ignoriert, wenn der [Neustart-Manager](../rstmgr/restart-manager-portal.md) nicht verfügbar oder deaktiviert ist.

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

 

 
