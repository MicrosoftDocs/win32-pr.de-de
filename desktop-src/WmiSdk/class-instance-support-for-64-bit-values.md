---
description: Stellt Einschränkungen für die Verwendung von 64-Bit-Werten als Teil eines Pfads bereit.
ms.assetid: 63f4f6c5-7803-425d-912f-bb1dd716e617
ms.tgt_platform: multiple
title: Unterstützung von Klassen Instanzen für 64-Bit-Werte
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 80f8a48f253cf2ef1902938ca6c54d01404b8466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373183"
---
# <a name="class-instance-support-for-64-bit-values"></a>Unterstützung von Klassen Instanzen für 64-Bit-Werte

Sie können einen 64-Bit-Schlüsselwert als Teil eines Pfads verwenden, wobei die folgenden Einschränkungen gelten:

-   Solange der 32-Bit-Bereich nicht überschritten wird, können Sie Werte aus dem Schlüssel wie eine 32-Bit-Eigenschaft zuweisen und abrufen.
-   Nachdem Sie den ganzzahligen Wert 0x7FFFFFFF (für signierte Typen), 0x80000000 (bei nicht signierten Typen) oder 32 Bits überschritten haben, müssen Sie Anführungszeichen verwenden.
-   Der einzige gültige Pfad für einen 64-Bit-Wert befindet sich in den **\_ \_ RelPath** -oder **\_ \_ path** -Eigenschaften der-Instanz. Daher unterstützt WMI die hexadezimale Notation für den entsprechenden Wert nicht.
-   Wenn WMI den Instanzschlüssel als negative Zahl aufzeichnet, müssen Sie die ursprüngliche Nummer verwenden, um die Instanz abzurufen.

Die Abfrage Semantik ist nicht betroffen und verhält sich wie erwartet. Dieses Verhalten wirkt sich nur auf die Vorgänge "Objekt Pfad", " [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)" und " [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) " aus.

Das folgende Beispiel zeigt, dass Klassen Instanzen 64-Bit-Schlüsselwerte aufweisen können.

``` syntax
class MyBig
{
  [key] sint64 k;
  sint64 p;
};

instance of MyBig
{
  k = 2;
  p = 3;
};
```

 

 



