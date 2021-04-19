---
description: Jeder Analyse Punkt verfügt über ein bezeichnertag, sodass Sie effizient zwischen den verschiedenen Arten von Analyse Punkten unterscheiden können, ohne die benutzerdefinierten Daten im Analyse Punkt untersuchen zu müssen.
ms.assetid: d02a2f50-d374-4149-bc04-49b7db052f62
title: Analyse Punkt Tags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a53b65034347e2a2c07afcd6c1f03e31f73cef7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350379"
---
# <a name="reparse-point-tags"></a>Analyse Punkt Tags

Jeder Analyse Punkt verfügt über ein bezeichnertag, sodass Sie effizient zwischen den verschiedenen Arten von Analyse Punkten unterscheiden können, ohne die benutzerdefinierten Daten im Analyse Punkt untersuchen zu müssen. Das System verwendet eine Reihe von vordefinierten Tags und einen für Microsoft reservierten Bereich von Tags. Wenn Sie einen der reservierten Tags verwenden, wenn Sie einen Analyse Punkt festlegen, schlägt der Vorgang fehl. Tags, die nicht in diesen Bereichen enthalten sind, sind nicht reserviert und sind für Ihre Anwendung verfügbar.

Wenn Sie einen Analyse Punkt festlegen, müssen Sie die Daten markieren, die im Analyse Punkt platziert werden sollen. Nachdem der Analyse Punkt festgelegt wurde, schlägt ein neuer Set-Vorgang fehl, wenn das Tag für die neuen Daten nicht mit dem Tag für die vorhandenen Daten identisch ist. Wenn die Tags Stimmen, überschreibt der Set-Vorgang den vorhandenen Analyse Punkt.

Um das Analyse Punkt-Tag abzurufen, verwenden Sie die [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) -Funktion. Wenn das Element **dwfileattribute** das Attribut "File Attribute Analyse **\_ \_ \_ Point** " enthält, gibt das **dwReserved0** -Element den Analyse Punkt an.

## <a name="tag-contents"></a>Taginhalt

Analyse Tags werden als **DWORD** -Werte gespeichert. Die Bits definieren bestimmte Attribute, wie im folgenden Diagramm dargestellt.

``` syntax
   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
  +-+-+-+-+-----------------------+-------------------------------+
  |M|R|N|R|     Reserved bits     |      Reparse tag value        |
  +-+-+-+-+-----------------------+-------------------------------+
```

Die unteren 16 Bits bestimmen die Art des Analyse Punkts. Die hohen 16 Bits verfügen über 12 Bits, die für die zukünftige Verwendung reserviert sind, und 4 Bits, die bestimmte Attribute der Tags und die durch den Analyse Punkt dargestellten Daten kennzeichnen. In der folgenden Tabelle werden diese Bits beschrieben.



| bit | BESCHREIBUNG                                                                                                  |
|-----|--------------------------------------------------------------------------------------------------------------|
| M   | Microsoft-Bit. Wenn dieses Bit festgelegt ist, befindet sich das Tag im Besitz von Microsoft. Alle anderen Tags müssen für dieses Bit 0 (null) verwenden. |
| R   | Bleiben muss für alle nicht-Microsoft-Tags NULL sein.                                                           |
| N   | Name Ersatz Zeichen Bit. Wenn dieses Bit festgelegt ist, stellt die Datei oder das Verzeichnis eine andere benannte Entität im System dar. |



 

Die folgenden Makros sind zur Unterstützung beim Testen von Tags vorhanden:

-   [**Isanalyse-tagmicrosoft**](/windows/desktop/api/Winnt/nf-winnt-isreparsetagmicrosoft)
-   [**Isreparsetagnamesurrogate**](/windows/desktop/api/Winnt/nf-winnt-isreparsetagnamesurrogate)

Jedes Makro gibt einen Wert ungleich NULL zurück, wenn das zugeordnete Bit festgelegt ist.

Es folgen die vordefinierten Analyse Tagwerte von Microsoft. Sie sind in "Winnt. h" definiert:

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

Um die Eindeutigkeit von Tags sicherzustellen, bietet Microsoft einen Mechanismus zum Verteilen neuer Tags. Weitere Informationen finden Sie im [IFS-Kit (Installable File System, installier bares Datei System)](https://www.microsoft.com/whdc/devtools/ifskit/reparse.mspx).

 

 



