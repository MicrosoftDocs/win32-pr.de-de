---
description: Die Intel-Eigenschaft wird vom Windows Installer auf die numerische Prozessorebene festgelegt, wenn auf einem Intel-Prozessor ausgeführt wird.
ms.assetid: c1190df2-0440-4dd1-bce5-61d899f71437
title: Intel-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd5b4fe488867a67da1f97ce4564bb8ce530b89417554a91a8734bee6e863f44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013238"
---
# <a name="intel-property"></a>Intel-Eigenschaft

Die **Intel-Eigenschaft** wird vom Windows Installer auf die numerische Prozessorebene festgelegt, wenn auf einem Intel-Prozessor ausgeführt wird. Die Werte sind identisch mit dem *Feld wProcessorLevel* der [**SYSTEM \_ INFO-Struktur.**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) Bei ausführung auf einem x64-Prozessor legt der Windows Installer die **Intel-Eigenschaft** so fest, dass sie den vom x64-Computer emulierten x86-Prozessor widerspiegelt, wie vom Betriebssystem gemeldet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den Windows Service [Pack-Mindestanforderungen,](windows-installer-portal.md) die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time Anforderungen für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 
