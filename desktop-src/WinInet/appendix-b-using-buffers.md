---
title: Verwenden der Zeichen folgen Puffer
description: Funktionen, die Zeichen folgen zurückgeben, enthalten den Eingabeparameter lpszbuffer und den Größen Parameter lpdwbufferlength. Obwohl lpszbuffer NULL sein kann, muss lpdwbufferlength ein gültiger Zeiger auf eine DWORD-Variable sein.
ms.assetid: ae7f84ba-15d4-483b-bdda-0042854f9e1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 309d887458521b99069b381f8bf6650ebeda488a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728761"
---
# <a name="using-string-buffers"></a>Verwenden der Zeichen folgen Puffer

Funktionen, die Zeichen folgen zurückgeben, enthalten den Eingabeparameter *lpszbuffer* und den Größen Parameter *lpdwbufferlength*. Obwohl *lpszbuffer* **null** sein kann, muss *lpdwbufferlength* ein gültiger Zeiger auf eine **DWORD** -Variable sein. Wenn der Eingabepuffer, auf den von *lpszbuffer* verwiesen wird, **null** oder zu klein ist, um die Ausgabe Zeichenfolge zu speichern, schlägt die Funktion fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt **fehlerhaften \_ \_ Puffer** zurück. Die Variable, auf die von *lpdwbufferlength* verwiesen wird, enthält eine Zahl, die die Anzahl der Bytes darstellt, die die Funktion zum Zurückgeben der angeforderten Zeichenfolge benötigt, einschließlich des **null** -Terminator. Die Anwendung muss einen Puffer dieser Größe zuordnen, die Variable, auf die von *lpdwbufferlength* verwiesen wird, auf diesen Wert festlegen und die Anforderung erneut senden. Wenn die Puffergröße ausreichend ist, um die angeforderte Zeichenfolge zu empfangen, wird die Zeichenfolge mit einem **null** -Terminator in den Ausgabepuffer kopiert, und die Funktion gibt eine Erfolgs Angabe zurück. Die Variable, auf die von *lpdwbufferlength* verwiesen wird, enthält jetzt die Anzahl der im Puffer gespeicherten Zeichen, ausgenommen das **null** -Terminator.

> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 