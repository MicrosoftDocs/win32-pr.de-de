---
description: Die ShowJavaConsole-Funktion ist eine Debughilfe für Java-Entwickler. Applets (oder anderer Java-Code), die in Internet Explorer ausgeführt werden, können damit Fehlermeldungen und andere Informationen anzeigen.
ms.assetid: 070dd833-f8cc-403e-afbf-325648760d5f
title: ShowJavaConsole-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- extern
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 0a8517d32057b6434d3822cc02977f6afd72c1b387b78e85e53810bd27f00550
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075854"
---
# <a name="showjavaconsole-function"></a>ShowJavaConsole-Funktion

Die **ShowJavaConsole-Funktion** ist eine Debughilfe für Java-Entwickler. Applets (oder anderer Java-Code), die in Internet Explorer ausgeführt werden, können damit Fehlermeldungen und andere Informationen anzeigen.

## <a name="syntax"></a>Syntax


```C++
void extern ShowJavaConsole(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

<dl></dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Aufruf von **ShowJavaConsole** bewirkt, dass der virtuelle Java-Computer (VM) das Java-Konsolenfenster anzeigt. Im Java-Konsolenfenster selbst kann die Debugausgabe von Java-Code angezeigt werden, der im aufrufenden Prozess ausgeführt wird. In der Regel wird dies nur von einer Anwendung verwendet, die die Java-VM hostet. Es gibt nur ein einzelnes Java-Konsolenfenster pro Prozess. Mehrere Aufrufe der API führen dazu, dass das gleiche Fenster angezeigt wird. Anders ausgedrückt: Wenn das Konsolenfenster bereits angezeigt wird, geschieht nichts. Wenn das Fenster nicht angezeigt wurde oder der Benutzer es geschlossen hat, wird das Fenster angezeigt.

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjava.dll</dt> </dl> |



 

 
