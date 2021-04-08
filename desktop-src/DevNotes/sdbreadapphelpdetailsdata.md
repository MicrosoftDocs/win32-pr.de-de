---
Description: Ruft Daten aus der AppHelp-Detail Datenbank ab.
ms.assetid: f3731561-bf3f-4139-9890-bd4ce73d83fa
title: Sdbreadapphelpdetailsdata-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadApphelpDetailsData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a0a352e3fe33115133b827b5ad03d99a14101b34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949812"
---
# <a name="sdbreadapphelpdetailsdata-function"></a>Sdbreadapphelpdetailsdata-Funktion

Ruft Daten aus der AppHelp-Detail Datenbank ab.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbReadApphelpDetailsData(
  _In_  PDB           pdb,
  _Out_ PAPPHELP_DATA pData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PDB* \[ in\]
</dt> <dd>

Ein Handle für die AppHelp-Detail Datenbank, "AppHelp. sdb".

</dd> <dt>

*pData* \[ vorgenommen\]
</dt> <dd>

Eine [**AppHelp- \_ Daten**](apphelp-data.md) Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei einem Fehler gibt die Funktion **true** oder **false** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




