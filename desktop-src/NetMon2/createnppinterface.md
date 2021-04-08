---
description: Die Funktion "-Funktion" verwendet das BLOB, das vom Finder zurückgegeben wurde, um eine NPP zu erstellen, die von der Anwendung verwendet werden kann.
ms.assetid: 41f48c72-3284-4ebc-baff-63553c8971e6
title: Kreatenppinterface-Funktion (Netmon. h)
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
ms.openlocfilehash: d0efa1c33dd5e0778f13ddd59290de324c92e813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960027"
---
# <a name="createnppinterface-function"></a>Kreatenppinterface-Funktion

Die **Funktion "** -Funktion" verwendet das BLOB, das vom Finder zurückgegeben wurde, um eine NPP zu erstellen, die von der Anwendung verwendet werden kann.

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

*hblob* \[ in\]
</dt> <dd>

Handle für das BLOB, das vom Finder zurückgegeben wurde.

</dd> <dt>

*IID* \[ in\]
</dt> <dd>

Der Bezeichner der Schnittstelle, die Sie von der NPP (z. b. "**iritc** " oder " **idelta aydc**") abrufen.

</dd> <dt>

*ppvobject* \[ vorgenommen\]
</dt> <dd>

Zeiger auf den zurückgegebenen Zeiger auf die angeforderte Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler beschreibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothek<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




