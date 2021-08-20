---
title: Leistungsmerkmale
description: Ein Aufruf der COM-Verbunddateiimplementierung der IPropertySetStorage-Schnittstelle zum Erstellen eines Eigenschaftensets bewirkt, dass entweder ein Stream oder Speicher durch einen Aufruf von IStorage CreateStream oder IStorage CreateStorage erstellt wird.
ms.assetid: 7773e649-19a4-4df2-84ed-027d73283140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ac11200b021cae1ea1d60438b57530f0dbc8c02ea3d26b5622ab859a99224aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117960830"
---
# <a name="performance-characteristics"></a>Leistungsmerkmale

Ein Aufruf der COM-Verbunddateiimplementierung der [**IPropertySetStorage-Schnittstelle**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) zum Erstellen eines Eigenschaftensets bewirkt, dass entweder ein Stream oder Speicher durch einen Aufruf von [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) oder [**IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)erstellt wird. Ein Standardeigenschaftssatz wird im Arbeitsspeicher erstellt, aber nicht auf den Datenträger geleert. Wenn [**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)aufruft, wird es innerhalb des Puffers betrieben.

Wenn ein Eigenschaftensatz geöffnet wird, [wird IStorage::OpenStream](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) oder [IStorage::OpenStorage](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) verwendet. Der gesamte Eigenschaftensatzstream wird in den zusammenhängenden Speicher gelesen. [**IPropertyStorage::ReadMultiple-Vorgänge**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) arbeiten dann durch Lesen des Speicherpuffers. Daher ist der erste Zugriff zeitintensiv (aufgrund von Datenträgerlesezugriffen), aber nachfolgende Zugriffe sind sehr effizient. Schreibvorgänge können etwas teurer sein, da SetSize-Vorgänge für den zugrunde liegenden Stream möglicherweise erforderlich sind, um zu gewährleisten, dass Speicherplatz verfügbar ist, wenn Daten hinzugefügt werden.

Es wird nicht garantiert, ob [**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) Updates leert. Im Allgemeinen sollte der Client davon ausgehen, dass **IPropertyStorage::WriteMultiple** nur den im Arbeitsspeicherpuffer aktualisiert. Zum Leeren von Daten sollten [**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) oder [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) (letzte Version) aufgerufen werden.

Dieser Entwurf bedeutet, [**dass WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) zwar erfolgreich ist, die Daten aber nicht dauerhaft geschrieben werden.

> [!Note]  
> Diese Größe des Eigenschaftensatzstreams darf 256.000 Bytes nicht überschreiten.

 

 

 