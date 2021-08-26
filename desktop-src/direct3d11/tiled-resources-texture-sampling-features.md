---
title: Textursyntaturfeatures für gekachelte Ressourcen
description: In diesem Abschnitt werden die Textursyntaturfeatures für kachelierte Ressourcen beschrieben.
ms.assetid: E56737CE-C468-4D3C-84EE-E8EB2AB6F505
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1356b274b5e101a730e3de92a6cdf98b1f293515228fb420a77642f4603757c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119476"
---
# <a name="tiled-resources-texture-sampling-features"></a>Textursyntaturfeatures für gekachelte Ressourcen

In diesem Abschnitt werden die Textursyntaturfeatures für kachelierte Ressourcen beschrieben.

## <a name="requirements-of-tiled-resources-texture-sampling-features"></a>Anforderungen von Textursyntaturfeatures für kachelierte Ressourcen

Die hier beschriebenen Textursyntatures erfordern [Die Ebene 2](tier-2.md) der Unterstützung von gekachelten Ressourcen.

## <a name="shader-feedback-about-mapped-areas"></a>Shaderfeedback zu zugeordneten Bereichen

Jede Shaderanweisung, die eine gekachelte Ressource liest und/oder schreibt, bewirkt, dass Statusinformationen aufgezeichnet werden. Dieser Status wird als optionaler zusätzlicher Rückgabewert für jede Ressourcenzugriffsanweisung verfügbar gemacht, die in ein temporäres 32-Bit-Register übergeht. Der Inhalt des Rückgabewerts ist nicht transparent. Das heißt, das direkte Lesen durch das Shaderprogramm ist nicht zu vererblich. Sie können jedoch die [**CheckAccessFullyMapped-Funktion**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) verwenden, um die Statusinformationen zu extrahieren.

## <a name="fully-mapped-check"></a>Vollständig zugeordnete Überprüfung

Die [**CheckAccessFullyMapped-Funktion**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) interpretiert den von einem Speicherzugriff zurückgegebenen Status und gibt an, ob alle Daten, auf die zugegriffen wird, in der Ressource zugeordnet wurden. **CheckAccessFullyMapped** gibt true (0xFFFFFFFF) zurück, wenn Daten zugeordnet wurden, oder false (0x00000000), wenn daten nicht zugeordnet wurden.

Bei Filtervorgängen beträgt die Gewichtung eines bestimmten Texels manchmal 0,0. Ein Beispiel ist ein lineares Beispiel mit Texturkoordinaten, die direkt auf ein Texelcenter fallen: 3 andere Texel (die sie je nach Hardware variieren können) tragen zum Filter bei, jedoch mit einer Gewichtung von 0. Diese 0-Gewicht-Texel tragen überhaupt nicht zum Filterergebnis bei.  Wenn sie also auf NULL-Kacheln fallen, werden sie nicht als nicht zugeordneter Zugriff gezählt. Beachten Sie, dass die gleiche Garantie für Texturfilter gilt, die mehrere MIP-Ebenen enthalten. Wenn die Texel auf einem der Mipmaps nicht zugeordnet sind, die Gewichtung dieser Texel jedoch 0 beträgt, werden diese Texel nicht als nicht zugeordneter Zugriff gezählt.

Beim Sampling aus einem Format mit weniger als 4 Komponenten (z. B. DXGI FORMAT R8 UNORM) führen alle \_ \_ \_ Texel,  die auf **NULL-Kacheln** fallen, dazu, dass ein NULL-zugeordneter Zugriff unabhängig davon gemeldet wird, welche Komponenten der Shader im Ergebnis tatsächlich untersucht. Wenn Sie z. B. aus R8 UNORM lesen und das Leseergebnis im Shader mit .gba/.yzw maskieren, scheint es überhaupt nicht notwendig zu sein, die Textur \_ zu lesen. Wenn es sich bei der Texeladresse jedoch um eine Kachel handelt, die **null** zugeordnet ist, zählt der Vorgang weiterhin als **NULL-Zuordnungszugriff.**

Der Shader kann den Status überprüfen und jede gewünschte Aktion bei einem Fehler verfolgen. Eine Aktion kann z. B. das Protokollieren von "Misses" (z. B. über UAV-Schreibzugriff) und/oder das Ausstellen eines weiteren Lesezugriffs sein, der an eine unebenere LOD-Datei geklammert ist, die als zugeordnet bekannt ist. Eine Anwendung möchte möglicherweise auch erfolgreiche Zugriffe nachverfolgen, um einen Überblick darüber zu erhalten, auf welchen Teil der zugeordneten Kacheln zugegriffen wurde.

Eine Mögliche Ursache für die Protokollierung ist, dass kein Mechanismus zum Melden der genauen Kacheln vorhanden ist, auf die zugegriffen worden wäre. Die Anwendung kann konservative Schätzungen treffen, indem sie die Koordinaten kennt, die sie für den Zugriff verwendet hat, sowie die LOD-Anweisung (z. B. [**tex2Dlod),**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-tex2dlod)die die Hardware-LOD-Berechnung zurückgibt.

