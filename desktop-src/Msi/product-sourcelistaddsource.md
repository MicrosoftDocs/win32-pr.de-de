---
description: Die SourceListAddSource-Methode fügt ein Netzwerk oder eine URL-Quelle hinzu. Akzeptiert SourcePath, Type und Index als Parameter. Diese Methode ruft MsiSourceListAddSourceEx auf.
ms.assetid: 61a8873f-c4ad-43d7-8bbb-5a2534ef2de7
title: Product.SourceListAddSource-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListAddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b95185cbd25354314eace5da7704da51dbbefe024ba8597c0eed41a688984117
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925870"
---
# <a name="productsourcelistaddsource-method"></a>Product.SourceListAddSource-Methode

Die **SourceListAddSource-Methode** fügt ein Netzwerk oder eine URL-Quelle hinzu. Akzeptiert *SourcePath*,*Type* und *Index* als Parameter. Diese Methode ruft [**MsiSourceListAddSourceEx auf.**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)

## <a name="syntax"></a>Syntax


```JScript
Product.SourceListAddSource(
  Type,
  SourcePath,
  Index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Typ* 
</dt> <dd>

Typ der quelle, die hinzugefügt werden soll: MSISOURCETYPE \_ NETWORK oder MSISOURCETYPE \_ URL.

</dd> <dt>

*Sourcepath* 
</dt> <dd>

Pfad zur quelle, die hinzugefügt werden soll.

</dd> <dt>

*Index* 
</dt> <dd>

Wenn **SourceListAddSource** mit einer neuen Quelle aufgerufen wird und *Index* auf 0 festgelegt ist, fügt das Installationsprogramm die Quelle am Ende der Quellliste hinzu.

Wenn diese Funktion mit einer quelle aufgerufen wird, die bereits in der Quellliste vorhanden ist, und *Index* auf 0 festgelegt ist, behält das Installationsprogramm den vorhandenen Index der Quelle bei.

Wenn die Funktion mit einer vorhandenen Quelle in der Quellliste aufgerufen wird und *Index* auf einen Wert von nicht 0 (null) festgelegt ist, wird die Quelle aus ihrer aktuellen Position in der Liste entfernt und an der durch *Index* angegebenen Position vor jeder Quelle eingefügt, die bereits an dieser Position vorhanden ist.

Wenn die Funktion mit einer neuen Quelle aufgerufen wird und *Index* auf einen Wert von nicht 0 (null) festgelegt ist, wird die Quelle an der von *Index* angegebenen Position vor jeder Quelle eingefügt, die bereits an dieser Position vorhanden ist. Der Indexwert für alle Quellen in der Liste, nachdem der durch *Index* angegebene Index aktualisiert wurde, um sicherzustellen, dass eindeutige Indexwerte und die bereits vorhandene Reihenfolge garantiert unverändert bleiben.

Wenn *Index* größer als die Anzahl der Quellen in der Liste ist, wird die Quelle am Ende der Liste mit einem Indexwert platziert, der größer als jede vorhandene Quelle ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installer 3.0 oder höher auf Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct ist als \_ 000C10A0-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Produkt**](product-object.md)
</dt> <dt>

[**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




