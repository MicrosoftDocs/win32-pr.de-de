---
description: Erstellt einen Moniker, der eine Hardwarekomponente und den zugehörigen Ereignishandler darstellt. Die automatische Wiedergabe verwendet diese Funktion, damit Anwendungen AutoPlay-Ereignisse verwenden können.
title: Funktion "kreatehardwareeventmoniker"
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
ms.openlocfilehash: 59100ab20cd997cc4ab35602698268ec6d76dea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977336"
---
# <a name="createhardwareeventmoniker-function"></a>Funktion "kreatehardwareeventmoniker"

\[Diese Funktion ist über Windows XP mit Service Pack 2 (SP2) und Windows Server 2003 verfügbar. Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar.\]

Erstellt einen Moniker, der eine Hardwarekomponente und den zugehörigen Ereignishandler darstellt. Die automatische Wiedergabe verwendet diese Funktion, damit Anwendungen AutoPlay-Ereignisse verwenden können.

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

*CLSID* \[ in\]
</dt> <dd>

Typ: **ref-sid**

Die ID der Klasse, an die der Moniker gebunden ist.

</dd> <dt>

*pszeventhandler* \[ in\]
</dt> <dd>

Typ: **LPCTSTR**

Der Name des Ereignis Handlers.

</dd> <dt>

*ppmoniker* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***

Die Adresse einer Zeiger Variablen, die den [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) -Schnittstellen Zeiger empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie beim Registrieren ausgelaufeigener Anwendungen den Wert von " **kreatehardwareeventmoniker** ", damit diese Anwendungen auf AutoPlay-Ereignisse zugreifen können. Zum Verwenden von AutoPlay-Ereignissen in laufenden Anwendungen müssen Sie zuerst eine neue Komponente erstellen, die die [**ihweventhandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) -Schnittstelle implementiert. Initialisieren Sie diese Schnittstelle mit dem initcmdline-Wert aus dem Eintrag eines bestimmten **Handlers** unter dem Handler-Schlüssel, da AutoPlay nicht die [**Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) -Methode aufruft.

Sie sollten " **whatehardwareeventmoniker** " aufrufen, um einen Moniker zu erhalten, der die Komponente und ihren Ereignishandler darstellt. Verwenden Sie dann den im *ppmoniker* -Parameter zurückgegebenen Wert, um die Komponente in der laufenden Objekttabelle (rot) zu registrieren, wie im Beispiel gezeigt.

Beachten Sie, dass " **kreatehardwareeventmoniker** " nicht in einer Header Datei definiert ist. Um es in Ihrem Code zu verwenden, müssen Sie durch einen [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)-Aufrufvorgang ein Handle für die Shsvcs.dll Datei abrufen. Anschließend verwenden Sie dieses Handle in einem Aufruf von [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) , um eine Instanz der Funktion " **featehardwareeventmoniker** " zu erhalten.

Für den Aufrufen von " [**iriunningobjec\:: Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) " müssen Sie die folgenden **AppID** -Informationen in die Registrierung eingeben.

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

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>None</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Shsvcs.dll</dt> </dl> |



 

 
