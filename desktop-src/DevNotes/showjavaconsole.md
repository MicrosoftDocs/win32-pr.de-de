---
description: Die showjavaconsole-Funktion ist eine Debughilfe für Java-Entwickler. Applets (oder anderer Java-Code), die in Internet Explorer ausgeführt werden, können diese zum Anzeigen von Fehlermeldungen und anderen Informationen verwenden.
ms.assetid: 070dd833-f8cc-403e-afbf-325648760d5f
title: Showjavaconsole-Funktion
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
ms.openlocfilehash: 522885bfdd07843549375977630d8d1a7c6776f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361921"
---
# <a name="showjavaconsole-function"></a>Showjavaconsole-Funktion

Die **showjavaconsole** -Funktion ist eine Debughilfe für Java-Entwickler. Applets (oder anderer Java-Code), die in Internet Explorer ausgeführt werden, können diese zum Anzeigen von Fehlermeldungen und anderen Informationen verwenden.

## <a name="syntax"></a>Syntax


```C++
void extern ShowJavaConsole(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

<dl></dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn Sie **showjavaconsole** aufrufen, zeigt der Java Virtual Machine (VM) das Java-Konsolenfenster an. Das Java-Konsolenfenster selbst kann Debugausgaben aus Java-Code anzeigen, der im aufrufenden Prozess ausgeführt wird. Dies wird in der Regel nur von einer Anwendung verwendet, die die Java-VM gehostet. Es gibt nur ein einzelnes Java-Konsolenfenster pro Prozess. mehrere Aufrufe der API führen zu einem Fenster, das angezeigt wird. Anders ausgedrückt: Wenn das Konsolenfenster bereits angezeigt wird, geschieht nichts. Wenn das Fenster nicht angezeigt wird oder der Benutzer es geschlossen hat, wird das Fenster angezeigt.

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjava.dll</dt> </dl> |



 

 
