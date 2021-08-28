---
title: DownloadManager.getDownloadCollection-Methode
description: Hinweis In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt. Die getDownloadCollection-Methode ruft die angegebene Downloadsammlung ab.
ms.assetid: 743d6bcf-2d5b-4a30-a4ef-4538cf7c901e
keywords:
- getDownloadCollection-Windows Media Player
- getDownloadCollection-Methode Windows Media Player , DownloadManager-Klasse
- DownloadManager-Klasse Windows Media Player , getDownloadCollection-Methode
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
ms.openlocfilehash: 57fc729296f15b39e603683cab38e3d0d878733ab0990d9876e32b4001a15cf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749620"
---
# <a name="downloadmanagergetdownloadcollection-method"></a>DownloadManager.getDownloadCollection-Methode

> [!Note]  
> In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die **getDownloadCollection-Methode** ruft die angegebene Downloadsammlung ab.

## <a name="syntax"></a>Syntax


```JScript
retVal = DownloadManager.getDownloadCollection(
  collectionId
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*collectionId* \[ In\]
</dt> <dd>

**Number** **(long)** gibt die ID der abzurufenden Downloadsammlung an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt ein **DownloadCollection-Objekt** zurück.

## <a name="remarks"></a>Hinweise

Sie müssen zuerst *DownloadManager aufrufen.* **createDownloadCollection,** um eine neue Sammlung zu erstellen und ihren ID-Wert abzurufen.

Eine vorhandene Downloadsammlung kann Elemente enthalten, die als abgebrochen markiert wurden.

In einer vorherigen Sitzung nicht abgeschlossene Echtzeitdownloadelemente werden nicht als Teil der Auflistung abgerufen. Hintergrunddownloads, die vor der aktuellen Sitzung abgeschlossen wurden, verbleiben bis zum Entfernen in der Downloadsammlung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DownloadManager-Objekt**](downloadmanager-object.md)
</dt> <dt>

[**DownloadManager. createDownloadCollection**](downloadmanager-createdownloadcollection.md)
</dt> <dt>

[**DownloadCollection-Objekt**](downloadcollection-object.md)
</dt> </dl>

 

 





