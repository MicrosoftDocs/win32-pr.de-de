---
description: Im folgenden Beispiel wird die Verwendung der Komprimierungs-API im Block Modus veranschaulicht.
ms.assetid: 7483BCE4-3B85-4659-98E3-670D2F7EE52D
title: Verwenden der Komprimierungs-API im Block Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddd1ecaec03d332262ffb24462e73a9fcb789d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127572"
---
# <a name="using-the-compression-api-in-block-mode"></a><span data-ttu-id="b30c1-103">Verwenden der Komprimierungs-API im Block Modus</span><span class="sxs-lookup"><span data-stu-id="b30c1-103">Using the Compression API in block mode</span></span>

<span data-ttu-id="b30c1-104">Im folgenden Beispiel wird die Verwendung der Komprimierungs-API im Block Modus veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b30c1-104">The following example demonstrates using the Compression API in block mode.</span></span> <span data-ttu-id="b30c1-105">Wenn Sie einen Kompressor oder Dekompressor mithilfe des Block Modus generieren möchten, muss die Anwendung das Flag zum **Komprimieren von \_ Rohdaten** enthalten, wenn Sie "up" oder " [**kreatedecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) [**" aufruft.**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor)</span><span class="sxs-lookup"><span data-stu-id="b30c1-105">To generate a compressor or decompressor using block mode, your application must include the **COMPRESS\_RAW** flag when it calls [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) or [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor).</span></span> <span data-ttu-id="b30c1-106">Der Block Modus ermöglicht es dem Entwickler, die Blockgröße zu steuern, erfordert jedoch mehr Arbeit durch die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b30c1-106">Block mode enables the developer to control the block size, but requires more work be done by the application.</span></span>

<span data-ttu-id="b30c1-107">Der Block Modus schlägt fehl, wenn die Größe des Eingabe Puffers größer als die interne Blockgröße des Komprimierungs Algorithmus ist.</span><span class="sxs-lookup"><span data-stu-id="b30c1-107">The block mode will fail if the size of the input buffer is greater than the internal block size of the compression algorithm.</span></span> <span data-ttu-id="b30c1-108">Die interne Blockgröße beträgt 32 KB für mszip und 1 GB für die Xpress-Komprimierungs Algorithmen.</span><span class="sxs-lookup"><span data-stu-id="b30c1-108">The internal block size is 32KB for the MSZIP and 1GB for the XPRESS compression algorithms.</span></span> <span data-ttu-id="b30c1-109">Die interne Blockgröße für lzms kann bis zu 64 GB mit einer entsprechenden Erhöhung der Arbeitsspeicher Nutzung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="b30c1-109">The internal block size for LZMS is configurable up to 64GB with a corresponding increase in memory use.</span></span> <span data-ttu-id="b30c1-110">Der Wert des *uncompressedbuffersize* -Parameters von [**Decompress**](/windows/desktop/api/compressapi/nf-compressapi-decompress) muss genau gleich der ursprünglichen Größe der nicht komprimierten Daten und nicht nur der Größe des Ausgabepuffers sein.</span><span class="sxs-lookup"><span data-stu-id="b30c1-110">The value of *UncompressedBufferSize* parameter of [**Decompress**](/windows/desktop/api/compressapi/nf-compressapi-decompress) must be exactly equal to the original size of the uncompressed data and not just the size of the output buffer.</span></span> <span data-ttu-id="b30c1-111">Dies bedeutet, dass Ihre Anwendung die Blockgröße angeben und die genaue ursprüngliche Größe der nicht komprimierten Daten für die Verwendung durch den-Debug speichern muss.</span><span class="sxs-lookup"><span data-stu-id="b30c1-111">This means your application will need to specify the block size and save the exact original size of the uncompressed data for use by the decompressor.</span></span> <span data-ttu-id="b30c1-112">Die Größe des komprimierten Puffers wird nicht automatisch gespeichert, und die Anwendung muss dies auch für die Komprimierung speichern.</span><span class="sxs-lookup"><span data-stu-id="b30c1-112">The size of the compressed buffer is not automatically saved, and the application also needs to save this for decompression.</span></span>

<span data-ttu-id="b30c1-113">Der Puffer Modus wird in den meisten Fällen empfohlen, da er automatisch den Eingabepuffer in Blöcke einer Größe aufteilt, die für den ausgewählten Komprimierungs Algorithmus geeignet ist, speichert die nicht komprimierte Puffergröße im komprimierten Puffer.</span><span class="sxs-lookup"><span data-stu-id="b30c1-113">The buffer mode is recommended in most cases because it automatically splits up the input buffer into blocks of a size that is appropriate for the selected compression algorithm stores the uncompressed buffer size in the compressed buffer.</span></span> <span data-ttu-id="b30c1-114">Informationen zur Verwendung des Puffer Modus finden [Sie unter Verwenden der Komprimierungs-API im Puffer Modus](using-the-compression-api-in-buffer-mode.md).</span><span class="sxs-lookup"><span data-stu-id="b30c1-114">For information on how to use buffer mode, see [Using the Compression API in buffer mode](using-the-compression-api-in-buffer-mode.md).</span></span>

<span data-ttu-id="b30c1-115">Anwendungen, die den Puffer-oder Block Modus verwenden, haben die Möglichkeit, eine benutzerdefinierte Speicher Belegungs Routine in dem Aufrufen von " [**anatecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) " oder " [**deedecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor)" anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b30c1-115">Applications using buffer or block mode have the option to specify a custom memory allocation routine in its call to [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) or [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor).</span></span>

<span data-ttu-id="b30c1-116">**Windows 8 und Windows Server 2012:** Wenn Sie den folgenden Beispielcode verwenden möchten, müssen Sie Windows 8 oder Windows Server 2012 ausführen und über "compressapi. h" und "cabinet.dll" und einen Link zu "CAB. lib" verfügen.</span><span class="sxs-lookup"><span data-stu-id="b30c1-116">**Windows 8 and Windows Server 2012:** To use the following example code, you must be running Windows 8 or Windows Server 2012 and have "compressapi.h" and "cabinet.dll" and link to the "Cabinet.lib".</span></span>

<span data-ttu-id="b30c1-117">Im folgenden Beispiel wird die Verwendung der Komprimierungs-API im Block Modus veranschaulicht, um eine Datei mit dem lzms-Komprimierungs Algorithmus und einer angepassten Speicher Belegungs Routine zu komprimieren.</span><span class="sxs-lookup"><span data-stu-id="b30c1-117">The following demonstrates using the Compression API in block mode to compress a file using the LZMS compression algorithm and a customized memory allocation routine.</span></span> <span data-ttu-id="b30c1-118">Die Anwendung muss das **komprimieren- \_ RAW** -Flag enthalten, um die Komprimierungs-API im Block Modus zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b30c1-118">Your application must include the **COMPRESS\_RAW** flag to use the Compression API in block mode.</span></span> <span data-ttu-id="b30c1-119">Zuerst Ruft die Anwendung " [**kreatecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) " mit dem **Komprimierungs \_ Algorithmus \_ lzms** \| **Compress \_ RAW** auf, um den Kompressor zu generieren.</span><span class="sxs-lookup"><span data-stu-id="b30c1-119">First the application calls [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) with **COMPRESS\_ALGORITHM\_LZMS**\|**COMPRESS\_RAW** to generate the compressor.</span></span> <span data-ttu-id="b30c1-120">Der *allocationroutinen* -Parameter gibt die Speicher Belegungs Routine an.</span><span class="sxs-lookup"><span data-stu-id="b30c1-120">The *AllocationRoutines* parameter specifies the memory allocation routine.</span></span> <span data-ttu-id="b30c1-121">Die Anwendung legt dann die Blockgröße für den Kompressor mithilfe von [**setcompressorinformation**](/windows/desktop/api/compressapi/nf-compressapi-setcompressorinformation)fest.</span><span class="sxs-lookup"><span data-stu-id="b30c1-121">The application then sets the block size for the compressor using [**SetCompressorInformation**](/windows/desktop/api/compressapi/nf-compressapi-setcompressorinformation).</span></span>

<span data-ttu-id="b30c1-122">Die Anwendung führt wiederholte Aufrufe von [**Compress**](/windows/desktop/api/compressapi/nf-compressapi-compress) aus, um den Datenblock nach Block zu komprimieren.</span><span class="sxs-lookup"><span data-stu-id="b30c1-122">The application makes repeated calls to [**Compress**](/windows/desktop/api/compressapi/nf-compressapi-compress) to compress the data block by block.</span></span> <span data-ttu-id="b30c1-123">Die Anwendung schreibt die nicht komprimierte Blockgröße, die komprimierte Blockgröße und die komprimierten Daten in den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="b30c1-123">The application writes the uncompressed block size, compressed block size, and compressed data into the output buffer.</span></span>


```C++
#include <Windows.h>
#include <stdio.h>
#include <compressapi.h>

#define META_DATA_SIZE (2 * sizeof(ULONG))
#define BLOCK_SIZE (1 * 1024 * 1024)                //  Block size is 1MB

PVOID SimpleAlloc(PVOID Context, SIZE_T Size)
{
    UNREFERENCED_PARAMETER(Context);
    return malloc(Size);
}

VOID SimpleFree(PVOID Context, PVOID Memory)
{
    UNREFERENCED_PARAMETER(Context);
    if (Memory != NULL)
    {
        free(Memory);
    }
    return;
}

BOOL BlockModeCompress(
    _In_ PBYTE InputData, 
    _In_ DWORD InputSize, 
    _Deref_out_opt_ PBYTE *OutputData, 
    _Out_ DWORD *CompressedSize
    )
{
    COMPRESSOR_HANDLE Compressor    = NULL;
    DWORD ProcessedSoFar            = 0;
    SIZE_T OutputSoFar              = 0;
    DWORD CurrentBlockSize          = 0;
    SIZE_T CompressedDataSize       = 0;
    SIZE_T CompressedBlockSize      = 0;
    SIZE_T OutputDataSize           = 0;  
    BOOL Success                    = FALSE;

    //  Set maximum input block size for compressor.
    DWORD BlockSize                    = BLOCK_SIZE;

    COMPRESS_ALLOCATION_ROUTINES AllocationRoutines;

    //  Init. allocation routines
    AllocationRoutines.Allocate = SimpleAlloc;
    AllocationRoutines.Free = SimpleFree;
    AllocationRoutines.UserContext = NULL;

    *CompressedSize = 0;
    *OutputData = NULL;

    //  Create a LZMS compressor and set to Block mode.
    Success = CreateCompressor(
        COMPRESS_ALGORITHM_LZMS|COMPRESS_RAW,   //  Compression algorithm is LZMS
        &AllocationRoutines,                    //  Optional Memory allocation routines
        &Compressor);                           //  Handle

    if (!Success)
    {
        wprintf(L"Cannot create compressor handle: %d\n", GetLastError());
        goto done;
    }

    Success = SetCompressorInformation(
        Compressor,
        COMPRESS_INFORMATION_CLASS_BLOCK_SIZE,  //  Set block size for LZMS compressor
        &BlockSize,                             //  Block size information
        sizeof(DWORD));                         //  Information size

    if (!Success)
    {
        wprintf(L"Set compressor information error: %d\n", GetLastError());
        goto done;
    }     

    //  Query max. possible compressed block size.
    Success = Compress(
        Compressor,                 //  Compressor Handle
        NULL,                       //  Input buffer, Uncompressed data
        BlockSize,                  //  Uncompressed block size
        NULL,                       //  Compressed Buffer
        0,                          //  Compressed Buffer size
        &CompressedBlockSize);      //  Compressed Data size

    if (!Success)
    {
        DWORD ErrorCode = GetLastError();
        if (ErrorCode != ERROR_INSUFFICIENT_BUFFER)
        {
            wprintf(L"Query compressed block size error: %d\n", GetLastError());
            goto done;
        }
    }

    //  Get max. possible size for compressed data for given input data    
    OutputDataSize = (InputSize % BLOCK_SIZE == 0) ? 0 : 1;
    OutputDataSize += InputSize / BLOCK_SIZE;
    OutputDataSize = OutputDataSize * (META_DATA_SIZE + CompressedBlockSize) + sizeof(ULONG);

    *OutputData = (PBYTE)malloc(OutputDataSize);
    if (!*OutputData)
    {
        wprintf(L"Cannot allocate memory for compressed buffer.\n");
        Success = FALSE;
        goto done;       
    }

    //  Write uncompressed size to beginning of the buffer
    *((ULONG UNALIGNED *)*OutputData) = InputSize;
    OutputSoFar = sizeof(ULONG);

    //  Compress data block by block.
    while (ProcessedSoFar < InputSize)
    {
        if (OutputSoFar + META_DATA_SIZE >= OutputDataSize) 
        {
            Success = FALSE;
            wprintf(L"Compression fails.\n");
            goto done;
        }                      

        CurrentBlockSize = 
            (InputSize - ProcessedSoFar < BlockSize) ?
            (InputSize - ProcessedSoFar) : BlockSize;

        //  Compress a block.
        Success = Compress(
            Compressor,                                     //  Compressor Handle
            InputData + ProcessedSoFar,                     //  Uncompressed data
            CurrentBlockSize,                               //  Uncompressed data size
            *OutputData + OutputSoFar + META_DATA_SIZE,     //  Start of compressed buffer
            OutputDataSize - OutputSoFar - META_DATA_SIZE,  //  Compressed block size
            &CompressedDataSize);                           //  Compressed data size

        if (!Success) 
        {
            wprintf(L"Compression fails: %d\n", GetLastError());
            goto done;
        }

        //  Write block information to output data.
        *((ULONG UNALIGNED *)(*OutputData + OutputSoFar)) = (ULONG)CompressedDataSize;
        OutputSoFar += sizeof(ULONG);
        *((ULONG UNALIGNED *)(*OutputData + OutputSoFar)) = (ULONG)CurrentBlockSize;
        OutputSoFar += sizeof(ULONG);
        OutputSoFar += CompressedDataSize;

        ProcessedSoFar += CurrentBlockSize;
    }    
    
    
    if (OutputSoFar > UINT32_MAX)
    {
        *CompressedSize = 0;
        Success = FALSE;
    }
    else
    {
        *CompressedSize = static_cast<DWORD>(OutputSoFar);
    }

done:
    if (Compressor != NULL)
    {
        CloseCompressor(Compressor);
    }
    return Success;
}

void wmain(_In_ int argc, _In_ WCHAR *argv[])
{
    PBYTE CompressedBuffer          = NULL;
    PBYTE InputBuffer               = NULL;
    HANDLE InputFile                = INVALID_HANDLE_VALUE;
    HANDLE CompressedFile           = INVALID_HANDLE_VALUE;    
    BOOL DeleteTargetFile           = TRUE;
    BOOL Success;
    SIZE_T CompressedDataSize;
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
        wprintf(L"Cannot allocate memory for input buffer.\n");
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

    StartTime = GetTickCount64();

    //  Call BlockModeCompress() again to do compression.    
    Success = BlockModeCompress(        
        InputBuffer,            //  Input buffer, Uncompressed data
        InputFileSize,          //  Uncompressed data size
        &CompressedBuffer,      //  Compressed Buffer
        &CompressedDataSize);   //  Compressed Data size

    if (!Success)
    {
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
        wprintf(L"Cannot write compressed data to file: %d\n", GetLastError());
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



<span data-ttu-id="b30c1-124">Im folgenden Beispiel wird die Datei Dekomprimierung mithilfe der Komprimierungs-API im Block Modus veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b30c1-124">The following demonstrates file decompression using the Compression API in block mode.</span></span>


```C++
#include <Windows.h>
#include <stdio.h>
#include <compressapi.h>

#define META_DATA_SIZE (2 * sizeof(ULONG))

PVOID SimpleAlloc(PVOID Context, SIZE_T Size)
{
    UNREFERENCED_PARAMETER(Context);
    return malloc(Size);
}

VOID SimpleFree(PVOID Context, PVOID Memory)
{
    UNREFERENCED_PARAMETER(Context);
    if (Memory != NULL)
    {
        free(Memory);
    }
    return;
}

BOOL BlockModeDecompress(
    _In_ PBYTE InputData, 
    _In_ DWORD InputSize, 
    _Deref_out_opt_ PBYTE *OutputData, 
    _Out_ DWORD *DecompressedSize
    )
{
    DECOMPRESSOR_HANDLE Decompressor    = NULL;
    DWORD ProcessedSoFar                = 0;    
    DWORD CompressedBlockSize           = 0;
    DWORD UncompressedBlockSize         = 0;
    DWORD DecompressedSoFar             = 0;
    DWORD OutputDataSize                = 0;
    BOOL Success                        = FALSE;

    COMPRESS_ALLOCATION_ROUTINES AllocationRoutines;

    //  Init. allocation routines
    AllocationRoutines.Allocate = SimpleAlloc;
    AllocationRoutines.Free = SimpleFree;
    AllocationRoutines.UserContext = NULL;

    *DecompressedSize = 0;
    *OutputData = NULL;

    //  Create a LZMS decompressor and set to Block mode.
    Success = CreateDecompressor(
        COMPRESS_ALGORITHM_LZMS|COMPRESS_RAW,   //  Compression algorithm is LZMS
        &AllocationRoutines,                    //  Memory allocation routines
        &Decompressor);                         //  handle

    if (!Success)
    {
        wprintf(L"Cannot create decompressor handle: %d\n", GetLastError());
        goto done;
    }

    //  Read uncompressed size
    ProcessedSoFar = 0;
    OutputDataSize = *((ULONG UNALIGNED *)(InputData + ProcessedSoFar));
    ProcessedSoFar += sizeof(ULONG);

    *OutputData = (PBYTE)malloc(OutputDataSize);
    if (!*OutputData)
    {
        wprintf(L"Cannot allocate memory for uncompressed buffer.\n");
        Success = FALSE;
        goto done;
    }  

    //  Decompress data block by block.
    while (ProcessedSoFar < InputSize)
    {
        if (ProcessedSoFar + META_DATA_SIZE > InputSize)
        {
            Success = FALSE;
            wprintf(L"Data corrupt.\n");
            goto done;     
        }

        //  Read block information.
        CompressedBlockSize = *((ULONG UNALIGNED *)(InputData + ProcessedSoFar));
        ProcessedSoFar += sizeof(ULONG);
        UncompressedBlockSize = *((ULONG UNALIGNED *)(InputData + ProcessedSoFar));
        ProcessedSoFar += sizeof(ULONG);

        if (ProcessedSoFar + CompressedBlockSize > InputSize)
        {
            Success = FALSE;
            wprintf(L"Data corrupt.\n");
            goto done;     
        }

        if (DecompressedSoFar + UncompressedBlockSize > OutputDataSize)
        {
            Success = FALSE;
            wprintf(L"Output buffer not enough to hold decompressed data.\n");
            goto done;     
        }

        //  Decompress a block
        Success = Decompress(
            Decompressor,                   //  Decompressor Handle
            InputData + ProcessedSoFar,     //  Compressed data
            CompressedBlockSize,            //  compressed data size
            *OutputData + DecompressedSoFar, //  Start of decompressed buffer
            UncompressedBlockSize,          //  Uncompressed block size
            NULL);                          //  Decompressed data size
        if (!Success) 
        {
            wprintf(L"Decompression failure: %d\n", GetLastError());
            goto done;
        }
        ProcessedSoFar += CompressedBlockSize;
        DecompressedSoFar += UncompressedBlockSize;
    }

    *DecompressedSize = DecompressedSoFar;

done:
    if (Decompressor != NULL)
    {
        CloseDecompressor(Decompressor);
    }
    return Success;
}

void wmain(_In_ int argc, _In_ WCHAR *argv[])
{       
    PBYTE CompressedBuffer              = NULL;
    PBYTE DecompressedBuffer            = NULL;
    HANDLE InputFile                    = INVALID_HANDLE_VALUE;
    HANDLE DecompressedFile             = INVALID_HANDLE_VALUE;    
    BOOL DeleteTargetFile               = TRUE;    
    BOOL Success;
    DWORD DecompressedDataSize;
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

    //  Allocate memory for compressed content.
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
            
    StartTime = GetTickCount64();

    //  Decompress data and write data to DecompressedBuffer.
    Success = BlockModeDecompress(        
        CompressedBuffer,           //  Compressed data
        InputFileSize,              //  Compressed data size
        &DecompressedBuffer,        //  Decompressed buffer        
        &DecompressedDataSize);     //  Decompressed data size

    if (!Success)
    {
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



<span data-ttu-id="b30c1-125">Eine Anwendung, die den Puffer-oder Block Modus verwendet, kann die Speicher Belegung anpassen, die von der Komprimierungs-API verwendet wird, wenn Sie " [**kreatecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) " oder " [**kreatedekompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor)" aufruft</span><span class="sxs-lookup"><span data-stu-id="b30c1-125">An application using buffer or block mode has the option to customize the memory allocation used by the Compression API when it calls [**CreateCompressor**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) or [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor).</span></span> <span data-ttu-id="b30c1-126">Im Block Modus muss die Anwendung Komprimierungs Block Informationen verarbeiten, z. b. die komprimierte Datengröße und die unkomprimierte Datengröße. andernfalls kann [**dekomprimieren**](/windows/desktop/api/compressapi/nf-compressapi-decompress) die Informationen nicht dekomprimieren.</span><span class="sxs-lookup"><span data-stu-id="b30c1-126">In block mode, the application must handle compression block information, such as compressed data size and uncompressed data size, otherwise [**Decompress**](/windows/desktop/api/compressapi/nf-compressapi-decompress) will be unable to decompress the information.</span></span>

<span data-ttu-id="b30c1-127">Der folgende Code Ausschnitt zeigt eine einfache angepasste Zuordnungs Routine.</span><span class="sxs-lookup"><span data-stu-id="b30c1-127">The following snippet shows a simple customized allocation routine.</span></span>


```C++
PVOID SimpleAlloc(PVOID Context, SIZE_T Size)
{
return malloc(Size);
}

VOID SimpleFree(PVOID Context, PVOID Memory)
{
if (Memory != NULL)
{
        free(Memory);
}
return;
}

//  Init. allocation routines
AllocationRoutines.Allocate = SimpleAlloc;
AllocationRoutines.Free = SimpleFree;
AllocationRoutines.UserContext = NULL;
```



 

 



