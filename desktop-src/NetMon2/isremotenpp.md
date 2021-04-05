---
description: Die isremotenpp-Funktion gibt an, ob das angegebene BLOB eine Remote-NPP angibt.
ms.assetid: 66ee0a9a-3199-479f-baec-da6ae6b46c65
title: Isremotenpp-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsRemoteNPP
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: c52346f368c0720601423f258e4dc73c27296311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755392"
---
# <a name="isremotenpp-function"></a>Isremotenpp-Funktion

Die **isremotenpp** -Funktion gibt an, ob das angegebene BLOB eine Remote-NPP angibt.

## <a name="syntax"></a>Syntax


```C++
BOOL IsRemoteNPP(
  _In_ HBLOB hBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hblob* \[ in\]
</dt> <dd>

Handle für ein BLOB.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert " **true**".

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Funktion, um zu testen, ob eine Remote Kategorie vorhanden ist.

Stellen Sie sicher, dass sich die Namen der Remote Computer und der lokalen Computer unterscheiden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




