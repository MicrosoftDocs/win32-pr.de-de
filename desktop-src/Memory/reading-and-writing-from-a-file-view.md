---
description: Um aus einer Dateiansicht zu lesen, dereferenzieren Sie den zeiger, der von der MapViewOfFile-Funktion zurückgegeben wird, wie in den folgenden Beispielen gezeigt.
ms.assetid: c2a3da09-d116-4c2c-9e6c-ec9e80c88b99
title: Lesen und Schreiben aus einer Dateiansicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee56f1d06e53bdfd6f7571e4ec296da0270ce0a7050b253b5900c4640d6df0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067680"
---
# <a name="reading-and-writing-from-a-file-view"></a>Lesen und Schreiben aus einer Dateiansicht

Um aus einer Dateiansicht zu lesen, dereferenzieren Sie den zeiger, der von der [**MapViewOfFile-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) zurückgegeben wird, wie in den folgenden Beispielen gezeigt.

Das Lesen aus einer Dateiansicht oder das Schreiben in eine andere Datei als die Seitendatei kann zu einer **EXCEPTION \_ IN PAGE \_ \_ ERROR-Ausnahme** führen. Beispielsweise kann der Zugriff auf eine zugeordnete Datei, die sich auf einem Remoteserver befindet, eine Ausnahme generieren, wenn die Verbindung mit dem Server verloren geht. Ausnahmen können auch aufgrund eines vollständigen Datenträgers, eines zugrunde liegenden Gerätefehlers oder eines Speicherbelegungsfehlers auftreten. Beim Schreiben in eine Dateiansicht können Ausnahmen auch auftreten, weil die Datei freigegeben ist und ein anderer Prozess einen Bytebereich gesperrt hat. Um sich vor Ausnahmen aufgrund von Eingabe- und Ausgabefehlern (E/A) zu schützen, sollten alle Versuche, auf Speicherabzugsdateien zu zugreifen, in strukturierte Ausnahmehandler umschlossen werden. Wenn SIE **EXCEPTION IN PAGE \_ \_ \_ ERROR** in Ihrem Filter **\_ \_ außer** erhalten, stellen Sie sicher, dass sich die Adresse innerhalb der Zuordnung befindet, auf die Sie gerade zugreifen. Wenn dies der Fehler ist, stellen Sie die Wiederherstellung ordnungsgemäß wieder auf, oder führen Sie einen Fehler aus. Andernfalls behandeln Sie die Ausnahme nicht.

Im folgenden Beispiel wird der von **MapViewOfFile** zurückgegebene Zeiger zum Lesen aus der Dateiansicht verwendet:


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



Die [**FlushViewOfFile-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) kopiert die angegebene Anzahl von Bytes der Dateiansicht in die physische Datei, ohne auf den Zwischenspeicherungsvorgang zu warten:


```C++
  if (!FlushViewOfFile(lpMapAddress, dwBytesToFlush)) 
  {
    printf("Could not flush memory to disk (%d).\n", GetLastError()); 
  }
```



Wenn Sie eine komprimierte Datei oder eine Sparsedatei auf einer NTFS-Partition zuordnen, besteht zusätzliches Potenzial für einen E/A-Fehler beim Paging in einem Teil der Datei. In diesem Fall wird der von [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) zugeordnete Adressraum möglicherweise nicht durch zugeordneten Speicherplatz auf dem Datenträger zurückgespiegelt. Dies liegt daran, dass eine Sparsedatei Bereiche mit Nullen haben kann, für die NTFS keinen Speicherplatz zuteilen kann, und eine komprimierte Datei kann weniger Speicherplatz als die tatsächlichen Daten, die sie darstellt, nutzen. Wenn Sie aus einem Teil einer Datei mit sparseer Oder komprimierter Datei lesen oder in diesen schreiben, der nicht durch Speicherplatz auf dem Datenträger bzw. nicht auf dem Datenträger gespeichert ist, versucht das Betriebssystem möglicherweise, Speicherplatz auf dem Datenträger zu reservieren. Wenn der Datenträger voll ist, kann dies zu einer Ausnahme führen, die auf einen E/A-Fehler hinweist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Strukturierte Ausnahmebehandlung](../debug/structured-exception-handling.md)
</dt> </dl>

 

 
