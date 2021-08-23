---
description: Jeder Auswertungspunkt verfügt über ein Bezeichnertag, sodass Sie effizient zwischen den verschiedenen Typen von Überprüfungspunkten unterscheiden können, ohne die benutzerdefinierten Daten im Auswertungspunkt untersuchen zu müssen.
ms.assetid: d02a2f50-d374-4149-bc04-49b7db052f62
title: Punkttags für die Wiederholung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b31d4a1765266295b85c95c0955ae9c51faeb34ae07f3af48288a17a50f2166
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015188"
---
# <a name="reparse-point-tags"></a>Punkttags für die Wiederholung

Jeder Auswertungspunkt verfügt über ein Bezeichnertag, sodass Sie effizient zwischen den verschiedenen Typen von Überprüfungspunkten unterscheiden können, ohne die benutzerdefinierten Daten im Auswertungspunkt untersuchen zu müssen. Das System verwendet eine Reihe vordefinierter Tags und einen Bereich von Tags, die für Microsoft reserviert sind. Wenn Sie beim Festlegen eines Wiederholungspunkts eines der reservierten Tags verwenden, schlägt der Vorgang fehl. Tags, die nicht in diesen Bereichen enthalten sind, sind nicht reserviert und für Ihre Anwendung verfügbar.

Wenn Sie einen Auswertungspunkt festlegen, müssen Sie die Daten markieren, die auf dem Auswertungspunkt platziert werden sollen. Nachdem der Auswertungspunkt eingerichtet wurde, schlägt ein neuer Set-Vorgang fehl, wenn das Tag für die neuen Daten nicht mit dem Tag für die vorhandenen Daten übereinstimmt. Wenn die Tags übereinstimmen, überschreibt der Set-Vorgang den vorhandenen Wiederholungspunkt.

Verwenden Sie die [**FindFirstFile-Funktion,**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) um das Analysepunkttag abzurufen. Wenn das **dwFileAttributes-Element** das **FILE ATTRIBUTE \_ \_ REPARSE \_ POINT-Attribut** enthält, gibt das **dwReserved0-Element** den Neusynpunkt an.

## <a name="tag-contents"></a>Taginhalt

Reparse-Tags werden als **DWORD-Werte** gespeichert. Die Bits definieren bestimmte Attribute, wie im folgenden Diagramm dargestellt.

``` syntax
   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
  +-+-+-+-+-----------------------+-------------------------------+
  |M|R|N|R|     Reserved bits     |      Reparse tag value        |
  +-+-+-+-+-----------------------+-------------------------------+
```

Die niedrigen 16 Bits bestimmen die Art des Wiederholungspunkts. Die hohen 16 Bits verfügen über 12 Bits für die zukünftige Verwendung und 4 Bits, die bestimmte Attribute der Tags und die durch den Auswertungspunkt dargestellten Daten kennzeichnen. In der folgenden Tabelle werden diese Bits beschrieben.



| bit | BESCHREIBUNG                                                                                                  |
|-----|--------------------------------------------------------------------------------------------------------------|
| M   | Microsoft-Bit. Wenn dieses Bit festgelegt ist, befindet sich das Tag im Besitz von Microsoft. Alle anderen Tags müssen 0 (null) für dieses Bit verwenden. |
| R   | Reserviert; muss für alle Nicht-Microsoft-Tags 0 (null) sein.                                                           |
| N   | Name des Ersatzzeichenbits. Wenn dieses Bit festgelegt ist, stellt die Datei oder das Verzeichnis eine andere benannte Entität im System dar. |



 

Die folgenden Makros sind vorhanden, um Tags zu testen:

-   [**IsReparseTagMicrosoft**](/windows/desktop/api/Winnt/nf-winnt-isreparsetagmicrosoft)
-   [**IsReparseTagNameSurrogate**](/windows/desktop/api/Winnt/nf-winnt-isreparsetagnamesurrogate)

Jedes Makro gibt einen Wert ungleich 0 (null) zurück, wenn das zugeordnete Bit festgelegt ist.

Im Folgenden sind die vordefinierten Tagwerte für die Analysen von Microsoft angegeben. sie werden in WinNT.h definiert:

-   **IO_REPARSE_TAG_AF_UNIX**
-   **IO_REPARSE_TAG_APPEXECLINK**
-   **IO_REPARSE_TAG_CLOUD**
-   **IO_REPARSE_TAG_CLOUD_1**
-   **IO_REPARSE_TAG_CLOUD_2**
-   **IO_REPARSE_TAG_CLOUD_3**
-   **IO_REPARSE_TAG_CLOUD_4**
-   **IO_REPARSE_TAG_CLOUD_5**
-   **IO_REPARSE_TAG_CLOUD_6**
-   **IO_REPARSE_TAG_CLOUD_7**
-   **IO_REPARSE_TAG_CLOUD_8**
-   **IO_REPARSE_TAG_CLOUD_9**
-   **IO_REPARSE_TAG_CLOUD_A**
-   **IO_REPARSE_TAG_CLOUD_B**
-   **IO_REPARSE_TAG_CLOUD_C**
-   **IO_REPARSE_TAG_CLOUD_D**
-   **IO_REPARSE_TAG_CLOUD_E**
-   **IO_REPARSE_TAG_CLOUD_F**
-   **IO_REPARSE_TAG_CLOUD_MASK**
-   **IO_REPARSE_TAG_CSV**
-   **IO_REPARSE_TAG_DEDUP**
-   **IO_REPARSE_TAG_DFS**
-   **IO_REPARSE_TAG_DFSR**
-   **IO_REPARSE_TAG_FILE_PLACEHOLDER**
-   **IO_REPARSE_TAG_GLOBAL_REPARSE**
-   **IO_REPARSE_TAG_HSM**
-   **IO_REPARSE_TAG_HSM2**
-   **IO_REPARSE_TAG_MOUNT_POINT**
-   **IO_REPARSE_TAG_NFS**
-   **IO_REPARSE_TAG_ONEDRIVE**
-   **IO_REPARSE_TAG_PROJFS**
-   **IO_REPARSE_TAG_PROJFS_TOMBSTONE**
-   **IO_REPARSE_TAG_SIS**
-   **IO_REPARSE_TAG_STORAGE_SYNC**
-   **IO_REPARSE_TAG_SYMLINK**
-   **IO_REPARSE_TAG_UNHANDLED**
-   **IO_REPARSE_TAG_WCI**
-   **IO_REPARSE_TAG_WCI_1**
-   **IO_REPARSE_TAG_WCI_LINK**
-   **IO_REPARSE_TAG_WCI_LINK_1**
-   **IO_REPARSE_TAG_WCI_TOMBSTONE**
-   **IO_REPARSE_TAG_WIM**
-   **IO_REPARSE_TAG_WOF**

Um die Eindeutigkeit von Tags sicherzustellen, stellt Microsoft einen Mechanismus zum Verteilen neuer Tags bereit. Weitere Informationen finden Sie unter [Installable File System (IFS) Kit](https://www.microsoft.com/whdc/devtools/ifskit/reparse.mspx).

 

 



