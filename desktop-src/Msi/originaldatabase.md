---
description: Der Windows Installer legt die OriginalDatabase-Eigenschaft auf den Pfad der Installationsdatenbank fest, die zum Starten der Installation verwendet wird.
ms.assetid: 985c70a4-1575-4226-a8c2-a7a21f7a0dbd
title: OriginalDatabase-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28b8ec6b77d013ee89d081c0ff20e3ad00750454e1fa9299d364fdb94e69ccb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145533"
---
# <a name="originaldatabase-property"></a>OriginalDatabase-Eigenschaft

Der Windows Installer legt die **OriginalDatabase-Eigenschaft** auf den Pfad der Installationsdatenbank fest, die zum Starten der Installation verwendet wird. Wenn die Installation über eine Befehlszeile gestartet wird, hängt der Wert davon ab, ob die Recache-Paketoption (das Flag -v) in der [**REINSTALLMODE-Eigenschaft vorhanden**](reinstallmode.md) ist.



| Installationsmethode                                                                                                                                                                                  | OriginalDatabase-Wert                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Jede Installation, die durch Aufrufen des Pfads des Installationspakets gestartet wird (.msi Datei).                                                                                                              | Pfad zum Installationspaket (.msi Datei). |
| Die Installation wird über die Befehlszeile gestartet. Die Installation wird nicht über einen Paketpfad gestartet. Die Recacheoption (-v-Flag) ist in der [**REINSTALLMODE-Eigenschaft**](reinstallmode.md) vorhanden.     | Pfad zur Datenbank in der Quelle.           |
| Die Installation wird über die Befehlszeile gestartet. Die Installation wird nicht über einen Paketpfad gestartet. Die Recacheoption (-v-Flag) ist in der [**REINSTALLMODE-Eigenschaft nicht**](reinstallmode.md) vorhanden. | Pfad zur zwischengespeicherten Datenbank.                  |



 

## <a name="remarks"></a>Hinweise

Bei einer erstmaligen Installation kann eine vor der [ResolveSource-Aktion](resolvesource-action.md) sequenzierte benutzerdefinierte Aktion die **OriginalDatabase-Eigenschaft** verwenden, um den Speicherort der Installationsquelle zu bestimmen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




