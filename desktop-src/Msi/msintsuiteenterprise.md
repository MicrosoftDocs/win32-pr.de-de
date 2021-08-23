---
description: Unter Windows Betriebssystemen 2000 und höher legt das Installationsprogramm die MsiNTSuiteEnterprise-Eigenschaft auf 1 fest, wenn Windows 2000 Advanced Server installiert ist.
ms.assetid: f5384467-3791-4b0b-a70e-b5343c70db46
title: MsiNTSuiteEnterprise(Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 242bf1c95db7d4101362a7b72b4cfa99009a93cc2fa399d1b4b81d93aabbd16c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944653"
---
# <a name="msintsuiteenterprise-property"></a>MsiNTSuiteEnterprise(Eigenschaft)

Unter Windows Betriebssystemen der Version 2000 und höher legt das Installationsprogramm die **MsiNTSuiteEnterprise-Eigenschaft** auf 1 fest, wenn Windows 2000 Advanced Server installiert ist. Das Installationsprogramm legt diese Eigenschaft nur dann auf 1 fest, wenn das VER \_ SUITE \_ ENTERPRISE-Flag in der [**OSVERSIONINFOEX-Struktur festgelegt**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) ist. Andernfalls wird diese Eigenschaft vom Installationsprogramm nicht festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 
