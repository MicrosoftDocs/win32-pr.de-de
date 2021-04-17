---
description: In diesem Abschnitt werden die Formate ([**DXGI_FORMAT_** _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) -Werte) angegeben, die auf Direct3D Feature Level 11,0-Hardware unterstützt werden.
ms.assetid: 735CDA40-557F-4D47-87B7-97A8E120B9D2
title: Formatunterstützung für Direct3D 11.0-Hardware auf Featureebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2f498028493781c841dff714c075449426b40c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104563288"
---
# <a name="format-support-for-direct3d-feature-level-110-hardware"></a>Formatunterstützung für Direct3D 11.0-Hardware auf Featureebene

In diesem Abschnitt werden die Formate ([_* DXGI_FORMAT_* * _](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) -Werte) angegeben, die auf Direct3D Feature Level 11,0-Hardware unterstützt werden.

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
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
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
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a>DXGI_FORMAT_R32G32B32A32 \_ Typen losen<sup>PCs</sup> (1)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a>DXGI_FORMAT_R32G32B32A32 \_ float<sup></sup> -Zeichen (2)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a>DXGI_FORMAT_R32G32B32A32 \_ uint-<sup>f</sup> (3)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | ![Optional](images/letter-o.jpg) |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a>DXGI_FORMAT_R32G32B32A32 \_ Sint<sup></sup> (4)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a>DXGI_FORMAT_R32G32B32 \_ Typen losen<sup>PCs</sup> (5)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 96 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a>DXGI_FORMAT_R32G32B32 \_ float<sup></sup> -Zeichen (6)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 96 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Optional](images/letter-o.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Optional](images/letter-o.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Optional](images/letter-o.jpg) |
| RenderTarget | ![Optional](images/letter-o.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![lässe](images/letter-d.jpg) |
| 8X-Multisample-renderTarget | ![lässe](images/letter-d.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a>DXGI_FORMAT_R32G32B32 \_ uint-<sup>f</sup> (7)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 96 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Optional](images/letter-o.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | ![Optional](images/letter-o.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![lässe](images/letter-d.jpg) |
| 8X-Multisample-renderTarget | ![lässe](images/letter-d.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a>DXGI_FORMAT_R32G32B32 \_ Sint<sup></sup> -Karten (8)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 96 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Optional](images/letter-o.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![lässe](images/letter-d.jpg) |
| 8X-Multisample-renderTarget | ![lässe](images/letter-d.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a>DXGI_FORMAT_R16G16B16A16 \_ Typen losen<sup>PCs</sup> (9)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a>DXGI_FORMAT_R16G16B16A16 \_ float<sup></sup> -Zeichen (10)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | ![Erforderlich](images/letter-r.jpg) |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Ausgabe des Video Prozessors | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a>DXGI_FORMAT_R16G16B16A16 \_ unorm-Datei-<sup>e</sup> /a (11)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a>DXGI_FORMAT_R16G16B16A16 \_ uint-<sup>f</sup> (12)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | ![Optional](images/letter-o.jpg) |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a>DXGI_FORMAT_R16G16B16A16 \_ snorm<sup></sup> -snorm (13)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a>DXGI_FORMAT_R16G16B16A16 \_ Sint<sup></sup> (14)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a>DXGI_FORMAT_R32G32 \_ Typen losen<sup>PCs</sup> (15)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a>DXGI_FORMAT_R32G32 \_ float<sup></sup> -Zeichen (16)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a>DXGI_FORMAT_R32G32 \_ uint<sup></sup> -Zeichen (17)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | ![Optional](images/letter-o.jpg) |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a>DXGI_FORMAT_R32G32 \_ Sint<sup></sup> -Datei (18)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a>DXGI_FORMAT_R32G8X24 \_ Typen losen<sup>PCs</sup> (19)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfcssup-20"></a>DXGI_FORMAT_D32 \_ float \_ S8X24 \_ uint-<sup>f</sup> (20)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfcssup-21"></a>DXGI_FORMAT_R32 \_ float \_ X8X24 \_ typlose<sup></sup> Rechtschreibfehler (21)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfcssup-22"></a>DXGI_FORMAT_X32 \_ typlose \_ G8X24 \_ uint-<sup>f</sup> (22)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a>DXGI_FORMAT_R10G10B10A2 \_ typlosen<sup>PCs</sup> (23)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a>DXGI_FORMAT_R10G10B10A2 \_ unorm-Datei-<sup>e</sup> /a (24)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | ![Erforderlich](images/letter-r.jpg) |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Ausgabe des Video Prozessors | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a>DXGI_FORMAT_R10G10B10A2 \_ uint<sup></sup> -Zeichen (25)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | ![Optional](images/letter-o.jpg) |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a>DXGI_FORMAT_R10G10B10 \_ XR \_ Bias \_ a2 \_ unorm-Datei-<sup>e</sup> /a (89)
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
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | ![Erforderlich](images/letter-r.jpg) |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Ausgabe des Video Prozessors | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a>DXGI_FORMAT_R11G11B10 \_ float<sup></sup> -Datentyp (26)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a>DXGI_FORMAT_R8G8B8A8 \_ typlosen<sup>PCs</sup> (27)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a>DXGI_FORMAT_R8G8B8A8 \_ unorm-Datei-<sup>e</sup> /a (28)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | ![Erforderlich](images/letter-r.jpg) |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Ausgabe des Video Prozessors | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a>DXGI_FORMAT_R8G8B8A8 \_ unorm \_ sRGB-<sup>FICS</sup> (29)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | ![Erforderlich](images/letter-r.jpg) |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Ausgabe des Video Prozessors | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a>DXGI_FORMAT_R8G8B8A8 \_ uint<sup></sup> -Zeichen (30)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | ![Optional](images/letter-o.jpg) |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a>DXGI_FORMAT_R8G8B8A8 \_ snorm<sup></sup> -snorm (31)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a>DXGI_FORMAT_R8G8B8A8 \_ Sint<sup></sup> -Werte (32)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a>DXGI_FORMAT_R16G16 \_ Typen losen<sup>PCs</sup> (33)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a>DXGI_FORMAT_R16G16 \_ float<sup></sup> -Zeichen (34)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a>DXGI_FORMAT_R16G16 \_ unorm-Datei-<sup>e</sup> /a (35)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a>DXGI_FORMAT_R16G16 \_ uint-<sup>f</sup> (36)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | ![Optional](images/letter-o.jpg) |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a>DXGI_FORMAT_R16G16 \_ snorm<sup></sup> -snorm (37)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a>DXGI_FORMAT_R16G16 \_ Sint<sup></sup> -Werte (38)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a>DXGI_FORMAT_R32 \_ Typen losen<sup>PCs</sup> (39)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | ![Erforderlich](images/letter-r.jpg) |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | \- |
| Mit UAV typisierter Speicher | \- |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a>DXGI_FORMAT_D32 \_ float<sup></sup> -Zeichen (40)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a>DXGI_FORMAT_R32 \_ float<sup></sup> -Zeichen (41)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | ![Erforderlich](images/letter-r.jpg) |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | ![Erforderlich](images/letter-r.jpg) |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a>DXGI_FORMAT_R32 \_ uint-<sup>f</sup> (42)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | ![Erforderlich](images/letter-r.jpg) |
| Stream-Ausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | ![Optional](images/letter-o.jpg) |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Add | ![Erforderlich](images/letter-r.jpg) |
| Atomarische UAV-OPS | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic CMP&Store/CMP&Exch | ![Erforderlich](images/letter-r.jpg) |
| Atomarer UAV-Austausch | ![Erforderlich](images/letter-r.jpg) |
| UAV-atomarischer Mindestwert/max. | ![Erforderlich](images/letter-r.jpg) |
| UAV-atomarische unsignierte Min/Max | ![Erforderlich](images/letter-r.jpg) |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a>DXGI_FORMAT_R32 \_ Sint<sup></sup> -Werte (43)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Add | ![Erforderlich](images/letter-r.jpg) |
| Atomarische UAV-OPS | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic CMP&Store/CMP&Exch | ![Erforderlich](images/letter-r.jpg) |
| Atomarer UAV-Austausch | ![Erforderlich](images/letter-r.jpg) |
| UAV-atomarischer Mindestwert/max. | ![Erforderlich](images/letter-r.jpg) |
| UAV-atomarische unsignierte Min/Max | ![Erforderlich](images/letter-r.jpg) |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a>DXGI_FORMAT_R24G8 \_ Typen losen<sup>PCs</sup> (44)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfcssup-45"></a>DXGI_FORMAT_D24 \_ unorm \_ S8 \_ uint<sup></sup> -Zeichen (45)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfcssup-46"></a>DXGI_FORMAT_R24 \_ unorm \_ X8- \_ typlosen<sup>f</sup> (46)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfcssup-47"></a>DXGI_FORMAT_X24 \_ typlose \_ G8 \_ uint<sup></sup> -Zeichen (47)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a>DXGI_FORMAT_R8G8 \_ Typen losen<sup>PCs</sup> (48)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a>DXGI_FORMAT_R8G8 \_ unorm-Datei-<sup>e</sup> /a (49)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a>DXGI_FORMAT_R8G8 \_ uint-<sup>f</sup> (50)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | ![Optional](images/letter-o.jpg) |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a>DXGI_FORMAT_R8G8 \_ snorm<sup></sup> -snorm (51)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a>DXGI_FORMAT_R8G8 \_ Sint<sup></sup> -Werte (52)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a>DXGI_FORMAT_R16 \_ Typen losen<sup>PCs</sup> (53)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a>DXGI_FORMAT_R16 \_ float<sup></sup> -Zeichen (54)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a>DXGI_FORMAT_D16 \_ unorm-Datei-<sup>e</sup> /a (55)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a>DXGI_FORMAT_R16 \_ unorm-Datei-<sup>e</sup> /a (56)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | ![Erforderlich](images/letter-r.jpg) |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a>DXGI_FORMAT_R16 \_ uint-<sup>f</sup> (57)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | ![Erforderlich](images/letter-r.jpg) |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | ![Optional](images/letter-o.jpg) |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a>DXGI_FORMAT_R16 \_ snorm<sup></sup> -snorm (58)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a>DXGI_FORMAT_R16 \_ Sint<sup></sup> -Werte (59)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a>DXGI_FORMAT_R8 \_ Typen losen<sup>PCs</sup> (60)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a>DXGI_FORMAT_R8 \_ unorm-Datei-<sup>e</sup> /a (61)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a>DXGI_FORMAT_R8 \_ uint-<sup>f</sup> (62)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | ![Optional](images/letter-o.jpg) |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a>DXGI_FORMAT_R8 \_ snorm<sup></sup> -snorm (63)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a>DXGI_FORMAT_R8 \_ Sint<sup></sup> -Werte (64)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a>DXGI_FORMAT_A8 \_ unorm<sup></sup> -Fehler (65)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a>DXGI_FORMAT_R9G9B9E5 \_ sharede XP-<sup>LNC</sup> (67)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
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
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a>DXGI_FORMAT_R8G8 \_ B8G8 \_ unorm<sup></sup> -Fehler (68)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
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
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a>DXGI_FORMAT_G8R8 \_ G8B8 \_ unorm<sup></sup> -Fehler (69)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
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
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a>DXGI_FORMAT_BC1 \_ typloses<sup>PCC</sup> (70)
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
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_bc1_unorm-supfccsup-71"></a>DXGI_FORMAT_BC1 \_ unorm <sup>FCC</sup> (71)
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
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_bc1_unorm_srgb-supfccsup-72"></a>DXGI_FORMAT_BC1 \_ unorm \_ sRGB <sup>FCC</sup> (72)
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
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a>DXGI_FORMAT_BC2 \_ typloses<sup>PCC</sup> (73)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_bc2_unorm-supfccsup-74"></a>DXGI_FORMAT_BC2 \_ unorm <sup>FCC</sup> (74)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_bc2_unorm_srgb-supfccsup-75"></a>DXGI_FORMAT_BC2 \_ unorm \_ sRGB <sup>FCC</sup> (75)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a>DXGI_FORMAT_BC3 \_ typloses<sup>PCC</sup> (76)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_bc3_unorm-supfccsup-77"></a>DXGI_FORMAT_BC3 \_ unorm <sup>FCC</sup> (77)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_bc3_unorm_srgb-supfccsup-78"></a>DXGI_FORMAT_BC3 \_ unorm \_ sRGB <sup>FCC</sup> (78)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a>DXGI_FORMAT_BC4 \_ typloses<sup>PCC</sup> (79)
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
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_bc4_unorm-supfccsup-80"></a>DXGI_FORMAT_BC4 \_ unorm <sup>FCC</sup> (80)
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
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_bc4_snorm-supfccsup-81"></a>DXGI_FORMAT_BC4 \_ snorm <sup>FCC</sup> (81)
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
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a>DXGI_FORMAT_BC5 \_ typloses<sup>PCC</sup> (82)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_bc5_unorm-supfccsup-83"></a>DXGI_FORMAT_BC5 \_ unorm <sup>FCC</sup> (83)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_bc5_snorm-supfccsup-84"></a>DXGI_FORMAT_BC5 \_ snorm <sup>FCC</sup> (84)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a>DXGI_FORMAT_B5G6R5 \_ unorm<sup></sup> -Fehler (85)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Optional](images/letter-o.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Optional](images/letter-o.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Optional](images/letter-o.jpg) |
| Mit UAV typisierter Speicher | ![Optional](images/letter-o.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a>DXGI_FORMAT_B5G5R5A1 \_ unorm<sup></sup> -Fehler (86)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Optional](images/letter-o.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Optional](images/letter-o.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Optional](images/letter-o.jpg) |
| RenderTarget | ![Optional](images/letter-o.jpg) |
| Blendable renderTarget | ![Optional](images/letter-o.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Optional](images/letter-o.jpg) |
| Mit UAV typisierter Speicher | ![Optional](images/letter-o.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| 8X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Optional](images/letter-o.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a>DXGI_FORMAT_B8G8R8A8 \_ Typen losen<sup>PCs</sup> (90)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a>DXGI_FORMAT_B8G8R8A8 \_ unorm-Datei-<sup>e</sup> /a (87)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | ![Erforderlich](images/letter-r.jpg) |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Ausgabe des Video Prozessors | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a>DXGI_FORMAT_B8G8R8A8 \_ unorm \_ sRGB-Datei-<sup>e</sup> /a (91)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | ![Erforderlich](images/letter-r.jpg) |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Ausgabe des Video Prozessors | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a>DXGI_FORMAT_B8G8R8X8 \_ Typen losen<sup>PCs</sup> (92)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a>DXGI_FORMAT_B8G8R8X8 \_ unorm-Datei-<sup>e</sup> /a (88)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Ausgabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a>DXGI_FORMAT_B8G8R8X8 \_ unorm \_ sRGB-Datei-<sup>e</sup> /a (93)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8X-Multisample-renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Erforderlich](images/letter-r.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_bc6h_typelesssuppccsup-94"></a>DXGI_FORMAT_BC6H \_ typloses<sup>PCC</sup> (94)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_bc6h_uf16-supfccsup-95"></a>DXGI_FORMAT_BC6H \_ UF16 <sup>FCC</sup> (95)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_bc6h_sf16-supfccsup-96"></a>DXGI_FORMAT_BC6H \_ - <sup></sup> SF16 (96)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_bc7_typelesssuppccsup-97"></a>DXGI_FORMAT_BC7 \_ typloses<sup>PCC</sup> (97)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_bc7_unorm-supfccsup-98"></a>DXGI_FORMAT_BC7 \_ unorm <sup>FCC</sup> (98)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

## <a name="dxgi_format_bc7_unorm_srgb-supfccsup-99"></a>DXGI_FORMAT_BC7 \_ unorm \_ sRGB <sup>FCC</sup> (99)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertex-Puffer des Eingabe Assemblers | \- |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

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
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | ![Optional](images/letter-o.jpg) |
| Eingabe des Video Prozessors | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
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
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
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
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
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
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
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
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_nv12supvsup-103"></a>DXGI_FORMAT_NV12<sup>V</sup> (103)
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
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | ![Erforderlich](images/letter-r.jpg) |
| Eingabe des Video Prozessors | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe des Video Prozessors | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
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
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
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
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
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
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
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
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
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
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
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
| Ausgabe des Video Prozessors | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a>DXGI_FORMAT_YUY2<sup>V</sup> (107)
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
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | \- |
| 8X-Multisample-renderTarget | \- |
| Andere Multisample count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Auslastung | \- |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | ![Optional](images/letter-o.jpg) |
| Eingabe des Video Prozessors | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe des Video Prozessors | ![Optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
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
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
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
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
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
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | \- |
| Blendable renderTarget | \- |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
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
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
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
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | \- |
| Automatische Generierung von MipMap | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable renderTarget | ![Erforderlich](images/letter-r.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Mit UAV typisierter Speicher | ![Erforderlich](images/letter-r.jpg) |
| UAV-typisierte Auslastung | \- |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
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
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
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
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
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
| BackBuffer-castfähig, auch vollständig typisiert | \- |
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
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
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
| BackBuffer-castfähig, auch vollständig typisiert | \- |
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
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
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
| BackBuffer-castfähig, auch vollständig typisiert | \- |
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
| Shader LD | \- |
| Shader-Beispiel (beliebiger Filter) | \- |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
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
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
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
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a>DXGI_FORMAT_B4G4R4A4 \_ unorm<sup></sup> -Fehler (115)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Format Unterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Optional](images/letter-o.jpg) |
| Vertex-Puffer des Eingabe Assemblers | ![Optional](images/letter-o.jpg) |
| Index Puffer für Eingabe Assembler | \- |
| Stream-Ausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader LD | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader-Beispiel \_ c (Vergleichs Filter) | \- |
| Shader-Beispiel (mono-1- \_ Bit- \_ Filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader gather4 \_ c | \- |
| MipMap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Generierung von MipMap | ![Optional](images/letter-o.jpg) |
| RenderTarget | ![Optional](images/letter-o.jpg) |
| Blendable renderTarget | ![Optional](images/letter-o.jpg) |
| Ausgabe der Zusammenführungs Logik op | \- |
| Tiefen-/Stencil-Ziel | \- |
| Unformatierte UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typisierte UAV | ![Optional](images/letter-o.jpg) |
| Mit UAV typisierter Speicher | ![Optional](images/letter-o.jpg) |
| UAV-typisierte Auslastung | ![Optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| Atomarische UAV-OPS | \- |
| UAV Atomic CMP&Store/CMP&Exch | \- |
| Atomarer UAV-Austausch | \- |
| UAV-atomarischer Mindestwert/max. | \- |
| UAV-atomarische unsignierte Min/Max | \- |
| CPU-Sperr fähig | ![Erforderlich](images/letter-r.jpg) |
| 4X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| 8X-Multisample-renderTarget | ![Optional](images/letter-o.jpg) |
| Andere Multisample count RT | ![Optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auslastung | ![Optional](images/letter-o.jpg) |
| Anzeige Scan-Out | \- |
| Umwandlung in bitlayout | \- |
| Unterstützung für Video Decoder | \- |
| Eingabe des Video Prozessors | \- |
| Ausgabe des Video Prozessors | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer-castfähig, auch vollständig typisiert | \- |
| Gekachelte Ressource | ![Optional](images/letter-o.jpg) |

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

[Programmier Handbuch für DXGI](dx-graphics-dxgi-overviews.md)
