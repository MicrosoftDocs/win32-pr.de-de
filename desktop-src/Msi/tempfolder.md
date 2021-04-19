---
description: Der Installer legt die TempFolder-Eigenschaft auf den vollständigen Pfad zum temporären Ordner fest. Autoren sollten die TempFolder-Eigenschaft nicht festlegen müssen.
ms.assetid: 841dd1b3-249c-49e1-b462-82da65b4b023
title: TempFolder (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf042086d8bb174a02a7b421ced1133a70016e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359230"
---
# <a name="tempfolder-property"></a>TempFolder (Eigenschaft)

Der Installer legt die **TempFolder** -Eigenschaft auf den vollständigen Pfad zum temporären Ordner fest.

Autoren sollten die **TempFolder** -Eigenschaft nicht festlegen müssen. Windows Installer verwendet die [**GetTempPath**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) -Funktion, um den Pfad des für temporäre Dateien vorgesehenen Verzeichnisses abzurufen und diese Eigenschaft festzulegen.

## <a name="remarks"></a>Bemerkungen

Ein allgemeiner Wert für diese Eigenschaft ist C: \\ Temp.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 
