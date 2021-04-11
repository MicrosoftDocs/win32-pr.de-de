---
description: In diesem Abschnitt werden die Formate ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) -Werte) angegeben, die in der Direct3D-Funktion 10level9 9,3-Hardware unterstützt werden.
ms.assetid: B2A843D5-6A6B-4180-8B94-D032B1322798
title: Formatunterstützung für Direct3D 9 9.3-Hardware auf Featureebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79185ddb360fe9359371671e3722372c3a1615f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041164"
---
# <a name="format-support-for-direct3d-feature-10level9-93-hardware"></a>Formatunterstützung für Direct3D 9 9.3-Hardware auf Featureebene

In diesem Abschnitt werden die Formate ([_* DXGI_FORMAT_* * _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) -Werte) angegeben, die in der Direct3D-Funktion 10level9 9,3-Hardware unterstützt werden.

Die Tabelle enthält eine Zusammenfassung der Featureunterstützung, die den folgenden Schlüssel verwendet.

| Symbol                            | BESCHREIBUNG                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| _ *-**                             | Nicht zulässig oder nicht verfügbar.                                                  |
| ![Erforderlich](images/letter-r.jpg)  | Hardware Unterstützung ist erforderlich.                                                 |
| ![Optional](images/letter-o.jpg)  | Hardwareunterstützung optional, das Format ist möglicherweise Hardware beschleunigt. |
| ![lässe](images/letter-d.jpg) | Erforderlich, wenn eine zugehörige optionale Funktion unterstützt wird.                            |

Dieses Thema enthält einen Abschnitt Pro Format. Ein Format *Ziel* (die Tabellen enthalten eine Zeile pro Ziel) kann ein Ressourcentyp, eine intrinsische HLSL-Funktion oder eine bestimmte Funktionalität sein, die von einem bestimmten Format abhängig ist.

Informationen zur programmgesteuerten Überprüfung der Formatunterstützung in D3D11 und D3D12 finden Sie unter über [Prüfen der Unterstützung von Hardwarefunktionen](checking-hardware-feature-support.md).

> [!NOTE] 
> Die Zahlen der Formate sind größtenteils, aber nicht alle in aufsteigender numerischer Reihenfolge, dass einige nicht in &mdash; numerischer Reihenfolge sind und neben anderen relevanten Formaten aufgeführt werden. Beachten Sie auch, dass *typlose* in einem Format Namen *teilweise* typisiert und nicht streng typlos sein kann (Weitere Informationen finden Sie im Abschnitt " [Format Notizen](#format-notes) " am Ende des Themas).

