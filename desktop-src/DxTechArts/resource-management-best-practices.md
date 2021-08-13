---
title: Bewährte Methoden für die Ressourcenverwaltung
description: In diesem Artikel werden bewährte Methoden für den allgemeinen Umgang mit Ressourcen, das Verhalten von verwalteten und nicht verwalteten Ressourcen und einige Details dazu erläutert, wie Ressourcen in der Regel von der Laufzeit und den Treibern behandelt werden.
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

Verwaltete Texturen, auch als automatische Texturverwaltung bezeichnet, sind in DirectX seit Version 6 verfügbar, mit mehreren Revisionen und Verbesserungen, die in nachfolgenden Releases vorgenommen wurden. Seit der Veröffentlichung der Direct3D 9-API bietet die automatische Ressourcenverwaltung Unterstützung für Texturen, Scheitelpunktpuffer und Indexpuffer mit einer konsistenten freigegebenen Schnittstelle. Mithilfe des Direct3D-Ressourcen-Managers können Anwendungen die Behandlung von Situationen mit verlorenen Geräten stark vereinfachen und sich darauf verlassen, dass das System eine angemessene Menge an Überbenutzung von Videospeicherressourcen bewältigen kann.

Entwickler haben manchmal Schwierigkeiten bei der Verwendung verwalteter Ressourcen, teilweise aufgrund der abstrakten Natur des Systems. Viele gängige Szenarien für Ressourcen sind zwar gut für verwaltete Ressourcen geeignet, aber in einigen Fällen ist die Leistung bei verwendung nicht verwalteter Ressourcen besser. In diesem Artikel werden bewährte Methoden für den allgemeinen Umgang mit Ressourcen, das Verhalten von verwalteten und nicht verwalteten Ressourcen und einige Details dazu erläutert, wie Ressourcen in der Regel von der Laufzeit und den Treibern behandelt werden.

In diesem Artikel werden die folgenden Konzepte behandelt:

