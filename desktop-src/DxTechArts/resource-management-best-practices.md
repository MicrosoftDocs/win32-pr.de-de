---
title: Bewährte Methoden für die Ressourcenverwaltung
description: In diesem Artikel werden bewährte Methoden für den Umgang mit Ressourcen in der Regel erläutert, wie sich verwaltete und nicht verwaltete Ressourcen Verhalten, und es werden einige Details dazu bereitstellt, wie Ressourcen normalerweise von der Laufzeit und den Treibern verarbeitet werden
ms.assetid: 265ae0b2-f268-a4a4-551e-9d3dae886517
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cdadb8cee3cb57f4208657054784937ecd1ea2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315855"
---
# <a name="resource-management-best-practices"></a>Bewährte Methoden für die Ressourcenverwaltung

Verwaltete Texturen, die auch als automatische Textur Verwaltung bezeichnet werden, sind seit Version 6 in DirectX verfügbar, wobei einige Revisionen und Erweiterungen in nachfolgenden Versionen vorgenommen wurden. Ab der Veröffentlichung der Direct3D 9-API unterstützt die automatische Ressourcenverwaltung die Unterstützung für Texturen, Vertex-Puffer und Index Puffer, alle mit einer konsistenten freigegebenen Schnittstelle. Durch die Verwendung des Ressourcen-Managers von Direct3D können Anwendungen die Handhabung verlorener Geräte erheblich vereinfachen und sich darauf verlassen, dass das System eine angemessene Menge an Videospeicher Ressourcen verarbeitet.

Entwickler haben manchmal Schwierigkeiten bei der Verwendung verwalteter Ressourcen, teilweise aufgrund der abstrakten Natur des Systems. Obwohl viele gängige Szenarien für Ressourcen für verwaltete Ressourcen gut geeignet sind, können einige Fälle bei der Verwendung nicht verwalteter Ressourcen besser funktionieren. In diesem Artikel werden bewährte Methoden für den Umgang mit Ressourcen in der Regel erläutert, wie sich verwaltete und nicht verwaltete Ressourcen Verhalten, und es werden einige Details dazu bereitstellt, wie Ressourcen normalerweise von der Laufzeit und den Treibern verarbeitet werden

In diesem Artikel werden die folgenden Konzepte behandelt:

