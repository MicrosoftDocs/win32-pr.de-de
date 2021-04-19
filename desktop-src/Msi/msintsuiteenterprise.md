---
description: Unter den Betriebssystemen Windows 2000 und höher legt das Installationsprogramm die msintsuiteenterprise-Eigenschaft auf 1 fest, wenn Windows 2000 Advanced Server installiert ist.
ms.assetid: f5384467-3791-4b0b-a70e-b5343c70db46
title: Msintsuiteenterprise (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 137b4ece4dbaecdd83b78fd2ce7cfd57820e029d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372244"
---
# <a name="msintsuiteenterprise-property"></a>Msintsuiteenterprise (Eigenschaft)

Unter den Betriebssystemen Windows 2000 und höher legt das Installationsprogramm die **msintsuiteenterprise** -Eigenschaft auf 1 fest, wenn Windows 2000 Advanced Server installiert ist. Der Installer legt diese Eigenschaft nur dann auf 1 fest, wenn das "Ver \_ Suite \_ Enterprise"-Flag in der [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) -Struktur festgelegt ist. Andernfalls legt das Installationsprogramm diese Eigenschaft nicht fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 
