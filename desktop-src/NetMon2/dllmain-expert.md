---
description: Der Experte implementiert die DllMain-Funktion. Das Betriebssystem ruft DllMain auf, um ein Handle für eine Instanz des Experten zu erhalten.
ms.assetid: 38593ba0-dc37-4620-bb49-2e50c3d9ea3c
title: DllMain Expert-Rückruffunktion (Process.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 3aa546d4bc75b237d7c77ed3fa7179a0c957309a31964a7e6c498e1cc998c71e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796256"
---
# <a name="dllmain-expert-callback-function"></a>DllMain Expert-Rückruffunktion

Der Experte implementiert die [**DllMain-Funktion.**](/windows/desktop/Dlls/dllmain) Das Betriebssystem ruft **DllMain auf,** um ein Handle für eine Instanz des Experten zu erhalten.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI DllMain(
  _Out_ HINSTANCE hInstance,
  _In_  ULONG     ulReason,
        LPVOID    Reserved
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hInstance* \[ out\]
</dt> <dd>

Handle für eine Instanz des Experten.

Wenn der Experte die Netzwerkmonitor verwendet, muss *der hInstance-Wert* in einer globalen Variablen gespeichert werden. Dieser Ansatz ist nur erforderlich, wenn der Wert des *ulReason-Parameters* auf DLL \_ PROCESS ATTACH festgelegt \_ ist.

</dd> <dt>

*ulReason* \[ In\]
</dt> <dd>

Gibt an, warum die Funktion aufgerufen wurde. Der Wert DLL PROCESS ATTACH (gilt, wenn die DLL zum ersten Mal geladen wird) gibt an, dass der Experte den \_ \_ *hInstance-Wert* in einer globalen Variablen speichern soll.

Mit jedem anderen Wert können alle Aufrufe der [**DllMain-Funktion**](/windows/desktop/Dlls/dllmain) ignoriert werden. Eine Liste aller möglichen Flags, die vom Betriebssystem festgelegt werden, finden Sie unter **DLLMain**.

</dd> <dt>

*Reserved* 
</dt> <dd>

Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert **TRUE.**

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **FALSE.**

## <a name="remarks"></a>Hinweise

Das Betriebssystem ruft die **DllMain** Expert-Funktion auf, wenn ein Prozess die Experten-DLL lädt oder entlädt. Die **DllMain-Expertenfunktion** muss nur exportiert werden, wenn der Experte über eine Benutzeroberfläche zum Anzeigen der Konfiguration oder der Ergebnisse verfügt und dann nur den richtigen *hInstance-Wert zurück* gibt.

Die **DllMain-Expertenfunktion** basiert auf der [**DllMain-Funktion**](/windows/desktop/Dlls/dllmain) der Dynamic Link Library.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Process.h</dt> </dl> |



 

