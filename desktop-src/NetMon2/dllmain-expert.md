---
description: Der Experte implementiert die DllMain-Funktion. Das Betriebssystem ruft DllMain auf, um ein Handle für eine Instanz des Experten abzurufen.
ms.assetid: 38593ba0-dc37-4620-bb49-2e50c3d9ea3c
title: DllMain-Funktion für expertenrückruf (Process. h)
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
ms.openlocfilehash: 914f50b75e83fdc67448770b32ac8d0f8e8ab656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866271"
---
# <a name="dllmain-expert-callback-function"></a>DllMain-Funktion für expertenrückruf

Der Experte implementiert die [**DllMain**](/windows/desktop/Dlls/dllmain) -Funktion. Das Betriebssystem ruft **DllMain** auf, um ein Handle für eine Instanz des Experten abzurufen.

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

*HINSTANCE* \[ vorgenommen\]
</dt> <dd>

Handle für eine Instanz des Experten.

Wenn der Experte den Netzwerkmonitor Benutzeroberfläche verwendet, muss der *HINSTANCE* -Wert in einer globalen Variablen gespeichert werden. Diese Vorgehensweise ist nur erforderlich, wenn der Wert des *ulReason* -Parameters auf DLL- \_ Prozess anfügen festgelegt ist \_ .

</dd> <dt>

*ulReason* \[ in\]
</dt> <dd>

Indikator für den Grund, warum die Funktion aufgerufen wurde. Ein Wert von DLL- \_ Prozess \_ Anfügen (gilt beim ersten Laden der dll) gibt an, dass der Experte den *HINSTANCE* -Wert in einer globalen Variablen speichern soll.

Mit jedem anderen Wert können alle Aufrufe der [**DllMain**](/windows/desktop/Dlls/dllmain) -Funktion ignoriert werden. Eine Liste aller möglichen Flags, die vom Betriebssystem festgelegt werden, finden Sie unter **DllMain**.

</dd> <dt>

*Reserved* 
</dt> <dd>

Der Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert " **true**".

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.

## <a name="remarks"></a>Bemerkungen

Das Betriebssystem Ruft die Funktion **DllMain** -Experte auf, wenn ein Prozess die Experten-dll lädt oder entlädt. Die Funktion **DllMain** -Experte muss nur exportiert werden, wenn der Experte über eine Benutzeroberfläche verfügt, um entweder die Konfiguration oder die Ergebnisse anzuzeigen, und dann nur den richtigen *HINSTANCE* -Wert zurückgibt.

Die Funktion **DllMain** -Experte basiert auf der [**DllMain**](/windows/desktop/Dlls/dllmain) -Funktion der Dynamic Link Library.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Process. h</dt> </dl> |



 

