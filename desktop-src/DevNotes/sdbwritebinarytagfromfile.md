---
description: Schreibt Binärdaten aus der angegebenen Datei in die angegebene Datenbank.
ms.assetid: 960633a8-5cec-462b-b7dc-72eb3e4fd0a2
title: Sdbschreitebinarytagfromfile-Funktion
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
ms.openlocfilehash: 75b45a935fd9630afcefe8f7d30338a6ad6b10a3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958280"
---
# <a name="sdbwritebinarytagfromfile-function"></a>Sdbschreitebinarytagfromfile-Funktion

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

*PDB* \[ in\]
</dt> <dd>

Ein Handle für die Shimdatenbank.

</dd> <dt>

*ttag* \[ in\]
</dt> <dd>

Das-Tag für den Eintrag. Dieses Tag muss vom Typ " **Tag \_ Type \_ Binary**" sein.

</dd> <dt>

*pwszpath* \[ in\]
</dt> <dd>

Der Pfad zu der Datei, die die Daten enthält. Dieser Parameter darf nicht **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei einem Fehler gibt die Funktion **true** oder **false** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbschreitebinarytag**](sdbwritebinarytag.md)
</dt> </dl>

 

 




