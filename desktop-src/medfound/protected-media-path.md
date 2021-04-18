---
description: 'In diesem Thema werden drei miteinander verbundene Themen erläutert: geschützte Umgebung, Medien Interoperabilitäts Gateway und Sperrung und Verlängerung.'
ms.assetid: e88806ae-0041-4b4a-a8df-69718a651e82
title: Geschützter Medien Pfad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7304edadf1623d41bc2f1f5c6b2b4cda2dd5f598
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104555414"
---
# <a name="protected-media-path"></a>Geschützter Medien Pfad

In diesem Thema werden drei miteinander verbundene Themen erläutert: geschützte Umgebung, Medien Interoperabilitäts Gateway und Sperrung und Verlängerung.

-   Bei einer geschützten Umgebung (PE) handelt es sich um eine Reihe von Technologien, mit denen geschützte Inhalte auf geschützte Weise von und in Windows Vista übertragen werden können. Alle Komponenten in einer geschützten Umgebung werden als vertrauenswürdig eingestuft, und der Prozess wird vor Manipulationen geschützt.
-   Der geschützte Medien Pfad (PMP) ist eine ausführbare Datei, die in einer geschützten Umgebung ausgeführt wird.
-   Wenn eine vertrauenswürdige Komponente im PE kompromittiert wird, wird Sie nach der fälligen Verarbeitung widerrufen. Microsoft bietet jedoch einen Erneuerungs Mechanismus, mit dem eine neuere vertrauenswürdige Version der Komponente installiert wird, sobald eine verfügbar ist.

Weitere Informationen zur Code Signierung geschützter Medienkomponenten finden Sie im Whitepaper [Code Signing for Protected Media Components in Windows Vista](/windows-hardware/test/hlk/).

Dieses Thema enthält folgende Abschnitte:

