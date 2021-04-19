---
description: Die folgenden Beispiele veranschaulichen die Verwendung der Komprimierungs-API im Puffer Modus.
ms.assetid: 0A062E5D-E5FA-4098-B76E-E136FC74D853
title: Verwenden der Komprimierungs-API im Puffer Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 676a5bea1ea4fa673bbf9a8fc2caf9fe84d9bc1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343012"
---
# <a name="using-the-compression-api-in-buffer-mode"></a><span data-ttu-id="eb39b-103">Verwenden der Komprimierungs-API im Puffer Modus</span><span class="sxs-lookup"><span data-stu-id="eb39b-103">Using the Compression API in buffer mode</span></span>

<span data-ttu-id="eb39b-104">Die folgenden Beispiele veranschaulichen die Verwendung der Komprimierungs-API im Puffer Modus.</span><span class="sxs-lookup"><span data-stu-id="eb39b-104">The following samples demonstrate using the Compression API in buffer mode.</span></span> <span data-ttu-id="eb39b-105">Der Puffer Modus wurde zur einfachen Verwendung entwickelt und teilt den Eingabepuffer automatisch in Blöcke einer Größe, die für den ausgewählten Komprimierungs Algorithmus geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="eb39b-105">Buffer mode was developed for ease of use and automatically splits up the input buffer into blocks of a size that is appropriate for the selected compression algorithm.</span></span> <span data-ttu-id="eb39b-106">Der Puffer Modus formatiert und speichert automatisch die nicht komprimierte Puffergröße im komprimierten Puffer, wo Sie für den Dekompressor verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="eb39b-106">Buffer mode automatically formats and stores the uncompressed buffer size in the compressed buffer where it is available to the decompressor.</span></span> <span data-ttu-id="eb39b-107">Die Größe des komprimierten Puffers wird nicht automatisch gespeichert, und die Anwendung muss dies für die Komprimierung speichern.</span><span class="sxs-lookup"><span data-stu-id="eb39b-107">The size of the compressed buffer is not automatically saved, and the application needs to save this for decompression.</span></span> <span data-ttu-id="eb39b-108">Fügen Sie beim Aufrufen von [**createcompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) oder [**createdecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) das Flag zum **Komprimieren von \_ RAW** nicht ein, wenn Sie die Komprimierungs-API im Puffer Modus verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="eb39b-108">Do not include the **COMPRESS\_RAW** flag when calling [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) or [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) if you want to use the Compression API in buffer mode.</span></span>

<span data-ttu-id="eb39b-109">Der Puffer Modus wird in den meisten Fällen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="eb39b-109">Buffer mode is recommended for most cases.</span></span> <span data-ttu-id="eb39b-110">Weitere Informationen zur Verwendung des Block Modus finden [Sie unter Verwenden der Komprimierungs-API im Block Modus](using-the-compression-api-in-block-mode.md) .</span><span class="sxs-lookup"><span data-stu-id="eb39b-110">For more information about how to use block mode, see [Using the Compression API in block mode](using-the-compression-api-in-block-mode.md)</span></span>

<span data-ttu-id="eb39b-111">Anwendungen, die den Puffer-oder Block Modus verwenden, können beim Aufrufen von [**createcompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) oder [**createdecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor)eine benutzerdefinierte Speicher Belegungs Routine angeben.</span><span class="sxs-lookup"><span data-stu-id="eb39b-111">Applications using buffer or block mode have the option to specify a custom memory allocation routine when calling [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) or [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor).</span></span> <span data-ttu-id="eb39b-112">Ein Beispiel für eine einfache, angepasste Zuordnungs Routine finden Sie im Abschnitt [Verwenden des Komprimierungs-API im Block Modus](using-the-compression-api-in-block-mode.md) .</span><span class="sxs-lookup"><span data-stu-id="eb39b-112">See the [Using the Compression API in block mode](using-the-compression-api-in-block-mode.md) section for an example of a simple customized allocation routine.</span></span>

<span data-ttu-id="eb39b-113">**Windows 8 und Windows Server 2012:** Wenn Sie den folgenden Beispielcode verwenden möchten, müssen Sie Windows 8 oder Windows Server 2012 ausführen und über "compressapi. h" und "cabinet.dll" und einen Link zu "CAB. lib" verfügen.</span><span class="sxs-lookup"><span data-stu-id="eb39b-113">**Windows 8 and Windows Server 2012:** To use the following example code, you must be running Windows 8 or Windows Server 2012 and have "compressapi.h" and "cabinet.dll" and link to the "Cabinet.lib".</span></span>

