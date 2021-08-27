---
description: Um visuelle Updates zu erstellen, sollte die Anwendung IDirectManipulationCompositor verwenden.
ms.assetid: 6D8FB359-F52B-43F9-8A62-6BB2AEDE4F2B
title: Kompositions-Engine
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 14bc2ad60405dba7874493096e022b553a8b276cd6f0bb21ea9ae3cf191f5d3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117900"
---
# <a name="composition-engine"></a>Kompositions-Engine

Um visuelle Updates zu erstellen, sollte die Anwendung [**IDirectManipulationCompositor verwenden.**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) Dieses Objekt ist für die [](direct-manipulation-portal.md) Aktualisierung von Visuals auf der Grundlage von Updates der direkten Manipulation, das Vorwärtsfahren von Trägheitsupdates und die Bereitstellung von Informationen zur Zeitlichen Steuerung der Komposition für die direkte Manipulation verantwortlich. Darüber hinaus sollte eine Anwendung den von direct [Manipulation](direct-manipulation-portal.md)bereitgestellten [DCompManipulationCompositor](direct-manipulation-guids.md) verwenden, der alle visuellen Updates im Auftrag der Anwendung verarbeitet und Trägheitsaktualisierungen voransetzt.

Der [DCompManipulationCompositor](direct-manipulation-guids.md) ist eine Implementierung der [**IDirectManipulationCompositor-Schnittstelle,**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) die [DirectComposition umschließt.](../directcomp/directcomposition-portal.md) Anstatt die Anwendung die Ausgabe anwenden zu lassen, kann die direkte [Manipulation](direct-manipulation-portal.md) über dieses Compositorobjekt die Ausgabe anwenden, indem die Transformationen direkt auf die DirectComposition-Struktur angewendet werden. Mit dieser Konfiguration können Eingaben verarbeitet und Ausgabetransformationen angewendet werden, unabhängig von der Aktivität im UI-Thread.

Um direkte [Manipulationsinformationen](direct-manipulation-portal.md) zum Zeitlichen der Kompositions-Engine zu erhalten, implementiert die [DCompManipulationCompositor-Klasse](direct-manipulation-guids.md) die [**IDirectManipulationFrameInfoProvider-Schnittstelle.**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationframeinfoprovider) Beim Erstellen eines Viewports stellt [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) den [**IDirectManipulationCompositor-Zeiger**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) bereit, der von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) für eine Instanz von **IDirectManipulationFrameInfoProvider erhalten wurde.** Der **IDirectManipulationFrameInfoProvider-Zeiger** wird an die [**IDirectManipulationManager::CreateViewport()-Funktion**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-createviewport) übergeben.
