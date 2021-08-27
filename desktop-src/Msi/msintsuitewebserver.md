---
description: Unter Windows Betriebssystemen 2000 und höher legt das Installationsprogramm die MsiNTSuiteWebServer-Eigenschaft auf 1 fest, wenn das Installationsprogramm auf einer Webedition von Windows Server 2003 ausgeführt wird.
ms.assetid: de462ba2-4654-4f47-9dd7-3bc9c6f0af0e
title: MsiNTSuiteWebServer (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60c920dc97733a6a8bc134f2ac0c76d449afd6a5ce39e5f8e0555d30daa78952
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129220"
---
# <a name="msintsuitewebserver-property"></a>MsiNTSuiteWebServer (Eigenschaft)

Unter Windows Betriebssystemen 2000 und höher legt das Installationsprogramm die **MsiNTSuiteWebServer-Eigenschaft** auf 1 fest, wenn das Installationsprogramm auf einer Webedition von Windows Server 2003 ausgeführt wird. Das Installationsprogramm legt diese Eigenschaft nur dann auf 1 fest, wenn das VER \_ SUITE \_ BLADE-Flag in der [**OSVERSIONINFOEX-Struktur festgelegt**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) ist. Andernfalls wird diese Eigenschaft vom Installationsprogramm nicht festgelegt.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist nur mit dem Windows Server 2003 des Installationsprogramms verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 
