---
description: 'In diesem Thema werden drei miteinander verknüpfte Themen behandelt: geschützte Umgebung, Medieninteroperabilitätsgateway und Sperrung und Verlängerung.'
ms.assetid: e88806ae-0041-4b4a-a8df-69718a651e82
title: Geschützter Medienpfad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ebb2b22e6ad887134f91e93b43a698afdef0ebc36e1521d70e5e17fefedd8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035026"
---
# <a name="protected-media-path"></a>Geschützter Medienpfad

In diesem Thema werden drei miteinander verknüpfte Themen behandelt: geschützte Umgebung, Medieninteroperabilitätsgateway und Sperrung und Verlängerung.

-   Eine geschützte Umgebung (PROTECTED Environment, PE) ist eine Reihe von Technologien, mit denen geschützte Inhalte geschützt von und über Windows Vista auf geschützte Weise fließen können. Alle Komponenten in einer geschützten Umgebung sind vertrauenswürdig, und der Prozess ist vor Manipulationen geschützt.
-   Der geschützte Medienpfad (PMP) ist eine ausführbare Datei, die in einer geschützten Umgebung ausgeführt wird.
-   Wenn eine vertrauenswürdige Komponente in pe kompromittiert wird, wird sie nach dem fälligen Prozess widerrufen. Microsoft stellt jedoch einen Erneuerungsmechanismus bereit, um eine neuere vertrauenswürdige Version der Komponente zu installieren, sobald eine verfügbar ist.

Informationen zum Signieren geschützter Medienkomponenten mit Code signing finden Sie im Whitepaper [Code Signing for Protected Media Components in Windows Vista](/windows-hardware/test/hlk/).

Dieses Thema enthält folgende Abschnitte:

-   [Geschützte Umgebung](#protected-environment)
-   [Entwurf der geschützten Umgebung](#design-of-the-protected-environment)
-   [Geschützter Medienpfad](#protected-media-path)
    -   [Eingabevertrauensstellungsstellen](#input-trust-authorities)
    -   [Ausgabevertrauensstellungsstellen](#output-trust-authorities)
    -   [Richtlinienobjekte](#policy-objects)
    -   [Erstellen von Objekten im PMP](#creating-objects-in-the-pmp)
-   [Übersicht über die Richtlinienaushandlung](#overview-of-policy-negotiation)
-   [Widerruf und Verlängerung](#revocation-and-renewal)
-   [Schutz von Ausgabelinks](#output-link-protection)
-   [Zugehörige Themen](#related-topics)

## <a name="protected-environment"></a>Geschützte Umgebung

Der Inhaltsschutz umfasst mehrere Technologien, von denen jede versucht, sicherzustellen, dass Inhalte nicht auf eine Weise verwendet werden können, die mit der Absicht des Inhaltsbesitzers oder -anbieters inkonsistent ist. Zu diesen Technologien gehören Kopierschutz, Linkschutz, bedingter Zugriff und Verwaltung digitaler Rechte (Digital Rights Management, DRM). Die Grundlage jedes ist Vertrauen: Der Zugriff auf den Inhalt wird nur Softwarekomponenten gewährt, die den Nutzungsbedingungen für diesen Inhalt einhalten.

Um Bedrohungen durch geschützte Inhalte zu minimieren, ermöglichen Windows Vista und Media Foundation Software die Ausführung von vertrauenswürdigen Code in einer geschützten Umgebung. Ein PE ist eine Reihe von Komponenten, Richtlinien und Tools, die entwickelt wurden, um den Schutz vor Inhaltsinhalten zu erhöhen.

Bevor Sie die PE genauer untersuchen, ist es wichtig, die Bedrohungen zu verstehen, die sie minimieren soll. Angenommen, Sie verwenden eine Medienanwendung in einem Benutzermodusprozess. Die Anwendung ist mit den verschiedenen DLLs (Dynamic Link Libraries) verknüpft, die Medien-Plug-Ins wie Decoder enthalten. Andere Prozesse werden auch im Benutzermodus ausgeführt, und verschiedene Treiber werden in den Kernel geladen. Wenn kein Vertrauensmechanismus vorhanden ist, sind die folgenden Bedrohungen vorhanden:

-   Die Anwendung kann direkt auf geschützte Medien zugreifen oder den Prozessspeicher hacken.
-   Plug-Ins können direkt auf den Inhalt zugreifen oder den Prozessspeicher hacken.
-   Andere Prozesse können den Medienprozessspeicher entweder direkt oder durch Einjizieren von Code hacken.
-   Kerneltreiber können den Speicher des Medienprozesses hacken.
-   Inhalte können außerhalb des Systems über ein ungeschütztes Medium gesendet werden. (Linkschutz wurde entwickelt, um diese Bedrohung zu minimieren.)

## <a name="design-of-the-protected-environment"></a>Entwurf der geschützten Umgebung

Eine geschützte Umgebung wird in einem separaten geschützten Prozess von der Medienanwendung ausgeführt. Die Geschützte Prozessfunktion von Windows Vista verhindert, dass andere Prozesse auf den geschützten Prozess zugreifen.

Wenn ein geschützter Prozess erstellt wird, identifizieren Kernkernelkomponenten nicht vertrauenswürdige Komponenten und Plug-Ins, sodass die geschützte Umgebung das Laden ablehnen kann. Eine vertrauenswürdige Komponente ist eine Komponente, die von Microsoft entsprechend signiert wurde. Der Kernel verfolgt auch Module nach, die in ihn geladen werden, sodass die geschützte Umgebung die Wiedergabe geschützter Inhalte beenden kann, wenn ein nicht vertrauenswürdiges Modul geladen wird. Bevor eine Kernelkomponente geladen wird, überprüft der Kernel, ob sie vertrauenswürdig ist. Ander denn, vertrauenswürdige Komponenten, die bereits in PE vorhanden sind, lehnen die Verarbeitung geschützter Inhalte ab. Um dies zu ermöglichen, führen PE-Komponenten regelmäßig einen kryptografisch geschützten Handshake mit dem Kernel aus. Wenn eine nicht vertrauenswürdige Kernelmoduskomponente vorhanden ist, schlägt der Handshake fehl und gibt dem PE an, dass eine nicht vertrauenswürdige Komponente vorhanden ist.

Wenn eine vertrauenswürdige Komponente kompromittiert wird, kann sie nach dem fälligen Prozess widerrufen werden. Microsoft bietet einen Erneuerungsmechanismus zum Installieren einer neueren vertrauenswürdigen Version, falls verfügbar.

## <a name="protected-media-path"></a>Geschützter Medienpfad

Der geschützte Medienpfad (PMP) ist die primäre ausführbare PE-Datei für Media Foundation. Der PMP ist erweiterbar, sodass Mechanismen zum Schutz von Inhalten von Drittanbietern unterstützt werden können.

Der PMP akzeptiert geschützte Inhalte und zugehörige Richtlinien von jeder Media Foundation quelle mithilfe eines beliebigen Inhaltsschutzsystems, einschließlich der von Drittanbietern bereitgestellten. Sie sendet Inhalte an Media Foundation Senke, solange die Senke den von der Quelle angegebenen Richtlinien entspricht. Sie unterstützt auch Transformationen zwischen Quelle und Senke, einschließlich Drittanbietertransformationen, solange sie vertrauenswürdig sind.

Der PMP wird in einem geschützten Prozess ausgeführt, der von der Medienanwendung isoliert ist. Die Anwendung kann nur Befehls- und Steuerungsmeldungen mit dem PMP austauschen, hat jedoch keinen Zugriff auf Inhalte, nachdem sie an den PMP übergeben wurden. Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![Diagramm des Geschützten Medienpfads](images/pmp04.png)

Schattierte Felder stellen Komponenten dar, die möglicherweise von Drittanbietern bereitgestellt werden. Alle im geschützten Prozess erstellten Komponenten müssen signiert und vertrauenswürdig sein.

Die Anwendung erstellt eine Instanz der Mediensitzung innerhalb des geschützten Prozesses und empfängt einen Zeiger auf eine Proxymediensitzung, die Schnittstellenzeiger über die Prozessgrenze marshallt.

Die Medienquelle kann entweder innerhalb des Anwendungsprozesses, wie hier gezeigt, oder innerhalb des geschützten Prozesses erstellt werden. Wenn die Medienquelle innerhalb des Anwendungsprozesses erstellt wird, erstellt die Quelle einen Proxy für sich selbst im geschützten Prozess.

Alle anderen Pipelinekomponenten, z. B. Decoder und Mediensenken, werden im geschützten Prozess erstellt. Wenn diese Objekte benutzerdefinierte Schnittstellen für Anwendungen verfügbar machen, müssen sie einen DCOM-Proxy/Stub bereitstellen, um die Schnittstelle zu marshallen.

Um Richtlinien für geschützte Inhalte zu erzwingen, während sie durch die Pipeline fließen, verwendet der PMP drei Arten von Komponenten: Eingabevertrauensstellungsstellen (INPUT Trust Authorities, ITAs), Ausgabevertrauensstellungsstellen (Output Trust Authorities, OTAs) und Richtlinienobjekte. Diese Komponenten arbeiten zusammen, um Rechte zur Verwendung von Inhalten zu gewähren oder einzuschränken und die Linkschutzelemente anzugeben, die bei der Wiedergabe von Inhalten verwendet werden müssen, z. B. High-bandwidth Digital Content Protection (HDCP).

### <a name="input-trust-authorities"></a>Eingabevertrauensstellungsstellen

Ein ITA wird von einer vertrauenswürdigen Medienquelle erstellt und führt mehrere Funktionen aus:

-   Gibt Die Rechte zur Verwendung von Inhalt an. Rechte können das Recht beinhalten, Inhalte wieder zu spielen, auf ein Gerät zu übertragen und so weiter. Sie definiert eine geordnete Liste der genehmigten Ausgabeschutzsysteme und die entsprechenden Ausgaberichtlinien für jedes System. Die ITA speichert diese Informationen in einem Richtlinienobjekt.
-   Stellt den Entschlüsselungsschlüssel für die Entschlüsselung des Inhalts zurEntschlüsselung zur
-   Richtet eine Vertrauensstellung mit dem Kernelmodul in der geschützten Umgebung ein, um sicherzustellen, dass das ITA in einer vertrauenswürdigen Umgebung ausgeführt wird.

Ein ITA ist einem einzelnen Stream zugeordnet, der geschützte Inhalte enthält. Ein Stream kann nur ein ITA haben, und eine Instanz eines ITA kann nur einem Stream zugeordnet werden.

### <a name="output-trust-authorities"></a>Ausgabevertrauensstellungsstellen

Eine OTA ist einer vertrauenswürdigen Ausgabe zugeordnet. Das OTA macht eine Aktion verfügbar, die die vertrauenswürdige Ausgabe für den Inhalt ausführen kann, z. B. Wiedergabe oder Kopiermodus. Die Aufgabe besteht in der Erzwingung eines oder mehrere Ausgabeschutzsysteme, die vom ITA benötigt werden. Der OTA fragt das von ITA bereitgestellte Richtlinienobjekt ab, um zu bestimmen, welches Schutzsystem erzwungen werden muss.

### <a name="policy-objects"></a>Richtlinienobjekte

Ein Richtlinienobjekt kapselt die Anforderungen an den Inhaltsschutz eines ITA. Sie wird von der Richtlinien-Engine verwendet, um die Unterstützung des Inhaltsschutzes mit einem OTA auszuhandeln. OTAs fragen Richtlinienobjekte ab, um zu bestimmen, welche Schutzsysteme sie für jede Ausgabe des aktuellen Inhalts erzwingen müssen.

### <a name="creating-objects-in-the-pmp"></a>Erstellen von Objekten im PMP

Um ein Objekt im geschützten Medienpfad (PMP) zu erstellen, ruft [**DIE -KLASSE**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) [**IMFPMPHostApp::ActivateClassById**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphostapp-activateclassbyid)auf, wobei der angegebene **Eingabe-IStream** wie folgt formatiert ist:

``` syntax
Format: (All DWORD values are serialized in little-endian order)
[GUID (content protection system guid, obtained from Windows.Media.Protection.MediaProtectionSystemId)]
[DWORD (track count, use the actual track count even if all tracks are encrypted using the same data, note that zero is invalid)]
[DWORD (next track ID, use -1 if all remaining tracks are encrypted using the same data)]
[DWORD (next track's binary data size)]
[BYTE* (next track's binary data)]
{ Repeat from "next track ID" above for each stream }
```

## <a name="overview-of-policy-negotiation"></a>Übersicht über die Richtlinienaushandlung

Es gibt drei grundlegende Anforderungen, die erfüllt sein müssen, bevor geschützte Inhalte im PMP verarbeitet werden können. Zunächst müssen geschützte Inhalte nur an vertrauenswürdige Ausgaben gesendet werden. Zweitens müssen nur zulässige Aktionen auf einen Stream angewendet werden. Drittens müssen nur genehmigte Ausgabeschutzsysteme für die Wiedergabe eines Streams verwendet werden. Die Richtlinien-Engine koordiniert zwischen ITAs und OTAs, um sicherzustellen, dass diese Anforderungen erfüllt werden.

Die einfachste Möglichkeit, den Prozess zu verstehen, besteht in einem vereinfachten Beispiel, das die erforderlichen Schritte zum Wiederverspielen von ASF-Inhalten (Advanced System Format) beschreibt, die durch Windows Media Digital Rights Management (WMDRM) geschützt sind.

Wenn ein Benutzer eine Playeranwendung startet und eine ASF-Datei öffnet, die über einen geschützten Audiostream und einen geschützten Videostream verfügt, müssen die folgenden Schritte ausgeführt werden:

1.  Die Anwendung erstellt die ASF-Medienquelle und die PMP-Sitzung (Protected Media Path). Media Foundation erstellt einen PMP-Prozess.
2.  Die Anwendung erstellt eine Teiltopologie, die einen mit dem Audiorenderer verbundenen Audioquellenknoten und einen Videoquellenknoten enthält, der mit dem erweiterten Videorenderer (EVR) verbunden ist. Für die Renderer erstellt die Anwendung den Renderer nicht direkt. Stattdessen erstellt die Anwendung im ungeschützten Prozess ein Objekt, das als *Aktivierungsobjekt bezeichnet wird.* Der PMP verwendet das Aktivierungsobjekt, um die Renderer im geschützten Prozess zu erstellen. (Weitere Informationen zu Aktivierungsobjekten finden Sie unter [Activation Objects](activation-objects.md).)
3.  Die Anwendung legt die Teiltopologie für die PMP-Sitzung fest.
4.  Die PMP-Sitzung serialisiert die Topologie und übergibt sie im geschützten Prozess an den PMP-Host. Der PMP-Host sendet die Topologie an die Richtlinien-Engine.
5.  Das Topologielader ruft AUF DEN ITAs [**DEN WERTINPUTTrustAuthority::GetDecrypter**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) auf und fügt die Decrypter direkt nach den entsprechenden Quellknoten in die Topologie ein.
6.  Das Topologielader fügt die Audio- und Videodecoder nach den Entschlüsselungsknoten ein.
7.  Die Richtlinien-Engine scannt die eingefügten Knoten, um zu bestimmen, ob [**eine der Knoten die BERTRUSTEDOutput-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imftrustedoutput) implementiert. Die EVR und der Audiorenderer implementieren **beide DENTTtrustedOutput,** da sie Daten außerhalb des PMP senden.
8.  Jedes ITA bestätigt, dass es in einem geschützten Prozess ausgeführt wird, indem ein kryptografischer Handshake mit einem Kernelmodul der geschützten Umgebung ausgeführt wird.
9.  Für jeden Stream handelt die Richtlinien-Engine die Richtlinie aus, indem sie ein Richtlinienobjekt vom ITA abfing und an die OTA überträgt. Die OTA stellt eine Liste der unterstützten Schutzsysteme zur Verfügung, und das Richtlinienobjekt gibt an, welche Schutzsysteme zusammen mit den richtigen Einstellungen angewendet werden müssen. Das OTA wendet dann diese Einstellungen an. Wenn dies nicht möglich ist, wird der Inhalt blockiert.

## <a name="revocation-and-renewal"></a>Widerruf und Verlängerung

Eine vertrauenswürdige Komponente kann widerrufen werden, wenn sie kompromittiert wird oder festgestellt wird, dass sie gegen die Lizenzverträge verstoßen hat, unter denen sie ursprünglich als vertrauenswürdig eingestuft wurde. Ein Erneuerungsmechanismus ist vorhanden, um eine neuere, vertrauenswürdigere Version der Komponente zu installieren.

Vertrauenswürdige Komponenten werden mit einem kryptografischen Zertifikat signiert. Microsoft veröffentlicht eine globale Sperrliste (GRL), die gesperrte Komponenten identifiziert. Der GRL wird digital signiert, um seine Authentizität sicherzustellen. Inhaltsbesitzer können über den Richtlinienmechanismus sicherstellen, dass die aktuelle Version der GRL auf dem Computer des Benutzers vorhanden ist.

## <a name="output-link-protection"></a>Schutz von Ausgabelinks

Wenn Premium-Videoinhalte angezeigt werden, werden die entschlüsselten, unkomprimierten Frames über einen physischen Connector zum Anzeigegerät übertragen. Inhaltsanbieter erfordern möglicherweise, dass die Videoframes an diesem Punkt geschützt werden, wenn sie über den physischen Connector hinweg verwendet werden. Zu diesem Zweck gibt es verschiedene Schutzmechanismen, einschließlich High-Bandwidth Digital Content Protection (HDCP) und DisplayPort Content Protection (DPCP). Das Video OTA erzwingt diese Schutzmaßnahmen mithilfe des [Ausgabeschutz-Managers](output-protection-manager.md) (Output Protection Manager, OPM). Der Ausgabeschutz-Manager sendet Befehle an den Grafiktreiber, und der Grafiktreiber erzwingt alle Linkschutzmechanismen, die für die Richtlinie erforderlich sind.

![Ein Diagramm, das die Beziehung zwischen dem Video ota und opm zeigt.](images/pmp05.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Info über Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Media Foundation-Architektur](media-foundation-architecture.md)
</dt> <dt>

[GPU-basierte Content Protection](gpu-based-content-protection.md)
</dt> <dt>

[Ausgabeschutz-Manager](output-protection-manager.md)
</dt> <dt>

[PMP-Mediensitzung](pmp-media-session.md)
</dt> </dl>

 

 
