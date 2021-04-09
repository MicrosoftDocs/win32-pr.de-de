---
description: Ruft die Zeichen folgen Daten für die angegebene TagID ab.
ms.assetid: c558e0bb-7e35-4298-93fb-400db00a2972
title: Sdbgetstringtagptr-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetStringTagPtr
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 56c80c4000df95fe13486d95bb872bfc39274389
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958363"
---
# <a name="sdbgetstringtagptr-function"></a>Sdbgetstringtagptr-Funktion

Ruft die Zeichen folgen Daten für die angegebene **TagID** ab.

## <a name="syntax"></a>Syntax


```C++
LPTSTR WINAPI SdbGetStringTagPtr(
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

Die **TagID** , die den abzurufenden Zeichen folgen Daten entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt einen Zeiger auf die Zeichen folgen Daten oder **null** zurück, wenn die **TagID** ungültig ist oder nicht vom Typ " **Tag \_ Type \_ String** " oder vom **\_ Tagtyp " \_ uningref**" ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbgetbinarytagdata**](sdbgetbinarytagdata.md)
</dt> <dt>

[**Sdbreaddwordtag**](sdbreaddwordtag.md)
</dt> <dt>

[**Sdbreadqwordtag**](sdbreadqwordtag.md)
</dt> <dt>

[**Sdbreadstringtag**](sdbreadstringtag.md)
</dt> </dl>

 

 




