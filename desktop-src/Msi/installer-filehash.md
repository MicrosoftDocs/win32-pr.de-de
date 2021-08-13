---
description: Die FileHash-Methode des Installer-Objekts verwendet den Pfad zu einer Datei und gibt einen 128-Bit-Hash dieser Datei zurück. Die Dateihashinformationen werden als Datensatzobjekt zurückgegeben. Der gesamte 128-Bit-Dateihash wird als vier 32-Bit-IntegerData-Eigenschaftenfelder zurückgegeben.
ms.assetid: 065ffde1-4d7c-4e71-9315-7926d4cd38ed
title: Installer.FileHash-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileHash
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a2da76ef3f0606002e26e8c320f83ca45e46bbbeb573d509c235c9fca8932247
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118630791"
---
# <a name="installerfilehash-method"></a>Installer.FileHash-Methode

Die **FileHash-Methode** des [**Installer-Objekts**](installer-object.md) verwendet den Pfad zu einer Datei und gibt einen 128-Bit-Hash dieser Datei zurück. Die Dateihashinformationen werden als [**Datensatzobjekt zurückgegeben.**](record-object.md) Der gesamte 128-Bit-Dateihash wird als vier [**32-Bit-IntegerData-Eigenschaftenfelder**](record-integerdata.md) zurückgegeben.

Die im [**Datensatzobjekt**](record-object.md) zurückgegebenen Werte entsprechen den vier Feldern der [**MSIFILEHASHINFO-Struktur,**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo) die von [**MsiGetFileHash zurückgegeben wird.**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) Die Nummerierung von vier Feldern basiert in der [MsiFileHash-Tabelle auf 1.](msifilehash-table.md)

-   Feld 1 entspricht der HashPart1-Spalte.
-   Feld 2 entspricht der HashPart2-Spalte.
-   Feld 3 entspricht der HashPart3-Spalte.
-   Feld 4 entspricht der HashPart4-Spalte.

## <a name="syntax"></a>Syntax


```JScript
Installer.FileHash(
  FilePath,
  Options
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Filepath* 
</dt> <dd>

Pfad zur Datei, für die ein Hashwert verwendet werden soll.

</dd> <dt>

*Optionen* 
</dt> <dd>

Für die zukünftige Verwendung reserviert.

Der Wert dieses Parameters muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg gibt diese Methode ein [**Datensatzobjekt zurück,**](record-object.md) das den Hash der Datei enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Standarddateiversionsierung](default-file-versioning.md)
</dt> <dt>

[Verwalten von Dateigrößen und -versionen](manage-file-sizes-and-versions.md)
</dt> <dt>

[MsiFileHash-Tabelle](msifilehash-table.md)
</dt> <dt>

[**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> </dl>

 

 




