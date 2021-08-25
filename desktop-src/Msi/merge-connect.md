---
description: Die Verbinden-Methode des Merge-Objekts verbindet ein Modul mit einem zusätzlichen Feature. Das Modul muss bereits mit der Datenbank zusammengeführt worden sein oder wird mit der Datenbank zusammengeführt. Das Feature muss vorhanden sein, bevor diese Funktion aufgerufen wird.
ms.assetid: 1c1ef664-792c-4cdc-b468-1ffe0b7810a5
title: Zusammenführen. Verbinden-Methode (Mergemod.h)
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
ms.openlocfilehash: c28aafaac9f8224ea4f622b2e63f81d9dc458d72e98c6e22c348087794e9e7a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926670"
---
# <a name="mergeconnect-method"></a>Zusammenführen. Verbinden-Methode

Die **Verbinden-Methode** des [**Merge-Objekts**](merge-object.md) verbindet ein Modul mit einem zusätzlichen Feature. Das Modul muss bereits mit der Datenbank zusammengeführt worden sein oder wird mit der Datenbank zusammengeführt. Das Feature muss vorhanden sein, bevor diese Funktion aufgerufen wird.

An der Datenbank vorgenommene Änderungen werden nicht auf dem Datenträger gespeichert, es sei denn, die [**CloseDatabase-Methode**](merge-closedatabase.md) wird aufgerufen, wobei *bCommit* auf **TRUE** festgelegt ist.

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

Der Name eines features, das bereits in der Datenbank vorhanden ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Fehler können über die [**Errors-Eigenschaft**](merge-errors.md) abgerufen werden. Fehler und Informationsmeldungen werden an die aktuelle Protokolldatei gesendet.

### <a name="c"></a>C++

Weitere Informationen finden Sie [**unter Verbinden-Funktion.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1.0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
