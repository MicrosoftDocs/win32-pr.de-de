---
description: Die ExtractCab-Methode des Merge-Objekts extrahiert die eingebettete CAB-Datei aus einem Modul und speichert Sie als die angegebene Datei. Das Installationsprogramm erstellt diese Datei, wenn Sie noch nicht vorhanden ist, und wird überschrieben, wenn Sie vorhanden ist.
ms.assetid: a6fe8b69-8f4a-45f7-b7e6-7620a00500bb
title: Merge. ExtractCab-Methode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractCAB
- IMsmMerge.ExtractCAB
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: d0bdc79fb0087456d035bf732faca384b35b2a9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359231"
---
# <a name="mergeextractcab-method"></a>Merge. ExtractCab-Methode

Die **ExtractCab** -Methode des [**Merge**](merge-object.md) -Objekts extrahiert die eingebettete CAB-Datei aus einem Modul und speichert Sie als die angegebene Datei. Das Installationsprogramm erstellt diese Datei, wenn Sie noch nicht vorhanden ist, und wird überschrieben, wenn Sie vorhanden ist.

## <a name="syntax"></a>Syntax


```JScript
Merge.ExtractCAB(
  FileName
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FileName* 
</dt> <dd>

Die voll qualifizierte Zieldatei.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="c"></a>C++

Siehe [**ExtractCab**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab) -Funktion.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
