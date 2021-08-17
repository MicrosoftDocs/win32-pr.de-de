---
description: Ruft die GetLastError-Funktion auf und konvertiert den Rückgabecode in ein HRESULT.
ms.assetid: 7b8eab85-212b-44bc-9d1b-60587652380d
title: SignError-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignError
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: f48f96ed867e6db41240a300d30e1f3a585e8b03a129d138c11a14ebf44ad42c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898434"
---
# <a name="signerror-function"></a>SignError-Funktion

> [!IMPORTANT]
> Diese API ist veraltet. Microsoft kann diese API in zukünftigen Versionen entfernen.

 

Die **SignError-Funktion** ruft die [**GetLastError-Funktion**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf und konvertiert den Rückgabecode in **ein HRESULT.**

> [!Note]  
> Dieser Funktion ist keine Headerdatei oder Importbibliothek zugeordnet. Zum Aufrufen dieser Funktion müssen Sie eine benutzerdefinierte Headerdatei erstellen und die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um eine dynamische Verknüpfung mit Mssign32.dll.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI SignError(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird **S \_ OK zurückgegeben.**

Wenn bei der Methode ein Fehler auftritt, wird ein **HRESULT-Wert** zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 
