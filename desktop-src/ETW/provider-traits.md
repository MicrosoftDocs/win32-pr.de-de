---
description: Anbietermerkmale sind eine Methode zum Anfügen weiterer Daten an eine individuelle Anbieterregistrierung.
ms.assetid: 97755D64-BF57-4C0D-8ED4-040FC375C4AF
title: Anbietermerkmale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2131ee4900fca40b26e8675b3eb4aade4e740fd49d1ed06098a21682ed55ff25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069890"
---
# <a name="provider-traits"></a>Anbietermerkmale

Anbietermerkmale sind eine Methode zum Anfügen weiterer Daten an eine individuelle Anbieterregistrierung. Sie können für manifestbasierte oder TraceLogging-Anbieter verwendet werden. Dies umfasst derzeit Unterstützung für das Hinzufügen eines Anbieternamens und/oder einer Anbietergruppe zu einer individuellen Anbieterregistrierung. In Zukunft werden wahrscheinlich weitere Merkmalstypen hinzugefügt. Diese Informationen werden im Kernel als binäres Blob eines festgelegten Formats gespeichert.

Merkmale können nur einmal für eine Registrierung festgelegt werden. Alle weiteren Versuche, die Merkmale für diese Registrierung festzulegen, schlagen fehl.

Um Anbietermerkmale für einen manifestbasierten Anbieter festzulegen, rufen Sie die [**EventSetInformation-Funktion**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) mit der EventProviderSetTraits-Informationsklasse auf. Der EventInformation-Puffer sollte ein binäres Blob im folgenden Format enthalten:

``` syntax
{
   UINT16 TraitsSize   // Total size of the traits including this field
   CHAR[] ProviderName // Null terminated utf-8 provider name
   TRAIT[] Traits      // Zero or more individual traits
}
```

Einzelne Merkmale sollten das folgende Format aufweisen:

``` syntax
TRAIT {
      UINT16 TraitSize // Size of this individual trait including this field
      UINT8 Type       // ETW_PROVIDER_TRAIT_TYPE
      BYTE[] Data
      }
```

Aus dem einzelnen Merkmal wird ETW PROVIDER TRAIT TYPE wie folgt \_ \_ \_ definiert:

``` syntax
typedef enum {
    EtwProviderTraitTypeGroup = 1,
    EtwProviderTraitTypeMax
} ETW_PROVIDER_TRAIT_TYPE;
```

TraceLogging-Anbieter legen die Anbietermerkmale automatisch fest, wenn die [**TraceLoggingRegister-Funktion**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) aufgerufen wird. Der Name des TraceLogging-Anbieters ist immer in seinen Merkmalen enthalten. Eine Gruppe kann für einen TraceLogging-Anbieter mithilfe des [**TraceLoggingOptionGroup-Makros**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup) in der Anbieterdefinition festgelegt werden.

## <a name="custom-traits"></a>Benutzerdefinierte Merkmale

Obwohl die meisten der 255 möglichen Merkmalstypen noch nicht definiert sind, sind die Merkmalstypen 1 bis 127 für die Definition durch Microsoft reserviert. Die verbleibenden höheren indizierten Typwerte können von externen Entwicklern nach Bedarf verwendet werden. Jeder, der seinem Anbieter eigene benutzerdefinierte Merkmale hinzufügen möchte, sollte aus den folgenden Gründen versuchen, die Gesamtgröße der Merkmale unter 256 Byte zu halten:

-   Die Merkmale sind in jedem Ereignis enthalten, das für den Anbieter geschrieben wurde. Große Merkmale können zu sehr großen Protokolldateien führen.
-   Die Merkmale werden für die Lebensdauer des Anbieters in einem nicht ausgelagerten Kernelpool gespeichert.

## <a name="provider-groups"></a>Anbietergruppen

Eine Anbietergruppe ist eine GUID-definierte steuerbare Entität, die einem Anbieter selbst ähnelt. Der Hauptunterschied besteht darin, dass eine Gruppe alle Memberregistrierungen steuert, während eine Anbieter-GUID verwendet wird, um registrierungen nur ihres Anbieters zu steuern. Wenn Sie beispielsweise eine Anbietergruppe mit einem bestimmten Schlüsselwort und einer bestimmten Ebene aktivieren, werden alle Gruppenmitgliedsregistrierungen mit diesem Schlüsselwort und dieser Ebene aktiviert.

Die Gruppenmitgliedschaft kann durch Berechtigungen eingeschränkt werden. Wenn der Aufrufer von [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) nicht über berechtigungen zum Beitreten zur angegebenen Gruppe verfügt, wird die Mitgliedschaft verweigert.

In einigen Fällen möchte der Ablaufverfolgungssitzungscontroller möglicherweise einige Anbieter von der Aktivierung einer Gruppe ausschließen. Dies kann durch Festlegen einer Liste mit nicht möglich erfolgen. Eine Unzulässigkeitsliste ist eine Liste von Anbieter-GUIDs, die nicht basierend auf den Gruppeneinstellungen für eine einzelne Protokollierungssitzung aktiviert werden. Disallow-Listen können dynamisch mit [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) und der TraceSetDisallowList-Informationsklasse geändert werden.

Während die meisten Aktivierungsaktionen für Anbietergruppen auf ähnliche Weise wie einzelne Anbieter ausgeführt werden können, gibt es einige Ausnahmen. Zu den Ausnahmen zählen:

-   Anbietergruppen können nicht von privaten Ablaufverfolgungssitzungen gesteuert werden.
-   Die Filter "Ereignisname", "Ereignis-ID" und "Nutzlast" gelten nicht für Anbietergruppen, da sie bestimmte Informationen eines einzelnen Anbieters voraussetzt.

 

 
