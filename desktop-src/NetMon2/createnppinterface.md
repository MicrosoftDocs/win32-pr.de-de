---
description: Die CreateNPPInterface-Funktion verwendet das vom Finder zurückgegebene BLOB, um ein NPP zu erstellen, das die Anwendung verwenden kann.
ms.assetid: 41f48c72-3284-4ebc-baff-63553c8971e6
title: CreateNPPInterface-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateNPPInterface
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 03c2bb7fae0f68e6d38016df353266cfc9ec11757eeb98f6a5e41ab4316e63c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744540"
---
# <a name="createnppinterface-function"></a>CreateNPPInterface-Funktion

Die **CreateNPPInterface-Funktion** verwendet das vom Finder zurückgegebene BLOB, um ein NPP zu erstellen, das die Anwendung verwenden kann.

## <a name="syntax"></a>Syntax


```C++
DWORD CreateNPPInterface(
  _In_  HBLOB  hBlob,
  _In_  REFIID iid,
  _Out_ void   **ppvObject
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hBlob* \[ In\]
</dt> <dd>

Handle für das BLOB, das vom Finder zurückgegeben wird.

</dd> <dt>

*iid* \[ in\]
</dt> <dd>

Bezeichner der Schnittstelle, die Sie vom NPP aufrufen (**z.** B. IRTC oder **IDelaydC).**

</dd> <dt>

*ppvObject* \[ out\]
</dt> <dd>

Zeiger auf den zurückgegebenen Zeiger auf die angeforderte Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein NMERR-Wert, der den Fehler beschreibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




