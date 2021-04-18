---
description: Netzwerkmonitor lädt eine Erfassung aus der Erfassungs Datei und beginnt dann mit dem Aufrufen der Register-Funktion für alle Protokolle, die Sie identifizieren kann. Jede Parser-DLL muss eine Register-Funktion für jedes Protokoll implementieren, das die Parser-DLL unterstützt.
ms.assetid: a53c64cb-569f-454b-ae85-7b850228c954
title: Implementieren von Register
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b59f34f5f97925627184db7188aac0a9eb796a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350914"
---
# <a name="implementing-register"></a><span data-ttu-id="9fa4f-104">Implementieren von Register</span><span class="sxs-lookup"><span data-stu-id="9fa4f-104">Implementing Register</span></span>

<span data-ttu-id="9fa4f-105">Netzwerkmonitor lädt eine Erfassung aus der Erfassungs Datei und beginnt dann mit dem Aufrufen der [**Register**](register-parser.md) -Funktion für alle Protokolle, die Sie identifizieren kann.</span><span class="sxs-lookup"><span data-stu-id="9fa4f-105">Network Monitor loads a capture from the capture file, and then starts calling the [**Register**](register-parser.md) function for all the protocols that it can identify.</span></span> <span data-ttu-id="9fa4f-106">Jede Parser-DLL muss eine **Register** -Funktion für jedes Protokoll implementieren, das die Parser-DLL unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9fa4f-106">Each parser DLL must implement a **Register** function for each protocol that the parser DLL supports.</span></span>

<span data-ttu-id="9fa4f-107">Jede Implementierung der [**Register**](register-parser.md) -Funktion muss die Funktionen " [**foratepropertydatabase**](createpropertydatabase.md) " und " [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) " aufrufen, um die [*Eigenschaften Datenbank*](p.md) für das [**Protokoll zu erstellen**](createhandofftable.md) und auszufüllen, und anschließend "" erstellt, um die [*Übergabe-Tabelle*](h.md) für das Protokoll zu erstellen – bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="9fa4f-107">Each implementation of the [**Register**](register-parser.md) function must call the [**CreatePropertyDatabase**](createpropertydatabase.md) and [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) functions to create and fill-in the [*property database*](p.md) for the protocol, and then the [**CreateHandoffTable**](createhandofftable.md) to create the [*handoff table*](h.md) for the protocol — if needed.</span></span>

> [!Note]  
> <span data-ttu-id="9fa4f-108">Protokoll Eigenschaften werden für Netzwerkmonitor definiert.</span><span class="sxs-lookup"><span data-stu-id="9fa4f-108">Protocol properties are defined for Network Monitor.</span></span> <span data-ttu-id="9fa4f-109">Eigenschaften werden erst dann einem Speicherort in einem Erfassungsdaten zugeordnet, wenn die " [**attachproperties**](attachproperties.md) "-Exportfunktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9fa4f-109">Properties are not mapped to a location in a capture data until the [**AttachProperties**](attachproperties.md) export function is called.</span></span>

 

<span data-ttu-id="9fa4f-110">Im folgenden Verfahren werden die Schritte beschrieben, die zum Implementieren der [**Register**](register-parser.md) -Funktion erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9fa4f-110">The following procedure identifies the steps necessary to implement the [**Register**](register-parser.md) function.</span></span>

<span data-ttu-id="9fa4f-111">**So implementieren Sie Register für ein Protokoll**</span><span class="sxs-lookup"><span data-stu-id="9fa4f-111">**To implement Register for one protocol**</span></span>

1.  <span data-ttu-id="9fa4f-112">Definieren Sie ein Array von [**PropertyInfo**](propertyinfo.md) -Strukturen, um jede Eigenschaft zu beschreiben, die das Protokoll unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9fa4f-112">Define an array of [**PROPERTYINFO**](propertyinfo.md) structures to describe each property that the protocol supports.</span></span>
2.  <span data-ttu-id="9fa4f-113">Aufrufen von " [**kreatepropertydatabase**](createpropertydatabase.md) " zur Bereitstellung eines Protokoll Handles und der Anzahl von Eigenschaften, die das Protokoll unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9fa4f-113">Call [**CreatePropertyDatabase**](createpropertydatabase.md) to provide a protocol handle, and the number of properties that the protocol supports.</span></span>
3.  <span data-ttu-id="9fa4f-114">Aufrufen von [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) in einer Schleife, um jede im [**PropertyInfo**](propertyinfo.md) -Struktur Array definierte Eigenschaft hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9fa4f-114">Call [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) in a loop to add each property defined in the [**PROPERTYINFO**](propertyinfo.md) structure array.</span></span>
4.  <span data-ttu-id="9fa4f-115">Wenn für das Protokoll eine Übergabe Tabelle verwendet wird, wird [**"–"**](createhandofftable.md)aufgerufen, nachdem alle Eigenschaften des Protokolls der Eigenschaften Datenbank hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="9fa4f-115">If the protocol uses a handoff table, call [**CreateHandoffTable**](createhandofftable.md)— after all the properties of the protocol are added to the property database.</span></span>

<span data-ttu-id="9fa4f-116">Im folgenden finden Sie eine grundlegende Implementierung von [**Register**](register-parser.md).</span><span class="sxs-lookup"><span data-stu-id="9fa4f-116">The following is a basic implementation of [**Register**](register-parser.md).</span></span> <span data-ttu-id="9fa4f-117">Beachten Sie, dass eine Eigenschaften Datenbank für ein Protokoll erstellt wird, das nur zwei Eigenschaften unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9fa4f-117">Note that a property database is created for a protocol that supports only two properties.</span></span> <span data-ttu-id="9fa4f-118">Dieses Codebeispiel stammt aus dem generischen Parser, den Netzwerkmonitor bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9fa4f-118">This code example is taken from the generic parser that Network Monitor provides.</span></span>

``` syntax
#include <windows.h>

PROPERTYINFO MyProtocolPropertyTable[]
{
  // Summary property (0)
  {
     0,                               // Handle to property.
     0,                               // Reserved.
     "Summary",                       // Property label.
     "Summary of protocol packet",    // Property comment.
     PROP_TYPE_SUMMARY,               // Data type of property.
     PROP_QUAL_NONE,                  // Data type qualifier.
     NULL,                            // Reserved.
     80,                              // 
     FormatPropertyInstance           // 
  }

  // WORD property (1)
  {
     0,                               // Handle to property.
     0,                               // Reserved.
     "WORD property",                 // Property label.
     "16-bit WORD property",         // Property comment.
     PROP_TYPE_WORD,                  // Data type of property.
     PROP_QUAL_NONE,                  // Data type qualifier.
     NULL,                            // Reserved.
     80,                              // 
     FormatPropertyInstance           // 
  }

}

void BHAPI MyProtocolRegister( HPPROTOCOL hProtocol) 
{
  // Create property database.
  DWORD dwNumberOfProperties = 2;
  CreatePropertyDatabase (hProtocol,
                          dwNumberOfProperties
                          );
  
  // Add properties to database.
  WORD i;
  for( i=0; i< dwNumberOfProperties; i++)
  {
     AddProperty(hProtocol, &MyProtocolPropertyTable[i]);
  }

  // Create handoff table.
  CreateHandoffTable("myProtocolHandoffTable",
                          "myProtocol.ini",
                           hTable,
                           MaxEntries,
                           10       // Handoff set values are base 10.
                          )
}
```

 

 
