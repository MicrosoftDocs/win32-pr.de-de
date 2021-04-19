---
description: Ruft die Binärdaten für die angegebene TagID ab.
ms.assetid: 18992406-67b4-4c48-9629-04d6bf1c5824
title: Sdbgetbinarytagdata-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetBinaryTagData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 028b073b149482b79b848216e44b8a425d6ffb56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342587"
---
# <a name="sdbgetbinarytagdata-function"></a>Sdbgetbinarytagdata-Funktion

Ruft die Binärdaten für die angegebene **TagID** ab.

## <a name="syntax"></a>Syntax


```C++
PVOID WINAPI SdbGetBinaryTagData(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PDB* \[ in\]
</dt> <dd>

Ein Handle für die Shimdatenbank.

</dd> <dt>

*tiwhat* \[ in\]
</dt> <dd>

Die **TagID** , die den abzurufenden Daten entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt einen Zeiger auf die Binärdaten oder **null** zurück, wenn die **TagID** ungültig ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbgetstringtagptr**](sdbgetstringtagptr.md)
</dt> <dt>

[**Sdbreaddwordtag**](sdbreaddwordtag.md)
</dt> <dt>

[**Sdbreadqwordtag**](sdbreadqwordtag.md)
</dt> <dt>

[**Sdbreadstringtag**](sdbreadstringtag.md)
</dt> </dl>

 

 




