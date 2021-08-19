---
description: Die CloseDatabase-Methode des Merge-Objekts schließt die derzeit geöffnete Windows Installer-Datenbank.
ms.assetid: a89fe77a-0099-4c49-b484-c05ee351a66a
title: Merge.CloseDatabase-Methode (Mergemod.h)
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
ms.openlocfilehash: 3f3b250cbaebd565f14ef7f10cd8180e497f20347d00a7e96a74298d3e5dc770
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013028"
---
# <a name="mergeclosedatabase-method"></a>Merge.CloseDatabase-Methode

Die **CloseDatabase-Methode** des [**Merge-Objekts**](merge-object.md) schließt die derzeit geöffnete Windows Installer-Datenbank.

## <a name="syntax"></a>Syntax


```JScript
Merge.CloseDatabase(
  bCommit
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bCommit* 
</dt> <dd>

**TRUE,** wenn Änderungen gespeichert werden sollen, **andernfalls FALSE.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Beim Schließen einer Datenbank werden alle Abhängigkeitsinformationen gelöscht, aber es sind keine Fehler betroffen, die nicht abgerufen wurden.

### <a name="c"></a>C++

Siehe [**CloseDatabase-Funktion.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1.0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
