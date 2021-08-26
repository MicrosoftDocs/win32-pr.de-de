---
description: Schreibt Binärdaten in die angegebene Datenbank.
ms.assetid: 935321b8-904e-46be-ad11-77d89670a072
title: SdbWriteBinaryTag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 06900cf49445b52c519b04f88ffc6d5b3ba539404bf64bd7f820a502f70ec2e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044850"
---
# <a name="sdbwritebinarytag-function"></a>SdbWriteBinaryTag-Funktion

Schreibt Binärdaten in die angegebene Datenbank.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbWriteBinaryTag(
  _In_ PDB   pdb,
  _In_ TAG   tTag,
  _In_ PBYTE pBuffer,
  _In_ DWORD dwSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdb* \[ In\]
</dt> <dd>

Ein Handle für die Shim-Datenbank.

</dd> <dt>

*tTag* \[ In\]
</dt> <dd>

Das TAG für den Eintrag. Dieses TAG muss vom Typ **TAG \_ TYPE \_ BINARY** sein.

</dd> <dt>

*pBuffer* \[ In\]
</dt> <dd>

Der Puffer, der die Daten enthält. Dieser Parameter darf nicht **NULL** sein.

</dd> <dt>

*dwSize* \[ In\]
</dt> <dd>

Die Größe des *pBuffer-Puffers* in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt **TRUE** bei Erfolg oder **FALSE** bei Einem Fehler zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SdbWriteBinaryTagFromFile**](sdbwritebinarytagfromfile.md)
</dt> <dt>

[**SdbWriteDWORDTag**](sdbwritedwordtag.md)
</dt> <dt>

[**SdbWriteQWORDTag**](sdbwriteqwordtag.md)
</dt> <dt>

[**SdbWriteStringTag**](sdbwritestringtag.md)
</dt> <dt>

[**SdbWriteWORDTag**](sdbwritewordtag.md)
</dt> </dl>

 

 




