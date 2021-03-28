---
description: Anbieter Merkmale sind eine Methode zum Anfügen von mehr Daten an eine einzelne Anbieter Registrierung.
ms.assetid: 97755D64-BF57-4C0D-8ED4-040FC375C4AF
title: Anbieter Merkmale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c67b25857070edb6419be9a2898d2667f3a179d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980393"
---
# <a name="provider-traits"></a>Anbieter Merkmale

Anbieter Merkmale sind eine Methode zum Anfügen von mehr Daten an eine einzelne Anbieter Registrierung. Sie können für Manifestressourcen oder tracelogging-Anbieter verwendet werden. Dies umfasst derzeit die Unterstützung für das Hinzufügen eines Anbieter namens und/oder einer Anbieter Gruppe zu einer einzelnen Anbieter Registrierung. In Zukunft werden wahrscheinlich weitere Merkmals Typen hinzugefügt. Diese Informationen werden im Kernel als binäres Blob eines festgelegten Formats gespeichert.

Merkmale können nur einmal für eine Registrierung festgelegt werden. Alle weiteren Versuche, die Merkmale dieser Registrierung festzulegen, können nicht ausgeführt werden.

Um Anbieter Merkmale für einen Manifest-basierten Anbieter festzulegen, müssen Sie die [**eventsetinformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) -Funktion mit der eventprovidersettrait-Informations Klasse aufrufen. Der eventinformation-Puffer sollte ein binäres Blob im folgenden Format enthalten:

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

Aus dem einzelnen Merkmal ist der etw- \_ Anbieter \_ Merkmals \_ Typ wie folgt definiert:

``` syntax
typedef enum {
    EtwProviderTraitTypeGroup = 1,
    EtwProviderTraitTypeMax
} ETW_PROVIDER_TRAIT_TYPE;
```

Die Anbieter Merkmale werden von tracelogging-Anbietern automatisch festgelegt, wenn die [**traceloggingregister**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) -Funktion aufgerufen wird. Der Name des tracelogging-Anbieters ist immer in seinen Merkmalen enthalten. Eine Gruppe kann für einen tracelogging-Anbieter mithilfe des [**traceloggingoptiongroup**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup) -Makros in der Anbieter Definition festgelegt werden.

## <a name="custom-traits"></a>Benutzerdefinierte Merkmale

Obwohl die meisten der 255 möglichen Merkmals Typen noch nicht definiert sind, sind Merkmals Typen 1-127 für die Definition durch Microsoft reserviert. Die verbleibenden Werte des indizierten Typs können von externen Entwicklern verwendet werden, wenn Sie passen. Jeder Benutzer, der seine eigenen benutzerdefinierten Merkmale dem Anbieter hinzufügt, sollte die gesamte Merkmals Größe in den folgenden Gründen unter 256 Bytes behalten:

-   Die Merkmale sind in jedem für den Anbieter geschriebenen Ereignis enthalten. Große Merkmale können zu sehr großen Protokolldateien führen.
-   Die Merkmale werden während der Lebensdauer des Anbieters im nicht ausgelagerten Kernel Pool gespeichert.

## <a name="provider-groups"></a>Anbietergruppen

Eine Anbieter Gruppe ist eine GUID-definierte, steuerbare Entität, ähnlich wie ein Anbieter selbst. Der Hauptunterschied besteht darin, dass während der Verwendung einer Anbieter-GUID zum Steuern der Registrierungen nur seines Anbieters eine Gruppe alle Registrierungen der Mitglieder steuert. Wenn Sie z. b. eine Anbieter Gruppe mit einem bestimmten Schlüsselwort und einer Ebene aktivieren, werden alle Gruppenmitglieder Registrierungen mit diesem Schlüsselwort und derselben Ebene aktiviert.

Die Gruppenmitgliedschaft kann durch Berechtigungen eingeschränkt werden. Wenn der Aufrufer von [**eventsetinformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) nicht über Berechtigungen zum Beitreten zur angegebenen Gruppe verfügt, wird die Mitgliedschaft verweigert.

In einigen Fällen möchte der Ablauf Verfolgungs Sitzungs Controller einige Anbieter von der Aktivierung einer Gruppe ausschließen. Dies kann durch Festlegen einer nicht zulassen-Liste erreicht werden. Eine nicht Zulassungsliste ist eine Liste von Anbieter-GUIDs, die auf der Grundlage der Gruppeneinstellungen für eine einzelne Protokollierungs Sitzung nicht aktiviert werden. Die Zulassungs Listen können dynamisch mit [**tracesetinformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) und der tracesetdisallowlist-Informations Klasse geändert werden.

Die meisten enable-Aktionen können für Anbietergruppen auf ähnliche Weise wie bei einzelnen Anbietern durchgeführt werden. es gibt jedoch einige Ausnahmen. Zu den Ausnahmen zählen:

-   Anbietergruppen können nicht von privaten Ablauf Verfolgungs Sitzungen gesteuert werden.
-   Der Ereignis Name, die Ereignis-ID und die Nutz Last Filter sind für Anbietergruppen nicht anwendbar, da Sie bestimmte Informationen eines einzelnen Anbieters annehmen.

 

 
