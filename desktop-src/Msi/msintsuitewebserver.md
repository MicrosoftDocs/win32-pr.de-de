---
description: Unter den Betriebssystemen Windows 2000 und höher legt das Installationsprogramm die Eigenschaft msintsuitewebserver auf 1 fest, wenn das Installationsprogramm auf einer Web Edition von Windows Server 2003 ausgeführt wird.
ms.assetid: de462ba2-4654-4f47-9dd7-3bc9c6f0af0e
title: Msintsuitewebserver (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 082e3ae7f107bf3499f5a48473d53ebb530138a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370655"
---
# <a name="msintsuitewebserver-property"></a>Msintsuitewebserver (Eigenschaft)

Unter den Betriebssystemen Windows 2000 und höher legt das Installationsprogramm die Eigenschaft **msintsuitewebserver** auf 1 fest, wenn das Installationsprogramm auf einer Web Edition von Windows Server 2003 ausgeführt wird. Der Installer legt diese Eigenschaft nur dann auf 1 fest, wenn das Blatt "Ver \_ Suite \_ Blade" in der [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) -Struktur festgelegt ist. Andernfalls legt das Installationsprogramm diese Eigenschaft nicht fest.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist nur mit der Windows Server 2003-Version des Installationsprogramms verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 