## <a name="dxgi_format_unknownsuplsup-0"></a>DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 0 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a>DXGI_FORMAT_R32G32B32A32 \_ Typen losen<sup>PCs</sup> (1)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfnssup-2"></a>DXGI_FORMAT_R32G32B32A32 \_ float<sup></sup> -Datentyp (2)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| 8X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfnssup-3"></a>DXGI_FORMAT_R32G32B32A32 \_ uint<sup></sup> -Benutzerkonten (3)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfnssup-4"></a>DXGI_FORMAT_R32G32B32A32 \_ Sint<sup></sup> (4)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a>DXGI_FORMAT_R32G32B32 \_ Typen losen<sup>PCs</sup> (5)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 96 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32b32_floatsupfnssup-6"></a>DXGI_FORMAT_R32G32B32 \_ float<sup></sup> -Datentyp (6)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 96 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | ![lässe](images/letter-d.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | ![lässe](images/letter-d.jpg) |
| 8X-Multisample-renderTarget | ![lässe](images/letter-d.jpg) |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32b32_uintsupfnssup-7"></a>DXGI_FORMAT_R32G32B32 \_ uint<sup></sup> -(7)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 96 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | ![lässe](images/letter-d.jpg) |
| 8X-Multisample-renderTarget | ![lässe](images/letter-d.jpg) |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32b32_sintsupfnssup-8"></a>DXGI_FORMAT_R32G32B32 \_ Sint<sup></sup> (8)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 96 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | ![lässe](images/letter-d.jpg) |
| 8X-Multisample-renderTarget | ![lässe](images/letter-d.jpg) |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a>DXGI_FORMAT_R16G16B16A16 \_ Typen losen<sup>PCs</sup> (9)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfnssup-10"></a>DXGI_FORMAT_R16G16B16A16 float-Dateinamen \_ (10)<sup></sup>
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Optional](images/letter-o.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| 8X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfnssup-11"></a>DXGI_FORMAT_R16G16B16A16 \_ unorm<sup></sup> -Fehler (11)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| 8X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfnssup-12"></a>DXGI_FORMAT_R16G16B16A16 \_ uint<sup></sup> -Benutzerkonten (12)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfnssup-13"></a>DXGI_FORMAT_R16G16B16A16 \_ snorm<sup></sup> -Kenn Wort (13)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfnssup-14"></a>DXGI_FORMAT_R16G16B16A16 \_ Sint<sup></sup> -nach SPT (14)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a>DXGI_FORMAT_R32G32 \_ Typen losen<sup>PCs</sup> (15)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32_floatsupfnssup-16"></a>DXGI_FORMAT_R32G32 \_ float<sup></sup> -Datentyp (16)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| 8X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32_uintsupfnssup-17"></a>DXGI_FORMAT_R32G32 \_ uint<sup></sup> -(17)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32_sintsupfnssup-18"></a>DXGI_FORMAT_R32G32 \_ Sint<sup></sup> (18)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a>DXGI_FORMAT_R32G8X24 \_ Typen losen<sup>PCs</sup> (19)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfnssup-20"></a>DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint<sup></sup> -(20)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfnssup-21"></a>DXGI_FORMAT_R32 \_ float \_ X8X24 \_ typlose<sup></sup> Rechtschreibfehler (21)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfnssup-22"></a>DXGI_FORMAT_X32 \_ typlose \_ G8X24 \_ uint<sup></sup> -Fehler (22)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a>DXGI_FORMAT_R10G10B10A2 \_ typlosen<sup>PCs</sup> (23)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfnssup-24"></a>DXGI_FORMAT_R10G10B10A2 \_ unorm<sup></sup> -Fehler (24)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfnssup-25"></a>DXGI_FORMAT_R10G10B10A2 \_ uint<sup></sup> -(25)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfnssup-89"></a>DXGI_FORMAT_R10G10B10 \_ XR \_ Bias \_ a2 \_ unorm<sup></sup> -Fehler (89)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a>DXGI_FORMAT_R11G11B10 \_ float<sup></sup> -Datentyp (26)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a>DXGI_FORMAT_R8G8B8A8 \_ typlosen<sup>PCs</sup> (27)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfnssup-28"></a>DXGI_FORMAT_R8G8B8A8 \_ unorm<sup></sup> -Fehler (28)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| 8X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | ![Erforderlich](images/letter-r.jpg) |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Ausgabe des Video Prozessors | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfnssup-29"></a>DXGI_FORMAT_R8G8B8A8 \_ unorm \_ sRGB<sup></sup> -Fehler (29)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| 8X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | ![Erforderlich](images/letter-r.jpg) |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Ausgabe des Video Prozessors | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfnssup-30"></a>DXGI_FORMAT_R8G8B8A8 \_ uint<sup></sup> -(30)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfnssup-31"></a>\_Snorm-<sup></sup> snorm (31) DXGI_FORMAT_R8G8B8A8
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfnssup-32"></a>DXGI_FORMAT_R8G8B8A8 \_ Sint<sup></sup> -SPT (32)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a>DXGI_FORMAT_R16G16 \_ Typen losen<sup>PCs</sup> (33)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16_floatsupfnssup-34"></a>DXGI_FORMAT_R16G16 \_ float-"<sup>f</sup> " (34)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| 8X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16_unormsupfnssup-35"></a>DXGI_FORMAT_R16G16 \_ unorm<sup></sup> -Fehler (35)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| 8X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16_uintsupfnssup-36"></a>DXGI_FORMAT_R16G16 \_ uint<sup></sup> -Benutzerkonten (36)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16_snormsupfnssup-37"></a>DXGI_FORMAT_R16G16 \_ snorm<sup></sup> -Kenn Wort (37)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16_sintsupfnssup-38"></a>DXGI_FORMAT_R16G16 \_ Sint<sup></sup> -SPT (38)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a>DXGI_FORMAT_R32 \_ Typen losen<sup>PCs</sup> (39)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_d32_floatsupfnssup-40"></a>DXGI_FORMAT_D32 \_ float-"<sup>f</sup> " (40)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32_floatsupfnssup-41"></a>DXGI_FORMAT_R32 \_ float-"<sup>f</sup> " (41)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| 8X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32_uintsupfnssup-42"></a>DXGI_FORMAT_R32 \_ uint<sup></sup> -Benutzerkonten (42)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | ![Erforderlich](images/letter-r.jpg) |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32_sintsupfnssup-43"></a>DXGI_FORMAT_R32 \_ Sint<sup></sup> -SPT (43)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a>DXGI_FORMAT_R24G8 \_ Typen losen<sup>PCs</sup> (44)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfnssup-45"></a>DXGI_FORMAT_D24 \_ unorm \_ S8 \_ uint<sup></sup> -Fehler (45)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | ![Erforderlich](images/letter-r.jpg) |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| 8X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfnssup-46"></a>DXGI_FORMAT_R24 \_ unorm \_ X8- \_ typlosen, nicht (46)<sup></sup>
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfnssup-47"></a>DXGI_FORMAT_X24 \_ typlose \_ G8 \_ uint<sup></sup> -Benutzerkonten (47)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a>DXGI_FORMAT_R8G8 \_ Typen losen<sup>PCs</sup> (48)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8_unormsupfnssup-49"></a>DXGI_FORMAT_R8G8 \_ unorm<sup></sup> -Fehler (49)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8_uintsupfnssup-50"></a>DXGI_FORMAT_R8G8 \_ uint<sup></sup> -Benutzerkonten (50)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8_snormsupfnssup-51"></a>DXGI_FORMAT_R8G8 \_ snorm<sup></sup> -Kenn Wort (51)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8_sintsupfnssup-52"></a>DXGI_FORMAT_R8G8 \_ Sint<sup></sup> -SPT (52)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a>DXGI_FORMAT_R16 \_ Typen losen<sup>PCs</sup> (53)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16_floatsupfnssup-54"></a>DXGI_FORMAT_R16 \_ float-"<sup>f</sup> " (54)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_d16_unormsupfnssup-55"></a>DXGI_FORMAT_D16 \_ unorm<sup></sup> -Fehler (55)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | ![Erforderlich](images/letter-r.jpg) |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| 8X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16_unormsupfnssup-56"></a>DXGI_FORMAT_R16 \_ unorm<sup></sup> -Fehler (56)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16_uintsupfnssup-57"></a>DXGI_FORMAT_R16 \_ uint<sup></sup> -Benutzerkonten (57)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | ![Erforderlich](images/letter-r.jpg) |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16_snormsupfnssup-58"></a>DXGI_FORMAT_R16 \_ snorm<sup></sup> -Kenn Wort (58)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16_sintsupfnssup-59"></a>DXGI_FORMAT_R16 \_ Sint<sup></sup> -SPT (59)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a>DXGI_FORMAT_R8 \_ Typen losen<sup>PCs</sup> (60)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8_unormsupfnssup-61"></a>DXGI_FORMAT_R8 \_ unorm<sup></sup> -Fehler (61)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8_uintsupfnssup-62"></a>DXGI_FORMAT_R8 \_ uint<sup></sup> -Benutzerkonten (62)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8_snormsupfnssup-63"></a>DXGI_FORMAT_R8 \_ snorm<sup></sup> -Kenn Wort (63)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8_sintsupfnssup-64"></a>DXGI_FORMAT_R8 \_ Sint<sup></sup> -SPT (64)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a>DXGI_FORMAT_A8 \_ unorm<sup></sup> -Fehler (65)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a>DXGI_FORMAT_R9G9B9E5 \_ sharede XP-<sup>LNC</sup> (67)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a>DXGI_FORMAT_R8G8 \_ B8G8 \_ unorm<sup></sup> -Fehler (68)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a>DXGI_FORMAT_G8R8 \_ G8B8 \_ unorm<sup></sup> -Fehler (69)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a>DXGI_FORMAT_BC1 \_ typloses<sup>PCC</sup> (70)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 4 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc1_unormsupfncsup-71"></a>DXGI_FORMAT_BC1 \_ unorm<sup></sup> -Fehler (71)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 4 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfncsup-72"></a>DXGI_FORMAT_BC1 \_ unorm \_ sRGB<sup></sup> -Fehler (72)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 4 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a>DXGI_FORMAT_BC2 \_ typloses<sup>PCC</sup> (73)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc2_unormsupfncsup-74"></a>DXGI_FORMAT_BC2 \_ unorm<sup></sup> -Fehler (74)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfncsup-75"></a>DXGI_FORMAT_BC2 \_ unorm \_ sRGB<sup></sup> -Fehler (75)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a>DXGI_FORMAT_BC3 \_ typloses<sup>PCC</sup> (76)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc3_unormsupfncsup-77"></a>DXGI_FORMAT_BC3 \_ unorm<sup></sup> -Fehler (77)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfncsup-78"></a>DXGI_FORMAT_BC3 \_ unorm \_ sRGB<sup></sup> -Fehler (78)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a>DXGI_FORMAT_BC4 \_ typloses<sup>PCC</sup> (79)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 4 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc4_unormsupfncsup-80"></a>DXGI_FORMAT_BC4 \_ unorm<sup></sup> -Fehler (80)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 4 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc4_snormsupfncsup-81"></a>DXGI_FORMAT_BC4 \_ snorm<sup></sup> -snorm (81)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 4 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a>DXGI_FORMAT_BC5 \_ typloses<sup>PCC</sup> (82)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc5_unormsupfncsup-83"></a>DXGI_FORMAT_BC5 \_ unorm<sup></sup> -Fehler (83)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc5_snormsupfncsup-84"></a>DXGI_FORMAT_BC5 \_ snorm<sup></sup> -snorm (84)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a>DXGI_FORMAT_B5G6R5 \_ unorm<sup></sup> -Fehler (85)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| 8X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a>DXGI_FORMAT_B5G5R5A1 \_ unorm<sup></sup> -Fehler (86)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a>DXGI_FORMAT_B8G8R8A8 \_ Typen losen<sup>PCs</sup> (90)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfnssup-87"></a>DXGI_FORMAT_B8G8R8A8 \_ unorm<sup></sup> -Fehler (87)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| 8X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | ![Erforderlich](images/letter-r.jpg) |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Ausgabe des Video Prozessors | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfnssup-91"></a>DXGI_FORMAT_B8G8R8A8 \_ unorm \_ sRGB<sup></sup> -Fehler (91)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| 8X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | ![Erforderlich](images/letter-r.jpg) |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Ausgabe des Video Prozessors | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a>DXGI_FORMAT_B8G8R8X8 \_ Typen losen<sup>PCs</sup> (92)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | \- |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfnssup-88"></a>DXGI_FORMAT_B8G8R8X8 \_ unorm<sup></sup> -Fehler (88)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| 8X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Ausgabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfnssup-93"></a>DXGI_FORMAT_B8G8R8X8 \_ unorm \_ sRGB<sup></sup> -Fehler (93)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| 8X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a>DXGI_FORMAT_AYUV<sup>V</sup> (100)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | ![Optional](images/letter-o.jpg) |
| Eingabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Ausgabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_y410supvsup-101"></a>DXGI_FORMAT_Y410<sup>V</sup> (101)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | ![Optional](images/letter-o.jpg) |
| Eingabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Ausgabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_y416supvsup-102"></a>DXGI_FORMAT_Y416<sup>V</sup> (102)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | ![Optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | ![Optional](images/letter-o.jpg) |
| Eingabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Ausgabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_nv12supvsup-103"></a>DXGI_FORMAT_NV12<sup>V</sup> (103)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | ![Optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | ![Optional](images/letter-o.jpg) |
| Eingabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Ausgabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_p010supvsup-104"></a>DXGI_FORMAT_P010<sup>V</sup> (104)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | ![Optional](images/letter-o.jpg) |
| Eingabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Ausgabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_p016supvsup-105"></a>DXGI_FORMAT_P016<sup>V</sup> (105)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | ![Optional](images/letter-o.jpg) |
| Eingabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Ausgabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a>DXGI_FORMAT_420 nicht transparent \_ <sup>V</sup> (106)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | \- |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | ![Erforderlich](images/letter-r.jpg) |
| Eingabe des Video Prozessors | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a>DXGI_FORMAT_YUY2<sup>V</sup> (107)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | ![Optional](images/letter-o.jpg) |
| Eingabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Ausgabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_y210supvsup-108"></a>DXGI_FORMAT_Y210<sup>V</sup> (108)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | ![Optional](images/letter-o.jpg) |
| Eingabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Ausgabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_y216supvsup-109"></a>DXGI_FORMAT_Y216<sup>V</sup> (109)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | ![Optional](images/letter-o.jpg) |
| Eingabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Ausgabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_nv11supvsup-110"></a>DXGI_FORMAT_NV11<sup>V</sup> (110)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | ![Optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | ![Optional](images/letter-o.jpg) |
| Eingabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Ausgabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_ai44supvsup-111"></a>DXGI_FORMAT_AI44<sup>V</sup> (111)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | ![Optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_ia44supvsup-112"></a>DXGI_FORMAT_IA44<sup>V</sup> (112)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | ![Optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_p8supvsup-113"></a>DXGI_FORMAT_P8<sup>V</sup> (113)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | ![Optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a>DXGI_FORMAT_A8P8<sup>V</sup> (114)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader-Beispiel (nur Punkt Stichprobe) | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a>DXGI_FORMAT_B4G4R4A4 \_ unorm<sup></sup> -Fehler (115)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (nur Punkt Stichprobe) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Optional](images/letter-o.jpg) |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert (min oder max) | \- |
| UAV-atomarer unsigniertes Minimum oder Maximum | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="format-notes"></a>Notizen formatieren

Der Zweck des-Formats kann sich von einer Hardware Funktionsebene zur nächsten ändern.

<dl> <dt>

<sup>L</sup> : typloses Format
</dt> <dt>

<sup>PCs</sup> : teilweise typisiertes, castbares und einfaches Layout
</dt> <dt>

 <sup>FCS</sup> : vollständig typisiertes, castbares und einfaches Layout
</dt> <dt>

<sup>FNS</sup> : vollständig typisiertes, nicht-castbares und einfaches Layout
</dt> <dt>

<sup>PCC</sup> : teilweise typisiertes, castbares und komplexes Layout
</dt> <dt>

 <sup>FCC</sup> : vollständig typisiertes, castbares und komplexes Layout
</dt> <dt>

<sup>FNC</sup> : vollständig typisiertes, nicht-castbares und komplexes Layout
</dt> <dt>

<sup>V</sup> : Videoformat
</dt> </dl>

## <a name="related-topics"></a>Zugehörige Themen

[D3D12-Hardware Funktionsebenen](../direct3d12/hardware-feature-levels.md)

[Implementieren von Schatten Puffern für Direct3D Feature Level 9](/previous-versions/windows/apps/jj262110(v=win.10))

[Mapping von Legacy Formaten](../direct3d10/d3d10-graphics-programming-guide-resources-legacy-formats.md)

[Programmier Handbuch für DXGI](dx-graphics-dxgi-overviews.md)
