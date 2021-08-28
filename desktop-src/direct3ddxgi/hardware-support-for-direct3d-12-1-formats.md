---
description: In diesem Abschnitt werden die Formate ([**DXGI_FORMAT_)** *](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) angegeben, die in der Direct3D Feature Level 12.1-Hardware unterstützt werden.
ms.assetid: 0DC50FF3-3193-4F3B-9976-EE504C6FCC87
title: Formatunterstützung für Direct3D 12.1-Hardware auf Featureebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 065192ffadf8667f82c0e1b0fc6fac165f103a7ed28982cba1fbc0e14ae47cce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068760"
---
# <a name="format-support-for-direct3d-feature-level-121-hardware"></a>Formatunterstützung für Direct3D 12.1-Hardware auf Featureebene

In diesem Abschnitt werden die Formate ([**DXGI_FORMAT_)** *](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) angegeben, die in der Direct3D Feature Level 12.1-Hardware unterstützt werden.

In der Tabelle wird die Featureunterstützung mithilfe des folgenden Schlüssels zusammengefasst.

| Symbol                            | BESCHREIBUNG                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| **-**                             | Nicht möglich oder nicht verfügbar.                                                  |
| ![Erforderlich](images/letter-r.jpg)  | Hardwareunterstützung ist erforderlich.                                                 |
| ![optional](images/letter-o.jpg)  | Hardwareunterstützung optional, das Format kann hardwarebeschleunigt sein oder nicht. |
| ![Abhängig](images/letter-d.jpg) | Erforderlich, wenn das zugehörige optionale Feature unterstützt wird.                            |

Dieses Thema enthält einen Abschnitt pro Format. Ein *Formatziel* (die Tabellen enthalten eine Zeile pro Ziel) kann ein Ressourcentyp, eine systeminterne HLSL-Funktion oder eine bestimmte Funktionalität sein, die von einem bestimmten Format abhängig ist.

Informationen zur programmgesteuerten Überprüfung der Formatunterstützung in D3D11 und D3D12 finden Sie unter Überprüfen der Unterstützung von [Hardwarefeatures.](checking-hardware-feature-support.md)

