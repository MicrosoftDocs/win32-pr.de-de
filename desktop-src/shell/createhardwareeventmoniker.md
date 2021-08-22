---
description: Erstellt einen Moniker, der eine Hardwarekomponente und den zugehörigen Ereignishandler darstellt. Die automatische Wiedergabe verwendet diese Funktion, um Anwendungen die Verwendung von AutoPlay-Ereignissen zu ermöglichen.
title: CreateHardwareEventMoniker-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHardwareEventMoniker
api_type:
- DllExport
api_location:
- Shsvcs.dll
ms.assetid: ff0ad023-42ea-4c74-adae-af55527b6ac3
ms.openlocfilehash: 42f2da51bac93733a74113d3a567802975aca18be2a34f6fa349ff65349749c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460554"
---
# <a name="createhardwareeventmoniker-function"></a>CreateHardwareEventMoniker-Funktion

\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar. Er kann in nachfolgenden Versionen von Windows geändert oder nicht verfügbar sein.\]

Erstellt einen Moniker, der eine Hardwarekomponente und den zugehörigen Ereignishandler darstellt. Die automatische Wiedergabe verwendet diese Funktion, um Anwendungen die Verwendung von AutoPlay-Ereignissen zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateHardwareEventMoniker(
  _In_  REFCLSID clsid,
  _In_  LPCTSTR  pszEventHandler,
  _Out_ IMoniker **ppmoniker
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*clsid* \[ In\]
</dt> <dd>

Typ: **REFCLSID**

Die ID der Klasse, an die der Moniker gebunden wird.

</dd> <dt>

*pszEventHandler* \[ In\]
</dt> <dd>

Typ: **LPCTSTR**

Der Name des Ereignishandlers.

</dd> <dt>

*ppmoniker* \[ out\]
</dt> <dd>

Typ: **[ **IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***

Die Adresse einer Zeigervariablen, die den [**IMoniker-Schnittstellenzeiger**](/windows/win32/api/objidl/nn-objidl-imoniker) empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Verwenden Sie **CreateHardwareEventMoniker,** wenn Sie ausgeführte Anwendungen registrieren, damit diese Anwendungen Zugriff auf AutoPlay-Ereignisse haben. Um AutoPlay-Ereignisse in ausgeführten Anwendungen zu verwenden, müssen Sie zunächst eine neue Komponente erstellen, die die [**IHWEventHandler-Schnittstelle**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) implementiert. Initialisieren Sie diese Schnittstelle mit dem InitCmdLine-Wert aus dem Eintrag des **jeweiligen** Handlers unter dem Handlerschlüssel, da autoPlay die [**Initialize-Methode**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) nicht aufruft.

Sie sollten **CreateHardwareEventMoniker** aufrufen, um einen Moniker abzurufen, der Ihre Komponente und ihren Ereignishandler darstellt. Verwenden Sie dann den wert, der im *ppmoniker-Parameter* zurückgegeben wird, um Ihre Komponente in der laufenden Objekttabelle (ROT) zu registrieren, wie im Beispiel gezeigt.

Beachten Sie, dass **CreateHardwareEventMoniker** nicht in einer Headerdatei definiert ist. Um sie in Ihrem Code zu verwenden, müssen Sie ein Handle für die Shsvcs.dll-Datei über einen Aufruf von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)abrufen. Anschließend verwenden Sie dieses Handle in einem Aufruf von [**GetProcAddress,**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) um eine Instanz der **CreateHardwareEventMoniker-Funktion** abzurufen.

Für den Aufruf von [**IRunningObjectTable::Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) müssen Sie die folgenden **AppID-Informationen** in die Registrierung eingeben.

```
HKEY_CLASSES_ROOT
   AppID
      MyApp.exe
         (Default) = MyApplication
         AppID [REG_SZ] = {Your GUID here}
```

```
HKEY_CLASSES_ROOT
   AppID
      {The same GUID here}
         (Default) = MyApplication
         RunAs = Interactive User
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Keine</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Shsvcs.dll</dt> </dl> |



 

 
