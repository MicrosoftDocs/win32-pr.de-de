---
description: Der Installer legt die VersionNT64-Eigenschaft nur dann auf die Versionsnummer des Betriebssystems fest, wenn das System auf einem 64-Bit-Computer ausgeführt wird.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: VersionNT64-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3b1b5a26b2ba45b859b6330bf153300e239074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352933"
---
# <a name="versionnt64-property"></a>VersionNT64-Eigenschaft

Der Installer legt die **VersionNT64** -Eigenschaft nur dann auf die Versionsnummer des Betriebssystems fest, wenn das System auf einem 64-Bit-Computer ausgeführt wird. Die-Eigenschaft ist nicht definiert, wenn das Betriebssystem nicht 64-Bit ist.

Der Wert ist eine ganze Zahl: MajorVersion \* 100 + MinorVersion.

Aus Kompatibilitätsgründen wird die-Eigenschaft ebenfalls nicht definiert, wenn die [**Vorlagen Zusammenfassungs**](template-summary.md) Eigenschaft angibt, dass das Paket für 32-Bit-Intel-Systeme und das Betriebssystem eine 64-Bit-Architektur ist, die nicht Intel64 oder x64 ist (z. b. ARM64).

## <a name="remarks"></a>Bemerkungen

Bedingte Ausdrücke testen für 64-Bit-Fenster einfach mithilfe des Eigenschafts namens oder durch Überprüfen der Version mithilfe eines Vergleichs Operators.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