<span data-ttu-id="eb39b-114">Der folgende Code Ausschnitt veranschaulicht die Dateikomprimierung mit dem Xpress-Komprimierungs Algorithmus und die Huffman-Codierung mithilfe der Komprimierungs-API im Puffer Modus.</span><span class="sxs-lookup"><span data-stu-id="eb39b-114">The following code snippet demonstrates file compression with the XPRESS compression algorithm and Huffman encoding using the Compression API in buffer mode.</span></span> <span data-ttu-id="eb39b-115">Die Anwendung akzeptiert eine Datei, komprimiert ihren Inhalt und generiert eine komprimierte Datei.</span><span class="sxs-lookup"><span data-stu-id="eb39b-115">The application accepts a file, compresses its contents and generates a compressed file.</span></span> <span data-ttu-id="eb39b-116">Zuerst Ruft die Anwendung mit dem **Komprimierungs \_ Algorithmus \_ Xpress \_ Huff** [**einen Kompressor auf**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) , um einen Kompressor zu generieren.</span><span class="sxs-lookup"><span data-stu-id="eb39b-116">First the application calls [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) with **COMPRESS\_ALGORITHM\_XPRESS\_HUFF** to generate a compressor.</span></span> <span data-ttu-id="eb39b-117">Anschließend wird [**Compress**](/windows/desktop/api/compressapi/nf-compressapi-compress)aufgerufen, wobei *compressedbuffersize* auf 0 festgelegt ist, um die erforderliche Größe des komprimierten Puffers abzufragen.</span><span class="sxs-lookup"><span data-stu-id="eb39b-117">Then it calls [**Compress**](/windows/desktop/api/compressapi/nf-compressapi-compress), with *CompressedBufferSize* set to 0, to query for the required size of the compressed buffer.</span></span> <span data-ttu-id="eb39b-118">Er ordnet einen Ausgabepuffer dem *compressedbuffersize* -Wert zu.</span><span class="sxs-lookup"><span data-stu-id="eb39b-118">It allocates an output buffer to the *CompressedBufferSize* value.</span></span> <span data-ttu-id="eb39b-119">Die Anwendung ruft ein zweites Mal **eine Komprimierung** auf, um die tatsächliche Komprimierung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="eb39b-119">The application calls **Compress** a second time to perform the actual compression.</span></span> <span data-ttu-id="eb39b-120">Schließlich schreibt die Anwendung die komprimierten Daten in die Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="eb39b-120">Finally, the application writes the compressed data to the output file.</span></span>


