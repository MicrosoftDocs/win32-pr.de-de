---
description: Zurückgeben von Änderungsjournaldatensätzen, die die angegebenen Kriterien erfüllen.
ms.assetid: 8946adb5-da47-4711-8800-86f323081c4c
title: Durchgehen eines Puffers von Änderungsjournaldatensätzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9242d671cedfb5c9ef2b5fa836e29c455d09a9e1287b1ed035712f49c6c7d627
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830150"
---
# <a name="walking-a-buffer-of-change-journal-records"></a>Durchgehen eines Puffers von Änderungsjournaldatensätzen

Die Steuerungscodes, die Änderungsjournaldatensätze der Updatesequenznummer (USN), [**FSCTL \_ READ \_ USN \_ JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) und [**FSCTL \_ ENUM \_ USN \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data)zurückgeben, geben ähnliche Daten im Ausgabepuffer zurück. Beide geben eine USN gefolgt von null oder mehr Änderungsjournaldatensätzen zurück, die jeweils in einer [**USN \_ RECORD \_ V2-**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) oder [**USN \_ RECORD \_ V3-Struktur**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) enthalten sind.

Das Zielvolume für USN-Vorgänge muss ReFS oder NTFS 3.0 oder höher sein. Um die NTFS-Version eines Volumes abzurufen, öffnen Sie eine Eingabeaufforderung mit Administratorzugriffsrechten, und führen Sie den folgenden Befehl aus:

**FSUtil.exe FSInfo NTFSInfo** *X::**

wobei *X* der Laufwerkbuchstabe des Volumes ist.

In der folgenden Liste werden Möglichkeiten zum Abrufen von Änderungsjournaldatensätzen aufgeführt:

-   Verwenden Sie [**FSCTL \_ ENUM \_ USN \_ DATA,**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) um eine Auflistung (Enumeration) aller Änderungsjournaldatensätze zwischen zwei USNs abzurufen.
-   Verwenden Sie [**FSCTL \_ READ \_ USN \_ JOURNAL,**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) um selektiver zu sein, z. B. das Auswählen bestimmter Gründe für Änderungen oder das Zurückgeben, wenn eine Datei geschlossen wird.

> [!Note]  
> Beide Vorgänge geben nur die Teilmenge der Änderungsjournaldatensätze zurück, die die angegebenen Kriterien erfüllen.

 

Die als erstes Element im Ausgabepuffer zurückgegebene USN ist die USN der nächsten abzurufenden Datensatznummer. Verwenden Sie diesen Wert, um datensätze von der Endgrenze weiterzulesen.

Das **FileName-Element** von [**USN \_ RECORD \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) oder [**USN RECORD \_ \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) enthält den Namen der Datei, für die der betreffende Datensatz gilt. Der Dateiname variiert je nach Länge, sodass **USN \_ RECORD \_ V2** und **USN \_ RECORD \_ V3** Strukturen variabler Länge sind. Ihr erster Member, **RecordLength,** ist die Länge der Struktur (einschließlich des Dateinamens) in Bytes.

Wenn Sie mit dem **FileName-Member** der [**USN \_ RECORD \_ V2-**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) und [**USN \_ RECORD \_ V3-Strukturen**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) arbeiten, gehen Sie nicht davon aus, dass der Dateiname ein nachgestelltes \\ '0'-Trennzeichen enthält. Um die Länge des Dateinamens zu bestimmen, verwenden Sie den **FileNameLength-Member.**

Das folgende Beispiel ruft [**FSCTL \_ READ \_ USN \_ JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) auf und durchläuft den Puffer der Änderungsjournaldatensätze, die der Vorgang zurückgibt.


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



Die Größe eines datensatzes, der durch eine [**USN \_ RECORD \_ V2-**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) oder [**USN \_ RECORD \_ V3-Struktur**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) angegeben wird, ist höchstens in `((MaxComponentLength - 1) * Width) + Size` Bytes, wobei *MaxComponentLength* die maximale Länge in Zeichen des Datensatzdateinamens ist. Die Breite ist die Größe eines Breitzeichens, und die *Größe* entspricht der Größe der -Struktur.

Rufen Sie zum Abrufen der maximalen Länge die [**GetVolumeInformation-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) auf, und untersuchen Sie den Wert, auf den der *lpMaximumComponentLength-Parameter* zeigt. Subtrahieren Sie eine von *MaxComponentLength,* um die Tatsache zu berücksichtigen, dass die Definition von [**USN \_ RECORD**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) und [**USN \_ RECORD \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) ein Zeichen des Dateinamens enthält.

In der Programmiersprache C ist die größtmögliche Datensatzgröße wie folgt:

`(MaxComponentLength - 1) * sizeof(WCHAR) + sizeof(USN_RECORD)`

 

 
