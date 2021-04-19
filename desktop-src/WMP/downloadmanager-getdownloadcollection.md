---
title: Download Manager. getdownloadcollection-Methode
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Mit der getdownloadcollection-Methode wird die angegebene Download Auflistung abgerufen.
ms.assetid: 743d6bcf-2d5b-4a30-a4ef-4538cf7c901e
keywords:
- getdownloadcollection-Methode, Windows Media Player
- getdownloadcollection-Methode, Windows Media Player, Download Manager-Klasse
- Download Manager-Klasse, Windows Media Player, getdownloadcollection-Methode
topic_type:
- apiref
api_name:
- DownloadManager.getDownloadCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e879d82c3f49db08d75b8aec37271e8d966019e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367598"
---
# <a name="downloadmanagergetdownloadcollection-method"></a>Download Manager. getdownloadcollection-Methode

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Mit der **getdownloadcollection** -Methode wird die angegebene Download Auflistung abgerufen.

## <a name="syntax"></a>Syntax


```JScript
retVal = DownloadManager.getDownloadCollection(
  collectionId
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*CollectionId* \[ in\]
</dt> <dd>

**Zahl** (**Long**), die die ID der abzurufenden Download Auflistung angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **downloadcollection** -Objekt zurück.

## <a name="remarks"></a>Bemerkungen

Sie müssen zuerst *Download Manager* anrufen. " **kreatedownloadcollection** " zum Erstellen einer neuen Sammlung und zum Abrufen des ID-Werts.

Eine vorhandene Download Sammlung kann Elemente enthalten, die als abgebrochen markiert wurden.

Echt Zeit Download Elemente, die nicht in einer vorherigen Sitzung abgeschlossen wurden, werden nicht als Teil der Sammlung abgerufen. Hintergrund Downloads, die vor der aktuellen Sitzung abgeschlossen wurden, verbleiben bis zum Entfernen in der Download Auflistung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Download Manager-Objekt**](downloadmanager-object.md)
</dt> <dt>

[**Download Manager. "kreatedownloadcollection"**](downloadmanager-createdownloadcollection.md)
</dt> <dt>

[**Download Collection-Objekt**](downloadcollection-object.md)
</dt> </dl>

 

 





