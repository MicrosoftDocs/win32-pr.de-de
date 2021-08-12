---
description: Bietet Einschränkungen für die Verwendung von 64-Bit-Werten als Teil eines Pfads.
ms.assetid: 63f4f6c5-7803-425d-912f-bb1dd716e617
ms.tgt_platform: multiple
title: Klasseninstanzunterstützung für 64-Bit-Werte
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ae778bcaad724d727bbda6d6a421ae19c562acdd50c33aa7764bea3b1861273e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556827"
---
# <a name="class-instance-support-for-64-bit-values"></a>Klasseninstanzunterstützung für 64-Bit-Werte

Sie können einen 64-Bit-Schlüsselwert als Teil eines Pfads mit den folgenden Einschränkungen verwenden:

-   Solange Sie den 32-Bit-Bereich nicht überschreiten, können Sie dem Schlüssel Werte wie eine 32-Bit-Eigenschaft zuweisen und daraus abrufen.
-   Nachdem Sie den ganzzahligen Wert von 0x7FFFFFFF (für Typen mit Vorzeichen), 0x80000000 (für Typen ohne Vorzeichen) oder 32 Bits überschreitet, müssen Sie Anführungszeichen verwenden.
-   Der einzige gültige Pfad für einen 64-Bit-Wert befindet sich in den **\_ \_ RELPATH-** oder **\_ \_ PATH-Eigenschaften** der -Instanz. Daher unterstützt WMI die Hexadezimal-Notation für den entsprechenden Wert nicht.
-   Wenn WMI den Instanzschlüssel als negative Zahl auf zeichnet, müssen Sie die ursprüngliche Zahl verwenden, um die Instanz abzurufen.

Die Abfragesemantik ist nicht betroffen und verhält sich wie erwartet. Dieses Verhalten wirkt sich nur auf die Vorgänge "Objektpfad", [**"GetObject"**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)und [**"GetObjectAsync"**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) aus.

Das folgende Beispiel zeigt, dass Klasseninstanzen 64-Bit-Schlüsselwerte haben können.

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

 

 



