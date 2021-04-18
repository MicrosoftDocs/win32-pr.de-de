---
description: Die Methode "flehash" des Installerobjekts nimmt den Pfad zu einer Datei an und gibt einen 128-Bit-Hash dieser Datei zurück. Die Datei Hash Informationen werden als Datensatz-Objekt zurückgegeben. Der gesamte 128-Bit-Dateihash wird als 4 32-Bit-IntegerData-Eigenschafts Felder zurückgegeben.
ms.assetid: 065ffde1-4d7c-4e71-9315-7926d4cd38ed
title: Installer. flehash-Methode
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
ms.openlocfilehash: 1a38ef741c5c3a33c526cc78fbdc4551716ed3ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364790"
---
# <a name="installerfilehash-method"></a>Installer. flehash-Methode

Die Methode " **flehash** " des [**Installerobjekts**](installer-object.md) nimmt den Pfad zu einer Datei an und gibt einen 128-Bit-Hash dieser Datei zurück. Die Datei Hash Informationen werden als Datensatz- [**Objekt**](record-object.md)zurückgegeben. Der gesamte 128-Bit-Dateihash wird als 4 32-Bit- [**IntegerData**](record-integerdata.md) -Eigenschafts Felder zurückgegeben.

Die Werte, die im [**Datensatz-Objekt**](record-object.md) zurückgegeben werden, entsprechen den vier Feldern der [**msigetatashinfo**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo) -Struktur, die von " [**msigetflehash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)" zurückgegeben wird. Die Nummerierung von vier Feldern ist 1-basiert in der [msimelehash-Tabelle](msifilehash-table.md).

-   Feld 1 entspricht der HashPart1-Spalte.
-   Feld 2 entspricht der HashPart2-Spalte.
-   Field 3 entspricht der HashPart3-Spalte.
-   Field 4 entspricht der HashPart4-Spalte.

## <a name="syntax"></a>Syntax


```JScript
Installer.FileHash(
  FilePath,
  Options
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FilePath* 
</dt> <dd>

Der Pfad zu der Datei, für die ein Hashwert erstellt werden soll.

</dd> <dt>

*Optionen* 
</dt> <dd>

Für die zukünftige Verwendung reserviert.

Der Wert dieses Parameters muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei erfolgreicher Ausführung gibt diese Methode ein [**Daten Satz Objekt**](record-object.md) zurück, das den Hash der Datei enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Standardmäßige Datei Versionsverwaltung](default-file-versioning.md)
</dt> <dt>

[Verwalten von Dateigrößen und-Versionen](manage-file-sizes-and-versions.md)
</dt> <dt>

[Msiflehash-Tabelle](msifilehash-table.md)
</dt> <dt>

[**Msigetflehash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> </dl>

 

 




