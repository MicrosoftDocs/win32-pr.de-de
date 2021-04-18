---
description: Unter den Betriebssystemen Windows 2000 und höher legt das Installationsprogramm die msintsuitebackoffice-Eigenschaft auf 1 fest, wenn Microsoft BackOffice-Komponenten installiert sind.
ms.assetid: 31493732-3082-4dd9-9a20-21658f53c8c2
title: Msintsuitebackoffice (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2d9f2f1d95446c32b4f2addf520f3d5b4dadc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371526"
---
# <a name="msintsuitebackoffice-property"></a>Msintsuitebackoffice (Eigenschaft)

Unter den Betriebssystemen Windows 2000 und höher legt das Installationsprogramm die **msintsuitebackoffice** -Eigenschaft auf 1 fest, wenn Microsoft BackOffice-Komponenten installiert sind. Das Installationsprogramm legt diese Eigenschaft nur dann auf 1 fest, wenn das "Ver \_ Suite \_ BackOffice"-Flag in der [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) -Struktur festgelegt ist. Andernfalls legt das Installationsprogramm diese Eigenschaft nicht fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 
