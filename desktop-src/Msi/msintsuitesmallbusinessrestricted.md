---
description: Unter den Betriebssystemen Windows 2000 und höher legt das Installationsprogramm die Eigenschaft msintsuitesmallbusinessrestricted auf 1 fest, wenn Microsoft Small Business Server mit der eingeschränkten Client Lizenz in Kraft installiert wird.
ms.assetid: a7100df4-6fe4-4159-ba94-9b5bd1803107
title: Msintsuitesmallbusinessrestricted (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d85fa7fe83c0c8c7cd40788453d1078e7a6b94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369492"
---
# <a name="msintsuitesmallbusinessrestricted-property"></a>Msintsuitesmallbusinessrestricted (Eigenschaft)

Unter den Betriebssystemen Windows 2000 und höher legt das Installationsprogramm die Eigenschaft **msintsuitesmallbusinessrestricted** auf 1 fest, wenn Microsoft Small Business Server mit der eingeschränkten Client Lizenz in Kraft installiert wird. Der Installer legt diese Eigenschaft nur dann auf 1 fest, wenn das Flag der Ver \_ Suite \_ SmallBusiness \_ restricted in der [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) -Struktur festgelegt ist. Andernfalls legt das Installationsprogramm diese Eigenschaft nicht fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 
