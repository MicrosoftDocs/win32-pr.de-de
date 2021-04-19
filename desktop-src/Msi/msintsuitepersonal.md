---
description: Unter den Betriebssystemen Windows XP und höher legt das Installationsprogramm die Eigenschaft msintsuitepersonal auf 1 fest, wenn das Betriebssystem Windows XP Home Edition ist.
ms.assetid: 324a4c45-bd64-4361-90ba-6a0554a9c5ef
title: Msintsuitepersonal (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e8932cf2d2c9c5079d6955571512cbc9836e41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369658"
---
# <a name="msintsuitepersonal-property"></a>Msintsuitepersonal (Eigenschaft)

Unter den Betriebssystemen Windows XP und höher legt das Installationsprogramm die Eigenschaft **msintsuitepersonal** auf 1 fest, wenn das Betriebssystem Windows XP Home Edition ist. Der Installer legt diese Eigenschaft nur dann auf 1 fest, wenn das \_ kennflag der Ver Suite \_ in der [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) -Struktur festgelegt ist. Andernfalls legt das Installationsprogramm diese Eigenschaft nicht fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 
