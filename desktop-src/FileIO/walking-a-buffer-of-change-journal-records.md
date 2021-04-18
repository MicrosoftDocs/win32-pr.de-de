---
description: Zurückgeben von Änderungs Journal Datensätzen, die bestimmte Kriterien erfüllen.
ms.assetid: 8946adb5-da47-4711-8800-86f323081c4c
title: Durchlaufen eines Puffers von Änderungs Journal Datensätzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9384316e38c23951849006efc259268a7bdf33df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347445"
---
# <a name="walking-a-buffer-of-change-journal-records"></a><span data-ttu-id="0ca9a-103">Durchlaufen eines Puffers von Änderungs Journal Datensätzen</span><span class="sxs-lookup"><span data-stu-id="0ca9a-103">Walking a Buffer of Change Journal Records</span></span>

<span data-ttu-id="0ca9a-104">Die Steuerungs Codes, die die Änderungs Journal Datensätze der Update Sequenznummer (Update Sequence Number, US-Journal), das [**esctl- \_ Lese \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) -und das esctl-enumerationsdataset zurückgeben, geben ähnliche Daten im Ausgabepuffer zurück. [**\_ \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data)</span><span class="sxs-lookup"><span data-stu-id="0ca9a-104">The control codes that return update sequence number (USN) change journal records, [**FSCTL\_READ\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) and [**FSCTL\_ENUM\_USN\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data), return similar data in the output buffer.</span></span> <span data-ttu-id="0ca9a-105">Beide geben eine "US-v", gefolgt von keinem oder mehreren Änderungs Journal Datensätzen zurück [**\_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) [**\_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3)</span><span class="sxs-lookup"><span data-stu-id="0ca9a-105">Both return a USN followed by zero or more change journal records, each in a [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) or [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) structure.</span></span>

<span data-ttu-id="0ca9a-106">Das Ziel Volume für die Vorgänge der betriebsbereit Stellung muss Refs oder NTFS 3,0 oder höher sein.</span><span class="sxs-lookup"><span data-stu-id="0ca9a-106">The target volume for USN operations must be ReFS or NTFS 3.0 or later.</span></span> <span data-ttu-id="0ca9a-107">Wenn Sie die NTFS-Version eines Volumes abrufen möchten, öffnen Sie eine Eingabeaufforderung mit Administrator Rechten, und führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="0ca9a-107">To obtain the NTFS version of a volume, open a command prompt with Administrator access rights and execute the following command:</span></span>

<span data-ttu-id="0ca9a-108">FSUtil.exe "f": " **NTF-FO** *X \* \* *:**</span><span class="sxs-lookup"><span data-stu-id="0ca9a-108">**FSUtil.exe FSInfo NTFSInfo** *X\*\*\*:*\*</span></span>

<span data-ttu-id="0ca9a-109">Dabei ist *X* der Laufwerk Buchstabe des Volumes.</span><span class="sxs-lookup"><span data-stu-id="0ca9a-109">where *X* is the drive letter of the volume.</span></span>

<span data-ttu-id="0ca9a-110">In der folgenden Liste finden Sie Informationen zum Aufrufen von Änderungs Journal Datensätzen:</span><span class="sxs-lookup"><span data-stu-id="0ca9a-110">The following list identifies ways to get change journal records:</span></span>

-   <span data-ttu-id="0ca9a-111">Verwenden Sie [**FSCTL \_ Enum- \_ Daten- \_ Daten**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) Sätze, um eine Auflistung (Enumeration) aller Datensätze von Änderungs Journal zwischen zwei-US-Dateien zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0ca9a-111">Use [**FSCTL\_ENUM\_USN\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) to get a listing (enumeration) of all change journal records between two USNs.</span></span>
-   <span data-ttu-id="0ca9a-112">Verwenden [**Sie das FSCTL- \_ gelesene Daten \_ \_ Journal**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) , um selektiver zu sein, z. b. die Auswahl bestimmter Gründe für Änderungen oder die Rückgabe beim Schließen einer Datei.</span><span class="sxs-lookup"><span data-stu-id="0ca9a-112">Use [**FSCTL\_READ\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) to be more selective, such as selecting specific reasons for changes or returning when a file is closed.</span></span>

