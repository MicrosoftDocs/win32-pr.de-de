---
description: Ruft ein Objekt Handle für das angegebene Objekt ab, das dem angegebenen Prozess zugeordnet ist.
ms.assetid: c7b371c3-02c0-4137-ad9d-dd07a74fe2a5
title: Obfindlenker forobject-Funktion (ntosp. h)
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
ms.openlocfilehash: 7ba87d05d4264f3bb160bae16053a338e38e2145
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860788"
---
# <a name="obfindhandleforobject-function"></a>Obfindlenker forobject-Funktion

\[Diese Funktion ist veraltet und kann in zukünftigen Versionen von Windows geändert werden oder nicht verfügbar sein. Vermeiden Sie die Verwendung dieser Funktion.\]

Ruft ein Objekt Handle für das angegebene Objekt ab, das dem angegebenen Prozess zugeordnet ist.

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

*Prozess* \[ in\]
</dt> <dd>

Der Prozess. Dieses Handle wird von der **iogetcurrentprocess** -oder der **psgetcurrentprocess** -Funktion zurückgegeben.

</dd> <dt>

*Objekt* \[ in\]
</dt> <dd>

Ein Zeiger auf das-Objekt.

</dd> <dt>

*"Reserved1"* \[ in, optional\]
</dt> <dd>

Reserviert.

</dd> <dt>

*"Reserved2"* \[ in, optional\]
</dt> <dd>

Reserviert.

</dd> <dt>

*Handle* \[ vorgenommen\]
</dt> <dd>

Das Objekt handle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt **true** zurück, wenn eine Entsprechung gefunden wird, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist in Ntoskrnl.exe verfügbar und kann nur aus dem Kernel Modus aufgerufen werden. Die entsprechende Import Bibliothek ist über das Windows-Treiberkit (WDK) verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Nzu SP. h</dt> </dl>      |
| Bibliothek<br/>                  | <dl> <dt>Nzu-nl. lib</dt> </dl> |



 

 




