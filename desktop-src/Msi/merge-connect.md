---
description: Mit der Connect-Methode des Merge-Objekts wird ein Modul mit einer zusätzlichen Funktion verbunden. Das Modul muss bereits in der Datenbank zusammengeführt worden sein oder in der Datenbank zusammengeführt werden. Die Funktion muss vorhanden sein, bevor diese Funktion aufgerufen wird.
ms.assetid: 1c1ef664-792c-4cdc-b468-1ffe0b7810a5
title: Merge. Connect-Methode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Connect
- IMsmMerge.Connect
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: da66f7dfe4203e80d4778ae9b39c665a66164384
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358369"
---
# <a name="mergeconnect-method"></a>Merge. Connect-Methode

Mit der **Connect** -Methode des [**Merge**](merge-object.md) -Objekts wird ein Modul mit einer zusätzlichen Funktion verbunden. Das Modul muss bereits in der Datenbank zusammengeführt worden sein oder in der Datenbank zusammengeführt werden. Die Funktion muss vorhanden sein, bevor diese Funktion aufgerufen wird.

An der Datenbank vorgenommene Änderungen werden nicht auf dem Datenträger gespeichert, es sei denn, die [**CloseDatabase**](merge-closedatabase.md) -Methode wird aufgerufen, wenn *bcommit* auf **true** festgelegt

## <a name="syntax"></a>Syntax


```JScript
Merge.Connect(
  Feature
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Feature* 
</dt> <dd>

Der Name eines Features, das bereits in der Datenbank vorhanden ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Fehler können mithilfe der [**Errors**](merge-errors.md) -Eigenschaft abgerufen werden. Fehler und Informationsmeldungen werden in der aktuellen Protokolldatei gepostet.

### <a name="c"></a>C++

Siehe [**Connect**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) -Funktion.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
