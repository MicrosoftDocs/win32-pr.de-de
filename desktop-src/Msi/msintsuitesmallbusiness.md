---
description: Unter Windows Betriebssystemen 2000 und höher legt das Installationsprogramm die MsiNTSuiteSmallBusiness-Eigenschaft auf 1 fest, wenn Microsoft Small Business Server installiert ist.
ms.assetid: 9ac578b9-316f-413c-aae0-4f414109583b
title: MsiNTSuiteSmallBusiness (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1e0dab7d024753a30d6a640cefd1652de137b5cd230a772a5041927dc0e725e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082740"
---
# <a name="msintsuitesmallbusiness-property"></a>MsiNTSuiteSmallBusiness (Eigenschaft)

Unter Windows Betriebssystemen 2000 und höher legt das Installationsprogramm die **MsiNTSuiteSmallBusiness-Eigenschaft** auf 1 fest, wenn Microsoft Small Business Server installiert ist. Das Installationsprogramm legt diese Eigenschaft nur dann auf 1 fest, wenn das VER \_ SUITE \_ SMALLBUSINESS-Flag in der [**OSVERSIONINFOEX-Struktur festgelegt**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) ist. Andernfalls wird diese Eigenschaft vom Installationsprogramm nicht festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 
