---
description: Die dllgetmonitorobject-Funktion muss vom Monitor implementiert werden. Die mcsvc ruft diese Funktion auf, um eine Instanz des Monitors zu erstellen.
ms.assetid: 2c39f752-264c-4ab9-8710-a0d660c4772f
title: Dllgetmonitorobject-Rückruffunktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetMonitorObject
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 723c085fe86e8c24ebc13d83c760e5bfdd08eab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868223"
---
# <a name="dllgetmonitorobject-callback-function"></a>Dllgetmonitorobject-Rückruffunktion

Die **dllgetmonitorobject** -Funktion muss vom Monitor implementiert werden. Die mcsvc ruft diese Funktion auf, um eine Instanz des Monitors zu erstellen.

## <a name="syntax"></a>Syntax


```C++
HRESULT DllGetMonitorObject(
  _In_  REFIID riid,
  _Out_ LPVOID *ppObj
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*riid* \[ in\]
</dt> <dd>

UUID der unten gezeigten Monitore, wie in der Header Datei "imonitor. h" definiert. Wenn eine ungültige UUID bereitgestellt wird, schlägt die Funktion fehl, und der Monitor muss E \_ nointerface zurückgeben.

``` syntax
IID_IMonitor
```

</dd> <dt>

*ppobj* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen Zeiger, der die in *riid* angeforderte Schnittstelle empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert S \_ OK (entspricht noError).

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Fehlercode. Wenn ein Fehlercode zurückgegeben wird, erstellt das mcsvc das Monitor Objekt nicht, und die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode wird nicht für den Schnittstellen Zeiger aufgerufen.

## <a name="remarks"></a>Bemerkungen

Die **dllgetmonitorobject** -Funktion wird jedes Mal aufgerufen, wenn der mcsvc versucht, eine Instanz des Monitors zu erstellen. Diese Funktion weist absichtlich eine starke Ähnlichkeit mit der gängigeren [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) -Funktion auf. Der Hauptunterschied besteht darin, dass eine CLSID nicht an **dllgetmonitorobject** übermittelt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

