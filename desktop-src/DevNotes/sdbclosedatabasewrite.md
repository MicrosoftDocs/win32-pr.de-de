---
description: Schließt die angegebene Datenbank.
ms.assetid: 69546f03-9912-401a-9c1a-b7fdbe16dbf8
title: Sdbclosedatabasewrite-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabaseWrite
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 24df6f9ce2c4f0fae4dd1c1ef244e006ea00c047
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860984"
---
# <a name="sdbclosedatabasewrite-function"></a>Sdbclosedatabasewrite-Funktion

Schließt die angegebene Datenbank.

## <a name="syntax"></a>Syntax


```C++
void WINAPI SdbCloseDatabaseWrite(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PDB* \[ in, out\]
</dt> <dd>

Ein Handle für die Shimdatenbank.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ruft [**sdbclosedatabase**](sdbclosedatabase.md)auf. Daher sind diese beiden Funktionen Äquivalent.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbbeginschreitelisttag**](sdbbeginwritelisttag.md)
</dt> <dt>

[**Sdbclosedatabase**](sdbclosedatabase.md)
</dt> <dt>

[**Sdbendschreitelisttag**](sdbendwritelisttag.md)
</dt> </dl>

 

 




