---
description: Advanced Topology Building
ms.assetid: 66aa07d8-6756-4d5b-9f0a-24b902da6fa2
title: Advanced Topology Building
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d7f2bba412a698d688bc9d88e9935ed0988cc909931634633a0d75b88c2fae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664870"
---
# <a name="advanced-topology-building"></a>Advanced Topology Building

In diesem Abschnitt werden einige erweiterte Techniken zum Erstellen von Topologien beschrieben. Sie können diese Techniken verwenden, wenn Sie mehr Kontrolle über die Topologien wünschen, die Sie an die Mediensitzung senden.

Da diese Techniken für Szenarien vorgesehen sind, die über die Vom Standardtopologielader bereitgestellte Funktionalität hinausgehen, hängen viele der Details von den speziellen Anforderungen Ihrer Anwendung ab. Daher ist dieser Abschnitt lose um kleinere Subtasks und nicht um vollständige End-to-End-Szenarien organisiert.

Die typische Wiedergabeanwendung folgt den folgenden Schritten:

1.  Die Anwendung erstellt eine Teiltopologie und stellt sie in der Mediensitzung in die Warteschlange.
2.  Die Mediensitzung ruft das Topologielader auf, um die Topologie aufzulösen.

Wenn Sie über die Funktionen des Topologielader hinausgehen möchten, gibt es drei allgemeine Ansätze:

-   Erstellen Sie eine vollständige Topologie. Wenn Sie die Topologie in der Mediensitzung in die Warteschlange stellen, rufen Sie MIT DEM FLAG MFSESSION SETTOPOLOGY NORESOLUTION [**DEN Aufruf FÜR DIE WARTESCHLANGE**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) \_ \_ AUF. Dieses Flag verhindert, dass die Mediensitzung versucht, die Topologie aufzulösen.

-   Rufen Sie das Topologielader direkt auf, um die Topologie aufzulösen. Anschließend können Sie die vollständige Topologie ändern, bevor Sie sie in die Mediensitzung einwarteschlangen.

-   Implementieren Sie ein benutzerdefiniertes Topologielader. Bei diesem Ansatz stellen Sie eine Teiltopologie in die Warteschlange, aber die Mediensitzung ruft Ihr benutzerdefiniertes Lader anstelle der Standard-Media Foundation auf. Ein Vorteil dieses Ansatzes besteht darin, dass Sie eine benutzerdefinierte Topologie in der geschützten Umgebung erstellen können. (In diesem Fall muss das Topologielader jedoch eine vertrauenswürdige Komponente sein. Weitere Informationen finden Sie unter [Protected Media Path](protected-media-path.md).)

In diesem Abschnitt werden die folgenden Themen behandelt:



| Thema                                                                          | BESCHREIBUNG                                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Benutzerdefinierte Topologielader](custom-topology-loaders.md)                         | Hier erfahren Sie, wie Sie eine benutzerdefinierte Implementierung von [**DURCHTTTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) für die Mediensitzung bereitstellen.          |
| [Binden von Ausgabeknoten an Mediensenken](binding-output-nodes-to-media-sinks.md) | Vorbereiten der Ausgabeknoten in einer Topologie, wenn Sie das Topologielader außerhalb der Mediensitzung verwenden. |
| [Hinzufügen eines Decoders zu einer Topologie](adding-a-decoder-to-a-topology.md)           | Hier erfahren Sie, wie Sie einen Decoder manuell auswählen und einer Topologie hinzufügen.                                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Topologien](topologies.md)
</dt> </dl>

 

 