> [!NOTE] 
> Die Zahlen der Formate sind größtenteils, aber nicht alle, in aufsteigender numerischer Reihenfolge, einige sind nicht in numerischer Reihenfolge und werden zusammen mit anderen &mdash; relevanten Formaten aufgeführt. Beachten Sie *auch,* dass typlose  Typen in einem Formatnamen teilweise typisch und nicht streng typlos sein können (siehe Abschnitt [Formathinweise](#format-notes) am Ende des Themas).

## <a name="dxgi_format_unknownsuplsup-0"></a>DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 0 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | \- |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a>DXGI_FORMAT_R32G32B32A32_TYPELESS<sup>PCS</sup> (1)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_floatsupfcssup-2"></a>DXGI_FORMAT_R32G32B32A32_FLOAT<sup>FCS</sup> (2)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 128 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Überblendbares RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| Vom UAV typisiertes Laden | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_uintsupfcssup-3"></a>DXGI_FORMAT_R32G32B32A32_UINT<sup>FCS</sup> (3)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | ![Erforderlich](images/letter-r.jpg) |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV-typiertes Laden | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32a32_sintsupfcssup-4"></a>DXGI_FORMAT_R32G32B32A32_SINT<sup>FCS</sup> (4)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV Typed Load | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a>DXGI_FORMAT_R32G32B32_TYPELESS<sup>PCS</sup> (5)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 96 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32b32_floatsupfcssup-6"></a>DXGI_FORMAT_R32G32B32_FLOAT<sup>FCS</sup> (6)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 96 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![optional](images/letter-o.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![optional](images/letter-o.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![optional](images/letter-o.jpg) |
| RenderTarget | ![optional](images/letter-o.jpg) |
| Überblendbares RenderTarget | ![Abhängig](images/letter-d.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Abhängig](images/letter-d.jpg) |
| 8x Multisample RenderTarget | ![Abhängig](images/letter-d.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32b32_uintsupfcssup-7"></a>DXGI_FORMAT_R32G32B32_UINT<sup>FCS</sup> (7)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 96 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![optional](images/letter-o.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | ![Erforderlich](images/letter-r.jpg) |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV-typiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Abhängig](images/letter-d.jpg) |
| 8x Multisample RenderTarget | ![Abhängig](images/letter-d.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32b32_sintsupfcssup-8"></a>DXGI_FORMAT_R32G32B32_SINT<sup>FCS</sup> (8)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 96 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![optional](images/letter-o.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV-typiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Abhängig](images/letter-d.jpg) |
| 8x Multisample RenderTarget | ![Abhängig](images/letter-d.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a>DXGI_FORMAT_R16G16B16A16_TYPELESS<sup>PCS</sup> (9)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV-typiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_floatsupfcssup-10"></a>DXGI_FORMAT_R16G16B16A16_FLOAT<sup>FCS</sup> (10)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Überblendbares RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| Vom UAV typisiertes Laden | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | ![Erforderlich](images/letter-r.jpg) |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | ![optional](images/letter-o.jpg) |
| Videoprozessorausgabe | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_unormsupfcssup-11"></a>DXGI_FORMAT_R16G16B16A16_UNORM<sup>FCS</sup> (11)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV Typed Load | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_uintsupfcssup-12"></a>DXGI_FORMAT_R16G16B16A16_UINT<sup>FCS</sup> (12)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | ![Erforderlich](images/letter-r.jpg) |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV Typed Load | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_snormsupfcssup-13"></a>DXGI_FORMAT_R16G16B16A16_SNORM<sup>FCS</sup> (13)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Überblendbares RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| Vom UAV typisiertes Laden | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16b16a16_sintsupfcssup-14"></a>DXGI_FORMAT_R16G16B16A16_SINT<sup>FCS</sup> (14)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV Typed Load | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a>DXGI_FORMAT_R32G32_TYPELESS<sup>PCS</sup> (15)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_floatsupfcssup-16"></a>DXGI_FORMAT_R32G32_FLOAT<sup>FCS</sup> (16)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Überblendbares RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| Vom UAV typisiertes Laden | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_uintsupfcssup-17"></a>DXGI_FORMAT_R32G32_UINT<sup>FCS</sup> (17)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | ![Erforderlich](images/letter-r.jpg) |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| Vom UAV typisiertes Laden | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32g32_sintsupfcssup-18"></a>DXGI_FORMAT_R32G32_SINT<sup>FCS</sup> (18)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV Typed Load | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32g8x24_typelesssupvsup-19"></a>DXGI_FORMAT_R32G8X24_TYPELESS<sup>V</sup> (19)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupvsup-20"></a>DXGI_FORMAT_D32_FLOAT_S8X24_UINT<sup>V</sup> (20)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | ![Erforderlich](images/letter-r.jpg) |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV-typiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupvsup-21"></a>DXGI_FORMAT_R32_FLOAT_X8X24_TYPELESS<sup>V</sup> (21)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | ![Erforderlich](images/letter-r.jpg) |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupvsup-22"></a>DXGI_FORMAT_X32_TYPELESS_G8X24_UINT<sup>V</sup> (22)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a>DXGI_FORMAT_R10G10B10A2_TYPELESS<sup>PCS</sup> (23)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10a2_unormsupfcssup-24"></a>DXGI_FORMAT_R10G10B10A2_UNORM<sup>FCS</sup> (24)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Überblendbares RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV-typiertes Laden | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | ![Erforderlich](images/letter-r.jpg) |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | ![optional](images/letter-o.jpg) |
| Videoprozessorausgabe | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10a2_uintsupfcssup-25"></a>DXGI_FORMAT_R10G10B10A2_UINT<sup>FCS</sup> (25)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | ![Erforderlich](images/letter-r.jpg) |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV-typiertes Laden | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfcssup-89"></a>DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM<sup>FCS</sup> (89)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | \- |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | ![Erforderlich](images/letter-r.jpg) |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | ![optional](images/letter-o.jpg) |
| Videoprozessorausgabe | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a>DXGI_FORMAT_R11G11B10_FLOAT<sup>FNS</sup> (26)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Überblendbares RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| Vom UAV typisiertes Laden | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a>DXGI_FORMAT_R8G8B8A8_TYPELESS<sup>PCS</sup> (27)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_unormsupfcssup-28"></a>DXGI_FORMAT_R8G8B8A8_UNORM<sup>FCS</sup> (28)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Überblendbares RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| Vom UAV typisiertes Laden | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | ![Erforderlich](images/letter-r.jpg) |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | ![optional](images/letter-o.jpg) |
| Videoprozessorausgabe | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfcssup-29"></a>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB<sup>FCS</sup> (29)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV-typiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | ![Erforderlich](images/letter-r.jpg) |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | ![optional](images/letter-o.jpg) |
| Videoprozessorausgabe | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_uintsupfcssup-30"></a>DXGI_FORMAT_R8G8B8A8_UINT<sup>FCS</sup> (30)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | ![Erforderlich](images/letter-r.jpg) |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV Typed Load | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_snormsupfcssup-31"></a>DXGI_FORMAT_R8G8B8A8_SNORM<sup>FCS</sup> (31)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV Typed Load | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8b8a8_sintsupfcssup-32"></a>DXGI_FORMAT_R8G8B8A8_SINT<sup>FCS</sup> (32)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| Vom UAV typisiertes Laden | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a>DXGI_FORMAT_R16G16_TYPELESS<sup>PCS</sup> (33)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV-typiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_floatsupfcssup-34"></a>DXGI_FORMAT_R16G16_FLOAT<sup>FCS</sup> (34)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV-typiertes Laden | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_unormsupfcssup-35"></a>DXGI_FORMAT_R16G16_UNORM<sup>FCS</sup> (35)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV-typiertes Laden | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_uintsupfcssup-36"></a>DXGI_FORMAT_R16G16_UINT<sup>FCS</sup> (36)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | ![Erforderlich](images/letter-r.jpg) |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| Vom UAV typisiertes Laden | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_snormsupfcssup-37"></a>DXGI_FORMAT_R16G16_SNORM<sup>FCS</sup> (37)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV-typiertes Laden | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16g16_sintsupfcssup-38"></a>DXGI_FORMAT_R16G16_SINT<sup>FCS</sup> (38)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV-typiertes Laden | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a>DXGI_FORMAT_R32_TYPELESS<sup>PCS</sup> (39)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | ![Erforderlich](images/letter-r.jpg) |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_d32_floatsupfcssup-40"></a>DXGI_FORMAT_D32_FLOAT<sup>FCS</sup> (40)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | ![Erforderlich](images/letter-r.jpg) |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV-typiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32_floatsupfcssup-41"></a>DXGI_FORMAT_R32_FLOAT<sup>FCS</sup> (41)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | ![Erforderlich](images/letter-r.jpg) |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV-typiertes Laden | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32_uintsupfcssup-42"></a>DXGI_FORMAT_R32_UINT<sup>FCS</sup> (42)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Streamausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | ![Erforderlich](images/letter-r.jpg) |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| Vom UAV typisiertes Laden | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Add | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Bitwise Ops | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Cmp&Store/Cmp&Exch | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Exchange | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Signed Min/Max | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Unsigned Min/Max | ![Erforderlich](images/letter-r.jpg) |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r32_sintsupfcssup-43"></a>DXGI_FORMAT_R32_SINT<sup>FCS</sup> (43)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | ![Erforderlich](images/letter-r.jpg) |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| Vom UAV typisiertes Laden | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Add | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Bitwise Ops | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Cmp&Store/Cmp&Exch | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Exchange | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Signed Min/Max | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Unsigned Min/Max | ![Erforderlich](images/letter-r.jpg) |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r24g8_typelesssupvsup-44"></a>DXGI_FORMAT_R24G8_TYPELESS<sup>V</sup> (44)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupvsup-45"></a>DXGI_FORMAT_D24_UNORM_S8_UINT<sup>V</sup> (45)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | ![Erforderlich](images/letter-r.jpg) |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupvsup-46"></a>DXGI_FORMAT_R24_UNORM_X8_TYPELESS<sup>V</sup> (46)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | ![Erforderlich](images/letter-r.jpg) |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupvsup-47"></a>DXGI_FORMAT_X24_TYPELESS_G8_UINT<sup>V</sup> (47)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a>DXGI_FORMAT_R8G8_TYPELESS<sup>PCS</sup> (48)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 16 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_unormsupfcssup-49"></a>DXGI_FORMAT_R8G8_UNORM<sup>FCS</sup> (49)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 16 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV-typiertes Laden | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_uintsupfcssup-50"></a>DXGI_FORMAT_R8G8_UINT<sup>FCS</sup> (50)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | ![Erforderlich](images/letter-r.jpg) |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| Vom UAV typisiertes Laden | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_snormsupfcssup-51"></a>DXGI_FORMAT_R8G8_SNORM<sup>FCS</sup> (51)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 16 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Überblendbares RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| Vom UAV typisiertes Laden | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_sintsupfcssup-52"></a>DXGI_FORMAT_R8G8_SINT<sup>FCS</sup> (52)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV-typiertes Laden | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a>DXGI_FORMAT_R16_TYPELESS<sup>PCS</sup> (53)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16_floatsupfcssup-54"></a>DXGI_FORMAT_R16_FLOAT<sup>FCS</sup> (54)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 16 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Überblendbares RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| Vom UAV typisiertes Laden | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_d16_unormsupfcssup-55"></a>DXGI_FORMAT_D16_UNORM<sup>FCS</sup> (55)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | ![Erforderlich](images/letter-r.jpg) |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16_unormsupfcssup-56"></a>DXGI_FORMAT_R16_UNORM<sup>FCS</sup> (56)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | ![Erforderlich](images/letter-r.jpg) |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV Typed Load | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16_uintsupfcssup-57"></a>DXGI_FORMAT_R16_UINT<sup>FCS</sup> (57)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | ![Erforderlich](images/letter-r.jpg) |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV-typiertes Laden | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16_snormsupfcssup-58"></a>DXGI_FORMAT_R16_SNORM<sup>FCS</sup> (58)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV-typiertes Laden | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r16_sintsupfcssup-59"></a>DXGI_FORMAT_R16_SINT<sup>FCS</sup> (59)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV-typiertes Laden | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a>DXGI_FORMAT_R8_TYPELESS<sup>PCS</sup> (60)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8_unormsupfcssup-61"></a>DXGI_FORMAT_R8_UNORM<sup>FCS</sup> (61)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 8 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Überblendbares RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| Vom UAV typisiertes Laden | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8_uintsupfcssup-62"></a>DXGI_FORMAT_R8_UINT<sup>FCS</sup> (62)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | ![Erforderlich](images/letter-r.jpg) |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV-typiertes Laden | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8_snormsupfcssup-63"></a>DXGI_FORMAT_R8_SNORM<sup>FCS</sup> (63)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 8 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Überblendbares RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| Vom UAV typisiertes Laden | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8_sintsupfcssup-64"></a>DXGI_FORMAT_R8_SINT<sup>FCS</sup> (64)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 8 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| Vom UAV typisiertes Laden | ![Erforderlich](images/letter-r.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a>DXGI_FORMAT_A8_UNORM<sup>FNS</sup> (65)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 8 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Überblendbares RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| Vom UAV typisiertes Laden | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a>DXGI_FORMAT_R9G9B9E5_SHAREDEXP<sup>FNC</sup> (67)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a>DXGI_FORMAT_R8G8_B8G8_UNORM<sup>FNC</sup> (68)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 16 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a>DXGI_FORMAT_G8R8_G8B8_UNORM<sup>FNC</sup> (69)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 16 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a>DXGI_FORMAT_BC1_TYPELESS<sup>PCC</sup> (70)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc1_unorm-supfccsup-71"></a>DXGI_FORMAT_BC1_UNORM <sup>FCC</sup> (71)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV-typiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc1_unorm_srgb-supfccsup-72"></a>DXGI_FORMAT_BC1_UNORM_SRGB <sup>FCC</sup> (72)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV-typiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a>DXGI_FORMAT_BC2_TYPELESS<sup>PCC</sup> (73)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_unorm-supfccsup-74"></a>DXGI_FORMAT_BC2_UNORM <sup>FCC</sup> (74)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 128 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc2_unorm_srgb-supfccsup-75"></a>DXGI_FORMAT_BC2_UNORM_SRGB <sup>FCC</sup> (75)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV-typiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a>DXGI_FORMAT_BC3_TYPELESS<sup>PCC</sup> (76)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_unorm-supfccsup-77"></a>DXGI_FORMAT_BC3_UNORM <sup>FCC</sup> (77)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc3_unorm_srgb-supfccsup-78"></a>DXGI_FORMAT_BC3_UNORM_SRGB <sup>FCC</sup> (78)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 128 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a>DXGI_FORMAT_BC4_TYPELESS<sup>PCC</sup> (79)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| UAV-typiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_unorm-supfccsup-80"></a>DXGI_FORMAT_BC4_UNORM <sup>FCC</sup> (80)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV-typiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc4_snorm-supfccsup-81"></a>DXGI_FORMAT_BC4_SNORM <sup>FCC</sup> (81)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a>DXGI_FORMAT_BC5_TYPELESS<sup>PCC</sup> (82)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_unorm-supfccsup-83"></a>DXGI_FORMAT_BC5_UNORM <sup>FCC</sup> (83)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 128 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc5_snorm-supfccsup-84"></a>DXGI_FORMAT_BC5_SNORM <sup>FCC</sup> (84)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 128 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a>DXGI_FORMAT_B5G6R5_UNORM<sup>FNS</sup> (85)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![optional](images/letter-o.jpg) |
| Vertexpuffer des Eingabe-Assemblers | ![optional](images/letter-o.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![optional](images/letter-o.jpg) |
| Typierte UAV-Store | ![optional](images/letter-o.jpg) |
| UAV Typed Load | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Andere Multisampleanzahl RT | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Last | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a>DXGI_FORMAT_B5G5R5A1_UNORM<sup>FNS</sup> (86)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![optional](images/letter-o.jpg) |
| Vertexpuffer des Eingabe-Assemblers | ![optional](images/letter-o.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![optional](images/letter-o.jpg) |
| RenderTarget | ![optional](images/letter-o.jpg) |
| Blendable RenderTarget | ![optional](images/letter-o.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![optional](images/letter-o.jpg) |
| Typierte UAV-Store | ![optional](images/letter-o.jpg) |
| UAV-typiertes Laden | ![optional](images/letter-o.jpg) |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Last | ![optional](images/letter-o.jpg) |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a>DXGI_FORMAT_B8G8R8A8_TYPELESS<sup>PCS</sup> (90)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_unormsupfcssup-87"></a>DXGI_FORMAT_B8G8R8A8_UNORM<sup>FCS</sup> (87)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Überblendbares RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | ![Erforderlich](images/letter-r.jpg) |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | ![optional](images/letter-o.jpg) |
| Videoprozessorausgabe | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfcssup-91"></a>DXGI_FORMAT_B8G8R8A8_UNORM_SRGB<sup>FCS</sup> (91)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Überblendbares RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | ![Erforderlich](images/letter-r.jpg) |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | ![optional](images/letter-o.jpg) |
| Videoprozessorausgabe | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a>DXGI_FORMAT_B8G8R8X8_TYPELESS<sup>PCS</sup> (92)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV-typiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_unormsupfcssup-88"></a>DXGI_FORMAT_B8G8R8X8_UNORM<sup>FCS</sup> (88)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | ![Erforderlich](images/letter-r.jpg) |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | ![optional](images/letter-o.jpg) |
| Videoprozessorausgabe | ![optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfcssup-93"></a>DXGI_FORMAT_B8G8R8X8_UNORM_SRGB<sup>FCS</sup> (93)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | ![Erforderlich](images/letter-r.jpg) |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Überblendbares RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| 8x Multisample RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Ladevorgang | ![Erforderlich](images/letter-r.jpg) |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_typelesssuppccsup-94"></a>DXGI_FORMAT_BC6H_TYPELESS<sup>PCC</sup> (94)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV-typiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_uf16-supfccsup-95"></a>DXGI_FORMAT_BC6H_UF16 <sup>FCC</sup> (95)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc6h_sf16-supfccsup-96"></a>DXGI_FORMAT_BC6H_SF16 <sup>FCC</sup> (96)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_typelesssuppccsup-97"></a>DXGI_FORMAT_BC7_TYPELESS<sup>PCC</sup> (97)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV-typiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_unorm-supfccsup-98"></a>DXGI_FORMAT_BC7_UNORM <sup>FCC</sup> (98)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 128 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV-typiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_bc7_unorm_srgb-supfccsup-99"></a>DXGI_FORMAT_BC7_UNORM_SRGB <sup>FCC</sup> (99)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 128 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | ![Erforderlich](images/letter-r.jpg) |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | ![Erforderlich](images/letter-r.jpg) |

## <a name="dxgi_format_ayuvsupvsup-100"></a>DXGI_FORMAT_AYUV<sup>V</sup> (100)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Überblendbares RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | ![optional](images/letter-o.jpg) |
| Videoprozessoreingabe | ![Erforderlich](images/letter-r.jpg) |
| Videoprozessorausgabe | ![optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_y410supvsup-101"></a>DXGI_FORMAT_Y410<sup>V</sup> (101)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | \- |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | ![optional](images/letter-o.jpg) |
| Videoprozessoreingabe | ![optional](images/letter-o.jpg) |
| Videoprozessorausgabe | ![optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_y416supvsup-102"></a>DXGI_FORMAT_Y416<sup>V</sup> (102)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Formatunterstützung | ![optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung für Videodecoder | ![optional](images/letter-o.jpg) |
| Videoprozessoreingabe | ![optional](images/letter-o.jpg) |
| Videoprozessorausgabe | ![optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_nv12supvsup-103"></a>DXGI_FORMAT_NV12<sup>V</sup> (103)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | \- |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV-typiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | ![Erforderlich](images/letter-r.jpg) |
| Videoprozessoreingabe | ![Erforderlich](images/letter-r.jpg) |
| Videoprozessorausgabe | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_p010supvsup-104"></a>DXGI_FORMAT_P010<sup>V</sup> (104)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Formatunterstützung | ![optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | \- |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV-typiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | ![optional](images/letter-o.jpg) |
| Videoprozessoreingabe | ![optional](images/letter-o.jpg) |
| Videoprozessorausgabe | ![optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_p016supvsup-105"></a>DXGI_FORMAT_P016<sup>V</sup> (105)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Formatunterstützung | ![optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | \- |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Überblendbares RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | ![optional](images/letter-o.jpg) |
| Videoprozessoreingabe | ![optional](images/letter-o.jpg) |
| Videoprozessorausgabe | ![optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a>DXGI_FORMAT_420_OPAQUE<sup>V</sup> (106)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 8 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | \- |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung für Videodecoder | ![Erforderlich](images/letter-r.jpg) |
| Videoprozessoreingabe | ![Erforderlich](images/letter-r.jpg) |
| Videoprozessorausgabe | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a>DXGI_FORMAT_YUY2<sup>V</sup> (107)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | \- |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung für Videodecoder | ![optional](images/letter-o.jpg) |
| Videoprozessoreingabe | ![Erforderlich](images/letter-r.jpg) |
| Videoprozessorausgabe | ![optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_y210supvsup-108"></a>DXGI_FORMAT_Y210<sup>V</sup> (108)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | ![optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | \- |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | ![optional](images/letter-o.jpg) |
| Videoprozessoreingabe | ![optional](images/letter-o.jpg) |
| Videoprozessorausgabe | ![optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_y216supvsup-109"></a>DXGI_FORMAT_Y216<sup>V</sup> (109)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | \- |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | ![Erforderlich](images/letter-r.jpg) |
| Typisierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | ![optional](images/letter-o.jpg) |
| Videoprozessoreingabe | ![optional](images/letter-o.jpg) |
| Videoprozessorausgabe | ![optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_nv11supvsup-110"></a>DXGI_FORMAT_NV11<sup>V</sup> (110)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Formatunterstützung | ![optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | ![Erforderlich](images/letter-r.jpg) |
| Shader-gather4_c | \- |
| Mipmap | \- |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Blendable RenderTarget | ![Erforderlich](images/letter-r.jpg) |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | ![Erforderlich](images/letter-r.jpg) |
| Typierte UAV-Store | ![Erforderlich](images/letter-r.jpg) |
| UAV-typiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | ![optional](images/letter-o.jpg) |
| Videoprozessoreingabe | ![optional](images/letter-o.jpg) |
| Videoprozessorausgabe | ![optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_ai44supvsup-111"></a>DXGI_FORMAT_AI44<sup>V</sup> (111)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Formatunterstützung | ![optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | \- |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | ![Erforderlich](images/letter-r.jpg) |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_ia44supvsup-112"></a>DXGI_FORMAT_IA44<sup>V</sup> (112)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 8 |
| Formatunterstützung | ![optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (mono 1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | \- |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | ![Erforderlich](images/letter-r.jpg) |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_p8supvsup-113"></a>DXGI_FORMAT_P8<sup>V</sup> (113)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 8 |
| Formatunterstützung | ![optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | \- |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV-typiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | ![Erforderlich](images/letter-r.jpg) |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_a8p8supvsup-114"></a>DXGI_FORMAT_A8P8<sup>V</sup> (114)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Formatunterstützung | ![optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shader ld | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shader sample_c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1_bit_filter) | \- |
| Shader gather4 | \- |
| Shader-gather4_c | \- |
| Mipmap | \- |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | \- |
| Unformat UAV und SRV | \- |
| Strukturierte UAV und SRV | \- |
| Typierte UAV | \- |
| Typierte UAV-Store | \- |
| UAV-typiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min/Max | \- |
| UAV Atomic Unsigned Min/Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | ![Erforderlich](images/letter-r.jpg) |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| BackBuffer Castable Even Fully Typed | \- |
| Gekachelte Ressource | \- |

## <a name="format-notes"></a>Formathinweise

Der Zweck des Formats kann sich von einer Hardwarefeatureebene zur nächsten ändern.

<dl> <dt>

<sup>L</sup> : typloses Format
</dt> <dt>

<sup>PCS:</sup> teilweise typisierbares, castable- und einfaches Layout
</dt> <dt>

 <sup>FCS:</sup> vollständig typisierbares, castfähiges und einfaches Layout
</dt> <dt>

<sup>FNS:</sup> vollständig typisch, nicht castierbar und einfaches Layout
</dt> <dt>

<sup>PCC:</sup> teilweise typiertes, castables und komplexes Layout
</dt> <dt>

 <sup>FCC:</sup> vollständig typisierbares, castables und komplexes Layout
</dt> <dt>

<sup>FNC:</sup> vollständig typiertes, nicht castierbares und komplexes Layout
</dt> <dt>

<sup>V:</sup> Videoformat
</dt> </dl>

## <a name="dxgi_format_related-topics"></a>DXGI_FORMAT_Related Themen

[D3D12-Hardwarefeatureebenen](../direct3d12/hardware-feature-levels.md)

[Programmierhandbuch für DXGI](dx-graphics-dxgi-overviews.md)
