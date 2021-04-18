---
description: Das Installationsprogramm legt die VersionNT-Eigenschaft auf die Versionsnummer des Betriebssystems fest. Dies ist nicht definiert, wenn das Betriebssystem nicht Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008 oder Windows 7 entspricht.
ms.assetid: 49005783-0bcb-458e-8266-56e6ea6afb43
title: VersionNT-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61ce8d7d5c738be3b2fd51f2ca3054b8800d4c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358115"
---
# <a name="versionnt-property"></a>VersionNT-Eigenschaft

Das Installationsprogramm legt die **VersionNT** -Eigenschaft auf die Versionsnummer des Betriebssystems fest. Dies ist nicht definiert, wenn das Betriebssystem nicht Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008 oder Windows 7 entspricht. Der Wert ist eine ganze Zahl: MajorVersion \* 100 + MinorVersion.

Bedingte Anweisungen, die vom Betriebssystem abhängen, können diese Eigenschaft verwenden.

Siehe auch [Betriebs System-Eigenschaftswerte](operating-system-property-values.md).

## <a name="remarks"></a>Bemerkungen

Bedingungs Ausdrücke können mit dem Eigenschaftsnamen auf Windows NT, Windows 2000 oder Windows XP testen oder die Version mithilfe eines Vergleichs Operators überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




