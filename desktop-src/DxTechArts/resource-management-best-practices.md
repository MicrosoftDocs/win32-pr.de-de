---
title: Bewährte Methoden für die Ressourcenverwaltung
description: In diesem Artikel werden bewährte Methoden für den allgemeinen Umgang mit Ressourcen, das Verhalten verwalteter und nicht verwalteter Ressourcen und einige Details zur Behandlung von Ressourcen in der Regel von der Laufzeit und den Treibern erläutert.
ms.assetid: 265ae0b2-f268-a4a4-551e-9d3dae886517
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf57c33ef765596ffa660ba884708ee000dd370c90edd3fcd158a9c526a7ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119213223"
---
# <a name="resource-management-best-practices"></a>Bewährte Methoden für die Ressourcenverwaltung

Verwaltete Texturen, auch als automatische Texturverwaltung bezeichnet, sind seit Version 6 in DirectX verfügbar, wobei in nachfolgenden Releases mehrere Revisionen und Verbesserungen vorgenommen wurden. Ab der Veröffentlichung der Direct3D 9-API umfasst die automatische Ressourcenverwaltung Unterstützung für Texturen, Scheitelpunktpuffer und Indexpuffer, die alle über eine konsistente freigegebene Schnittstelle verfügen. Durch die Verwendung des Direct3D-Ressourcen-Managers können Anwendungen die Behandlung von Situationen mit verlorenen Geräten erheblich vereinfachen und sich darauf verlassen, dass das System eine angemessene Menge an Zu vielen Videospeicherressourcen verarbeitet.

Entwickler haben manchmal Schwierigkeiten bei der Verwendung verwalteter Ressourcen, teilweise aufgrund der abstrakten Natur des Systems. Obwohl viele gängige Szenarien für Ressourcen gut für verwaltete Ressourcen geeignet sind, funktionieren einige Fälle besser, wenn sie nicht verwaltete Ressourcen verwenden. In diesem Artikel werden bewährte Methoden für den allgemeinen Umgang mit Ressourcen, das Verhalten verwalteter und nicht verwalteter Ressourcen und einige Details zur Behandlung von Ressourcen in der Regel von der Laufzeit und den Treibern erläutert.

In diesem Artikel werden die folgenden Konzepte behandelt:

