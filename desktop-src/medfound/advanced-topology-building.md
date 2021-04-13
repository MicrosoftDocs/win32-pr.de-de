---
description: Erweiterte topologiebildung
ms.assetid: 66aa07d8-6756-4d5b-9f0a-24b902da6fa2
title: Erweiterte topologiebildung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4cc061d4e557dda4ccbb81eabc55e8e1b3e33b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343338"
---
# <a name="advanced-topology-building"></a>Erweiterte topologiebildung

In diesem Abschnitt werden einige erweiterte Techniken zum Entwickeln von Topologien beschrieben. Sie können diese Techniken verwenden, wenn Sie mehr Kontrolle über die Topologien wünschen, die Sie an die Medien Sitzung senden.

Da diese Techniken für Szenarien vorgesehen sind, die über die vom Standard-topologielader bereitgestellte Funktionalität hinausgehen, hängen viele der Details von den speziellen Anforderungen Ihrer Anwendung ab. Daher ist dieser Abschnitt nicht durchgängige Szenarios, sondern durch kleinere Unteraufgaben organisiert.

Die typische Wiedergabe Anwendung führt folgende Schritte aus:

1.  Die Anwendung erstellt eine partielle Topologie und fügt Sie in die Medien Sitzung ein.
2.  Die Medien Sitzung ruft den topologielader auf, um die Topologie aufzulösen.

Wenn Sie über die Funktionen des topologieladers hinausgehen möchten, gibt es drei allgemeine Ansätze:

-   Erstellen Sie eine komplette Topologie. Wenn Sie die Topologie in der Medien Sitzung in die Warteschlange stellen, wenden Sie [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) mit dem Flag "mfsession \_ settopology \_ noresolution" an. Dieses Flag verhindert, dass die Medien Sitzung versucht, die Topologie aufzulösen.

-   Rufen Sie den topologielader direkt auf, um die Topologie aufzulösen. Anschließend können Sie die vollständige Topologie ändern, bevor Sie Sie in der Medien Sitzung in die Warteschlange eingereiht.

-   Implementieren eines benutzerdefinierten topologieladers. Bei dieser Vorgehensweise wird eine partielle Topologie in die Warteschlange eingereiht, aber die Medien Sitzung ruft das benutzerdefinierte Lade Modul anstelle der Standard Media Foundation Implementierung auf. Ein Vorteil dieses Ansatzes besteht darin, dass Sie die benutzerdefinierte Topologie innerhalb der geschützten Umgebung durchführen können. (In diesem Fall muss das topologielader jedoch eine vertrauenswürdige Komponente sein. Weitere Informationen finden Sie unter [geschützter Medien Pfad](protected-media-path.md).)

In diesem Abschnitt werden die folgenden Themen behandelt:



| Thema                                                                          | BESCHREIBUNG                                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Benutzerdefinierte topologielader](custom-topology-loaders.md)                         | Gibt an, wie eine benutzerdefinierte Implementierung von [**imftopoloader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) für die Medien Sitzung bereitgestellt wird.          |
| [Binden von Ausgabe Knoten an Medien senken](binding-output-nodes-to-media-sinks.md) | Vorbereiten der Ausgabe Knoten in einer Topologie, wenn Sie das topologielader außerhalb der Medien Sitzung verwenden. |
| [Hinzufügen eines Decoders zu einer Topologie](adding-a-decoder-to-a-topology.md)           | Wie Sie einen Decoder manuell auswählen und einer Topologie hinzufügen.                                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Topologien](topologies.md)
</dt> </dl>

 

 



