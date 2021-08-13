---
description: Öffnet ein angegebenes Volume und initialisiert das Kontingentsteuerobjekt.
ms.assetid: 20eae2a3-f602-48a2-bf1c-65570e7a5d21
title: DiskQuotaControl.Initialize-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.Initialize
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0df879c626ccdac7494077f021c23a6e42b24f0df3aa780d1be8b1af8225527a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455900"
---
# <a name="diskquotacontrolinitialize-method"></a>DiskQuotaControl.Initialize-Methode

Öffnet ein angegebenes Volume und initialisiert das Kontingentsteuerobjekt.

## <a name="syntax"></a>Syntax


```JScript
DiskQuotaControl.Initialize(
  sPath,
  bReadWrite
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Spath* 
</dt> <dd>

Typ: **Zeichenfolge**

Ein Zeichenfolgenwert, der den vollqualifizierten Pfad des zu initialisierenden Volumes enthält.

</dd> <dt>

*bReadWrite* 
</dt> <dd>

Typ: **Boolesch**

Ein boolescher Wert, der angibt, wie das Volume geöffnet werden soll. Legen *Sie bReadWrite* für Lese-/Schreibzugriff auf **TRUE** oder **FALSE** für schreibgeschützten Zugriff fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DiskQuotaControl-Objekt**](diskquotacontrol-object.md)
</dt> </dl>

 

 




