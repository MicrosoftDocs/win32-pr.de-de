---
description: Zum Lesen aus einer Dateiansicht müssen Sie den von der MapViewOfFile-Funktion zurückgegebenen Zeiger dereferenzieren, wie in den folgenden Beispielen gezeigt.
ms.assetid: c2a3da09-d116-4c2c-9e6c-ec9e80c88b99
title: Lesen und schreiben aus einer Dateiansicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98ec50dc6cd8b0224f2ba33a17ba80c7b0fc658
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373368"
---
# <a name="reading-and-writing-from-a-file-view"></a>Lesen und schreiben aus einer Dateiansicht

Zum Lesen aus einer Dateiansicht müssen Sie den von der [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) -Funktion zurückgegebenen Zeiger dereferenzieren, wie in den folgenden Beispielen gezeigt.

Das Lesen aus oder schreiben in eine Dateiansicht einer anderen Datei als der Auslagerungs Datei kann eine **Ausnahme \_ in der \_ Seiten \_ Fehler** Ausnahme auslösen. Beispielsweise kann beim Zugriff auf eine zugeordnete Datei, die sich auf einem Remote Server befindet, eine Ausnahme generiert werden, wenn die Verbindung mit dem Server unterbrochen wird. Ausnahmen können auch auftreten, wenn ein vollständiger Datenträger, ein zugrunde liegender Gerätefehler oder ein Fehler bei der Speicher Belegung vorliegt. Beim Schreiben in eine Dateiansicht können Ausnahmen auch auftreten, da die Datei freigegeben ist und ein anderer Prozess einen Byte Bereich gesperrt hat. Um auf Ausnahmen aufgrund von Eingabe-und Ausgabe Fehlern zu schützen, sollten alle Versuche, auf Speicher Abbild Dateien zuzugreifen, in strukturierten Ausnahme Handlern umschließt werden. Wenn Sie in einem **\_ \_ Ausnahme Filter eine** **Ausnahme \_ in \_ Seiten \_ Fehler** erhalten, stellen Sie sicher, dass sich die Adresse innerhalb der Zuordnung befindet, auf die Sie zurzeit zugreifen. Wenn dies der Fall ist, führen Sie eine ordnungsgemäße Wiederherstellung durch Andernfalls wird die Ausnahme nicht behandelt.

Im folgenden Beispiel wird der von **MapViewOfFile** zurückgegebene Zeiger verwendet, um aus der Dateiansicht zu lesen:


```C++
  DWORD dwLength;

  __try
  {
    dwLength = *((LPDWORD) lpMapAddress);
  }
  __except(GetExceptionCode()==EXCEPTION_IN_PAGE_ERROR ?
    EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
  {
    // Failed to read from the view.
  }
```



Im folgenden Beispiel wird der von **MapViewOfFile** zurückgegebene Zeiger verwendet, um in die Dateiansicht zu schreiben:


```C++
  DWORD dwLength;

  __try
  {
    *((LPDWORD) lpMapAddress) = dwLength;
  }
  __except (GetExceptionCode() == EXCEPTION_IN_PAGE_ERROR ? 
    EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
  {
    // Failed to write to the view.
  }
```



Die [**flushviewoffile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) -Funktion kopiert die angegebene Anzahl von Bytes der Dateiansicht in die physische Datei, ohne darauf zu warten, dass der zwischengespeicherte Schreibvorgang stattfindet:


```C++
  if (!FlushViewOfFile(lpMapAddress, dwBytesToFlush)) 
  {
    printf("Could not flush memory to disk (%d).\n", GetLastError()); 
  }
```



Wenn Sie eine komprimierte Datei oder eine sparsespalte auf einer NTFS-Partition zuteilen, besteht bei einem Paging in einem Teil der Datei ein zusätzliches Potenzial für einen e/a-Fehler. In diesem Fall wird der von [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) zugeordnete Adressraum möglicherweise nicht durch den zugewiesenen Speicherplatz gesichert. Dies liegt daran, dass eine sparsedatei Regionen mit Nullen aufweisen kann, für die NTFS keinen Speicherplatz zuweist, und eine komprimierte Datei kann weniger Speicherplatz in Anspruch nehmen als die tatsächlich dargestellten Daten. Wenn Sie einen Teil einer Datei mit geringer Dichte oder komprimierte Datei lesen oder in diesen schreiben, die nicht durch Speicherplatz gesichert ist, kann das Betriebssystem versuchen, Speicherplatz zuzuweisen. Wenn der Datenträger voll ist, kann dies zu einer Ausnahme führen, die auf einen e/a-Fehler hinweist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Strukturierte Ausnahmebehandlung](../debug/structured-exception-handling.md)
</dt> </dl>

 

 
