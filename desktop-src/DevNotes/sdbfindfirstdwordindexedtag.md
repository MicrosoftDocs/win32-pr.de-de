---
description: Sucht den ersten DWORD-Datensatz im angegebenen Index, der die angegebenen Kriterien erfüllt.
ms.assetid: 81302f84-497d-4fef-b348-eee2a53284c7
title: Sdbfindfirstdwordindexedtag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstDWORDIndexedTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4f3c9290f98fb24d856561114bc654da0315c5a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522816"
---
# <a name="sdbfindfirstdwordindexedtag-function"></a>Sdbfindfirstdwordindexedtag-Funktion

Sucht den ersten **DWORD** -Datensatz im angegebenen Index, der die angegebenen Kriterien erfüllt.

## <a name="syntax"></a>Syntax


```C++
TAGID WINAPI SdbFindFirstDWORDIndexedTag(
  _In_  PDB       pdb,
  _In_  TAG       tWhich,
  _In_  TAG       tKey,
  _In_  DWORD     dwName,
  _Out_ FIND_INFO *pFindInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PDB* \[ in\]
</dt> <dd>

Ein Handle für die Shimdatenbank.

</dd> <dt>

*TDas* \[ in\]
</dt> <dd>

Der Indextyp. Eine Liste der Werte finden Sie unter [**Tag**](tag.md) .

</dd> <dt>

*TKey* \[ in\]
</dt> <dd>

Der Schlüsseltyp.

</dd> <dt>

*dwname* \[ in\]
</dt> <dd>

Der Name der Daten, die gesucht werden sollen. Dieser Wert wird in einen Schlüssel konvertiert.

</dd> <dt>

*pfindinfo* \[ vorgenommen\]
</dt> <dd>

Eine [**Find \_ Info**](find-info.md) -Struktur, die den Datensatz empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die **TagID** der ersten Entsprechung oder des **Tags \_ null** , wenn keine Entsprechung gefunden wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbfindfirsttag**](sdbfindfirsttag.md)
</dt> </dl>

 

 




