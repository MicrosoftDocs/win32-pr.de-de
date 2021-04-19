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
# <a name="reading-and-writing-from-a-file-view"></a><span data-ttu-id="8206e-103">Lesen und schreiben aus einer Dateiansicht</span><span class="sxs-lookup"><span data-stu-id="8206e-103">Reading and Writing From a File View</span></span>

<span data-ttu-id="8206e-104">Zum Lesen aus einer Dateiansicht müssen Sie den von der [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) -Funktion zurückgegebenen Zeiger dereferenzieren, wie in den folgenden Beispielen gezeigt.</span><span class="sxs-lookup"><span data-stu-id="8206e-104">To read from a file view, dereference the pointer returned by the [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) function as shown in the examples below.</span></span>

<span data-ttu-id="8206e-105">Das Lesen aus oder schreiben in eine Dateiansicht einer anderen Datei als der Auslagerungs Datei kann eine **Ausnahme \_ in der \_ Seiten \_ Fehler** Ausnahme auslösen.</span><span class="sxs-lookup"><span data-stu-id="8206e-105">Reading from or writing to a file view of a file other than the page file can cause an **EXCEPTION\_IN\_PAGE\_ERROR** exception.</span></span> <span data-ttu-id="8206e-106">Beispielsweise kann beim Zugriff auf eine zugeordnete Datei, die sich auf einem Remote Server befindet, eine Ausnahme generiert werden, wenn die Verbindung mit dem Server unterbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="8206e-106">For example, accessing a mapped file that resides on a remote server can generate an exception if the connection to the server is lost.</span></span> <span data-ttu-id="8206e-107">Ausnahmen können auch auftreten, wenn ein vollständiger Datenträger, ein zugrunde liegender Gerätefehler oder ein Fehler bei der Speicher Belegung vorliegt.</span><span class="sxs-lookup"><span data-stu-id="8206e-107">Exceptions can also occur because of a full disk, an underlying device failure, or a memory allocation failure.</span></span> <span data-ttu-id="8206e-108">Beim Schreiben in eine Dateiansicht können Ausnahmen auch auftreten, da die Datei freigegeben ist und ein anderer Prozess einen Byte Bereich gesperrt hat.</span><span class="sxs-lookup"><span data-stu-id="8206e-108">When writing to a file view, exceptions can also occur because the file is shared and a different process has locked a byte range.</span></span> <span data-ttu-id="8206e-109">Um auf Ausnahmen aufgrund von Eingabe-und Ausgabe Fehlern zu schützen, sollten alle Versuche, auf Speicher Abbild Dateien zuzugreifen, in strukturierten Ausnahme Handlern umschließt werden.</span><span class="sxs-lookup"><span data-stu-id="8206e-109">To guard against exceptions due to input and output (I/O) errors, all attempts to access memory mapped files should be wrapped in structured exception handlers.</span></span> <span data-ttu-id="8206e-110">Wenn Sie in einem **\_ \_ Ausnahme Filter eine** **Ausnahme \_ in \_ Seiten \_ Fehler** erhalten, stellen Sie sicher, dass sich die Adresse innerhalb der Zuordnung befindet, auf die Sie zurzeit zugreifen.</span><span class="sxs-lookup"><span data-stu-id="8206e-110">When you receive **EXCEPTION\_IN\_PAGE\_ERROR** in your **\_\_except** filter, make sure that the address is within the mapping you are currently accessing.</span></span> <span data-ttu-id="8206e-111">Wenn dies der Fall ist, führen Sie eine ordnungsgemäße Wiederherstellung durch Andernfalls wird die Ausnahme nicht behandelt.</span><span class="sxs-lookup"><span data-stu-id="8206e-111">If so, recover or fail gracefully; otherwise, do not handle the exception.</span></span>

<span data-ttu-id="8206e-112">Im folgenden Beispiel wird der von **MapViewOfFile** zurückgegebene Zeiger verwendet, um aus der Dateiansicht zu lesen:</span><span class="sxs-lookup"><span data-stu-id="8206e-112">The following example uses the pointer returned by **MapViewOfFile** to read from the file view:</span></span>


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



<span data-ttu-id="8206e-113">Im folgenden Beispiel wird der von **MapViewOfFile** zurückgegebene Zeiger verwendet, um in die Dateiansicht zu schreiben:</span><span class="sxs-lookup"><span data-stu-id="8206e-113">The following example uses the pointer returned by **MapViewOfFile** to write to the file view:</span></span>


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



<span data-ttu-id="8206e-114">Die [**flushviewoffile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) -Funktion kopiert die angegebene Anzahl von Bytes der Dateiansicht in die physische Datei, ohne darauf zu warten, dass der zwischengespeicherte Schreibvorgang stattfindet:</span><span class="sxs-lookup"><span data-stu-id="8206e-114">The [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) function copies the specified number of bytes of the file view to the physical file, without waiting for the cached write operation to occur:</span></span>


```C++
  if (!FlushViewOfFile(lpMapAddress, dwBytesToFlush)) 
  {
    printf("Could not flush memory to disk (%d).\n", GetLastError()); 
  }
```



<span data-ttu-id="8206e-115">Wenn Sie eine komprimierte Datei oder eine sparsespalte auf einer NTFS-Partition zuteilen, besteht bei einem Paging in einem Teil der Datei ein zusätzliches Potenzial für einen e/a-Fehler.</span><span class="sxs-lookup"><span data-stu-id="8206e-115">If you are mapping a compressed or sparse file on an NTFS partition, there is additional potential for an I/O error when paging in a portion of the file.</span></span> <span data-ttu-id="8206e-116">In diesem Fall wird der von [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) zugeordnete Adressraum möglicherweise nicht durch den zugewiesenen Speicherplatz gesichert.</span><span class="sxs-lookup"><span data-stu-id="8206e-116">In this case, the address space mapped by [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) may not be backed by allocated disk space.</span></span> <span data-ttu-id="8206e-117">Dies liegt daran, dass eine sparsedatei Regionen mit Nullen aufweisen kann, für die NTFS keinen Speicherplatz zuweist, und eine komprimierte Datei kann weniger Speicherplatz in Anspruch nehmen als die tatsächlich dargestellten Daten.</span><span class="sxs-lookup"><span data-stu-id="8206e-117">This is because a sparse file can have regions of zeros for which NTFS does not allocate disk space, and a compressed file can take up less disk space than the actual data that it represents.</span></span> <span data-ttu-id="8206e-118">Wenn Sie einen Teil einer Datei mit geringer Dichte oder komprimierte Datei lesen oder in diesen schreiben, die nicht durch Speicherplatz gesichert ist, kann das Betriebssystem versuchen, Speicherplatz zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="8206e-118">If you read from or write to a portion of a sparse or compressed file that is not backed by disk space, the operating system may try to allocate disk space.</span></span> <span data-ttu-id="8206e-119">Wenn der Datenträger voll ist, kann dies zu einer Ausnahme führen, die auf einen e/a-Fehler hinweist.</span><span class="sxs-lookup"><span data-stu-id="8206e-119">If the disk is full, this can result in an exception indicating an I/O error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8206e-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8206e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8206e-121">Strukturierte Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="8206e-121">Structured Exception Handling</span></span>](../debug/structured-exception-handling.md)
</dt> </dl>

 

 
