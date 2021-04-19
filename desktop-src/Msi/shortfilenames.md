---
description: Das Festlegen der Eigenschaft shortfileames bewirkt, dass kurze Dateinamen für die Namen von Zieldateien anstelle von langen Dateinamen verwendet werden. Dies hat keine Auswirkung auf die Dateinamen, nach denen das Installationsprogramm an der Quelle sucht.
ms.assetid: b330f9c3-3297-45cf-915c-5fbb291b8afb
title: Shortfile Ames (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e347e5ec400a1593858f0cac558f33528e25396e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362174"
---
# <a name="shortfilenames-property"></a>Shortfile Ames (Eigenschaft)

Das Festlegen der Eigenschaft **shortfileames** bewirkt, dass kurze Dateinamen für die Namen von Zieldateien anstelle von langen Dateinamen verwendet werden. Dies hat keine Auswirkung auf die Dateinamen, nach denen das Installationsprogramm an der Quelle sucht.

## <a name="default-value"></a>Standardwert

Lange Namen werden vom Installationsprogramm verwendet, wenn die **shortfile Ames** -Eigenschaft nicht festgelegt ist und das Ziel Volume lange Namen unterstützt. Kurznamen werden vom Installationsprogramm verwendet, wenn das Ziel Volume keine langen Namen unterstützt.

## <a name="remarks"></a>Bemerkungen

Wenn die **shortfileames** -Eigenschaft festgelegt ist, erstellt das Installationsprogramm Ordner und installiert Dateien mit kurzen Dateinamen aus allen kurzen \| langen Paaren, die in der [Dateitabelle](file-table.md) oder der [Verzeichnis Tabelle](directory-table.md)aufgeführt sind.

Anwendungen können die [**GetShortPathName**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) -Funktion verwenden, um die Kurzpfad Form eines angegebenen Dateipfads abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 
