---
description: Der Installer legt die msitabletpc-Eigenschaft auf einen Wert ungleich 0 (null) fest, wenn das aktuelle Betriebssystem Windows XP Tablet PC Edition ist.
ms.assetid: b178a98e-b6f8-4ff8-b554-e47c3b39f892
title: Msitabletpc (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf2878dbaa895e0924a50900d331db0b879edc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362042"
---
# <a name="msitabletpc-property"></a>Msitabletpc (Eigenschaft)

Der Installer legt die **msitabletpc** -Eigenschaft auf einen Wert ungleich 0 (null) fest, wenn das aktuelle Betriebssystem Windows XP Tablet PC Edition ist. Das Installationsprogramm verwendet die [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) -Funktion mit **SM \_ TabletPC**, und die-Eigenschaft empfängt den von dieser Funktion zurückgegebenen Wert ungleich 0 (null). Wenn das aktuelle System nicht Windows XP Tablet PC Edition ist, gibt die **GetSystemMetrics** -Funktion 0 (null) zurück, und das Installationsprogramm legt diese Eigenschaft nicht fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 4,5 unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
