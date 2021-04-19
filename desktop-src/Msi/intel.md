---
description: Die Intel-Eigenschaft wird von der Windows Installer auf die numerische Prozessor Ebene festgelegt, wenn Sie auf einem Intel-Prozessor ausgeführt wird.
ms.assetid: c1190df2-0440-4dd1-bce5-61d899f71437
title: Intel-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab73f35b371d3bf8323fe2a3f3de1608666bc181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361333"
---
# <a name="intel-property"></a>Intel-Eigenschaft

Die **Intel** -Eigenschaft wird von der Windows Installer auf die numerische Prozessor Ebene festgelegt, wenn Sie auf einem Intel-Prozessor ausgeführt wird. Die Werte sind identisch mit dem *wprocessorlevel* -Feld der [**System \_ Info**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) -Struktur. Bei der Ausführung auf einem x64-Prozessor legt der Windows Installer die **Intel** -Eigenschaft so fest, dass der vom x64-Computer durch das Betriebssystem gemeldete x86-Prozessor wiedergegeben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 
