---
title: Verwenden von Zeichenfolgenpuffern
description: Funktionen, die Zeichenfolgen zurückgeben, enthalten den Eingabeparameter lpszBuffer und den Größenparameter lpdwBufferLength. Obwohl lpszBuffer NULL sein kann, muss lpdwBufferLength ein gültiger Zeiger auf eine DWORD-Variable sein.
ms.assetid: ae7f84ba-15d4-483b-bdda-0042854f9e1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15750da215267a4922bb0cd8c5dd8c08f77e1874af75fb9a671f9ef4cb1f0960
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413152"
---
# <a name="using-string-buffers"></a>Verwenden von Zeichenfolgenpuffern

Funktionen, die Zeichenfolgen zurückgeben, enthalten den Eingabeparameter *lpszBuffer* und den Größenparameter *lpdwBufferLength.* Obwohl *lpszBuffer* **NULL** sein kann, muss *lpdwBufferLength* ein gültiger Zeiger auf eine **DWORD-Variable** sein. Wenn der Eingabepuffer, auf den *lpszBuffer* zeigt, **NULL** oder zu klein ist, um die Ausgabezeichenfolge aufzunehmen, schlägt die Funktion fehl, und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt **ERROR INSUFFICIENT \_ \_ BUFFER** zurück. Die Variable, auf die *lpdwBufferLength* zeigt, enthält eine Zahl, die die Anzahl der Bytes darstellt, die die Funktion zum Zurückgeben der angeforderten Zeichenfolge benötigt, einschließlich des **NULL-Abschlusszeichens.** Die Anwendung sollte einen Puffer dieser Größe zuordnen, die Variable, auf die von *lpdwBufferLength* verwiesen wird, auf diesen Wert festlegen und die Anforderung erneut übermitteln. Wenn die Puffergröße ausreicht, um die angeforderte Zeichenfolge zu empfangen, wird die Zeichenfolge mit einem **NULL-Abschlusszeichen** in den Ausgabepuffer kopiert, und die Funktion gibt eine Erfolgsanzeige zurück. Die Variable, auf die *lpdwBufferLength* zeigt, enthält jetzt die Anzahl der im Puffer gespeicherten Zeichen, mit Ausnahme des **NULL-Abschlusszeichens.**

> [!Note]  
> WinINet unterstützt keine Serverimplementierungen. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP-Dienste (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 