> [!Note]  
> <span data-ttu-id="0ca9a-113">Bei beiden Vorgängen wird nur die Teilmenge der Änderungs Journal Datensätze zurückgegeben, die die angegebenen Kriterien erfüllen.</span><span class="sxs-lookup"><span data-stu-id="0ca9a-113">Both of these operations return only the subset of change journal records that meet the specified criteria.</span></span>

 

<span data-ttu-id="0ca9a-114">Die USN, die als erstes Element im Ausgabepuffer zurückgegeben wird, ist die USN der nächsten Datensatznummer, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0ca9a-114">The USN returned as the first item in the output buffer is the USN of the next record number to be retrieved.</span></span> <span data-ttu-id="0ca9a-115">Verwenden Sie diesen Wert, um das Lesen von Datensätzen aus der End-Grenze fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="0ca9a-115">Use this value to continue reading records from the end boundary forward.</span></span>

<span data-ttu-id="0ca9a-116">Das **Dateiname** -Element von " [**US- \_ Datensatz \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) " oder " [**US- \_ Datensatz \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) " enthält den Namen der Datei, für die der betreffende Datensatz gilt.</span><span class="sxs-lookup"><span data-stu-id="0ca9a-116">The **FileName** member of [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) or [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) contains the name of the file to which the record in question applies.</span></span> <span data-ttu-id="0ca9a-117">Der Dateiname variiert in der Länge, d. & # amp; a **\_ \_** **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="0ca9a-117">The file name varies in length, so **USN\_RECORD\_V2** and **USN\_RECORD\_V3** are variable length structures.</span></span> <span data-ttu-id="0ca9a-118">Der erste Member, **RecordLength**, ist die Länge der Struktur (einschließlich des Datei namens) in Bytes.</span><span class="sxs-lookup"><span data-stu-id="0ca9a-118">Their first member, **RecordLength**, is the length of the structure (including the file name), in bytes.</span></span>

<span data-ttu-id="0ca9a-119">Wenn Sie mit dem **filename** -Element von " [**RN \_ Record \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) " und " [**RN \_ Record \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) -Strukturen" arbeiten, gehen Sie nicht davon aus, dass der Dateiname ein nach gestelltes Trennzeichen " \\ 0" enthält.</span><span class="sxs-lookup"><span data-stu-id="0ca9a-119">When you work with the **FileName** member of [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) and [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) structures, do not assume that the file name contains a trailing '\\0' delimiter.</span></span> <span data-ttu-id="0ca9a-120">Verwenden Sie zum Bestimmen der Länge des Datei namens das dateinameitth-Member. </span><span class="sxs-lookup"><span data-stu-id="0ca9a-120">To determine the length of the file name, use the **FileNameLength** member.</span></span>

<span data-ttu-id="0ca9a-121">Im folgenden Beispiel wird ein [**Lese- \_ /Lese-Journal \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) von "f" aufgerufen, und der Puffer der Änderungs Journal Datensätze, die vom Vorgang zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="0ca9a-121">The following example calls [**FSCTL\_READ\_USN\_JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) and walks the buffer of change journal records that the operation returns.</span></span>


