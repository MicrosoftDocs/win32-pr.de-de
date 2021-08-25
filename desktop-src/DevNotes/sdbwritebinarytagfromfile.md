---
description: Schreibt Binärdaten aus der angegebenen Datei in die angegebene Datenbank.
ms.assetid: 960633a8-5cec-462b-b7dc-72eb3e4fd0a2
title: SdbWriteBinaryTagFromFile-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTagFromFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: ec2acf733a870d3dcff57ceb7cdea996c6b6dc1e5d950ec85944285e6ba6cc35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815140"
---
# <a name="sdbwritebinarytagfromfile-function"></a>SdbWriteBinaryTagFromFile-Funktion

Schreibt Binärdaten aus der angegebenen Datei in die angegebene Datenbank.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbWriteBinaryTagFromFile(
  _In_ PDB     pdb,
  _In_ TAG     tTag,
  _In_ LPCWSTR pwszPath
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

Das TAG für den Eintrag. Dieses TAG muss vom Typ **TAG \_ TYPE BINARY \_ sein.**

</dd> <dt>

*pwszPath* \[ In\]
</dt> <dd>

Der Pfad zu der Datei, die die Daten enthält. Dieser Parameter darf nicht **NULL sein.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt **TRUE bei** Erfolg oder **FALSE bei** Einem Fehler zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SdbWriteBinaryTag**](sdbwritebinarytag.md)
</dt> </dl>

 

 