```C++
#include <Windows.h>
#include <stdio.h>
#include <compressapi.h>

void wmain(_In_ int argc, _In_ WCHAR *argv[])
{
    COMPRESSOR_HANDLE Compressor    = NULL;
    PBYTE CompressedBuffer          = NULL;
    PBYTE InputBuffer               = NULL;
    HANDLE InputFile                = INVALID_HANDLE_VALUE;
    HANDLE CompressedFile           = INVALID_HANDLE_VALUE;    
    BOOL DeleteTargetFile           = TRUE;
    BOOL Success;
    SIZE_T CompressedDataSize, CompressedBufferSize;
    DWORD InputFileSize, ByteRead, ByteWritten;
    LARGE_INTEGER FileSize;    
    ULONGLONG StartTime, EndTime;
    double TimeDuration;

    if (argc != 3)
    {
        wprintf(L"Usage:\n\t%s <input_file_name> <compressd_file_name>\n", argv[0]);
        return;
    }

    //  Open input file for reading, existing file only.
    InputFile = CreateFile(
        argv[1],                  //  Input file name
        GENERIC_READ,             //  Open for reading
        FILE_SHARE_READ,          //  Share for read
        NULL,                     //  Default security
        OPEN_EXISTING,            //  Existing file only
        FILE_ATTRIBUTE_NORMAL,    //  Normal file
        NULL);                    //  No attr. template

    if (InputFile == INVALID_HANDLE_VALUE)
    {
        wprintf(L"Cannot open \t%s\n", argv[1]);
        goto done;
    }

    //  Get input file size.
    Success = GetFileSizeEx(InputFile, &FileSize);
    if ((!Success)||(FileSize.QuadPart > 0xFFFFFFFF))
    {
        wprintf(L"Cannot get input file size or file is larger than 4GB.\n");        
        goto done;
    }
    InputFileSize = FileSize.LowPart;

    //  Allocate memory for file content.
    InputBuffer = (PBYTE)malloc(InputFileSize);
    if (!InputBuffer)
    {
        wprintf(L"Cannot allocate memory for uncompressed buffer.\n");
        goto done;
    }                              

    //  Read input file.
    Success = ReadFile(InputFile, InputBuffer, InputFileSize, &ByteRead, NULL);
    if ((!Success)||(ByteRead != InputFileSize))
    {
        wprintf(L"Cannot read from \t%s\n", argv[1]);
        goto done;
    }

    //  Open an empty file for writing, if exist, overwrite it.
    CompressedFile = CreateFile(
        argv[2],                  //  Compressed file name
        GENERIC_WRITE|DELETE,     //  Open for writing; delete if cannot compress
        0,                        //  Do not share
        NULL,                     //  Default security
        CREATE_ALWAYS,            //  Create a new file; if exist, overwrite it
        FILE_ATTRIBUTE_NORMAL,    //  Normal file
        NULL);                    //  No template

    if (CompressedFile == INVALID_HANDLE_VALUE)
    {
        wprintf(L"Cannot create file \t%s\n", argv[2]);
        goto done;
    }

    //  Create an XpressHuff compressor.
    Success = CreateCompressor(
        COMPRESS_ALGORITHM_XPRESS_HUFF, //  Compression Algorithm
        NULL,                           //  Optional allocation routine
        &Compressor);                   //  Handle

    if (!Success)
    {
        wprintf(L"Cannot create a compressor %d.\n", GetLastError());
        goto done;
    }

    //  Query compressed buffer size.
    Success = Compress(
        Compressor,                  //  Compressor Handle
        InputBuffer,                 //  Input buffer, Uncompressed data
        InputFileSize,               //  Uncompressed data size
        NULL,                        //  Compressed Buffer
        0,                           //  Compressed Buffer size
        &CompressedBufferSize);      //  Compressed Data size

    //  Allocate memory for compressed buffer.
    if (!Success)
    {
        DWORD ErrorCode = GetLastError();

        if (ErrorCode != ERROR_INSUFFICIENT_BUFFER)
        {
            wprintf(L"Cannot compress data: %d.\n", ErrorCode);
            goto done;
        }
            
        CompressedBuffer = (PBYTE)malloc(CompressedBufferSize);
        if (!CompressedBuffer)
        {
            wprintf(L"Cannot allocate memory for compressed buffer.\n");
            goto done;
        }
    }

    StartTime = GetTickCount64();

    //  Call Compress() again to do real compression and output the compressed
    //  data to CompressedBuffer.
    Success = Compress(
        Compressor,             //  Compressor Handle
        InputBuffer,            //  Input buffer, Uncompressed data
        InputFileSize,          //  Uncompressed data size
        CompressedBuffer,       //  Compressed Buffer
        CompressedBufferSize,   //  Compressed Buffer size
        &CompressedDataSize);   //  Compressed Data size

    if (!Success)
    {
        wprintf(L"Cannot compress data: %d\n", GetLastError());
        goto done;
    }

    EndTime = GetTickCount64();

    //  Get compression time.
    TimeDuration = (EndTime - StartTime)/1000.0;

    //  Write compressed data to output file.
    Success = WriteFile(
        CompressedFile,     //  File handle
        CompressedBuffer,   //  Start of data to write
        CompressedDataSize, //  Number of byte to write
        &ByteWritten,       //  Number of byte written
        NULL);              //  No overlapping structure

    if ((ByteWritten != CompressedDataSize) || (!Success))
    {
        wprintf(L"Cannot write compressed data to file: %d.\n", GetLastError());
        goto done;
    }

    wprintf(
        L"Input file size: %d; Compressed Size: %d\n", 
        InputFileSize, 
        CompressedDataSize);
    wprintf(L"Compression Time(Exclude I/O): %.2f seconds\n", TimeDuration);
    wprintf(L"File Compressed.\n");

    DeleteTargetFile = FALSE;

done:
    if (Compressor != NULL)
    {
        CloseCompressor(Compressor);
    }

    if (CompressedBuffer) 
    {
        free(CompressedBuffer);
    }

    if (InputBuffer)
    {
        free(InputBuffer);
    }

    if (InputFile != INVALID_HANDLE_VALUE)
    {
        CloseHandle(InputFile);
    }

    if (CompressedFile != INVALID_HANDLE_VALUE)
    {
        //  Compression fails, delete the compressed file.
        if (DeleteTargetFile)
        {
            FILE_DISPOSITION_INFO fdi;
            fdi.DeleteFile = TRUE;      //  Marking for deletion
            Success = SetFileInformationByHandle(
                CompressedFile,
                FileDispositionInfo,
                &fdi,
                sizeof(FILE_DISPOSITION_INFO));    
            if (!Success) {
                wprintf(L"Cannot delete corrupted compressed file.\n");
            }
        }
        CloseHandle(CompressedFile);
    }
}
```