Eine weitere Komplikation ist, dass viele Zugriffe auf dieselben Kacheln erfolgen, sodass eine große Menge redundanter Protokollierung und möglicherweise Schwierigkeiten im Arbeitsspeicher auftreten. Es könnte praktisch sein, wenn die Hardware die Option erhalten könnte, kachelzugriffe nicht zu melden, wenn sie zuvor an anderer Stelle gemeldet wurden. Möglicherweise kann der Status einer solchen Nachverfolgung von der API zurückgesetzt werden (wahrscheinlich an Rahmengrenzen).

## <a name="per-sample-minlod-clamp"></a>MinLOD-Klammer pro Beispiel

Damit Shader Bereiche in gekachelten Ressourcen mit Mipmappe vermeiden können, die bekannterweise nicht zugeordnet sind, verfügen die meisten Shaderanweisungen, die die Verwendung eines Samplers (Filtern) umfassen, über einen neuen Modus, mit dem der Shader einen zusätzlichen float32 MinLOD-Klammerparameter an das Texturbeispiel übergeben kann. Dieser Wert befindet sich im Mipmap-Zahlenbereich der Ansicht, im Gegensatz zur zugrunde liegenden Ressource.

Die Hardware führt [**die maximale**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-max)Leistung (fShaderMinLODClamp,fComputedLOD) an der gleichen Stelle in der LOD-Berechnung aus, an der die MinLOD-Klammer pro Ressource auftritt, die ebenfalls ein Max. **()** ist.

Wenn das Ergebnis der Anwendung der LOD-Klammer pro Stichprobe und anderer im Sampler definierter LOD-Klammern ein leerer Satz ist, ist das Ergebnis das gleiche Ergebnis des Zugriffs über grenzenlose Grenzen wie die minLOD-Klammer pro Ressource: 0 für Komponenten im Oberflächenformat und Standardwerte für fehlende Komponenten.

Die LOD-Anweisung (z. B. [**tex2Dlod),**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-tex2dlod)die der hier beschriebenen minLOD-Klammer pro Stichprobe vorangibt, gibt sowohl eine geklammerte als auch eine nicht geblendete LOD zurück. Die von dieser LOD-Anweisung zurückgegebene geklammerte LOD spiegelt alle Klammern wider, einschließlich der ressourcenspezifischen Klammer, aber keine Klammer pro Stichprobe. Die Klammer pro Beispiel wird sowieso gesteuert und vom Shader bekannt, sodass der Shaderautor diese Klammer bei Wunsch manuell auf den Rückgabewert der LOD-Anweisung anwenden kann.

## <a name="minmax-reduction-filtering"></a>Filterung der Mindest-/Maximalreduzierung

Anwendungen können ihre eigenen Datenstrukturen verwalten, die sie darüber informieren, wie die Zuordnungen für eine gekachelte Ressource aussehen. Ein Beispiel wäre eine Oberfläche, die ein Texel enthält, das Informationen für jede Kachel in einer gekachelten Ressource enthält. Sie können die erste LOD speichern, die an einer bestimmten Kachelposition zugeordnet ist. Durch eine sorgfältige Stichprobenentnahme dieser Datenstruktur auf eine ähnliche Weise wie die gekachelte Ressource, die für die Stichprobenentnahme vorgesehen ist, kann man feststellen, wie die minimale LOD sein wird, die vollständig für einen gesamten Texturfilterbedarf zugeordnet ist. Um diesen Prozess zu vereinfachen, führt Direct3D 11.2 den neuen allgemeinen Samplermodus min/max filtering ein.

Das Hilfsprogramm der Min/Max-Filterung für die LOD-Nachverfolgung kann für andere Zwecke nützlich sein, z. B. für das Filtern von Tiefenoberflächen.

Min/max reduction filtering ist ein Modus für Sampler, der den gleichen Satz von Texeln abruft, den ein normaler Texturfilter abrufen würde. Anstatt jedoch die Werte zu mischen, um eine Antwort zu erhalten, wird min() oder max() der abgerufenen Texel auf Komponentenbasis zurückgegeben (z. B. der Mindestwert aller R-Werte, getrennt vom Mindestwert aller G-Werte und so weiter).

Die Min/Max-Vorgänge folgen den Regeln für die arithmetische Genauigkeit von Direct3D. Die Reihenfolge der Vergleiche spielt keine Rolle.

Bei Filtervorgängen, die nicht min/max sind, beträgt die Gewichtung eines bestimmten Texels manchmal 0,0. Ein Beispiel ist ein lineares Beispiel mit Texturkoordinaten, die direkt auf ein Texelcenter fallen. 3 andere Texel (die sie je nach Hardware variieren können) tragen zum Filter bei, jedoch mit einer Gewichtung von 0. Für jedes dieser Texel, das eine Gewichtung von 0 (0) auf einem Nicht-Min/Max-Filter haben würde, tragen diese Texel immer noch nicht zum Ergebnis bei (und die Gewichtungen wirken sich ansonsten nicht auf den Min/Max-Filtervorgang aus).

Die vollständige Liste der Filtermodi wird in der [**FILTER-Enumeration \_ D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter) mit MINIMUM und MAXIMUM in den Enumerationswerten angezeigt.

Die Unterstützung für dieses Feature hängt von der [Unterstützung der Ebene 2](tier-2.md) für gekachelte Ressourcen ab.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pipelinezugriff auf gekachelte Ressourcen](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 