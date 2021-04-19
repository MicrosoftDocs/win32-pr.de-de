---
description: Die CloseDatabase-Methode des Merge-Objekts schließt die aktuell geöffnete Windows Installer Datenbank.
ms.assetid: a89fe77a-0099-4c49-b484-c05ee351a66a
title: Merge. CloseDatabase-Methode (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseDatabase
- IMsmMerge.CloseDatabase
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 5df72b9423ad212264736d16db0ae73ded9afef5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350748"
---
# <a name="mergeclosedatabase-method"></a>Merge. CloseDatabase-Methode

Die **CloseDatabase** -Methode des [**Merge**](merge-object.md) -Objekts schließt die aktuell geöffnete Windows Installer Datenbank.

## <a name="syntax"></a>Syntax


```JScript
Merge.CloseDatabase(
  bCommit
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bcommit* 
</dt> <dd>

**True** , wenn Änderungen gespeichert werden sollen, andernfalls **false** .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Durch das Schließen einer Datenbank werden alle Abhängigkeitsinformationen gelöscht, aber keine Fehler, die noch nicht abgerufen wurden.

### <a name="c"></a>C++

Siehe [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) -Funktion.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
