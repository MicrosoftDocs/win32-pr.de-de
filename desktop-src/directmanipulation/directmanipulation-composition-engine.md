---
description: Um visuelle Updates zu steuern, sollte die Anwendung idirectmanipulationcompositor verwenden.
ms.assetid: 6D8FB359-F52B-43F9-8A62-6BB2AEDE4F2B
title: Kompositions Modul
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: aa4d922893472c1fe235bae60e41a00924d13bba
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481598"
---
# <a name="composition-engine"></a>Kompositions Modul

Um visuelle Updates zu steuern, sollte die Anwendung [**idirectmanipulationcompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor)verwenden. Dieses Objekt ist verantwortlich für das Aktualisieren von visuellen Elementen auf der Grundlage von Updates für die [direkte Bearbeitung](direct-manipulation-portal.md) , das Vorantreiben von Trägheit-Aktualisierungen und das Bereitstellen von Informationen zur Zusammensetzung von Informationen zur direkten Bearbeitung. eine Anwendung sollte den [dcompmanipulationcompositor](direct-manipulation-guids.md) verwenden, der von [direkter Bearbeitung](direct-manipulation-portal.md)bereitgestellt wird. Dadurch werden alle visuellen Updates im Auftrag der Anwendung und die Laufwerks Trägheit

Der [dcompmanipulationcompositor](direct-manipulation-guids.md) ist eine Implementierung der [**idirectmanipulationcompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) -Schnittstelle, die [directcomposition](../directcomp/directcomposition-portal.md)umschließt. Damit die Anwendung die Ausgabe nicht anwendet, kann die [direkte Manipulation](direct-manipulation-portal.md) über diese Compositor-Objekt die Ausgabe durch Festlegen der Transformationen direkt in der directcomposition-Struktur anwenden. Mithilfe dieser Konfiguration können die Eingaben verarbeitet und Ausgabe Transformationen unabhängig von der Aktivität im UI-Thread angewendet werden.

Um [direkte Manipulations](direct-manipulation-portal.md) Informationen zur zeitlichen Steuerung der Kompositions-Engine zu erhalten, implementiert die [dcompmanipulationcompositor](direct-manipulation-guids.md) -Klasse die [**idirectmanipulationframeinfoprovider**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationframeinfoprovider) -Schnittstelle. Beim Erstellen eines Viewports ist [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) der [**idirectmanipulationcompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) -Zeiger, der von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) für eine Instanz von **idirectmanipulationframeineoprovider** abgerufen wurde. Der **idirectmanipulationframeinfoprovider** -Zeiger wird an die [**idirectmanipulationmanager:: deateviewport ()**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-createviewport) -Funktion übergeben.
