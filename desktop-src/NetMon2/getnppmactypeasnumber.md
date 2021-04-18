---
description: Ruft den Mac-Typ aus der Kategorie networkinfo des NPP-Abschnitts des BLOBs ab und konvertiert die Typdaten in eine Mac-Typnummer.
ms.assetid: 53aa538c-69ee-4b34-93fb-9e61c6baadea
title: Getnppmactybäuernumber-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPMacTypeAsNumber
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9174b1deeb04d8d9665509daeff56d832d447892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525133"
---
# <a name="getnppmactypeasnumber-function"></a>Getnppmactybäuernumber-Funktion

Die **getnppmactybäuernumber** -Funktion Ruft den Mac-Typ aus der Kategorie networkinfo des NPP-Abschnitts des BLOBs ab und konvertiert die Typdaten in eine Mac-Typnummer.

## <a name="syntax"></a>Syntax


```C++
DWORD GetNPPMacTypeAsNumber(
  _In_  HBLOB   hBlob,
  _Out_ LPDWORD lpMacType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hblob* \[ in\]
</dt> <dd>

Ein Handle für das angegebene BLOB.

</dd> <dt>

*lpmactype* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf den Mac-Typ.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn das Tag nicht verfügbar ist, lautet der Rückgabewert "Mac- \_ Typ \_ unbekannt".

## <a name="remarks"></a>Bemerkungen

Diese Funktion ordnet das Tag **NPP: networkinfo: MacType** dem Mac- **\_ Typ \_ \*** zu, wie in der Datei npptypes. h definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