-   [Geschützte Umgebung](#protected-environment)
-   [Entwurf der geschützten Umgebung](#design-of-the-protected-environment)
-   [Geschützter Medien Pfad](#protected-media-path)
    -   [Eingabe Vertrauensstellungs Autorität](#input-trust-authorities)
    -   [Ausgabe Vertrauensstellungs Behörden](#output-trust-authorities)
    -   [Richtlinien Objekte](#policy-objects)
    -   [Erstellen von Objekten im PMP](#creating-objects-in-the-pmp)
-   [Übersicht über die Richtlinien Aushandlung](#overview-of-policy-negotiation)
-   [Sperrung und Verlängerung](#revocation-and-renewal)
-   [Ausgabe Link Schutz](#output-link-protection)
-   [Zugehörige Themen](#related-topics)

## <a name="protected-environment"></a>Geschützte Umgebung

Der Inhalts Schutz umfasst mehrere Technologien, von denen jede versucht, sicherzustellen, dass Inhalte nicht in einer Weise verwendet werden können, die nicht mit der Absicht des Inhalts Besitzers oder-Anbieters konsistent ist. Diese Technologien umfassen den Kopierschutz, den Link Schutz, den bedingten Zugriff und Digital Rights Management (DRM). Die Grundlage der einzelnen Vertrauens Stellungen besteht darin, dass der Zugriff auf den Inhalt nur Softwarekomponenten gewährt wird, die den Nutzungsbedingungen entsprechen, die diesem Inhalt zugewiesen sind.

Um Bedrohungen gegen geschützte Inhalte zu minimieren, ermöglichen Windows Vista und Media Foundation Software vertrauenswürdigen Code, der in einer geschützten Umgebung ausgeführt werden kann. Ein PE besteht aus einer Reihe von Komponenten, Richtlinien und Tools, mit denen der Schutz gegen Inhalts Piraterie erhöht werden kann.

Bevor Sie die PE genauer untersuchen, ist es wichtig, die Bedrohungen zu verstehen, die für eine Minimierung entwickelt wurden. Angenommen, Sie führen eine Medien Anwendung in einem Benutzermodusprozess aus. Die Anwendung ist mit den verschiedenen DLLs (Dynamic Link Libraries) verknüpft, die Medien-Plug-ins (z. b. Decoders) enthalten. Andere Prozesse werden ebenfalls im Benutzermodus ausgeführt, und verschiedene Treiber werden in den Kernel geladen. Wenn kein Vertrauens Mechanismus vorhanden ist, sind die folgenden Bedrohungen vorhanden:

-   Die Anwendung kann direkt auf geschützte Medien zugreifen oder den Prozess Speicher hacken.
-   Plug-Ins können direkt auf den Inhalt zugreifen oder den Prozess Speicher hacken.
-   Andere Prozesse können den Medien Prozess Speicher entweder direkt oder durch Einfügen von Code hacken.
-   Kernel Treiber können den Medien Prozess Speicher hacken.
-   Der Inhalt kann über ein ungeschütztes Medium außerhalb des Systems gesendet werden. (Der Link Schutz ist dafür ausgelegt, diese Bedrohung zu mindern.)

## <a name="design-of-the-protected-environment"></a>Entwurf der geschützten Umgebung

Eine geschützte Umgebung wird in einem separaten geschützten Prozess von der Medien Anwendung ausgeführt. Mit dem geschützten Prozess Feature von Windows Vista wird verhindert, dass andere Prozesse auf den geschützten Prozess zugreifen.

Wenn ein geschützter Prozess erstellt wird, identifizieren Kern-Kernel Komponenten nicht vertrauenswürdige Komponenten und Plug-ins, sodass Sie von der geschützten Umgebung nicht geladen werden können. Eine vertrauenswürdige Komponente wurde von Microsoft entsprechend signiert. Der Kernel verfolgt auch Module, die darin geladen werden, sodass die geschützte Umgebung die Wiedergabe geschützter Inhalte nicht beenden kann, wenn ein nicht vertrauenswürdiges Modul geladen wird. Bevor eine Kernel Komponente geladen wird, überprüft der Kernel, ob er vertrauenswürdig ist. Wenn dies nicht der Fall ist, lehnen vertrauenswürdige Komponenten, die bereits in der PE vorhanden sind, geschützte Inhalte ab. Um dies zu ermöglichen, führen PE-Komponenten in regelmäßigen Abständen einen kryptografisch geschützten Handshake mit dem Kernel aus. Wenn eine nicht vertrauenswürdige Kernelmoduskomponente vorhanden ist, schlägt der Handshake fehl und gibt dem PE an, dass eine nicht vertrauenswürdige Komponente vorhanden ist.

Wenn eine vertrauenswürdige Komponente kompromittiert wird, kann Sie nach dem Fälligkeits Vorgang widerrufen werden. Microsoft bietet einen Erneuerungs Mechanismus zur Installation einer neueren vertrauenswürdigen Version, falls verfügbar.

## <a name="protected-media-path"></a>Geschützter Medien Pfad

Der geschützte Medien Pfad (PMP) ist die primäre ausführbare PE-Datei für Media Foundation. Das PMP ist erweiterbar, sodass Schutzmechanismen von Drittanbietern unterstützt werden können.

Das PMP akzeptiert geschützte Inhalte und zugehörige Richtlinien aus beliebigen Media Foundation Quellen unter Verwendung eines beliebigen Inhalts Schutzsystems, einschließlich derjenigen, die von Drittanbietern bereitgestellt werden. Der Inhalt wird an alle Media Foundation Senke gesendet, solange die Senke den von der Quelle angegebenen Richtlinien entspricht. Außerdem werden Transformationen zwischen der Quelle und der Senke unterstützt, einschließlich Transformationen von Drittanbietern, solange Sie vertrauenswürdig sind.

Das PMP wird in einem geschützten Prozess ausgeführt, der von der Medien Anwendung isoliert ist. Die Anwendung kann nur Befehls-und Steuerungs Meldungen mit dem PMP austauschen, hat aber keinen Zugriff auf Inhalte, nachdem Sie an das PMP übergeben wurde. Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![Diagramm des Pfads geschützter Medien](images/pmp04.png)

Schattierte Felder stellen Komponenten dar, die von Drittanbietern bereitgestellt werden können. Alle Komponenten, die im geschützten Prozess erstellt werden, müssen signiert und vertrauenswürdig sein.

Die Anwendung erstellt eine Instanz der Medien Sitzung innerhalb des geschützten Prozesses und empfängt einen Zeiger auf eine Proxy Medien Sitzung, die Schnittstellen Zeiger über die Prozess Grenze hinweg marshunkt.

Die Medienquelle kann entweder innerhalb des Anwendungsprozesses, wie hier gezeigt, oder innerhalb des geschützten Prozesses erstellt werden. Wenn die Medienquelle innerhalb des Anwendungsprozesses erstellt wird, erstellt die Quelle im geschützten Prozess einen Proxy für sich selbst.

Alle anderen Pipeline Komponenten, z. b. Decoder und Medien senken, werden im geschützten Prozess erstellt. Wenn diese Objekte benutzerdefinierte Schnittstellen für Anwendungen verfügbar machen, müssen Sie einen DCOM-Proxy/Stub bereitstellen, um die Schnittstelle zu Mars Hallen.

Zum Erzwingen einer Richtlinie für geschützte Inhalte beim Durchlaufen der Pipeline verwendet das PMP drei Arten von Komponenten: Input Trust Autoritäten (ITAs), Output Trust Autoritäten (OTAS) und Policy Objects. Diese Komponenten arbeiten zusammen, um Rechte zur Verwendung von Inhalten zu erteilen oder einzuschränken sowie um die Link Schutzmaßnahmen anzugeben, die bei der Wiedergabe von Inhalten verwendet werden müssen, z. b. HDCP (High-Bandwidth Digital Content Protection).

### <a name="input-trust-authorities"></a>Eingabe Vertrauensstellungs Autorität

Eine ITA wird von einer vertrauenswürdigen Medienquelle erstellt und führt mehrere Funktionen aus:

-   Gibt die Rechte für die Verwendung von Inhalten an. Rechte können das Recht enthalten, Inhalte wiederzugeben, auf ein Gerät zu übertragen usw. Es definiert eine geordnete Liste genehmigter Ausgabe Schutzsysteme und die entsprechenden Ausgabe Richtlinien für jedes System. Die ITA speichert diese Informationen in einem Richtlinien Objekt.
-   Stellt den entschlüsselten zum Entschlüsseln des Inhalts bereit.
-   Stellt eine Vertrauensstellung mit dem Kernelmodul in der geschützten Umgebung her, um sicherzustellen, dass die ITA in einer vertrauenswürdigen Umgebung ausgeführt wird.

Eine ITA ist einem einzelnen Stream zugeordnet, der geschützte Inhalte enthält. Ein Datenstrom kann nur über eine ITA verfügen, und eine Instanz einer ITA kann nur einem Stream zugeordnet werden.

### <a name="output-trust-authorities"></a>Ausgabe Vertrauensstellungs Behörden

Eine OTA ist einer vertrauenswürdigen Ausgabe zugeordnet. Die OTA macht eine Aktion verfügbar, die von der vertrauenswürdigen Ausgabe für den Inhalt ausgeführt werden kann, z. b. Wiedergabe oder kopieren. Seine Rolle besteht darin, ein oder mehrere für die ITA erforderliche Ausgabe Schutzsysteme zu erzwingen. Das OTA fragt das von ITA bereitgestellte Richtlinien Objekt ab, um zu bestimmen, welches Schutzsystem es erzwingen muss.

### <a name="policy-objects"></a>Richtlinien Objekte

Ein Richtlinien Objekt kapselt die Inhalts Schutzanforderungen einer ITA. Sie wird von der-Richtlinien-Engine verwendet, um die Unterstützung von Inhalts Schutz mit einer OTA auszuhandeln. OTAS-Abfrage Richtlinien Objekte, um zu bestimmen, welche Schutzsysteme Sie für die einzelnen Ausgaben des aktuellen Inhalts erzwingen müssen.

### <a name="creating-objects-in-the-pmp"></a>Erstellen von Objekten im PMP

Zum Erstellen eines Objekts im geschützten Medien Pfad (PMP) ruft [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) [**imfpmphostapp:: activateclassbyid**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphostapp-activateclassbyid)auf, wobei die angegebene Eingabe- **IStream** wie folgt formatiert ist:

``` syntax
Format: (All DWORD values are serialized in little-endian order)
[GUID (content protection system guid, obtained from Windows.Media.Protection.MediaProtectionSystemId)]
[DWORD (track count, use the actual track count even if all tracks are encrypted using the same data, note that zero is invalid)]
[DWORD (next track ID, use -1 if all remaining tracks are encrypted using the same data)]
[DWORD (next track's binary data size)]
[BYTE* (next track's binary data)]
{ Repeat from "next track ID" above for each stream }
```

## <a name="overview-of-policy-negotiation"></a>Übersicht über die Richtlinien Aushandlung

Es gibt drei grundlegende Anforderungen, die erfüllt sein müssen, damit geschützte Inhalte im PMP verarbeitet werden können. Zunächst muss geschützter Inhalt nur an vertrauenswürdige Ausgaben gesendet werden. Zweitens müssen nur zulässige Aktionen auf einen Stream angewendet werden. Drittens müssen nur genehmigte Ausgabe Schutzsysteme verwendet werden, um einen Stream wiederzugeben. Die Richtlinien-Engine koordiniert zwischen ITAs und OTAS, um sicherzustellen, dass diese Anforderungen erfüllt werden.

Die einfachste Möglichkeit, den Prozess zu verstehen, ist die exemplarische Vorgehensweise für ein vereinfachtes Beispiel, das die erforderlichen Schritte zur Wiedergabe von durch Windows Media Digital Rights Management (WMDRM) geschützten Inhalt von erweiterten System Formaten (Windows Media Digital)

Wenn ein Benutzer eine Player Anwendung gestartet und eine ASF-Datei mit einem geschützten Audiostream und einem geschützten Videostream öffnet, müssen die folgenden Schritte ausgeführt werden:

1.  Die Anwendung erstellt die ASF-Medienquelle und die PMP-Sitzung (Protected Media Path). Media Foundation erstellt einen PMP-Prozess.
2.  Die Anwendung erstellt eine partielle Topologie, die einen audioquellknoten enthält, der mit dem audiorenderer verbunden ist, sowie einen mit dem erweiterten Videorenderer (EVR) verbundenen Video Quellknoten. Bei den Renderers erstellt die Anwendung den Renderer nicht direkt. Stattdessen erstellt die Anwendung im ungeschützten Prozess ein Objekt, das als *Aktivierungs Objekt* bezeichnet wird. Das PMP verwendet das Activation-Objekt, um die Renderer im geschützten Prozess zu erstellen. (Weitere Informationen zu Aktivierungs Objekten finden Sie unter [Activation Objects](activation-objects.md).)
3.  Die Anwendung legt die partielle Topologie für die PMP-Sitzung fest.
4.  Die PMP-Sitzung serialisiert die Topologie und übergibt Sie im geschützten Prozess an den PMP-Host. Der PMP-Host sendet die Topologie an die Richtlinien-Engine.
5.  Das topologielade Programm ruft [**imfinputtrustauthority:: getdecrypter**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) auf der ITAs-Instanz auf und fügt die entschlüsselungssätze in die Topologie direkt nach unten der entsprechenden Quellknoten ein.
6.  Das topologielader fügt die Audio-und Video-decoderer in den entschlüsselungsknoten ein.
7.  Die Richtlinien-Engine scannt die eingefügten Knoten, um zu bestimmen, ob die [**imftreudoutput**](/windows/desktop/api/mfidl/nn-mfidl-imftrustedoutput) -Schnittstelle implementiert. Der EVR und der audiorenderer implementieren " **IMF Treuhänder doutput**", da Sie Daten außerhalb des PMP senden.
8.  Jede ITA bestätigt, dass Sie innerhalb eines geschützten Prozesses ausgeführt wird, indem Sie einen kryptografischen Handshake mit einem Kernelmodul der geschützten Umgebung ausführt.
9.  Für jeden Stream aushandiert das Richtlinien Modul die Richtlinie, indem es ein Richtlinien Objekt aus der ITA erhält und es an die OTA übergibt. Die OTA bietet eine Liste der Schutzsysteme, die von ihr unterstützt werden, und das Richtlinien Objekt gibt an, welche Schutzsysteme zusammen mit den richtigen Einstellungen angewendet werden müssen. Die OTA wendet dann diese Einstellungen an. Wenn dies nicht möglich ist, wird der Inhalt blockiert.

## <a name="revocation-and-renewal"></a>Sperrung und Verlängerung

Eine vertrauenswürdige Komponente kann widerrufen werden, wenn Sie kompromittiert wird oder ermittelt wird, dass Sie gegen die Lizenzverträge verstößt, denen Sie anfänglich vertraut war. Ein Erneuerungs Mechanismus ist vorhanden, um eine neuere, vertrauenswürdigere Version der Komponente zu installieren.

Vertrauenswürdige Komponenten werden mithilfe eines kryptografiezertifikats signiert. Microsoft veröffentlicht eine globale Sperr Liste (GRL), mit der nicht wider sperrte Komponenten identifiziert werden. Die GRL ist digital signiert, um ihre Echtheit sicherzustellen. Inhalts Besitzer können über den Richtlinien Mechanismus sicherstellen, dass die aktuelle Version der GRL auf dem Computer des Benutzers vorhanden ist.

## <a name="output-link-protection"></a>Ausgabe Link Schutz

Wenn hochwertige Videoinhalte angezeigt werden, werden die entschlüsselten, nicht komprimierten Frames über einen physischen Connector auf das Anzeigegerät übertragen. Bei Inhaltsanbietern ist es möglicherweise erforderlich, dass die Videorahmen an dieser Stelle geschützt werden, da Sie über den physischen Connector übertragen werden. Zu diesem Zweck gibt es verschiedene Schutzmechanismen, einschließlich High-Bandwidth Digital Content Protection (HDCP) und DisplayPort Content Protection (dpcp). Die Video-OTA erzwingt diese Schutzmaßnahmen mithilfe des [Output Protection Managers](output-protection-manager.md) (OPM). Der Output Protection Manager sendet Befehle an den Grafiktreiber, und der Grafiktreiber erzwingt, welche Schutzmechanismen für die Richtlinie erforderlich sind.

![ein Diagramm, das die Beziehung zwischen der Video-OTA und OPM anzeigt.](images/pmp05.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Info über Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Media Foundation-Architektur](media-foundation-architecture.md)
</dt> <dt>

[GPU-basiertes Content Protection](gpu-based-content-protection.md)
</dt> <dt>

[Output Protection Manager](output-protection-manager.md)
</dt> <dt>

[PMP-Medien Sitzung](pmp-media-session.md)
</dt> </dl>

 

 