-   [Video Speicher](#video-memory)
-   [Verwaltete Ressourcen](#managed-resources)
-   [Vom Treiber verwaltete Ressourcen](#driver-managed-resources)
-   [Standardressourcen](#default-resources)
    -   [Verwenden verwalteter und standardmäßiger Ressourcen](#using-both-managed-and-default-resources)
    -   [Dynamische Standard Ressourcen](#dynamic-default-resources)
-   [System Speicherressourcen](#system-memory-resources)
-   [Allgemeine Empfehlungen](#general-recommendations)
-   [Zugehörige Themen](#related-topics)

## <a name="video-memory"></a>Video Speicher

Damit das Videosystem eine Ressource verwendet, muss Sie sich im Arbeitsspeicher befinden, auf den die GPU zugreifen kann. Der lokale Videospeicher bietet die beste Leistung für die GPU, und bestimmte Ressourcen (z. b. Renderziele und Tiefe/Schablonen Puffer) müssen sich im lokalen Videospeicher befinden. Mit der Einführung von AGP kann die GPU auch direkt auf einen Teil des System Arbeitsspeichers zugreifen. Dieser Speicherbereich, der als AGP-Aperture bezeichnet wird, wird als nicht lokaler Videospeicher bezeichnet und ist nicht für andere Zwecke verfügbar. Nicht lokaler Videospeicher kann von der CPU gelesen und geschrieben werden, die in der Regel keinen hochleistungsfähigen Zugriff auf den lokalen Videospeicher hat und daher ideal für die Verwendung als freigegebene Speicher Ressource ist. Ein wichtiger Aspekt für den AGP-Arbeitsspeicher ist, dass er wie der lokale Video Arbeitsspeicher in verlorenen Geräte Fällen ungültig ist und dass persistente Assets wieder hergestellt werden müssen.

**Abbildung 1. Beziehung zwischen GPU, CPU, Video RAM und System-RAM**

![Beziehung zwischen GPU, CPU, Video RAM und System-RAM](images/managingresources1.gif)

Einige integrierte Videolösungen nutzen eine Unified Memory Architecture (UMA), bei der der Hauptspeicher von allen Komponenten der Systeme adressierbar ist. Direct3D unterstützt UMA, ohne dass Änderungen an der Anwendung erforderlich sind. dabei werden dieselben Hinweise wie für lokale Videospeicher Konfigurationen genutzt. Bei solchen Systemen befinden sich Ressourcen immer im Systemspeicher, und der Treiber ist dafür verantwortlich, sicherzustellen, dass die Ressourcen sehr ähnlich wie in einer herkömmlichen Architektur funktionieren und dabei die Eigenschaften von Uma und ein bestimmtes Verhalten der Hardware Implementierung nutzen.

**Abbildung 2. GPU und CPU haben gleichen Zugriff auf den System-RAM in einer vereinheitlichten Speicherarchitektur**

![GPU und CPU haben gleichen Zugriff auf den System-RAM in einer vereinheitlichten Speicherarchitektur](images/managingresources2.gif)

## <a name="managed-resources"></a>Verwaltete Ressourcen

Der Großteil ihrer Ressourcen sollte als verwaltete Ressourcen in der Pool Verwaltung erstellt werden \_ . Alle Ressourcen werden im Systemspeicher erstellt und dann nach Bedarf in den Videospeicher kopiert. Verlorene Geräte Situationen werden automatisch über die Systemspeicher Kopie behandelt. Da nicht alle verwalteten Ressourcen gleichzeitig in den Videospeicher eingefügt werden müssen, können Sie den Arbeitsspeicher überschreiben, bei dem ein kleineres Arbeits Satz von Arbeitsspeicher Ressourcen für das Rendering in einem beliebigen Frame benötigt wird. Beachten Sie, dass es wahrscheinlich ist, dass der Großteil dieses Sicherungs Speicher-System Arbeitsspeichers über einen Zeitraum auf den Datenträger ausgelagert wird. aus diesem Grund kann der Zurücksetzungs Vorgang langsam sein, da Sie diese Daten zurücksetzen müssen, um den verlorenen Videospeicher wiederherzustellen.

Die Laufzeit behält einen Zeitstempel für den Zeitpunkt der letzten Verwendung einer Ressource bei, und wenn die Speicher Belegung eines Videos beim Laden einer benötigten verwalteten Ressource fehlschlägt, werden Ressourcen basierend auf diesem Zeitstempel in einer LRU-Weise freigegeben. Die Verwendung von [**SetPriority**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority) hat Vorrang vor dem Zeitstempel, sodass für häufig verwendete Ressourcen ein höherer Prioritätswert festgelegt werden sollte. Direct3D 9,0 weist eingeschränkte Informationen über den vom Treiber verwalteten Videospeicher auf. Daher muss die Laufzeit möglicherweise mehrere Ressourcen entfernen, um einen ausreichend großen Bereich zu erstellen, damit die Zuordnung erfolgreich ist. Die richtigen Prioritäten können dabei helfen, Situationen auszuschließen, in denen etwas entfernt wird, und dann in Kürze erneut erforderlich ist. Die Anwendung kann auch [**evictmanagedresources**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-evictmanagedresources) aufzurufen, um zu erzwingen, dass alle verwalteten Ressourcen entfernt werden. Auch hier kann es sich um einen zeitaufwändigen Vorgang zum erneuten Laden aller für den nächsten Frame benötigten Ressourcen handeln. er ist jedoch sehr nützlich für Ebenenübergänge, bei denen sich das Workingset erheblich ändert und die Fragmentierung des Grafik Speichers entfernt wird.

Eine Frame Anzahl wird auch beibehalten, damit von der Common Language Runtime erkannt werden kann, ob die Ressource, die gerade entfernt wurde, früher als aktueller Frame verwendet wurde. Dies impliziert eine Überlastung, bei der mehr Ressourcen in einem einzelnen Frame verwendet werden, als in den Videospeicher passen. Dadurch wird die Ersetzungs Richtlinie ausgelöst, um für den Rest des Frames auf eine MRU-Weise anstelle von LRU zu wechseln, da dies unter solchen Bedingungen tendenziell etwas besser ist. Dieses Verhalten der Überlastung wirkt sich erheblich auf die Renderingleistung aus. Beachten Sie, dass das Konzept des aktuellen Frames an [**EndScene**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-endscene)gebunden ist, sodass jede Anwendung, die verwaltete Ressourcen verwendet, regelmäßig Aufrufe an diese Methode ausführen muss.

Entwickler, die mehr Informationen darüber finden, wie sich verwaltete Ressourcen in Ihrer Anwendung Verhalten, können die ResourceManager-Ereignis Abfrage über die [**IDirect3DQuery9**](/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dquery9) -Schnittstelle verwenden. Dies funktioniert nur bei Verwendung der debuglaufzeiten, sodass diese Informationen von der Anwendung nicht abhängig sind. Sie erhalten jedoch ausführliche Informationen zu den Ressourcen, die von der Laufzeit verwaltet werden.

Wenn Sie wissen, wie der Ressourcen-Manager funktioniert, wenn Sie Ihre Anwendungen optimieren und Debuggen, ist es wichtig, die Anwendung nicht zu eng an die Implementierungsdetails der aktuellen Laufzeit oder der Treiber zu binden. Änderungen des Treibers oder der Hardwareänderungen können das Verhalten erheblich ändern, und zukünftige Versionen von Direct3D verfügen über eine deutlich verbesserte und ausgereifte Ressourcenverwaltung.

## <a name="driver-managed-resources"></a>Driver-Managed Ressourcen

Direct3D-Treiber können die vom Treiber verwaltete Texturen-Funktion implementieren, die durch D3DCAPS2 \_ canmanageresource angegeben wird, sodass der Treiber die Ressourcenverwaltung anstelle der Laufzeit verarbeiten kann. Für den (seltenen) Treiber, der diese Funktion implementiert, kann das genaue Verhalten des Ressourcen-Managers des Treibers stark variieren, und Sie sollten sich an den Hersteller des Treibers wenden, um ausführliche Informationen zur Funktionsweise für die Implementierung zu erhalten. Wahlweise können Sie auch sicherstellen, dass der Lauf Zeit-Manager immer verwendet wird, indem Sie \_ \_ \_ beim Erstellen des Geräts D3DCREATE Deaktivieren der Treiber Verwaltung angeben.

## <a name="default-resources"></a>Standardressourcen

Verwaltete Ressourcen sind zwar einfach, effizient und leicht zu verwenden, aber es gibt Zeiten, in denen Sie den Videospeicher direkt bevorzugen oder sogar benötigen. Diese Ressourcen werden in der Standard Kategorie des Pools erstellt \_ . Die Verwendung solcher Ressourcen führt zu zusätzlichen Komplikationen für Ihre Anwendung. Code ist erforderlich, um die Situation verlorener Geräte für alle Standard Ressourcen des Pools zu bewältigen \_ , und beim Kopieren von Daten in die Daten müssen Leistungsaspekte berücksichtigt werden. Wenn Sie nicht \_ nur die Verwendung schreiben oder eine renderzielsperre festlegen, kann dies zu schwerwiegenden Leistungseinbußen führen.

Das Aufrufen einer **Sperre** für eine Pool- \_ Standardressource bewirkt wahrscheinlich, dass die GPU nicht mehr als eine von Pools \_ verwaltete Ressource funktioniert, es sei denn, es werden bestimmte Hinweis Flags verwendet. Abhängig vom Speicherort der Ressource kann der zurückgegebene Zeiger zu einem temporären Systemspeicher Puffer werden, oder es kann ein Zeiger direkt in den AGP-Speicher sein. Wenn es sich um einen temporären Systemspeicher Puffer handelt, müssen Daten nach dem **entsperren** -Befehl in den Videospeicher übertragen werden. Wenn die Video Ressource nicht schreibgeschützt ist, müssen die Daten während der **Sperre** in den temporären Puffer übertragen werden. Wenn es sich um einen AGP-Speicherbereich handelt, werden temporäre Kopien vermieden, aber das erforderliche Cache Verhalten kann zu einer langsamen Leistung führen.

Es sollte darauf geachtet werden, eine vollständige Cache Daten Zeile in einen beliebigen Zeiger auf den AGP-Öffnungs Speicher zu schreiben, um das Schreiben von Schreib Vorgriffen zu vermeiden. Dadurch wird ein Lese-/Schreib-Cycle ausgelöst, und der sequenzielle Zugriff auf den Speicherbereich wird bevorzugt. Wenn Ihre Anwendung während der Erstellung zufälligen Zugriff auf Daten erstellen muss und Sie keine verwaltete Ressource für den Puffer verwenden möchten, sollten Sie stattdessen mit einer Kopie des System Speichers arbeiten. Nachdem die Daten erstellt wurden, können Sie das Ergebnis in den gesperrten Ressourcen Speicher streamen, um zu vermeiden, dass für den Cache Schreibvorgang ein hoher Verlust gezahlt wird.

Das Flag "Lock \_ noüberschreibung" kann verwendet werden, um Daten auf effiziente Weise für einige Ressourcen anzufügen, aber im Idealfall können mehrere **Sperr** -und **entsperrungs** Aufrufe für dieselbe Ressource vermieden werden. Die ordnungsgemäße Verwendung der verschiedenen Sperrflags ist wichtig für eine optimale Leistung, wie bei der Verwendung eines Cache freundlichen Datenzugriffs Musters beim Auffüllen des gesperrten Speichers.

### <a name="using-both-managed-and-default-resources"></a>Verwenden verwalteter und standardmäßiger Ressourcen

Das Kombinieren von Zuordnungen von verwalteten und Pool \_ -Standard Ressourcen kann eine Fragmentierung des Grafik Speichers verursachen und die Ansicht des für verwaltete Ressourcen verfügbaren Video Speichers in der Laufzeit verwechseln. Im Idealfall sollten Sie alle Pool- \_ Standard Ressourcen erstellen, bevor Sie von \_ Pools verwaltete Ressourcen verwenden oder den [**evictmanagedresources**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-evictmanagedresources) -Befehl verwenden, bevor Sie nicht verwaltete Ressourcen zuordnen. Beachten Sie, dass alle Zuordnungen aus \_ dem Pool Standard, die sich im Videospeicher befinden, den Arbeitsspeicher für die Lebensdauer der Ressource, die nicht für die Verwendung durch den Ressourcen-Manager verfügbar ist, oder für einen anderen Zweck

Beachten Sie, dass im Gegensatz zu früheren Versionen von Direct3D automatisch einige verwaltete Ressourcen entfernt werden, bevor bei nicht verwalteten Ressourcen Zuordnungen ein fehlender Videospeicher vorhanden ist. Dies kann jedoch zu einer zusätzlichen Fragmentierung führen und sogar eine Ressource in einem suboptimalen Speicherort erzwingen (z. b. eine statische Textur im nicht lokalen Videospeicher). Auch hier empfiehlt es sich, alle erforderlichen nicht verwalteten Ressourcen vorab und vor der Verwendung verwalteter Ressourcen zuzuordnen.

### <a name="dynamic-default-resources"></a>Dynamische Standard Ressourcen

Daten, die mit hoher Häufigkeit generiert und aktualisiert werden, benötigen den Sicherungs Speicher nicht, da alle Informationen beim Wiederherstellen des Geräts neu erstellt werden. Diese Daten werden in der Regel in \_ der Standardeinstellung des Pools erstellt und \_ geben den dynamischen Verwendungs Hinweis an, sodass der Treiber beim Platzieren der Ressource Optimierungs Entscheidungen treffen kann, da er weiß, dass er häufig aktualisiert wird. Dies bedeutet in der Regel, dass die Ressource nicht in den lokalen Videospeicher versetzt wird. Daher ist die GPU in der Regel viel langsamer als der lokale Videospeicher. Bei Uma-Architekturen wählt der Treiber möglicherweise eine bestimmte Platzierung für dynamische Ressourcen aus, um den CPU-Schreibzugriff zu optimieren.

Diese Verwendung ist typisch für softwareskinning-Lösungen und CPU-basierte Partikelsysteme, die Vertex-/Indexpuffer ausfüllen. das Flag zum Sperren \_ verwerfen stellt sicher, dass keine Staus in Fällen erstellt werden, in denen die Ressource noch aus dem vorherigen Frame verwendet wird. Wenn Sie in diesem Fall eine verwaltete Ressource verwenden, aktualisieren Sie einen Systemspeicher Puffer, der dann in den Videospeicher kopiert und dann nur für einen Frame oder zwei verwendet wird, bevor Sie ersetzt werden. Bei Systemen mit nicht lokalem Videospeicher wird die zusätzliche Kopie durch die ordnungsgemäße Verwendung dieses dynamischen Musters entfernt.

Standard Texturen können nicht gesperrt werden und können nur über [**updatesurface**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface) oder [**UpdateTexture**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture)aktualisiert werden. Einige Systeme unterstützen dynamische Texturen, die gesperrt werden können, und verwenden das \_ sperrenverwerfungs-Muster, aber ein Funktionen-Bit (D3DCAPS2 \_ dynamictexturen) muss geprüft werden, bevor diese Ressourcen verwendet werden können. Für hochdynamische Texturen (Video oder Prozeduren) könnte Ihre Anwendung übereinstimmende Pool \_ -Standard \_ Ressourcen und-Pool System-Ressourcen erstellen und Video-Memory-Updates mithilfe von **UpdateTexture** verarbeiten. Bei sehr häufigen und partiellen Aktualisierungen ist das **UpdateTexture** -Paradigma wahrscheinlich die bessere Wahl.

So nützlich wie dynamische Ressourcen sein können, sollten Sie beim Entwerfen von Systemen, die stark auf dynamische Übermittlung basieren, vorsichtig sein. Statische Ressourcen sollten in Pools verwaltet werden, \_ um sowohl eine gute Auslastung des lokalen Grafik Speichers sicherzustellen als auch eine effizientere Nutzung der Bandbreite für den Bus und den Hauptspeicher zu ermöglichen. Für Ressourcen, die halb statisch sind, können Sie feststellen, dass die Kosten für einen gelegentlichen Upload auf den lokalen Videospeicher wesentlich geringer sind als der durch dynamische Bus-Datenverkehr, der durch dynamische Erstellung von Daten verursacht wird.

## <a name="system-memory-resources"></a>System Speicherressourcen

Ressourcen können auch in \_ poolsystemmem erstellt werden. Obwohl Sie nicht von der Grafik Pipeline verwendet werden können, können Sie als Quellen zum Aktualisieren \_ von Standard Ressourcen des Pools mithilfe von [**updatesurface**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface) oder [**UpdateTexture**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture)verwendet werden. Das Sperr Verhalten ist einfach, auch wenn Sie von einer der zuvor erwähnten Methoden verwendet werden können.

Obwohl Sie sich im Systemspeicher befinden, \_ sind die Ressourcen des Pool Systems auf die gleichen Formate und Funktionen (z. b. die maximale Größe) beschränkt, die vom Gerätetreiber unterstützt werden. Der \_ Ressourcentyp "Pool Scratch" ist eine andere Form der Systemspeicher Ressource, die alle von der Laufzeit unterstützten Formate und Funktionen nutzen kann, auf die das Gerät jedoch nicht zugreifen kann. GRUNDRESSOURCEN sind hauptsächlich für die Verwendung durch Inhalts Tools vorgesehen.

**Abbildung 3. Arbeitsspeicher Ressourcen in Video-RAM, AGP-Aperture und System-RAM**

![Arbeitsspeicher Ressourcen in Video-RAM, AGP-Aperture und System-RAM](images/managingresources3.gif)

## <a name="general-recommendations"></a>Allgemeine Empfehlungen

Das erzielen der technischen Implementierungsdetails für die Ressourcenverwaltung ist ein langer Weg, um Ihre Leistungsziele für Ihre Anwendung zu erreichen. Die Planung der Bereitstellung der Ressourcen für Direct3D und das Architektur Design, um die Daten rechtzeitig zu laden, ist eine kompliziertere Aufgabe. Wir empfehlen eine Reihe bewährter Methoden, wenn Sie diese Entscheidungen für Ihre Anwendung treffen:

-   Verarbeiten Sie alle Ihre Ressourcen vorab. Wenn Sie sich auf eine teure Lade Zeit-und Optimierungs Optimierung für Ihre Ressourcen verlassen, ist es während der Entwicklung praktisch, aber auf diese Weise ist die Leistung Ihrer Benutzer Computer sehr hoch. Vorab verarbeitete Ressourcen sind schneller zu laden und schneller zu verwenden, und Sie haben die Möglichkeit, ausgereifte Offline Arbeiten durchführen zu können.
-   Vermeiden Sie das Erstellen von vielen Ressourcen pro Frame. Die erforderlichen Treiber Interaktionen können die CPU und die GPU serialisieren, und die beteiligten Vorgänge sind schwerwiegend, da Sie häufig Kernel Übergänge erfordern. Verteilen Sie die Erstellung über mehrere Frames, oder verwenden Sie Ressourcen, ohne Sie zu erstellen oder freizugeben. Im Idealfall sollten Sie mehrere Frames warten, bevor Sie Ressourcen sperren oder freigeben, die vor kurzem zum Rendervorgang verwendet wurden.
-   Stellen Sie am Ende des Frames sicher, dass die Bindung aller Ressourcen Kanäle (d. h. Datenstrom Quellen, Textur Stufen und aktuelle Indizes) aufgehoben wird. Dadurch wird sichergestellt, dass verbleibende Verweise auf Ressourcen entfernt werden, bevor Sie den Ressourcen-Manager dazu veranlassen, Ressourcen Residenten, die tatsächlich nicht mehr verwendet werden.
-   Verwenden Sie für Texturen komprimierte Formate (z. b. DXTn) mit MIP-Maps, und verwenden Sie die Verwendung eines Textur Atlas. Dadurch werden die Bandbreitenanforderungen erheblich reduziert, und Sie können die Gesamtgröße der Ressourcen verringern, sodass Sie effizienter werden.
-   Verwenden Sie für Geometrie die indizierte Geometrie, da dies dazu beiträgt, Vertex-Puffer Ressourcen zu komprimieren, und die moderne Video Hardware ist für die Wiederverwendung von Vertices stark optimiert. Durch die Verwendung programmierbarer Vertex-Shader können Sie die Scheitelpunkt Informationen komprimieren und während der Vertexverarbeitung erweitern. Dies trägt auch dazu bei, die Bandbreitenanforderungen zu verringern und Vertex-Puffer Ressourcen effizienter zu machen.
-   Vermeiden Sie eine über Optimierung Ihrer Ressourcenverwaltung. Zukünftige Revisionen von Treibern, Hardware und Betriebssystem können zu Kompatibilitätsproblemen führen, wenn die Anwendung zu stark auf eine besondere Kombination abgestimmt ist. Da die meisten Anwendungen CPU-gebunden sind, verursacht die teure CPU-basierte Verwaltung im Allgemeinen mehr Leistungsprobleme, als Sie löst.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten von Ressourcen](/windows/desktop/direct3d9/managing-resources)
</dt> <dt>

[Verlorene Geräte](/windows/desktop/direct3d9/lost-devices)
</dt> <dt>

[Leistungsoptimierungen](/windows/desktop/direct3d9/performance-optimizations)
</dt> <dt>

[Komprimierte Textur Ressourcen](/windows/desktop/direct3d9/compressed-texture-resources)
</dt> <dt>

[Abfragen](/windows/desktop/direct3d9/queries)
</dt> <dt>

[**D3DUSAGE**](/windows/desktop/direct3d9/d3dusage)
</dt> <dt>

[**D3DPOOL**](/windows/desktop/direct3d9/d3dpool)
</dt> <dt>

[D3DCREATE](/windows/desktop/direct3d9/d3dcreate)
</dt> </dl>

 

 