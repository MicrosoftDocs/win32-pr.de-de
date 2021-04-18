---
title: Strukturierte Speicherzugriffs Modi
description: Mechanismen zum Steuern des gleichzeitigen Zugriffs auf ein Objekt, von mehreren Prozessen und Benutzern, sind von entscheidender Bedeutung.
ms.assetid: 2d524c2b-f2b4-49f2-9be8-2037846eb9e9
keywords:
- Strukturierter Speicherplatz Halter-STG, Grundlagen, API-Funktionen, Flags für den Zugriff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e46a231cb5168d15564f0b86b064c8bfd19e38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339190"
---
# <a name="structured-storage-access-modes"></a>Strukturierte Speicherzugriffs Modi

Mechanismen zum Steuern des gleichzeitigen Zugriffs auf ein Objekt, von mehreren Prozessen und Benutzern, sind von entscheidender Bedeutung. COM bietet diese Mechanismen durch Definieren von Zugriffs Modi für Speicher-und Streamobjekte. Der für ein übergeordnete Speicher Objekt angegebene Zugriffsmodus wird von seinen untergeordneten Elementen geerbt, Sie können jedoch auch zusätzliche Einschränkungen für den untergeordneten Speicher oder Datenstrom platzieren. Ein gespeichertes Speicher-oder Datenstrom Objekt kann im gleichen Modus oder in einem stärker eingeschränkten Modus geöffnet werden als das übergeordnete Objekt, aber es kann nicht in einem weniger eingeschränkten Modus geöffnet werden als das übergeordnete Element.

Sie geben Zugriffs Modi mithilfe der Werte an, die in [**STGM-Konstanten**](stgm-constants.md)aufgeführt sind. Diese Werte dienen als Flags, die als Argumente an Methoden in der [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle und den zugehörigen API-Funktionen übermittelt werden. In der Regel werden mehrere Flags im *grsmode*-Parameter mit einem booleschen **oder** -Vorgang kombiniert.

Die Flags fallen in sechs Gruppen. Es kann immer nur ein Flag aus jeder Gruppe angegeben werden:

-   [Transaktionsflags](transaction-flags.md)
-   [Speichererstellungsflags](storage-creation-flags.md)
-   [Temporäre erstellungsflags](temporary-creation-flags.md)
-   [Prioritätsflags](priority-flags.md)
-   [Zugriffs Berechtigungs Flags](access-permission-flags.md)
-   [Shared Access-Flags](shared-access-flags.md)

 

 




