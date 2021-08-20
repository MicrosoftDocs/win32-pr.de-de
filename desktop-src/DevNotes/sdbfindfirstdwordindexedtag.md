---
description: Sucht den ersten DWORD-Datensatz im angegebenen Index, der die angegebenen Kriterien erfüllt.
ms.assetid: 81302f84-497d-4fef-b348-eee2a53284c7
title: SdbFindFirstDWORDIndexedTag-Funktion
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
ms.openlocfilehash: 40f54dfc109ec2f7f4807d57052b9c4e1f99d5b629e8028be2931d9b42081f43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161571"
---
# <a name="sdbfindfirstdwordindexedtag-function"></a>SdbFindFirstDWORDIndexedTag-Funktion

Sucht den ersten **DWORD-Datensatz** im angegebenen Index, der die angegebenen Kriterien erfüllt.

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

*pdb* \[ In\]
</dt> <dd>

Ein Handle für die Shim-Datenbank.

</dd> <dt>

*tWhich* \[ In\]
</dt> <dd>

Der Indextyp. Eine Liste der Werte finden Sie unter [**TAG.**](tag.md)

</dd> <dt>

*tKey* \[ In\]
</dt> <dd>

Der Schlüsseltyp.

</dd> <dt>

*dwName* \[ In\]
</dt> <dd>

Der Name der zu findenden Daten. Dieser Wert wird in einen Schlüssel konvertiert.

</dd> <dt>

*pFindInfo* \[ out\]
</dt> <dd>

Eine [**FIND \_ INFO-Struktur,**](find-info.md) die den Datensatz empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die **TAGID** der ersten Übereinstimmung oder **TAG \_ NULL,** wenn keine Übereinstimmung gefunden wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> </dl>

 

 




