---
description: Die sourcelistaddsource-Methode fügt eine Netzwerk-oder URL-Quelle hinzu. Akzeptiert SourcePath, Type und Index als Parameter. Diese Methode ruft msisourcelistaddsourceex auf.
ms.assetid: 61a8873f-c4ad-43d7-8bbb-5a2534ef2de7
title: Product. sourcelistaddsource-Methode
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
ms.openlocfilehash: e0cfda9b8eab0e7dd00afd15eb701a6e7decf2ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372316"
---
# <a name="productsourcelistaddsource-method"></a>Product. sourcelistaddsource-Methode

Die **sourcelistaddsource** -Methode fügt eine Netzwerk-oder URL-Quelle hinzu. Akzeptiert *SourcePath*,*Type* und *Index* als Parameter. Diese Methode ruft [**msisourcelistaddsourceex**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)auf.

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

*Type* 
</dt> <dd>

Typ der hinzu zufügenden Quelle: msisourcetype \_ Network oder msisourcetype \_ URL.

</dd> <dt>

*SourcePath* 
</dt> <dd>

Der Pfad zur hinzu zufügenden Quelle.

</dd> <dt>

*Index* 
</dt> <dd>

Wenn **sourcelistaddsource** mit einer neuen Quelle aufgerufen wird und *Index* auf 0 festgelegt ist, fügt das Installationsprogramm die Quelle am Ende der Quell Liste hinzu.

Wenn diese Funktion mit einer bereits in der Quell Liste vorhandenen Quelle aufgerufen wird und der *Index* auf 0 festgelegt ist, behält das Installationsprogramm den vorhandenen Index der Quelle bei.

Wenn die Funktion mit einer vorhandenen Quelle in der Quell Liste aufgerufen wird und der *Index* auf einen Wert ungleich 0 (null) festgelegt ist, wird die Quelle aus der aktuellen Position in der Liste entfernt und an der durch *Index* angegebenen Position eingefügt, bevor eine Quelle vorhanden ist, die an dieser Position bereits vorhanden ist.

Wenn die Funktion mit einer neuen Quelle aufgerufen wird und der *Index* auf einen Wert ungleich 0 (null) festgelegt ist, wird die Quelle an der durch *Index* angegebenen Position eingefügt, bevor eine Quelle vorhanden ist, die an dieser Position bereits vorhanden ist. Der Indexwert für alle Quellen in der Liste nach dem durch *Index* angegebenen Index wird aktualisiert, um sicherzustellen, dass eindeutige Indexwerte und die bereits vorhandene Reihenfolge unverändert bleiben.

Wenn *Index* größer als die Anzahl der Quellen in der Liste ist, wird die Quelle am Ende der Liste mit einem Indexwert eingefügt, der größer als jede vorhandene Quelle ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ iproduct ist definiert als 000c10a0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Product**](product-object.md)
</dt> <dt>

[**Msisourcelistaddsourceex**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




