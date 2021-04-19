---
title: DownloadCollection.id
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die ID-Eigenschaft ruft die ID der Download Auflistung ab.
ms.assetid: b5b17f22-913c-4055-8958-e3efac819b2b
keywords:
- DownloadCollection.ID Windows Media Player
topic_type:
- apiref
api_name:
- DownloadCollection.id
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9edcca4f56c485951ca907ae228dfec7a958b308
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362158"
---
# <a name="downloadcollectionid"></a>DownloadCollection.id

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **ID** -Eigenschaft ruft die ID der Download Auflistung ab.

## <a name="syntax"></a>Syntax

``` syntax
DownloadManager.getDownloadCollection(
        collectionId
        ).id
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).

## <a name="remarks"></a>Bemerkungen

Wenn der Download-Manager eine neue Download Sammlung erstellt, wird der Sammlung eine ID-Nummer zugewiesen. ID-Nummern werden zwischen Windows Media Player-Sitzungen und Betriebssystem Sitzungen beibehalten.

Die ID-Nummern sind nicht eindeutig. Es sind jedoch genügend ID-Nummern im 32-Bit-Wert verfügbar, dass es äußerst unwahrscheinlich ist, dass eine vorhandene ID jemals durch eine neue ID überschrieben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Download Collection-Objekt**](downloadcollection-object.md)
</dt> </dl>

 

 





