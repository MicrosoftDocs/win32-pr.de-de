---
description: Das Festlegen der SHORTFILENAMES-Eigenschaft bewirkt, dass anstelle von langen Dateinamen kurze Dateinamen für die Namen von Zieldateien verwendet werden. Dies wirkt sich nicht auf die Dateinamen aus, die das Installationsprogramm an der Quelle sucht.
ms.assetid: b330f9c3-3297-45cf-915c-5fbb291b8afb
title: SHORTFILENAMES(Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb64d9f2078a1455aa79bfec077e6108f4a8a5bd9ced7d246c5fe588919b33d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628410"
---
# <a name="shortfilenames-property"></a>SHORTFILENAMES(Eigenschaft)

Das Festlegen **der SHORTFILENAMES-Eigenschaft** bewirkt, dass anstelle von langen Dateinamen kurze Dateinamen für die Namen von Zieldateien verwendet werden. Dies wirkt sich nicht auf die Dateinamen aus, die das Installationsprogramm an der Quelle sucht.

## <a name="default-value"></a>Standardwert

Lange Namen werden vom Installationsprogramm verwendet, wenn die **SHORTFILENAMES-Eigenschaft** nicht festgelegt ist und das Zielvolumen lange Namen unterstützt. Kurznamen werden vom Installationsprogramm verwendet, wenn das Zielvolumen lange Namen nicht unterstützt.

## <a name="remarks"></a>Hinweise

Wenn die **SHORTFILENAMES-Eigenschaft** festgelegt ist, erstellt das Installationsprogramm Ordner und installiert Dateien mit kurzen Dateinamen aus kurzen langen Paaren, die in der Dateitabelle oder der \| [Verzeichnistabelle aufgeführt sind.](directory-table.md) [](file-table.md)

Anwendungen können die [**GetShortPathName-Funktion**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) verwenden, um die Kurzpfadform eines angegebenen Dateipfads abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 
