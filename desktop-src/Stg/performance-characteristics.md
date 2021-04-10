---
title: Leistungsmerkmale
description: Ein Aufrufen der com-Verbund Datei Implementierung der IPropertySetStorage-Schnittstelle zum Erstellen eines Eigenschafts Satzes bewirkt, dass entweder ein Stream oder ein Speicher durch einen IStorage-Erstellungs-oder IStorage-Vorgang erstellt wird.
ms.assetid: 7773e649-19a4-4df2-84ed-027d73283140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8597862602a367ed93a3d6e5e0bcac76035c337a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948891"
---
# <a name="performance-characteristics"></a>Leistungsmerkmale

Ein Aufrufen der com-Verbund Datei Implementierung der [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle zum Erstellen eines Eigenschafts Satzes bewirkt, dass entweder ein Stream oder ein Speicher durch einen [**IStorage:: foratestream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) -oder [**IStorage:: anatestorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)-Anforderungstyp erstellt wird. Ein Standardeigenschaften Satz wird im Arbeitsspeicher erstellt, aber nicht auf den Datenträger geleert. Wenn ein [**IPropertyStorage:: Write-Multiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)-Befehl aufgerufen wird, wird dieser innerhalb des Puffers verarbeitet.

Wenn ein Eigenschaften Satz geöffnet ist, wird [IStorage:: OpenStream](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) oder [IStorage:: OpenStorage](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) verwendet. Der gesamte Eigenschaften Satz-Stream wird in zusammenhängenden Speicher gelesen. [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) -Vorgänge werden dann ausgeführt, indem der Speicherpuffer gelesen wird. Daher ist der erste Zugriff in Bezug auf die zeitaufwendig (aufgrund von Datenträger Lesevorgängen). nachfolgende Zugriffe sind jedoch sehr effizient. Schreibvorgänge können etwas teurer sein, da SetSize-Vorgänge für den zugrunde liegenden Stream möglicherweise erforderlich sind, um sicherzustellen, dass der Speicherplatz verfügbar ist, wenn Daten hinzugefügt werden.

Es wird nicht sichergestellt, ob [**IPropertyStorage:: Write-Multiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) Updates leert. Im Allgemeinen sollte der Client davon ausgehen, dass **IPropertyStorage:: schreitemultiple** nur den im Arbeitsspeicher Puffer aktualisiert. Zum leeren von Daten muss [**IPropertyStorage:: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) oder [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) (letzte Version) aufgerufen werden.

Dieser Entwurf bedeutet, dass " [**schreitemultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) " erfolgreich sein kann, aber die Daten nicht wirklich dauerhaft geschrieben werden.

> [!Note]  
> Diese Größe des Eigenschaften Satz-Streams darf 256 KB nicht überschreiten.

 

 

 