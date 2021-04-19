---
description: Der Installer legt die msintproducttype-Eigenschaft für Windows NT, Windows 2000 und spätere Betriebssysteme fest.
ms.assetid: 6bbc8283-5911-4fbd-8a0f-09c398280e74
title: Msintproducttype (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe7fef0791f5842163812b62a7314578d480676c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361351"
---
# <a name="msintproducttype-property"></a>Msintproducttype (Eigenschaft)

Der Installer legt die **msintproducttype** -Eigenschaft für Windows NT, Windows 2000 und spätere Betriebssysteme fest. Diese Eigenschaft gibt den Windows-Produkttyp an.

Für Windows 2000 und spätere Betriebssysteme legt das Installationsprogramm die folgenden Werte fest. Beachten Sie, dass die Werte mit dem Feld **wProductType** der [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) -Struktur identisch sind.



| Wert | Bedeutung                                  |
|-------|------------------------------------------|
| 1     | Windows 2000 Professional und höher      |
| 2     | Windows 2000-Domänen Controller und höher |
| 3     | Windows 2000-Server und höher            |



 

Für ältere Betriebssysteme als Windows 2000 legt das Installationsprogramm die folgenden Werte fest.



| Wert | Bedeutung                      |
|-------|------------------------------|
| 1     | Windows NT-Arbeitsstation       |
| 2     | Windows NT-Domänen Controller |
| 3     | Windows NT-Server            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 
