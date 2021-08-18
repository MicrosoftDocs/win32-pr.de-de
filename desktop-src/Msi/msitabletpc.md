---
description: Das Installationsprogramm legt die MsiTabletPC-Eigenschaft auf einen Wert ungleich 0 (null) fest, wenn das aktuelle Betriebssystem Windows XP Tablet PC Edition ist.
ms.assetid: b178a98e-b6f8-4ff8-b554-e47c3b39f892
title: MsiTabletPC-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac47dd0d8db3c0e882a965685bb1507dc0103f3e965dfbcb8f4857ada19e17ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145609"
---
# <a name="msitabletpc-property"></a>MsiTabletPC-Eigenschaft

Das Installationsprogramm legt die **MsiTabletPC-Eigenschaft** auf einen Wert ungleich 0 (null) fest, wenn das aktuelle Betriebssystem Windows XP Tablet PC Edition ist. Das Installationsprogramm verwendet die [**GetSystemMetrics-Funktion**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) mit **SM \_ TABLETPC,** und die -Eigenschaft empfängt den von dieser Funktion zurückgegebenen Wert ungleich 0 (null). Wenn das aktuelle System nicht Windows XP Tablet PC Edition ist, gibt die **GetSystemMetrics-Funktion** 0 (null) zurück, und das Installationsprogramm legt diese Eigenschaft nicht fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm 4.5 auf Windows Server 2003 oder Windows XP. Informationen zu den Windows Service [Pack-Mindestanforderungen,](windows-installer-portal.md) die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time Anforderungen für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 3.1 und früheren Versionen](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
