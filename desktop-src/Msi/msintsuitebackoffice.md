---
description: Unter Windows Betriebssystemen 2000 und höher legt das Installationsprogramm die MsiNTSuiteBackOffice-Eigenschaft auf 1 fest, wenn Microsoft BackOffice-Komponenten installiert sind.
ms.assetid: 31493732-3082-4dd9-9a20-21658f53c8c2
title: MsiNTSuiteBackOffice (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cf3c65e1f5d1d528dd35232900a9aef12bdf344d1d2859eef814d1030e6249d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944825"
---
# <a name="msintsuitebackoffice-property"></a>MsiNTSuiteBackOffice (Eigenschaft)

Unter Windows Betriebssystemen 2000 und höher legt das Installationsprogramm die **MsiNTSuiteBackOffice-Eigenschaft** auf 1 fest, wenn Microsoft BackOffice-Komponenten installiert sind. Das Installationsprogramm legt diese Eigenschaft nur dann auf 1 fest, wenn das \_ VER SUITE \_ BACKOFFICE-Flag in der [**OSVERSIONINFOEX-Struktur festgelegt**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) ist. Andernfalls wird diese Eigenschaft vom Installationsprogramm nicht festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 