-   [Videospeicher](#video-memory)
-   [Verwaltete Ressourcen](#managed-resources)
-   [Vom Treiber verwaltete Ressourcen](#driver-managed-resources)
-   [Standardressourcen](#default-resources)
    -   [Verwenden von verwalteten und Standardressourcen](#using-both-managed-and-default-resources)
    -   [Dynamische Standardressourcen](#dynamic-default-resources)
-   [Systemspeicherressourcen](#system-memory-resources)
-   [Allgemeine Empfehlungen](#general-recommendations)
-   [Zugehörige Themen](#related-topics)

## <a name="video-memory"></a>Videospeicher

Damit das Videosystem eine Ressource verwenden kann, muss sie sich im Arbeitsspeicher befinden, auf den die GPU zugriff kann. Der lokale Videospeicher bietet die beste Leistung für die GPU, und bestimmte Ressourcen (z. B. Renderziele und Tiefen-/Schablonenpuffer) müssen sich im lokalen Videospeicher befinden. Mit der Einführung von AGP kann die GPU auch direkt auf einen Teil des Systemspeichers zugreifen. Dieser Als AGP-Öffnung bezeichnete Arbeitsspeicherbereich wird als nicht lokaler Videospeicher bezeichnet und ist für andere Zwecke nicht verfügbar. Der nicht lokale Videospeicher kann von der CPU gelesen und in diesen geschrieben werden, die in der Regel keinen Hochleistungszugriff auf den lokalen Videospeicher hat und daher ideal für die Verwendung als Freigegebene Speicherressource geeignet ist. Ein wichtiger Punkt beim AGP-Speicher ist, dass er wie der lokale Videospeicher in Situationen mit verlorenen Geräten ungültig gemacht wird und persistente Ressourcen, die sich dort befinden, wiederhergestellt werden müssen.

**Abbildung 1: Beziehung zwischen GPU, CPU, Video-RAM und System-RAM**

![Beziehung zwischen GPU, CPU, Video-RAM und System-RAM](images/managingresources1.gif)

Einige integrierte Videolösungen nutzen eine einheitliche Speicherarchitektur (Unified Memory Architecture, UMA), bei der der Hauptspeicher von allen Komponenten der Systeme adressiert werden kann. Direct3D unterstützt UMA, ohne dass Änderungen an der Anwendung erforderlich sind. Dabei werden die gleichen Hinweise wie für konfigurationen des lokalen Videospeichers verwendet. Für solche Systeme befinden sich Ressourcen immer im Systemspeicher, und der Treiber ist dafür verantwortlich, sicherzustellen, dass Ressourcen ähnlich wie in einer herkömmlichen Architektur funktionieren und gleichzeitig die Uma-Eigenschaften und jedes spezifische Verhalten der Hardwareimplementierung nutzen.

**Abbildung 2: GPU und CPU haben gleichen Zugriff auf den System-RAM in einer einheitlichen Speicherarchitektur.**

![GPU und CPU haben gleichen Zugriff auf den System-RAM in einer einheitlichen Speicherarchitektur](images/managingresources2.gif)

## <a name="managed-resources"></a>Verwaltete Ressourcen

Der Großteil Ihrer Ressourcen sollte als verwaltete Ressourcen in POOL MANAGED erstellt \_ werden. Alle Ihre Ressourcen werden im Systemspeicher erstellt und dann nach Bedarf in den Videospeicher kopiert. Situationen mit verloren gegangenen Geräten werden automatisch aus der Systemspeicherkopie verarbeitet. Da nicht alle verwalteten Ressourcen gleichzeitig in den Videospeicher passen müssen, können Sie einen Over-Commit für Den Arbeitsspeicher verwenden, bei dem nur ein kleinerer Arbeitssatz von Videoarbeitsspeichern erforderlich ist, um in einem bestimmten Frame gerendert zu werden. Beachten Sie, dass es wahrscheinlich ist, dass der Großteil dieses Sicherungsspeichersystemspeichers im Laufe der Zeit auf den Datenträger auslagert. Aus diesem Grund kann der Vorgang Zurücksetzen langsam sein, da diese Daten zurückgeladen werden müssen, um den verloren gegangenen Videospeicher wiederherzustellen.

Die Runtime behält einen Zeitstempel für die letzte Verwendung einer Ressource bei, und wenn eine Videospeicherbelegung beim Laden einer benötigten verwalteten Ressource fehlschlägt, gibt sie Ressourcen basierend auf diesem Zeitstempel auf LRU-Weise frei. Die Verwendung [**von SetPriority**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority) hat Vorrang vor dem Zeitstempel, daher sollten häufig verwendete Ressourcen auf einen höheren Prioritätswert festgelegt werden. Direct3D 9.0 verfügt über eingeschränkte Informationen über den vom Treiber verwalteten Videospeicher, sodass die Runtime möglicherweise mehrere Ressourcen aus dem System verdringt, um eine ausreichend große Region zu erstellen, damit die Zuordnung erfolgreich ist. Die richtigen Prioritäten können dazu beitragen, Situationen zu beseitigen, in denen etwas entfernt wird und kurz danach wieder erforderlich ist. Die Anwendung kann auch [**EvictManagedResources**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-evictmanagedresources) aufrufen, um das Entfernen aller verwalteten Ressourcen zu erzwingen. Auch hier kann dies ein zeitaufwändiger Vorgang sein, um alle ressourcen, die für den nächsten Frame erforderlich sind, neu zu laden, ist jedoch sehr nützlich für Übergänge auf Ebene, bei denen sich das Arbeitssatz erheblich ändert, und zum Entfernen der Fragmentierung des Videospeichers.

Es wird auch eine Frameanzahl beibehalten, damit die Runtime erkennen kann, ob die Ressource, die sie gerade aus dem aktuellen Frame entziehen möchte, frühzeitig verwendet wurde. Dies impliziert eine überschlagende Situation, in der mehr Ressourcen in einem einzelnen Frame verwendet werden, als in den Videospeicher passen. Dies löst die Ersetzungsrichtlinie aus, um für den Rest des Rahmens zu einer MRU-Art und nicht zu LRU zu wechseln, da dies unter solchen Bedingungen tendenziell etwas besser ist. Ein solches Thrashingverhalten wirkt sich erheblich auf die Renderingleistung aus. Beachten Sie, dass das Konzept des aktuellen Frames an [**EndScene**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-endscene)gebunden ist, sodass jede Anwendung, die verwaltete Ressourcen verwendet, regelmäßige Aufrufe dieser Methode tätigen muss.

Entwickler, die weitere Informationen zum Verhalten verwalteter Ressourcen in ihrer Anwendung suchen, können die RESOURCEMANAGER-Ereignisabfrage über die [**IDirect3DQuery9-Schnittstelle**](/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dquery9) verwenden. Dies funktioniert nur bei Verwendung der Debuglaufzeiten, sodass diese Informationen nicht von der Anwendung abhängig sein können, sondern detaillierte Informationen zu den von der Laufzeit verwalteten Ressourcen bieten.

Obwohl das Verständnis der Funktionsweise des Ressourcen-Managers beim Optimieren und Debuggen Ihrer Anwendungen helfen kann, ist es wichtig, Ihre Anwendung nicht zu eng an die Implementierungsdetails der aktuellen Laufzeit oder treiber zu binden. Änderungen des Treibers oder Hardwareänderungen können das Verhalten erheblich ändern, und zukünftige Versionen von Direct3D werden die Ressourcenverwaltung erheblich verbessert und ausgefeilt haben.

## <a name="driver-managed-resources"></a>Driver-Managed Ressourcen

Direct3D-Treiber können die vom Treiber verwaltete Texturfunktion implementieren, die durch D3DCAPS2 CANMANAGERESOURCE angegeben wird. Dadurch kann der Treiber die Ressourcenverwaltung anstelle der Laufzeit \_ übernehmen. Für den (seltenen) Treiber, der dieses Feature implementiert, kann das genaue Verhalten des Ressourcen-Managers des Treibers stark variieren, und Sie sollten sich an den Hersteller des Treibers wenden, um Details zur Funktionsweise der Implementierung zu erhalten. Alternativ können Sie sicherstellen, dass der Laufzeit-Manager immer verwendet wird, indem Sie beim Erstellen des Geräts D3DCREATE \_ DISABLE \_ DRIVER MANAGEMENT \_ angeben.

## <a name="default-resources"></a>Standardressourcen

Verwaltete Ressourcen sind zwar einfach, effizient und einfach zu verwenden, es gibt jedoch Manchmal, wenn die direkte Verwendung von Videospeicher bevorzugt oder sogar erforderlich ist. Solche Ressourcen werden in der Kategorie POOL \_ DEFAULT erstellt. Die Verwendung solcher Ressourcen führt zu zusätzlichen Schwierigkeiten für Ihre Anwendung. Code ist erforderlich, um die Situation mit verlorenen Geräten für alle POOL DEFAULT-Ressourcen zu bewältigen, und beim Kopieren von Daten in diese müssen \_ Leistungsüberlegungen berücksichtigt werden. Wenn USAGE WRITEONLY nicht angegeben oder ein Renderziel gesperrt werden kann, kann dies \_ auch zu schwerwiegenden Leistungsausfällen führen.

Das **Aufrufen von Lock** für eine POOL DEFAULT-Ressource verursacht wahrscheinlicher, dass die GPU nicht mehr funktioniert, als mit einer POOL MANAGED-Ressource zu arbeiten, es sei denn, bestimmte \_ \_ Hinweisflags werden verwendet. Je nach Speicherort der Ressource kann der zurückgegebene Zeiger auf einen temporären Systemspeicherpuffer oder ein Zeiger direkt in den AGP-Speicher sein. Wenn es sich um einen temporären Systemspeicherpuffer handelt, müssen Daten nach dem Entsperrungsaufruf in den **Videospeicher übertragen** werden. Wenn die Videoressource nicht write-only ist, müssen Daten während der Sperre in den temporären Puffer **übertragen werden.** Wenn es sich um einen AGP-Speicherbereich handelt, werden temporäre Kopien vermieden, aber das erforderliche Cacheverhalten kann zu einer langsamen Leistung führen.

Es sollte darauf achten, eine vollständige Cachezeile von Daten in einen beliebigen Zeiger auf den Speicher der AGP-Öffnung zu schreiben, um die Berücksichtigung der Berücksichtigung von Schreib-Kombinationen zu vermeiden, die einen Lese-/Schreibzyklus auslösen, und der sequenzielle Zugriff auf den Arbeitsspeicherbereich wird bevorzugt. Wenn Ihre Anwendung während der Erstellung zufälligen Zugriff auf Daten haben muss und Sie keine verwaltete Ressource für den Puffer verwenden möchten, sollten Sie stattdessen mit einer Systemspeicherkopie arbeiten. Nachdem die Daten erstellt wurden, können Sie das Ergebnis in den gesperrten Ressourcenspeicher streamen, um zu vermeiden, dass für den Cache-Schreib-Kombinierungsvorgang hohe Kosten entstehen.

Das LOCK NOOVERWRITE-Flag kann verwendet werden, um Daten für einige Ressourcen effizient anfügen. Im Idealfall können jedoch mehrere \_ **Lock-** und **Unlock-Aufrufe** derselben Ressource vermieden werden. Die richtige Verwendung der verschiedenen Sperrflags ist wichtig, um eine optimale Leistung zu erzielen, ebenso wie die Verwendung eines cachefreundlichen Musters für den Datenzugriff beim Auffüllen von gesperrtem Speicher.

### <a name="using-both-managed-and-default-resources"></a>Verwenden von verwalteten und Standardressourcen

Das Kombinieren von Zuordnungen von verwalteten und POOL DEFAULT-Ressourcen kann zu einer Fragmentierung des Videospeichers führen und die Laufzeitansicht des Videospeichers verwirren, der für \_ verwaltete Ressourcen verfügbar ist. Im Idealfall sollten Sie alle POOL DEFAULT-Ressourcen erstellen, bevor Sie POOL MANAGED-Ressourcen verwenden, oder den \_ \_ Aufruf [**EvictManagedResources**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-evictmanagedresources) verwenden, bevor Sie nicht verwaltete Ressourcen zuweisen. Denken Sie daran, dass alle Zuordnungen aus POOL DEFAULT, die sich im Videospeicher befinden, Arbeitsspeicher für die Lebensdauer dieser Ressource binden, die nicht für die Verwendung durch den Ressourcen-Manager oder für andere Zwecke verfügbar \_ ist.

Beachten Sie, dass die Runtime von Version 9 im Gegensatz zu früheren Versionen von Direct3D automatisch einige verwaltete Ressourcen lässt, bevor sie auf eine fehlerhafte nicht verwaltete Ressourcenzuordnung aufgrund von unzureichendem Videospeicher hinweist. Dies kann jedoch möglicherweise zu einer zusätzlichen Fragmentierung und sogar zur Erzwingen einer Ressource an einem suboptimierten Speicherort (z. B. mit einer statischen Textur im nicht lokalen Videospeicher) führt. Auch hier ist es am besten, alle erforderlichen nicht verwalteten Ressourcen im Vorhinhin und vor der Verwendung verwalteter Ressourcen zu reservieren.

### <a name="dynamic-default-resources"></a>Dynamische Standardressourcen

Daten, die mit hoher Häufigkeit generiert und aktualisiert werden, benötigen den Unterstützungsspeicher nicht, da alle Informationen beim Wiederherstellen des Geräts neu erstellt werden. Solche Daten werden in der Regel am besten in POOL DEFAULT erstellt und geben den USAGE DYNAMIC-Hinweis an, damit der Treiber beim Platzieren der Ressource Optimierungsentscheidungen treffen kann, in dem Wissen, dass sie häufig \_ \_ aktualisiert werden. Dies bedeutet in der Regel, dass die Ressource in den nicht lokalen Videospeicher eingespeichert wird. Daher ist es in der Regel viel langsamer, dass die GPU auf sie zugeht als auf den lokalen Videospeicher. Bei UMA-Architekturen kann der Treiber eine bestimmte Platzierung für dynamische Ressourcen auswählen, um den CPU-Schreibzugriff zu optimieren.

Diese Verwendung ist typisch für Software-Skinninglösungen und CPU-basierte Partikelsysteme, die Scheitelpunkt-/Indexpuffer füllen, und das LOCK DISCARD-Flag stellt sicher, dass in Fällen, in denen die Ressource noch im vorherigen Frame verwendet wird, keine Stags erstellt \_ werden. Durch die Verwendung einer verwalteten Ressource wird in diesem Fall ein Systemspeicherpuffer aktualisiert, der dann in den Videospeicher kopiert und dann nur für ein oder zwei Frames verwendet wird, bevor er ersetzt wird. Bei Systemen mit nicht lokalem Videospeicher wird die zusätzliche Kopie durch die ordnungsgemäße Verwendung dieses dynamischen Musters beseitigt.

Standardtexturen können nicht gesperrt und nur über [**UpdateSurface oder**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface) [**UpdateTexture aktualisiert werden.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture) Einige Systeme unterstützen dynamische Texturen, die gesperrt werden können, und verwenden das LOCK DISCARD-Muster, aber ein Funktionenbit \_ (D3DCAPS2 DYNAMICTEXTURES) muss überprüft werden, bevor solche Ressourcen verwendet \_ werden. Für hoch dynamische Texturen (Video oder Prozedur) könnte Ihre Anwendung übereinstimmende POOL DEFAULT- und POOL SYSTEMMEM-Ressourcen erstellen und Videospeicherupdates mit \_ \_ **updateTexture verarbeiten.** Bei sehr häufigen und teilweisen Updates ist das **UpdateTexture-Paradigma** wahrscheinlich die bessere Wahl.

So nützlich dynamische Ressourcen auch sein können, seien Sie vorsichtig, wenn Sie Systeme entwerfen, die stark von dynamischer Übermittlung abhängig sind. Statische Ressourcen sollten in POOL MANAGED platziert werden, um sowohl eine gute Auslastung des lokalen Videospeichers als auch eine effizientere Nutzung der eingeschränkten Bus- und \_ Hauptspeicherbandbreite sicherzustellen. Bei ressourcen, die teilweise statisch sind, stellen Sie möglicherweise fest, dass die Kosten für einen gelegentlichen Upload in den lokalen Videospeicher viel geringer sind als der konstante Busdatenverkehr, der generiert wird, indem sie dynamisch werden.

## <a name="system-memory-resources"></a>Systemspeicherressourcen

Ressourcen können auch in POOL \_ SYSTEMMEM erstellt werden. Obwohl sie nicht von der Grafikpipeline verwendet werden können, können sie als Quellen zum Aktualisieren von POOL DEFAULT-Ressourcen mit \_ [**updateSurface**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface) oder [**UpdateTexture verwendet werden.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture) Ihr Sperrverhalten ist einfach, obwohl Es zu Stags kommen kann, wenn sie von einer der zuvor erwähnten Methoden verwendet werden.

Obwohl sie sich im Systemspeicher befinden, sind POOL SYSTEMMEM-Ressourcen auf die gleichen Formate und Funktionen (z. B. die maximale Größe) beschränkt, die \_ vom Gerätetreiber unterstützt werden. Der POOL SCRATCH-Ressourcentyp ist eine weitere Form der Systemspeicherressource, die alle von der Laufzeit unterstützten Formate und Funktionen nutzen kann, aber nicht vom \_ Gerät aufgerufen werden kann. Scratch-Ressourcen sind in erster Linie für die Verwendung durch Inhaltstools vorgesehen.

**Abbildung 3: Arbeitsspeicherressourcen in Video-RAM, AGP-Öffnung und System-RAM**

![Arbeitsspeicherressourcen in Video-RAM, AGP-Öffnung und System-RAM](images/managingresources3.gif)

## <a name="general-recommendations"></a>Allgemeine Empfehlungen

Wenn Sie die technischen Implementierungsdetails der Ressourcenverwaltung korrigieren, können Sie ihre Leistungsziele für Ihre Anwendung erreichen. Die Planung, wie die Ressourcen Direct3D präsentiert werden, und das Architekturdesign für die rechtzeitige Datenladung ist eine kompliziertere Aufgabe. Es wird eine Reihe von bewährten Methoden empfohlen, wenn Sie diese Entscheidungen für Ihre Anwendung treffen:

-   Verarbeiten Sie alle Ihre Ressourcen vorab. Die Kosten für die Konvertierung und Optimierung der Ladezeit für Ihre Ressourcen sind während der Entwicklung praktisch. Dies stellt jedoch eine große Leistungsbelastung für die Computer Ihrer Benutzer dar. Vorverarbeitete Ressourcen sind schneller zu laden, schneller zu verwenden und bieten Ihnen die Möglichkeit, anspruchsvolle Off-Line-Arbeit zu machen.
-   Vermeiden Sie es, viele Ressourcen pro Frame zu erstellen. Die erforderlichen Treiberinteraktionen können die CPU und GPU serialisieren, und die beteiligten Vorgänge sind stark gewichtet, da sie häufig Kernelübergänge erfordern. Verteilen Sie die Erstellung auf mehrere Frames, oder verwenden Sie Ressourcen wieder, ohne sie zu erstellen/frei zu geben. Im Idealfall sollten Sie mehrere Frames warten, bevor Sie Ressourcen sperren oder freigeben, die kürzlich zum Rendern verwendet wurden.
-   Stellen Sie am Ende des Frames sicher, dass Sie die Bindung aller Ressourcenkanäle (d. h. Streamquellen, Texturstufen und aktuelle Indizes) entbinden. Dadurch wird sichergestellt, dass verwesende Verweise auf Ressourcen entfernt werden, bevor sie dazu führen, dass der Ressourcen-Manager ressourcenresident bleibt, die tatsächlich nicht mehr verwendet werden.
-   Verwenden Sie für Texturen komprimierte Formate (z. B. DXTn) mit Mipmaps, und ziehen Sie die Verwendung eines Texturatlas in Betracht. Dadurch werden die Bandbreitenanforderungen deutlich reduziert, und sie können die Gesamtgröße der Ressourcen reduzieren, wodurch sie effizienter werden.
-   Verwenden Sie für die Geometrie indizierte Geometrie, da dies beim Komprimieren von Scheitelpunktpufferressourcen hilft und moderne Videohardware stark für die Wiederverwendung von Scheitelpunkt optimiert ist. Wenn Sie programmierbare Vertex-Shader verwenden, können Sie die Scheitelpunktinformationen komprimieren und während der Scheitelpunktverarbeitung erweitern. Dies trägt wiederum dazu bei, die Bandbreitenanforderungen zu reduzieren und Die Ressourcen des Scheitelpunktpuffers effizienter zu gestalten.
-   Vermeiden Sie eine überoptimierende Ressourcenverwaltung. Zukünftige Revisionen von Treibern, Hardware und Betriebssystem können zu Kompatibilitätsproblemen führen, wenn die Anwendung zu stark auf eine besonders kombinierte Anwendung abgestimmt ist. Da die meisten Anwendungen CPU-gebunden sind, verursacht die teure CPU-basierte Verwaltung in der Regel mehr Leistungsprobleme als sie löst.

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

 

 