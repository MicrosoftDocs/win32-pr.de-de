---
description: Der Netzwerkmonitor Binary Large Object (BLOB) ist eine generische Datenstruktur, die Konfigurations-und Speicherort Informationen von Netzwerkschnittstellenkarten (NICs) enthält.
ms.assetid: 910bf929-aa89-434d-83c3-07c80c627405
title: BlobNetzwerkmonitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce6dd6ca8643eabe8ab49387c0ef39eb49b6f2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354029"
---
# <a name="network-monitor-blobs"></a>BlobNetzwerkmonitor

Der Netzwerkmonitor Binary Large Object (BLOB) ist eine generische Datenstruktur, die Konfigurations-und Speicherort Informationen von Netzwerkschnittstellenkarten (NICs) enthält. Verwenden Sie blobfunktionen zum Darstellen von NICs und zum Filtern von Einträgen in einer Liste von NICs. Blobdaten können auch anwendungsspezifische Daten enthalten, ohne dass sich dies auf die anderen Daten auswirkt, die Sie enthalten. Die BLOB-Implementierung ist für alle Ebenen, die auf BLOBs mit BLOB-APIs zugreifen müssen, nicht transparent.

## <a name="blob-structure"></a>BLOB-Struktur

Ein BLOB kann als hierarchische Struktur angesehen werden, die zum Festlegen von Zeichen folgen verwendet wird. Diese Struktur verfügt über drei Ebenen: "Owner", "Category" und "Tag". Owner ist eine Zeichenfolge, die im allgemeinen angibt, wer einen Eintrag liest. Die Kategorie ist auch eine Zeichenfolge, die eine allgemeine funktionale Gruppierung von Tags unter dem Besitzer angibt. Das-Tag ist der tatsächliche Name des Eintrags.

Zu den strukturellen Merkmalen von blobden zählen folgende:

-   BLOB-Hilfsprogramme innerhalb eines Prozesses werden von einem in jedem BLOB integrierten Mutex voneinander geschützt.
-   Jedes BLOB verfügt über eine interne Versionsnummer, sodass die Hilfsprogramme sowohl das vorhandene als auch das zukünftige BLOB-Formular verarbeiten können. Versions Konflikte können auftreten, wenn Sie ein BLOB über einen Remote Prozedur Rückruf an einen anderen Computer senden.
-   Das BLOB selbst ist ein Zeiger auf eine leere. Beachten Sie, dass Anwendungen dem **Konstanten** -Modifizierer blobzuordnungen zuordnen sollten, um zu vermeiden, dass der Inhalt geändert wird.
-   Jeder der Kenn Zeichner und ihre Werte sind Zeichen folgen. Beachten Sie, dass die von **GetString** -Funktionen zurückgegebenen Zeichen folgen tatsächlich Zeiger auf das BLOB sind und nicht geändert werden sollten. Aus diesem Grund müssen diese Zeichen folgen als "Konstante **char** _ px *" angegeben werden \_ , damit Anwendungen nicht versehentlich geändert werden.

Im Allgemeinen wird der Aufrufer von allen Parametern mit dem Konstanten Kenn Zeichner ermutigt, das Ändern der Werte zu unterbinden, anstatt zu verhindern, dass die **Hilfsfunktionen** diese ändern. Tatsächlich ändern die Hilfsfunktionen diese Werte in der Regel.

 

 