```C++
#include <Windows.h>
#include <WinIoCtl.h>
#include <stdio.h>

#define BUF_LEN 4096

void main()
{
   HANDLE hVol;
   CHAR Buffer[BUF_LEN];

   USN_JOURNAL_DATA JournalData;
   READ_USN_JOURNAL_DATA ReadData = {0, 0xFFFFFFFF, FALSE, 0, 0};
   PUSN_RECORD UsnRecord;  

   DWORD dwBytes;
   DWORD dwRetBytes;
   int I;

   hVol = CreateFile( TEXT("\\\\.\\c:"), 
               GENERIC_READ | GENERIC_WRITE, 
               FILE_SHARE_READ | FILE_SHARE_WRITE,
               NULL,
               OPEN_EXISTING,
               0,
               NULL);

   if( hVol == INVALID_HANDLE_VALUE )
   {
      printf("CreateFile failed (%d)\n", GetLastError());
      return;
   }

   if( !DeviceIoControl( hVol, 
          FSCTL_QUERY_USN_JOURNAL, 
          NULL,
          0,
          &JournalData,
          sizeof(JournalData),
          &dwBytes,
          NULL) )
   {
      printf( "Query journal failed (%d)\n", GetLastError());
      return;
   }

   ReadData.UsnJournalID = JournalData.UsnJournalID;

   printf( "Journal ID: %I64x\n", JournalData.UsnJournalID );
   printf( "FirstUsn: %I64x\n\n", JournalData.FirstUsn );

   for(I=0; I<=10; I++)
   {
      memset( Buffer, 0, BUF_LEN );

      if( !DeviceIoControl( hVol, 
            FSCTL_READ_USN_JOURNAL, 
            &ReadData,
            sizeof(ReadData),
            &Buffer,
            BUF_LEN,
            &dwBytes,
            NULL) )
      {
         printf( "Read journal failed (%d)\n", GetLastError());
         return;
      }

      dwRetBytes = dwBytes - sizeof(USN);

      // Find the first record
      UsnRecord = (PUSN_RECORD)(((PUCHAR)Buffer) + sizeof(USN));  

      printf( "****************************************\n");

      // This loop could go on for a long time, given the current buffer size.
      while( dwRetBytes > 0 )
      {
         printf( "USN: %I64x\n", UsnRecord->Usn );
         printf("File name: %.*S\n", 
                  UsnRecord->FileNameLength/2, 
                  UsnRecord->FileName );
         printf( "Reason: %x\n", UsnRecord->Reason );
         printf( "\n" );

         dwRetBytes -= UsnRecord->RecordLength;

         // Find the next record
         UsnRecord = (PUSN_RECORD)(((PCHAR)UsnRecord) + 
                  UsnRecord->RecordLength); 
      }
      // Update starting USN for next call
      ReadData.StartUsn = *(USN *)&Buffer; 
   }

   CloseHandle(hVol);

}
```



<span data-ttu-id="0ca9a-122">Die Größe eines beliebigen Datensatzes in Byte, der von einem [**compun- \_ Datensatz \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) oder einer [**\_ Daten Satz- \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) -Struktur des US-Datensatzes angegeben wird, ist höchstens mit `((MaxComponentLength - 1) * Width) + Size` *maxcomponentlength* die maximale Länge in Zeichen für den Namen der Daten Satz Datei.</span><span class="sxs-lookup"><span data-stu-id="0ca9a-122">The size in bytes of any record specified by a [**USN\_RECORD\_V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) or [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) structure is at most `((MaxComponentLength - 1) * Width) + Size` where *MaxComponentLength* is the maximum length in characters of the record file name.</span></span> <span data-ttu-id="0ca9a-123">Die Breite ist die Größe eines breit Zeichens, und die Größe *entspricht der* Größe der Struktur.</span><span class="sxs-lookup"><span data-stu-id="0ca9a-123">The width is the size of a wide character, and the *Size* is the size of the structure.</span></span>

<span data-ttu-id="0ca9a-124">Um die maximale Länge zu erhalten, rufen Sie die [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) -Funktion auf, und überprüfen Sie den Wert, auf den der *lpmaximumcomponentlength* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="0ca9a-124">To obtain the maximum length, call the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examine the value pointed to by the *lpMaximumComponentLength* parameter.</span></span> <span data-ttu-id="0ca9a-125">Subtrahieren Sie einen von *maxcomponentlength* , um die Tatsache zu berücksichtigen, dass die Definition des Daten [**\_ Satzes**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) und des Daten [**\_ Satzes \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) ein Zeichen des Datei namens enthält.</span><span class="sxs-lookup"><span data-stu-id="0ca9a-125">Subtract one from *MaxComponentLength* to account for the fact that the definition of [**USN\_RECORD**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) and [**USN\_RECORD\_V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) includes one character of the file name.</span></span>

<span data-ttu-id="0ca9a-126">In der Programmiersprache C ist die größtmögliche Daten Satz Größe wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0ca9a-126">In the C programming language, the largest possible record size is the following:</span></span>

`(MaxComponentLength - 1) * sizeof(WCHAR) + sizeof(USN_RECORD)`

 

 
