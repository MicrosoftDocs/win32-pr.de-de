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
# <a name="walking-a-buffer-of-change-journal-records"></a>Durchlaufen eines Puffers von Änderungs Journal Datensätzen

Die Steuerungs Codes, die die Änderungs Journal Datensätze der Update Sequenznummer (Update Sequence Number, US-Journal), das [**esctl- \_ Lese \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) -und das esctl-enumerationsdataset zurückgeben, geben ähnliche Daten im Ausgabepuffer zurück. [**\_ \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) Beide geben eine "US-v", gefolgt von keinem oder mehreren Änderungs Journal Datensätzen zurück [**\_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) [**\_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3)

Das Ziel Volume für die Vorgänge der betriebsbereit Stellung muss Refs oder NTFS 3,0 oder höher sein. Wenn Sie die NTFS-Version eines Volumes abrufen möchten, öffnen Sie eine Eingabeaufforderung mit Administrator Rechten, und führen Sie den folgenden Befehl aus:

FSUtil.exe "f": " **NTF-FO** *X * * *:**

Dabei ist *X* der Laufwerk Buchstabe des Volumes.

In der folgenden Liste finden Sie Informationen zum Aufrufen von Änderungs Journal Datensätzen:

-   Verwenden Sie [**FSCTL \_ Enum- \_ Daten- \_ Daten**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) Sätze, um eine Auflistung (Enumeration) aller Datensätze von Änderungs Journal zwischen zwei-US-Dateien zu erhalten.
-   Verwenden [**Sie das FSCTL- \_ gelesene Daten \_ \_ Journal**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) , um selektiver zu sein, z. b. die Auswahl bestimmter Gründe für Änderungen oder die Rückgabe beim Schließen einer Datei.

> [!Note]  
> Bei beiden Vorgängen wird nur die Teilmenge der Änderungs Journal Datensätze zurückgegeben, die die angegebenen Kriterien erfüllen.

 

Die USN, die als erstes Element im Ausgabepuffer zurückgegeben wird, ist die USN der nächsten Datensatznummer, die abgerufen werden soll. Verwenden Sie diesen Wert, um das Lesen von Datensätzen aus der End-Grenze fortzusetzen.

Das **Dateiname** -Element von " [**US- \_ Datensatz \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) " oder " [**US- \_ Datensatz \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) " enthält den Namen der Datei, für die der betreffende Datensatz gilt. Der Dateiname variiert in der Länge, d. & # amp; a **\_ \_** **\_ \_** Der erste Member, **RecordLength**, ist die Länge der Struktur (einschließlich des Datei namens) in Bytes.

Wenn Sie mit dem **filename** -Element von " [**RN \_ Record \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) " und " [**RN \_ Record \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) -Strukturen" arbeiten, gehen Sie nicht davon aus, dass der Dateiname ein nach gestelltes Trennzeichen " \\ 0" enthält. Verwenden Sie zum Bestimmen der Länge des Datei namens das dateinameitth-Member. 

Im folgenden Beispiel wird ein [**Lese- \_ /Lese-Journal \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) von "f" aufgerufen, und der Puffer der Änderungs Journal Datensätze, die vom Vorgang zurückgegeben werden


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



Die Größe eines beliebigen Datensatzes in Byte, der von einem [**compun- \_ Datensatz \_ v2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) oder einer [**\_ Daten Satz- \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) -Struktur des US-Datensatzes angegeben wird, ist höchstens mit `((MaxComponentLength - 1) * Width) + Size` *maxcomponentlength* die maximale Länge in Zeichen für den Namen der Daten Satz Datei. Die Breite ist die Größe eines breit Zeichens, und die Größe *entspricht der* Größe der Struktur.

Um die maximale Länge zu erhalten, rufen Sie die [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) -Funktion auf, und überprüfen Sie den Wert, auf den der *lpmaximumcomponentlength* -Parameter verweist. Subtrahieren Sie einen von *maxcomponentlength* , um die Tatsache zu berücksichtigen, dass die Definition des Daten [**\_ Satzes**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) und des Daten [**\_ Satzes \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) ein Zeichen des Datei namens enthält.

In der Programmiersprache C ist die größtmögliche Daten Satz Größe wie folgt:

`(MaxComponentLength - 1) * sizeof(WCHAR) + sizeof(USN_RECORD)`

 

 
