---
description: Ruft ein Objekthandle für das angegebene Objekt ab, das dem angegebenen Prozess zugeordnet ist.
ms.assetid: c7b371c3-02c0-4137-ad9d-dd07a74fe2a5
title: ObFindHandleForObject-Funktion (Ntosp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObFindHandleForObject
api_type:
- LibDef
api_location:
- Ntoskrnl.lib
- Ntoskrnl.dll
ms.openlocfilehash: 481def34e3e8656205eefe96058fe3c7558d2c898c7e05ddc78f9a67435c507e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984150"
---
# <a name="obfindhandleforobject-function"></a>ObFindHandleForObject-Funktion

\[Diese Funktion ist veraltet und kann in zukünftigen Versionen von Windows geändert oder nicht verfügbar sein. Vermeiden Sie die Verwendung dieser Funktion.\]

Ruft ein Objekthandle für das angegebene Objekt ab, das dem angegebenen Prozess zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
BOOLEAN WINAPI ObFindHandleForObject(
  _In_     PEPROCESS Process,
  _In_     PVOID     Object,
  _In_opt_ PVOID     Reserved1,
  _In_opt_ PVOID     Reserved2,
  _Out_    PHANDLE   Handle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Prozess* \[ In\]
</dt> <dd>

Der Prozess. Dieses Handle wird von der **IoGetCurrentProcess-** oder **PsGetCurrentProcess-Funktion** zurückgegeben.

</dd> <dt>

*Objekt* \[ In\]
</dt> <dd>

Ein Zeiger auf das -Objekt.

</dd> <dt>

*Reserviert1* \[ in, optional\]
</dt> <dd>

Reserviert.

</dd> <dt>

*Reserviert2* \[ in, optional\]
</dt> <dd>

Reserviert.

</dd> <dt>

*Handle* \[ out\]
</dt> <dd>

Das Objekthandle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt **TRUE** zurück, wenn eine Übereinstimmung gefunden wird, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Diese Funktion ist in Ntoskrnl.exe verfügbar und kann nur im Kernelmodus aufgerufen werden. Die entsprechende Importbibliothek ist über das Windows Driver Kit (WDK) verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Ntosp.h</dt> </dl>      |
| Bibliothek<br/>                  | <dl> <dt>Ntoskrnl.lib</dt> </dl> |



 

 




