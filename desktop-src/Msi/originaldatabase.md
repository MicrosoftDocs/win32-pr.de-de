---
description: Der Windows Installer legt die Eigenschaft originaldatabase auf den Pfad der Installations Datenbank fest, mit der die Installation gestartet wird.
ms.assetid: 985c70a4-1575-4226-a8c2-a7a21f7a0dbd
title: Originaldatabase (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 592bc86a9ef53602f686e48b3c98dad17a49cfe1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367011"
---
# <a name="originaldatabase-property"></a>Originaldatabase (Eigenschaft)

Der Windows Installer legt die Eigenschaft **originaldatabase** auf den Pfad der Installations Datenbank fest, mit der die Installation gestartet wird. Wenn die Installation über eine Befehlszeile gestartet wird, hängt der Wert davon ab, ob die Option "Recache Package" (das-v-Flag) in der Eigenschaft " [**REINSTALLMODE**](reinstallmode.md) " vorhanden ist.



| Installationsmethode                                                                                                                                                                                  | Originaldatabase-Wert                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Alle Installationen, die durch Aufrufen des Pfads des Installationspakets (MSI-Datei) gestartet wurden.                                                                                                              | Pfad zum Installationspaket (MSI-Datei). |
| Die Installation wurde von der Befehlszeile aus gestartet. Die Installation wird nicht von einem Paketpfad gestartet. Die Recache-Option (-v-Flag) ist in der [**REINSTALLMODE**](reinstallmode.md) -Eigenschaft vorhanden.     | Der Pfad zur Datenbank in der Quelle.           |
| Die Installation wurde von der Befehlszeile aus gestartet. Die Installation wird nicht von einem Paketpfad gestartet. Die Recache-Option (-v-Flag) ist in der [**REINSTALLMODE**](reinstallmode.md) -Eigenschaft nicht vorhanden. | Der Pfad zur zwischengespeicherten Datenbank.                  |



 

## <a name="remarks"></a>Bemerkungen

Bei der erstmaligen Installation kann eine benutzerdefinierte Aktion, die vor der [ResolveSource-Aktion](resolvesource-action.md) sequenziert wurde, die **originaldatabase** -Eigenschaft verwenden, um den Speicherort der Installationsquelle zu ermitteln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