<span data-ttu-id="eb39b-121">Der folgende Code Ausschnitt veranschaulicht die Datei Dekomprimierung mithilfe der Komprimierungs-API im Puffer Modus.</span><span class="sxs-lookup"><span data-stu-id="eb39b-121">The following code snippet demonstrates file decompression using the Compression API in buffer mode.</span></span>


```C++
#include <Windows.h>
#include <stdio.h>
#include <compressapi.h>

void wmain(_In_ int argc, _In_ WCHAR *argv[])
{
    DECOMPRESSOR_HANDLE Decompressor    = NULL;
    PBYTE CompressedBuffer              = NULL;
    PBYTE DecompressedBuffer            = NULL;
    HANDLE InputFile                    = INVALID_HANDLE_VALUE;
    HANDLE DecompressedFile             = INVALID_HANDLE_VALUE;    
    BOOL DeleteTargetFile               = TRUE;    
    BOOL Success;
    SIZE_T DecompressedBufferSize, DecompressedDataSize;
    DWORD InputFileSize, ByteRead, ByteWritten;
    ULONGLONG StartTime, EndTime;
    LARGE_INTEGER FileSize;    
    double TimeDuration;

    if (argc != 3) 
    {
        wprintf(L"Usage:\n\t%s <compressed_file_name> <decompressed_file_name>\n", argv[0]);
        return;
    }

    //  Open input file for reading, existing file only.
    InputFile = CreateFile(
        argv[1],                  //  Input file name, compressed file
        GENERIC_READ,             //  Open for reading
        FILE_SHARE_READ,          //  Share for read
        NULL,                     //  Default security
        OPEN_EXISTING,            //  Existing file only
        FILE_ATTRIBUTE_NORMAL,    //  Normal file
        NULL);                    //  No template

    if (InputFile == INVALID_HANDLE_VALUE)
    {
        wprintf(L"Cannot open \t%s\n", argv[1]);
        goto done;
    }

    //  Get compressed file size.
    Success = GetFileSizeEx(InputFile, &FileSize);
    if ((!Success)||(FileSize.QuadPart > 0xFFFFFFFF))
    {
        wprintf(L"Cannot get input file size or file is larger than 4GB.\n");        
        goto done;
    }
    InputFileSize = FileSize.LowPart;

    //  Allocation memory for compressed content.
    CompressedBuffer = (PBYTE)malloc(InputFileSize);
    if (!CompressedBuffer)
    {
        wprintf(L"Cannot allocate memory for compressed buffer.\n");
        goto done;
    }

    //  Read compressed content into buffer.
    Success = ReadFile(InputFile, CompressedBuffer, InputFileSize, &ByteRead, NULL);
    if ((!Success) || (ByteRead != InputFileSize))
    {
        wprintf(L"Cannot read from \t%s\n", argv[1]);
        goto done;
    }

    //  Open an empty file for writing, if exist, destroy it.
    DecompressedFile = CreateFile(
        argv[2],                  //  Decompressed file name
        GENERIC_WRITE|DELETE,     //  Open for writing
        0,                        //  Do not share
        NULL,                     //  Default security
        CREATE_ALWAYS,            //  Create a new file, if exists, overwrite it.
        FILE_ATTRIBUTE_NORMAL,    //  Normal file
        NULL);                    //  No template

    if (DecompressedFile == INVALID_HANDLE_VALUE)
    {
        wprintf(L"Cannot create file \t%s\n", argv[2]);
        goto done;
    }

    //  Create an XpressHuff decompressor.
    Success = CreateDecompressor(
        COMPRESS_ALGORITHM_XPRESS_HUFF, //  Compression Algorithm
        NULL,                           //  Optional allocation routine
        &Decompressor);                 //  Handle

    if (!Success)
    {
        wprintf(L"Cannot create a decompressor: %d.\n", GetLastError());
        goto done;
    }

    //  Query decompressed buffer size.
    Success = Decompress(
        Decompressor,                //  Compressor Handle
        CompressedBuffer,            //  Compressed data
        InputFileSize,               //  Compressed data size
        NULL,                        //  Buffer set to NULL
        0,                           //  Buffer size set to 0
        &DecompressedBufferSize);    //  Decompressed Data size

    //  Allocate memory for decompressed buffer.
    if (!Success)
    {
        DWORD ErrorCode = GetLastError();

        // Note that the original size returned by the function is extracted 
        // from the buffer itself and should be treated as untrusted and tested
        // against reasonable limits.
        if (ErrorCode != ERROR_INSUFFICIENT_BUFFER) 
        {
            wprintf(L"Cannot decompress data: %d.\n",ErrorCode);
            goto done;
        }

        DecompressedBuffer = (PBYTE)malloc(DecompressedBufferSize);
        if (!DecompressedBuffer)
        {
            wprintf(L"Cannot allocate memory for decompressed buffer.\n");
            goto done;
        }           
    }
        
    StartTime = GetTickCount64();

    //  Decompress data and write data to DecompressedBuffer.
    Success = Decompress(
        Decompressor,               //  Decompressor handle
        CompressedBuffer,           //  Compressed data
        InputFileSize,              //  Compressed data size
        DecompressedBuffer,         //  Decompressed buffer
        DecompressedBufferSize,     //  Decompressed buffer size
        &DecompressedDataSize);     //  Decompressed data size

    if (!Success)
    {
        wprintf(L"Cannot decompress data: %d.\n", GetLastError());
        goto done;
    }

EndTime = GetTickCount64();

    //  Get decompression time.
    TimeDuration = (EndTime - StartTime)/1000.0;

    //  Write decompressed data to output file.
    Success = WriteFile(
        DecompressedFile,       //  File handle
        DecompressedBuffer,     //  Start of data to write
        DecompressedDataSize,   //  Number of byte to write
        &ByteWritten,           //  Number of byte written
        NULL);                  //  No overlapping structure
    if ((ByteWritten != DecompressedDataSize) || (!Success))
    {
        wprintf(L"Cannot write decompressed data to file.\n");
        goto done;
    }
    
    wprintf(
        L"Compressed size: %d; Decompressed Size: %d\n",
        InputFileSize,
        DecompressedDataSize);
    wprintf(L"Decompression Time(Exclude I/O): %.2f seconds\n", TimeDuration);
    wprintf(L"File decompressed.\n");

    DeleteTargetFile = FALSE;

done:
    if (Decompressor != NULL)
    {
        CloseDecompressor(Decompressor);
    }

    if (CompressedBuffer) 
    {
        free(CompressedBuffer);
    }

    if (DecompressedBuffer)
    {
        free(DecompressedBuffer);
    }

    if (InputFile != INVALID_HANDLE_VALUE)
    {
        CloseHandle(InputFile);
    }

    if (DecompressedFile != INVALID_HANDLE_VALUE)
    {
        //  Compression fails, delete the compressed file.
        if (DeleteTargetFile)
        {
            FILE_DISPOSITION_INFO fdi;
            fdi.DeleteFile = TRUE;      //  Marking for deletion
            Success = SetFileInformationByHandle(
                DecompressedFile,
                FileDispositionInfo,
                &fdi,
                sizeof(FILE_DISPOSITION_INFO));    
            if (!Success) {
                wprintf(L"Cannot delete corrupted decompressed file.\n");
            }
        }
        CloseHandle(DecompressedFile); 
    }
}
```



 

 



