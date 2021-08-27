---
description: Das Installationsprogramm legt die MsiNTProductType-Eigenschaft für Windows NT-, Windows 2000- und höher-Betriebssysteme fest.
ms.assetid: 6bbc8283-5911-4fbd-8a0f-09c398280e74
title: MsiNTProductType-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93e4c5083e5d1f0195e2e8a8e0cc46213853cb5cf1431535afee7e5362ff5eda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082820"
---
# <a name="msintproducttype-property"></a>MsiNTProductType-Eigenschaft

Das Installationsprogramm legt die **MsiNTProductType-Eigenschaft** für Windows NT-, Windows 2000- und höher-Betriebssysteme fest. Diese Eigenschaft gibt den Windows Produkttyp an.

Für Windows Betriebssysteme 2000 und höher legt das Installationsprogramm die folgenden Werte fest. Beachten Sie, dass die Werte mit denen des **wProductType-Felds** der [**OSVERSIONINFOEX-Struktur**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) identisch sind.



| Wert | Bedeutung                                  |
|-------|------------------------------------------|
| 1     | Windows 2000 Professional und höher      |
| 2     | Windows Domänencontroller 2000 und höher |
| 3     | Windows Server 2000 und höher            |



 

Für Betriebssysteme vor Windows 2000 legt das Installationsprogramm die folgenden Werte fest.



| Wert | Bedeutung                      |
|-------|------------------------------|
| 1     | Windows NT-Arbeitsstation       |
| 2     | Windows NT-Domänencontroller |
| 3     | Windows NT-Server            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den Windows Service [Pack-Mindestanforderungen,](windows-installer-portal.md) die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time Anforderungen für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 
