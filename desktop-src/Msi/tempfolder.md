---
description: Das Installationsprogramm legt die TempFolder-Eigenschaft auf den vollständigen Pfad zum Ordner Temp fest. Autoren sollten die TempFolder-Eigenschaft nicht festlegen müssen.
ms.assetid: 841dd1b3-249c-49e1-b462-82da65b4b023
title: TempFolder-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5ded141982c12204eb5267357cedded6521eccb7cc47a3bf000b026faf9aed4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626505"
---
# <a name="tempfolder-property"></a>TempFolder-Eigenschaft

Das Installationsprogramm legt die **TempFolder-Eigenschaft** auf den vollständigen Pfad zum Ordner Temp fest.

Autoren sollten die **TempFolder-Eigenschaft nicht festlegen** müssen. Windows Das Installationsprogramm verwendet [**die GetTempPath-Funktion,**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) um den Pfad des Verzeichnisses abzurufen, das für temporäre Dateien vorgesehen ist, und um diese Eigenschaft zu festlegen.

## <a name="remarks"></a>Hinweise

Ein gängiger Wert für diese Eigenschaft ist C: \\ Temp.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 