-   [Videospeicher](#video-memory)
-   [Verwaltete Ressourcen](#managed-resources)
-   [Vom Treiber verwaltete Ressourcen](#driver-managed-resources)
-   [Standardressourcen](#default-resources)
    -   [Verwenden von verwalteten ressourcen und Standardressourcen](#using-both-managed-and-default-resources)
    -   [Dynamische Standardressourcen](#dynamic-default-resources)
-   [Systemspeicherressourcen](#system-memory-resources)
-   [Allgemeine Empfehlungen](#general-recommendations)
-   [Zugehörige Themen](#related-topics)

## <a name="video-memory"></a>Videospeicher

Damit das Videosystem eine Ressource verwenden kann, muss es sich im Arbeitsspeicher befinden, auf den die GPU zugreifen kann. Der lokale Videospeicher bietet die beste Leistung für die GPU, und bestimmte Ressourcen (wie Renderziele und Tiefen-/Schablonenpuffer) müssen sich im lokalen Videospeicher befinden. Mit der Einführung von AGP kann die GPU auch direkt auf einen Teil des Systemspeichers zugreifen. Dieser Als AGP-Öffnung bezeichnete Speicherbereich wird als nicht lokaler Videospeicher bezeichnet und ist für andere Zwecke nicht verfügbar. Der nicht lokale Videospeicher kann von der CPU gelesen und in diesen geschrieben werden. Dieser verfügt in der Regel über keinen Hochleistungszugriff auf den lokalen Videospeicher und eignet sich daher ideal für die Verwendung als freigegebene Speicherressource. Ein wichtiger Punkt beim AGP-Speicher ist, dass er wie der lokale Videospeicher in Situationen mit verlorenen Geräten ungültig wird und persistente Objekte, die sich dort befinden, wiederhergestellt werden müssen.

**Abbildung 1: Beziehung zwischen GPU, CPU, Video-RAM und System-RAM**

![Beziehung zwischen GPU, CPU, Video-RAM und System-RAM](images/managingresources1.gif)

Einige integrierte Videolösungen nutzen eine einheitliche Speicherarchitektur (Unified Memory Architecture, UMA), bei der der Hauptspeicher von allen Komponenten der Systeme adressiert werden kann. Direct3D unterstützt UMA, ohne dass änderungen an der Anwendung erforderlich sind. Dabei werden die gleichen Hinweise wie bei konfigurationen des lokalen Videospeichers verwendet. Bei solchen Systemen befinden sich Ressourcen immer im Systemspeicher, und der Treiber ist dafür verantwortlich, sicherzustellen, dass Ressourcen ähnlich wie in einer herkömmlicheren Architektur funktionieren und gleichzeitig die Uma-Eigenschaften und jedes spezifische Verhalten der Hardwareimplementierung nutzen.

**Abbildung 2. GPU und CPU haben gleichen Zugriff auf den System-RAM in einer einheitlichen Speicherarchitektur**

![GPU und CPU haben in einer einheitlichen Speicherarchitektur den gleichen Zugriff auf den System-RAM](images/managingresources2.gif)

## <a name="managed-resources"></a>Verwaltete Ressourcen

Der Großteil Ihrer Ressourcen sollte als verwaltete Ressourcen in POOL MANAGED erstellt \_ werden. Alle Ihre Ressourcen werden im Systemspeicher erstellt und nach Bedarf in den Videospeicher kopiert. Situationen mit verlorenen Geräten werden automatisch von der Systemspeicherkopie verarbeitet. Da nicht alle verwalteten Ressourcen gleichzeitig in den Videospeicher passen müssen, können Sie arbeitsspeicherüberschreiben, wenn ein kleinerer Arbeitssatz von Videoarbeitsspeicherressourcen zum Rendern in einem bestimmten Frame erforderlich ist. Beachten Sie, dass es wahrscheinlich ist, dass der Großteil dieses Sicherungsspeichersystemspeichers im Laufe der Zeit auf den Datenträger ausgelagert wird. Aus diesem Grund kann der Zurücksetzungsvorgang langsam sein, da diese Daten zurückgelagert werden müssen, um den verlorenen Videospeicher wiederherzustellen.

Die Runtime behält einen Zeitstempel für den zeitpunkt der letzten Verwendung einer Ressource bei, und wenn beim Laden einer benötigten verwalteten Ressource eine Videospeicherbelegung fehlschlägt, gibt sie Ressourcen basierend auf diesem Zeitstempel auf LRU-Weise frei. Die Verwendung von [**SetPriority**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority) hat Vorrang vor dem Zeitstempel, sodass häufig verwendete Ressourcen auf einen höheren Prioritätswert festgelegt werden sollten. Direct3D 9.0 verfügt über eingeschränkte Informationen über den vom Treiber verwalteten Videospeicher, sodass die Runtime möglicherweise mehrere Ressourcen entfernt, um eine ausreichend große Region zu erstellen, damit die Zuordnung erfolgreich ist. Richtige Prioritäten können dazu beitragen, Situationen zu beseitigen, in denen etwas entfernt wird und kurz darauf wieder erforderlich ist. Die Anwendung kann auch [**EvictManagedResources**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-evictmanagedresources) aufrufen, um zu erzwingen, dass alle verwalteten Ressourcen entfernt werden. Auch hier kann dies ein zeitaufwändiger Vorgang sein, um alle für den nächsten Frame erforderlichen Ressourcen erneut zu laden. Dies ist jedoch sehr nützlich für Ebenenübergänge, bei denen sich das Arbeitsset erheblich ändert, und zum Entfernen der Fragmentierung des Videospeichers.

Außerdem wird eine Frameanzahl beibehalten, damit die Runtime erkennen kann, ob die gerade entfernte Ressource früh im aktuellen Frame verwendet wurde. Dies impliziert eine Auslastungssituation, in der mehr Ressourcen in einem einzelnen Frame verwendet werden, als in den Videospeicher passen. Dies löst die Ersetzungsrichtlinie aus, um für den Rest des Frames zu einer MRU-Mode und nicht zu LRU zu wechseln, da dies unter solchen Bedingungen tendenziell etwas besser abschneiden kann. Ein solches Thrashingverhalten wirkt sich erheblich auf die Renderingleistung aus. Beachten Sie, dass das Konzept des aktuellen Frames an [**EndScene**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-endscene)gebunden ist, sodass jede Anwendung, die verwaltete Ressourcen verwendet, regelmäßig Aufrufe dieser Methode vornehmen muss.

Entwickler, die weitere Informationen dazu erhalten möchten, wie sich verwaltete Ressourcen in ihrer Anwendung verhalten, können die RESOURCEMANAGER-Ereignisabfrage über die [**IDirect3DQuery9-Schnittstelle**](/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dquery9) verwenden. Dies funktioniert nur bei Verwendung der Debugruntimes, sodass diese Informationen nicht von der Anwendung abhängen können, aber sie bieten ausführliche Details zu den ressourcen, die von der Runtime verwaltet werden.

Obwohl das Verständnis der Funktionsweise des Ressourcen-Managers beim Optimieren und Debuggen Ihrer Anwendungen hilfreich sein kann, ist es wichtig, ihre Anwendung nicht zu eng an die Implementierungsdetails der aktuellen Runtime oder treiber zu binden. Revisionen des Treibers oder Änderungen an der Hardware können das Verhalten erheblich ändern, und zukünftige Versionen von Direct3D haben die Ressourcenverwaltung erheblich verbessert und ausgereift.

## <a name="driver-managed-resources"></a>Driver-Managed-Ressourcen

Direct3D-Treiber können die Funktion für verwaltete Texturen des Treibers implementieren, die durch D3DCAPS2 \_ CANMANAGERESOURCE angegeben wird, wodurch der Treiber die Ressourcenverwaltung anstelle der Laufzeit verarbeiten kann. Für den (seltenen) Treiber, der dieses Feature implementiert, kann das genaue Verhalten des Ressourcen-Managers des Treibers stark variieren, und Sie sollten sich an den Hersteller des Treibers wenden, um Details zur Funktionsweise der Implementierung zu erhalten. Alternativ können Sie sicherstellen, dass der Laufzeit-Manager immer verwendet wird, indem Sie beim Erstellen des Geräts D3DCREATE \_ DISABLE \_ DRIVER MANAGEMENT \_ angeben.

## <a name="default-resources"></a>Standardressourcen

Verwaltete Ressourcen sind zwar einfach, effizient und einfach zu verwenden, aber es gibt Zeiten, in denen die direkte Verwendung des Videospeichers bevorzugt oder sogar erforderlich ist. Solche Ressourcen werden in der Kategorie POOL \_ DEFAULT erstellt. Die Nutzung solcher Ressourcen führt zu zusätzlichen Schwierigkeiten für Ihre Anwendung. Code ist erforderlich, um die Situation mit verlorenen Geräten für alle POOL DEFAULT-Ressourcen zu bewältigen, und Beim Kopieren von \_ Daten in diese Ressourcen müssen Leistungsaspekte berücksichtigt werden. Das Nichtvorgeben von USAGE \_ WRITEONLY oder das Sperren eines Renderziels kann auch schwerwiegende Leistungseinbußen nach sich bringen.

Das Aufrufen der **Sperre** für eine POOL \_ DEFAULT-Ressource führt eher dazu, dass die GPU angehalten wird als die Arbeit mit einer \_ VERWALTETEN POOL-Ressource, es sei denn, es werden bestimmte Hinweisflags verwendet. Je nach Speicherort der Ressource kann der zurückgegebene Zeiger auf einen temporären Systemspeicherpuffer oder ein Zeiger direkt auf den AGP-Speicher sein. Wenn es sich um einen temporären Systemspeicherpuffer handelt, müssen die Daten nach dem **Entsperren-Aufruf** in den Videospeicher übertragen werden. Wenn die Videoressource nicht schreibgesperrt ist, müssen daten während der **Sperre** in den temporären Puffer übertragen werden. Wenn es sich um einen AGP-Speicherbereich handelt, werden temporäre Kopien vermieden, aber das erforderliche Cacheverhalten kann zu einer langsamen Leistung führen.

Es sollte sorgfältig darauf geachtet werden, eine vollständige Cachezeile von Daten in einen Zeiger auf den AGP-Öffnungsspeicher zu schreiben, um die Einbußen beim Schreiben/Kombinieren zu vermeiden, die einen Lese-/Schreibzyklus auslösen, und der sequenzielle Zugriff auf den Speicherbereich wird bevorzugt. Wenn Ihre Anwendung während der Erstellung zufälligen Zugriff auf Daten haben muss und Sie keine verwaltete Ressource für den Puffer verwenden möchten, sollten Sie stattdessen mit einer Systemspeicherkopie arbeiten. Nachdem die Daten erstellt wurden, können Sie das Ergebnis in den gesperrten Ressourcenspeicher streamen, um zu vermeiden, dass für den Cacheschreib-Combining-Vorgang hohe Kosten entstehen.

Das LOCK \_ NOOVERWRITE-Flag kann verwendet werden, um Daten effizient für einige Ressourcen anzufügen. Im Idealfall können jedoch mehrere **Lock-** und **Unlock-Aufrufe** an dieselbe Ressource vermieden werden. Die ordnungsgemäße Verwendung der verschiedenen Sperrflags ist wichtig für eine optimale Leistung, ebenso wie die Verwendung eines cachefreundlichen Musters des Datenzugriffs beim Auffüllen von gesperrtem Speicher.

### <a name="using-both-managed-and-default-resources"></a>Verwenden von verwalteten ressourcen und Standardressourcen

Das Kombinieren von Zuordnungen verwalteter und POOL \_ DEFAULT-Ressourcen kann zu einer Fragmentierung des Videospeichers führen und die Ansicht der Laufzeit des für verwaltete Ressourcen verfügbaren Videospeichers verwirren. Im Idealfall sollten Sie alle POOL DEFAULT-Ressourcen erstellen, \_ bevor Sie VERWALTETE \_ POOL-Ressourcen verwenden, oder den [**EvictManagedResources-Aufruf**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-evictmanagedresources) nutzen, bevor Sie nicht verwaltete Ressourcen zuordnen. Denken Sie daran, dass alle Zuordnungen aus POOL \_ DEFAULT, die sich im Videospeicher befinden, Arbeitsspeicher für die Lebensdauer der Ressource binden, die für die Verwendung durch den Ressourcen-Manager oder für einen anderen Zweck nicht verfügbar ist.

Beachten Sie, dass die Runtime von Version 9 im Gegensatz zu früheren Versionen von Direct3D einige verwaltete Ressourcen automatisch entfernt, bevor sie bei fehlendem Videospeicher auf eine fehlerhafte nicht verwaltete Ressourcenzuordnung verzichten. Dies kann jedoch möglicherweise zu einer zusätzlichen Fragmentierung führen und sogar eine Ressource an einem suboptimalen Speicherort erzwingen (z. B. eine statische Textur im nicht lokalen Videospeicher). Auch hier ist es am besten, alle erforderlichen nicht verwalteten Ressourcen im Voraus und vor der Verwendung verwalteter Ressourcen zuzuordnen.

### <a name="dynamic-default-resources"></a>Dynamische Standardressourcen

Daten, die mit hoher Häufigkeit generiert und aktualisiert werden, benötigen den Sicherungsspeicher nicht, da alle Informationen beim Wiederherstellen des Geräts neu erstellt werden. Solche Daten werden in der Regel am besten in POOL DEFAULT erstellt \_ und geben den \_ DYNAMIC-Hinweis USAGE an, damit der Treiber optimierungsentscheidungen treffen kann, wenn er die Ressource platziert, da er weiß, dass sie häufig aktualisiert wird. Dies bedeutet in der Regel, dass die Ressource in einem nicht lokalen Videospeicher gespeichert wird. Daher ist der Gpu-Zugriff in der Regel viel langsamer als der lokale Videospeicher. Bei UMA-Architekturen kann der Treiber eine bestimmte Platzierung für dynamische Ressourcen auswählen, um den CPU-Schreibzugriff zu optimieren.

Diese Verwendung ist typisch für Softwareskinninglösungen und CPU-basierte Partikelsysteme, die Scheitelpunkt-/Indexpuffer auffüllen, und das LOCK \_ DISCARD-Flag stellt sicher, dass keine Hänge erstellt werden, wenn die Ressource noch aus dem vorherigen Frame verwendet wird. Die Verwendung einer verwalteten Ressource würde in diesem Fall einen Systemspeicherpuffer aktualisieren, der dann in den Videospeicher kopiert und dann nur für ein oder zwei Frames verwendet wird, bevor er ersetzt wird. Bei Systemen mit nicht lokalem Videospeicher wird die zusätzliche Kopie durch die ordnungsgemäße Verwendung dieses dynamischen Musters entfernt.

Standardtexturen können nicht gesperrt und nur über [**UpdateSurface**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface) oder [**UpdateTexture**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture)aktualisiert werden. Einige Systeme unterstützen dynamische Texturen, die gesperrt werden können, und verwenden das LOCK \_ DISCARD-Muster, aber ein Capabilities Bit (D3DCAPS2 \_ DYNAMICTEXTURES) muss überprüft werden, bevor solche Ressourcen verwendet werden. Für hochgradig dynamische Texturen (Video oder Prozeduren) könnte Ihre Anwendung mithilfe von UpdateTexture übereinstimmende POOL \_ DEFAULT- und POOL \_ SYSTEMMEM-Ressourcen erstellen und Videospeicherupdates verarbeiten.  Bei häufigen und partiellen Updates ist das **UpdateTexture-Paradigma** wahrscheinlich die bessere Wahl.

So nützlich dynamische Ressourcen auch sein können, seien Sie vorsichtig, wenn Sie Systeme entwerfen, die stark von der dynamischen Übermittlung abhängig sind. Statische Ressourcen sollten in POOL MANAGED platziert \_ werden, um eine gute Auslastung des lokalen Videospeichers sicherzustellen und die eingeschränkte Bus- und Hauptspeicherbandbreite effizienter zu nutzen. Bei ressourcen, die semi statisch sind, stellen Sie möglicherweise fest, dass die Kosten für einen gelegentlichen Upload in den lokalen Videospeicher viel geringer sind als der konstante Busdatenverkehr, der durch die Dynamische Generierung generiert wird.

## <a name="system-memory-resources"></a>Systemspeicherressourcen

Ressourcen können auch in POOL \_ SYSTEMMEM erstellt werden. Obwohl sie nicht von der Grafikpipeline verwendet werden können, können sie als Quellen zum Aktualisieren von POOL \_ DEFAULT-Ressourcen mithilfe von [**UpdateSurface**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface) oder [**UpdateTexture**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture)verwendet werden. Ihr Sperrverhalten ist einfach, obwohl es zu Hängen kommen kann, wenn sie von einer der zuvor erwähnten Methoden verwendet werden.

Obwohl sie sich im Systemspeicher befinden, sind POOL \_ SYSTEMMEM-Ressourcen auf die gleichen Formate und Funktionen (z. B. maximale Größe) beschränkt, die vom Gerätetreiber unterstützt werden. Der POOL \_ SCRATCH-Ressourcentyp ist eine weitere Form der Systemspeicherressource, die alle Formate und Funktionen nutzen kann, die von der Laufzeit unterstützt werden, aber nicht vom Gerät aufgerufen werden können. Scratch-Ressourcen sind in erster Linie für die Verwendung durch Inhaltstools vorgesehen.

**Abbildung 3: Arbeitsspeicherressourcen in Video-RAM, AGP-Öffnung und System-RAM**

![Arbeitsspeicherressourcen in Video-RAM, AGP-Öffnung und System-RAM](images/managingresources3.gif)

## <a name="general-recommendations"></a>Allgemeine Empfehlungen

Das Abrufen der technischen Implementierungsdetails der Ressourcenverwaltung ist ein langer Weg zum Erreichen Ihrer Leistungsziele für Ihre Anwendung. Die Planung der Darstellung der Ressourcen in Direct3D und des Architekturentwurfs zum rechtzeitigen Laden der Daten ist eine kompliziertere Aufgabe. Wir empfehlen eine Reihe von bewährten Methoden, wenn Sie diese Entscheidungen für Ihre Anwendung treffen:

-   Verarbeiten Sie alle Ihre Ressourcen vorab. Die Nutzung von teuren Konvertierungs- und Optimierungszeiten für Ihre Ressourcen ist während der Entwicklung praktisch, aber dies stellt eine große Leistungslast für die Computer Ihrer Benutzer dar. Vorverarbeitete Ressourcen sind schneller zu laden, schneller zu verwenden und bieten Ihnen die Möglichkeit, anspruchsvolle Off-Line-Arbeiten zu erledigen.
-   Vermeiden Sie es, viele Ressourcen pro Frame zu erstellen. Die erforderlichen Treiberinteraktionen können die CPU und GPU serialisieren, und die beteiligten Vorgänge sind stark gewichtet, da sie häufig Kernelübergänge erfordern. Verteilen Sie die Erstellung auf mehrere Frames, oder verwenden Sie Ressourcen wieder, ohne sie zu erstellen/freizugeben. Im Idealfall sollten Sie mehrere Frames warten, bevor Sie Ressourcen sperren oder freigeben, die kürzlich zum Rendern verwendet wurden.
-   Stellen Sie am Ende des Frames sicher, dass Sie die Bindung aller Ressourcenkanäle aufheben (d. b. Streamquellen, Texturstufen und aktuelle Indizes). Dadurch wird sichergestellt, dass verrauschte Verweise auf Ressourcen entfernt werden, bevor sie dazu führen, dass der Ressourcen-Manager ressourcenresident bleibt, die tatsächlich nicht mehr verwendet werden.
-   Verwenden Sie für Texturen komprimierte Formate (z. B. DXTn) mit MIP-Karten, und erwägen Sie die Verwendung eines Texturat atlas. Diese verringern die Bandbreitenanforderungen erheblich, und sie können die Gesamtgröße der Ressourcen reduzieren, wodurch sie effizienter werden.
-   Verwenden Sie für die Geometrie indizierte Geometrie, da dies beim Komprimieren von Scheitelpunktpufferressourcen hilft und moderne Videohardware stark für die Wiederverwendung von Scheitelpunkten optimiert ist. Wenn Sie programmierbare Vertex-Shader verwenden, können Sie die Scheitelpunktinformationen komprimieren und während der Vertexverarbeitung erweitern. Dies trägt wiederum dazu bei, die Bandbreitenanforderungen zu reduzieren und vertexpufferressourcen effizienter zu machen.
-   Vermeiden Sie eine Überoptimierung Ihrer Ressourcenverwaltung. Zukünftige Revisionen von Treibern, Hardware und Betriebssystem können möglicherweise Kompatibilitätsprobleme verursachen, wenn die Anwendung zu stark auf eine besonders kombinationslastig optimiert ist. Da die meisten Anwendungen CPU-gebunden sind, verursacht die teure CPU-basierte Verwaltung im Allgemeinen mehr Leistungsprobleme als sie löst.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten von Ressourcen](/windows/desktop/direct3d9/managing-resources)
</dt> <dt>

[Verlorene Geräte](/windows/desktop/direct3d9/lost-devices)
</dt> <dt>

[Leistungsoptimierungen](/windows/desktop/direct3d9/performance-optimizations)
</dt> <dt>

[Komprimierte Texturressourcen](/windows/desktop/direct3d9/compressed-texture-resources)
</dt> <dt>

[Abfragen](/windows/desktop/direct3d9/queries)
</dt> <dt>

[**D3DUSAGE**](/windows/desktop/direct3d9/d3dusage)
</dt> <dt>

[**D3DPOOL**](/windows/desktop/direct3d9/d3dpool)
</dt> <dt>

[D3DCREATE](/windows/desktop/direct3d9/d3dcreate)
</dt> </dl>

 

 