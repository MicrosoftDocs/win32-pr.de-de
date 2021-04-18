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
# <a name="implementing-register"></a>Implementieren von Register

Netzwerkmonitor lädt eine Erfassung aus der Erfassungs Datei und beginnt dann mit dem Aufrufen der [**Register**](register-parser.md) -Funktion für alle Protokolle, die Sie identifizieren kann. Jede Parser-DLL muss eine **Register** -Funktion für jedes Protokoll implementieren, das die Parser-DLL unterstützt.

Jede Implementierung der [**Register**](register-parser.md) -Funktion muss die Funktionen " [**foratepropertydatabase**](createpropertydatabase.md) " und " [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) " aufrufen, um die [*Eigenschaften Datenbank*](p.md) für das [**Protokoll zu erstellen**](createhandofftable.md) und auszufüllen, und anschließend "" erstellt, um die [*Übergabe-Tabelle*](h.md) für das Protokoll zu erstellen – bei Bedarf.

> [!Note]  
> Protokoll Eigenschaften werden für Netzwerkmonitor definiert. Eigenschaften werden erst dann einem Speicherort in einem Erfassungsdaten zugeordnet, wenn die " [**attachproperties**](attachproperties.md) "-Exportfunktion aufgerufen wird.

 

Im folgenden Verfahren werden die Schritte beschrieben, die zum Implementieren der [**Register**](register-parser.md) -Funktion erforderlich sind.

**So implementieren Sie Register für ein Protokoll**

1.  Definieren Sie ein Array von [**PropertyInfo**](propertyinfo.md) -Strukturen, um jede Eigenschaft zu beschreiben, die das Protokoll unterstützt.
2.  Aufrufen von " [**kreatepropertydatabase**](createpropertydatabase.md) " zur Bereitstellung eines Protokoll Handles und der Anzahl von Eigenschaften, die das Protokoll unterstützt.
3.  Aufrufen von [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) in einer Schleife, um jede im [**PropertyInfo**](propertyinfo.md) -Struktur Array definierte Eigenschaft hinzuzufügen.
4.  Wenn für das Protokoll eine Übergabe Tabelle verwendet wird, wird [**"–"**](createhandofftable.md)aufgerufen, nachdem alle Eigenschaften des Protokolls der Eigenschaften Datenbank hinzugefügt wurden.

Im folgenden finden Sie eine grundlegende Implementierung von [**Register**](register-parser.md). Beachten Sie, dass eine Eigenschaften Datenbank für ein Protokoll erstellt wird, das nur zwei Eigenschaften unterstützt. Dieses Codebeispiel stammt aus dem generischen Parser, den Netzwerkmonitor bereitstellt.

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

 

 
