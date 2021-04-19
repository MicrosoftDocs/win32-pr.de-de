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
# <a name="class-instance-support-for-64-bit-values"></a><span data-ttu-id="e6e70-103">Unterstützung von Klassen Instanzen für 64-Bit-Werte</span><span class="sxs-lookup"><span data-stu-id="e6e70-103">Class Instance Support for 64-Bit Values</span></span>

<span data-ttu-id="e6e70-104">Sie können einen 64-Bit-Schlüsselwert als Teil eines Pfads verwenden, wobei die folgenden Einschränkungen gelten:</span><span class="sxs-lookup"><span data-stu-id="e6e70-104">You can use a 64-bit key value as part of a path, with the following restrictions:</span></span>

-   <span data-ttu-id="e6e70-105">Solange der 32-Bit-Bereich nicht überschritten wird, können Sie Werte aus dem Schlüssel wie eine 32-Bit-Eigenschaft zuweisen und abrufen.</span><span class="sxs-lookup"><span data-stu-id="e6e70-105">As long as you do not exceed the 32-bit range, you can assign and retrieve values from the key as you would a 32-bit property.</span></span>
-   <span data-ttu-id="e6e70-106">Nachdem Sie den ganzzahligen Wert 0x7FFFFFFF (für signierte Typen), 0x80000000 (bei nicht signierten Typen) oder 32 Bits überschritten haben, müssen Sie Anführungszeichen verwenden.</span><span class="sxs-lookup"><span data-stu-id="e6e70-106">After you exceed the integer value of 0x7FFFFFFF (for signed types), 0x80000000 (for unsigned types), or 32 bits, you must use quotation marks.</span></span>
-   <span data-ttu-id="e6e70-107">Der einzige gültige Pfad für einen 64-Bit-Wert befindet sich in den **\_ \_ RelPath** -oder **\_ \_ path** -Eigenschaften der-Instanz.</span><span class="sxs-lookup"><span data-stu-id="e6e70-107">The only valid path for a 64-bit value is located in the **\_\_RELPATH** or **\_\_PATH** properties of the instance.</span></span> <span data-ttu-id="e6e70-108">Daher unterstützt WMI die hexadezimale Notation für den entsprechenden Wert nicht.</span><span class="sxs-lookup"><span data-stu-id="e6e70-108">As such, WMI does not support the hexadecimal notation for the equivalent value.</span></span>
-   <span data-ttu-id="e6e70-109">Wenn WMI den Instanzschlüssel als negative Zahl aufzeichnet, müssen Sie die ursprüngliche Nummer verwenden, um die Instanz abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e6e70-109">If WMI records the instance key as a negative number, then you must use the original number to retrieve the instance.</span></span>

<span data-ttu-id="e6e70-110">Die Abfrage Semantik ist nicht betroffen und verhält sich wie erwartet.</span><span class="sxs-lookup"><span data-stu-id="e6e70-110">Query semantics are unaffected and behave as expected.</span></span> <span data-ttu-id="e6e70-111">Dieses Verhalten wirkt sich nur auf die Vorgänge "Objekt Pfad", " [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)" und " [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) " aus.</span><span class="sxs-lookup"><span data-stu-id="e6e70-111">This behavior only affects the object path, [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), and [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) operations.</span></span>

<span data-ttu-id="e6e70-112">Das folgende Beispiel zeigt, dass Klassen Instanzen 64-Bit-Schlüsselwerte aufweisen können.</span><span class="sxs-lookup"><span data-stu-id="e6e70-112">The following example shows that class instances can have 64-bit key values.</span></span>

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

 

 



