---
title: Konvertierung
description: Wird vom Dialogfeld konvertieren verwendet, um die Formate zu ermitteln, die eine Anwendung lesen und schreiben kann.
ms.assetid: ff12c4b3-9548-4135-aaf4-d8b49f9aed41
keywords:
- COM für Konvertierungs Registrierungsschlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7f3a87594513c37a558d21fb7d001fc393763d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516071"
---
# <a name="conversion"></a><span data-ttu-id="3b7ef-104">Konvertierung</span><span class="sxs-lookup"><span data-stu-id="3b7ef-104">Conversion</span></span>

<span data-ttu-id="3b7ef-105">Wird vom Dialogfeld **konvertieren** verwendet, um die Formate zu ermitteln, die eine Anwendung lesen und schreiben kann.</span><span class="sxs-lookup"><span data-stu-id="3b7ef-105">Used by the **Convert** dialog box to determine the formats an application can read and write.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="3b7ef-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="3b7ef-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Conversion
         Readable
            Main = rformat, ...
         ReadWritable
            Main = rwformat, ...
```

## <a name="remarks"></a><span data-ttu-id="3b7ef-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b7ef-107">Remarks</span></span>

<span data-ttu-id="3b7ef-108">Die Konvertierungs Informationen werden im Dialogfeld **konvertieren** verwendet, um zu bestimmen, welche Formate eine Anwendung lesen und schreiben kann.</span><span class="sxs-lookup"><span data-stu-id="3b7ef-108">Conversion information is used by the **Convert** dialog box to determine what formats an application can read and write.</span></span> <span data-ttu-id="3b7ef-109">Ein durch Trennzeichen getrenntes Dateiformat wird durch eine Zahl angegeben, wenn es sich um eines der in Windows. h definierten Zwischenablage Formate handelt.</span><span class="sxs-lookup"><span data-stu-id="3b7ef-109">A comma-delimited file format is indicated by a number if it is one of the Clipboard formats defined in Windows.h.</span></span> <span data-ttu-id="3b7ef-110">Eine Zeichenfolge gibt an, dass das Format in Windows. h (privat) nicht definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3b7ef-110">A string indicates the format is not one defined in Windows.h (private).</span></span> <span data-ttu-id="3b7ef-111">In diesem Fall ist das lesbare und beschreibbare Format CF \_ Umriss (privat).</span><span class="sxs-lookup"><span data-stu-id="3b7ef-111">In this case, the readable and writable format is CF\_OUTLINE (private).</span></span>

<span data-ttu-id="3b7ef-112">Der *rformat* -Wert gibt das Dateiformat an, das von einer Anwendung gelesen werden kann (Konvertieren von).</span><span class="sxs-lookup"><span data-stu-id="3b7ef-112">The *rformat* value specifies the file format an application can read (convert from).</span></span>

<span data-ttu-id="3b7ef-113">Der Wert *rwformat* gibt das Dateiformat an, das von einer Anwendung gelesen und geschrieben werden kann (aktivieren als).</span><span class="sxs-lookup"><span data-stu-id="3b7ef-113">The *rwformat* value specifies the file format an application can read and write (activate as).</span></span>

 

 




