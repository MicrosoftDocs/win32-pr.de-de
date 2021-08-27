---
description: Unter Windows XP- und höher-Betriebssystemen legt das Installationsprogramm die MsiNTSuitePersonal-Eigenschaft auf 1 fest, wenn das Betriebssystem Windows XP Home Edition ist.
ms.assetid: 324a4c45-bd64-4361-90ba-6a0554a9c5ef
title: MsiNTSuitePersonal (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c946b707e0d66a2c5bd3cd9cb6bf75828be9dd8f21e0e81080910a9fac73d353
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944493"
---
# <a name="msintsuitepersonal-property"></a>MsiNTSuitePersonal (Eigenschaft)

Unter Windows XP-Betriebssystemen und höher legt das Installationsprogramm die **MsiNTSuitePersonal-Eigenschaft** auf 1 fest, wenn das Betriebssystem auf XP Home Edition Windows ist. Das Installationsprogramm legt diese Eigenschaft nur dann auf 1 fest, wenn das VER \_ SUITE \_ PERSONAL-Flag in der [**OSVERSIONINFOEX-Struktur festgelegt**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) ist. Andernfalls wird diese Eigenschaft vom Installationsprogramm nicht festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 
