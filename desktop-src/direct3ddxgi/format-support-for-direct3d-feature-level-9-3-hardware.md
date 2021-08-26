---
description: In diesem Abschnitt werden die Formate [**(DXGI_FORMAT_** *](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) Werte) angegeben, die von Direct3D Feature 10Level9 9.3-Hardware unterstützt werden.
ms.assetid: B2A843D5-6A6B-4180-8B94-D032B1322798
title: Formatunterstützung für Direct3D 9 9.3-Hardware auf Featureebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ad2746ce0d6e277f04783ae7140f3855fa7078e9a50b67d1e52bc827403c4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951280"
---
# <a name="format-support-for-direct3d-feature-10level9-93-hardware"></a>Formatunterstützung für Direct3D 9 9.3-Hardware auf Featureebene

In diesem Abschnitt werden die Formate [**(DXGI_FORMAT_** *](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) Werte) angegeben, die von Direct3D Feature 10Level9 9.3-Hardware unterstützt werden.

In der Tabelle wird die Featureunterstützung mithilfe des folgenden Schlüssels zusammengefasst.

| Symbol                            | BESCHREIBUNG                                                                   |
|-----------------------------------|-------------------------------------------------------------------------------|
| **-**                             | Nicht zulässig oder nicht verfügbar.                                                  |
| ![Erforderlich](images/letter-r.jpg)  | Hardwareunterstützung ist erforderlich.                                                 |
| ![optional](images/letter-o.jpg)  | Hardwareunterstützung optional, das Format kann hardwarebeschleunigend sein oder nicht. |
| ![Abhängig](images/letter-d.jpg) | Erforderlich, wenn das zugehörige optionale Feature unterstützt wird.                            |

Dieses Thema enthält einen Abschnitt pro Format. Ein *Formatziel* (die Tabellen enthalten eine Zeile pro Ziel) kann ein Ressourcentyp, eine systeminterne HLSL-Funktion oder eine bestimmte Funktionalität sein, die von einem bestimmten Format abhängig ist.

Informationen zum programmgesteuerten Überprüfen der Formatunterstützung in D3D11 und D3D12 finden Sie unter [Überprüfen der Unterstützung von Hardwarefeatures.](checking-hardware-feature-support.md)

> [!NOTE] 
> Die Zahlen der Formate sind größtenteils, aber nicht alle, in aufsteigender numerischer Reihenfolge, &mdash; einige liegen außerhalb der numerischen Reihenfolge und werden zusammen mit anderen relevanten Formaten aufgeführt. Beachten Sie auch, dass *typlos* in einem Formatnamen *teilweise typisiert* und nicht streng typlos sein kann (siehe Abschnitt [Formathinweise](#format-notes) am Ende des Themas).

## <a name="dxgi_format_unknownsuplsup-0"></a>DXGI_FORMAT_UNKNOWN<sup>L</sup> (0)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 0 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32b32a32_typelesssuppcssup-1"></a>DXGI_FORMAT_R32G32B32A32 \_ TYPLOSE<sup>PCS</sup> (1)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 128 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32b32a32_floatsupfnssup-2"></a>DXGI_FORMAT_R32G32B32A32 \_ <sup>FLOAT-FNS</sup> (2)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 128 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32b32a32_uintsupfnssup-3"></a>DXGI_FORMAT_R32G32B32A32 \_ <sup>UINT-FNS</sup> (3)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 128 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32b32a32_sintsupfnssup-4"></a>DXGI_FORMAT_R32G32B32A32 \_ <sup>SINT-FNS</sup> (4)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 128 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32b32_typelesssuppcssup-5"></a>DXGI_FORMAT_R32G32B32 \_ TYPLOSE<sup>PCS</sup> (5)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 96 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32b32_floatsupfnssup-6"></a>DXGI_FORMAT_R32G32B32 \_ <sup>FLOAT-FNS</sup> (6)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 96 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Blendable RenderTarget | ![Abhängig](images/letter-d.jpg) |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | \- |
| 4x Multisample RenderTarget | ![Abhängig](images/letter-d.jpg) |
| 8x Multisample RenderTarget | ![Abhängig](images/letter-d.jpg) |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32b32_uintsupfnssup-7"></a>DXGI_FORMAT_R32G32B32 \_ <sup>UINT-FNS</sup> (7)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 96 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
| 4x Multisample RenderTarget | ![Abhängig](images/letter-d.jpg) |
| 8x Multisample RenderTarget | ![Abhängig](images/letter-d.jpg) |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32b32_sintsupfnssup-8"></a>DXGI_FORMAT_R32G32B32 \_ <sup>SINT-FNS</sup> (8)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 96 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
| 4x Multisample RenderTarget | ![Abhängig](images/letter-d.jpg) |
| 8x Multisample RenderTarget | ![Abhängig](images/letter-d.jpg) |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16b16a16_typelesssuppcssup-9"></a>DXGI_FORMAT_R16G16B16A16 \_ TYPLOSE<sup>PCS</sup> (9)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 64 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16b16a16_floatsupfnssup-10"></a>DXGI_FORMAT_R16G16B16A16 \_ <sup>FLOAT-FNS</sup> (10)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![optional](images/letter-o.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16b16a16_unormsupfnssup-11"></a>DXGI_FORMAT_R16G16B16A16 \_ <sup>UNORM-FNS</sup> (11)
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
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16b16a16_uintsupfnssup-12"></a>DXGI_FORMAT_R16G16B16A16 \_ <sup>UINT-FNS</sup> (12)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 64 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16b16a16_snormsupfnssup-13"></a>DXGI_FORMAT_R16G16B16A16 \_ <sup>SNORM-FNS</sup> (13)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16b16a16_sintsupfnssup-14"></a>DXGI_FORMAT_R16G16B16A16 \_ <sup>SINT-FNS</sup> (14)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32_typelesssuppcssup-15"></a>DXGI_FORMAT_R32G32 \_ <sup>TYPLOSEN PCS</sup> (15)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32_floatsupfnssup-16"></a>DXGI_FORMAT_R32G32 \_ <sup>FLOAT-FNS</sup> (16)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32_uintsupfnssup-17"></a>DXGI_FORMAT_R32G32 \_ <sup>UINT-FNS</sup> (17)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 64 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g32_sintsupfnssup-18"></a>DXGI_FORMAT_R32G32 \_ <sup>SINT-FNS</sup> (18)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 64 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32g8x24_typelesssuppcssup-19"></a>DXGI_FORMAT_R32G8X24 \_ TYPLOSEN<sup>PCS</sup> (19)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_d32_float_s8x24_uintsupfnssup-20"></a>DXGI_FORMAT_D32 FLOAT \_ \_ S8X24 \_ UINT<sup>FNS</sup> (20)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32_float_x8x24_typelesssupfnssup-21"></a>DXGI_FORMAT_R32 \_ FLOAT \_ X8X24 \_ TYPELESS<sup>FNS</sup> (21)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_x32_typeless_g8x24_uintsupfnssup-22"></a>DXGI_FORMAT_X32 \_ TYPLOSEN \_ G8X24-UINT-FNS \_ (22)<sup></sup>
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 64 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r10g10b10a2_typelesssuppcssup-23"></a>DXGI_FORMAT_R10G10B10A2 \_ TYPLOSEN<sup>PCS</sup> (23)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r10g10b10a2_unormsupfnssup-24"></a>DXGI_FORMAT_R10G10B10A2 \_ <sup>UNORM-FNS</sup> (24)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r10g10b10a2_uintsupfnssup-25"></a>DXGI_FORMAT_R10G10B10A2 \_ <sup>UINT-FNS</sup> (25)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r10g10b10_xr_bias_a2_unormsupfnssup-89"></a>DXGI_FORMAT_R10G10B10 \_ XR \_ BIAS \_ A2 \_ UNORM<sup>FNS</sup> (89)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r11g11b10_floatsupfnssup-26"></a>DXGI_FORMAT_R11G11B10 \_ <sup>FLOAT-FNS</sup> (26)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8b8a8_typelesssuppcssup-27"></a>DXGI_FORMAT_R8G8B8A8 \_ TYPLOSE<sup>PCS</sup> (27)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8b8a8_unormsupfnssup-28"></a>DXGI_FORMAT_R8G8B8A8 \_ <sup>UNORM-FNS</sup> (28)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Last | \- |
| Anzeigen Scan-Out | ![Erforderlich](images/letter-r.jpg) |
| Cast Within Bit Layout | \- |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | ![optional](images/letter-o.jpg) |
| Videoprozessorausgabe | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8b8a8_unorm_srgbsupfnssup-29"></a>DXGI_FORMAT_R8G8B8A8 \_ UNORM \_ SRGB<sup>FNS</sup> (29)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Last | \- |
| Anzeigen Scan-Out | ![Erforderlich](images/letter-r.jpg) |
| Cast Within Bit Layout | \- |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | ![optional](images/letter-o.jpg) |
| Videoprozessorausgabe | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8b8a8_uintsupfnssup-30"></a>DXGI_FORMAT_R8G8B8A8 \_ <sup>UINT-FNS</sup> (30)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8b8a8_snormsupfnssup-31"></a>DXGI_FORMAT_R8G8B8A8 \_ <sup>SNORM-FNS</sup> (31)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8b8a8_sintsupfnssup-32"></a>DXGI_FORMAT_R8G8B8A8 \_ <sup>SINT-FNS</sup> (32)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16_typelesssuppcssup-33"></a>DXGI_FORMAT_R16G16 \_ TYPLOSE<sup>PCS</sup> (33)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16_floatsupfnssup-34"></a>DXGI_FORMAT_R16G16 \_ <sup>FLOAT-FNS</sup> (34)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16_unormsupfnssup-35"></a>DXGI_FORMAT_R16G16 \_ <sup>UNORM-FNS</sup> (35)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16_uintsupfnssup-36"></a>DXGI_FORMAT_R16G16 \_ <sup>UINT-FNS</sup> (36)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16_snormsupfnssup-37"></a>DXGI_FORMAT_R16G16 \_ <sup>SNORM-FNS</sup> (37)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16g16_sintsupfnssup-38"></a>DXGI_FORMAT_R16G16 \_ <sup>SINT-FNS</sup> (38)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32_typelesssuppcssup-39"></a>DXGI_FORMAT_R32 \_ TYPLOSE<sup>PCS</sup> (39)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_d32_floatsupfnssup-40"></a>DXGI_FORMAT_D32 \_ <sup>FLOAT-FNS</sup> (40)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32_floatsupfnssup-41"></a>DXGI_FORMAT_R32 \_ <sup>FLOAT-FNS</sup> (41)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![Erforderlich](images/letter-r.jpg) |
| RenderTarget | ![Erforderlich](images/letter-r.jpg) |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32_uintsupfnssup-42"></a>DXGI_FORMAT_R32 \_ <sup>UINT-FNS</sup> (42)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | ![Erforderlich](images/letter-r.jpg) |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r32_sintsupfnssup-43"></a>DXGI_FORMAT_R32 \_ <sup>SINT-FNS</sup> (43)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r24g8_typelesssuppcssup-44"></a>DXGI_FORMAT_R24G8 \_ TYPLOSE<sup>PCS</sup> (44)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_d24_unorm_s8_uintsupfnssup-45"></a>DXGI_FORMAT_D24 \_ UNORM \_ S8 \_ UINT<sup>FNS</sup> (45)
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
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Automatische Mipmap-Generierung | \- |
| RenderTarget | \- |
| Überblendbares RenderTarget | \- |
| Output Merger Logic Op | \- |
| Tiefen-/Schablonenziel | ![Erforderlich](images/letter-r.jpg) |
| Unformatiertes UAV und SRV | \- |
| Strukturiertes UAV und SRV | \- |
| Typisierter UAV | \- |
| Typisierte UAV-Store | \- |
| Vom UAV typisiertes Laden | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
| 4x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r24_unorm_x8_typelesssupfnssup-46"></a>DXGI_FORMAT_R24 \_ UNORM \_ X8 \_ TYPELESS<sup>FNS</sup> (46)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 32 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_x24_typeless_g8_uintsupfnssup-47"></a>DXGI_FORMAT_X24 \_ TYPELESS \_ G8 \_ UINT<sup>FNS</sup> (47)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8_typelesssuppcssup-48"></a>DXGI_FORMAT_R8G8 \_ TYPLOSEN<sup>PCS</sup> (48)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8_unormsupfnssup-49"></a>DXGI_FORMAT_R8G8 \_ <sup>UNORM-FNS</sup> (49)
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
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Automatische Mipmap-Generierung | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8_uintsupfnssup-50"></a>DXGI_FORMAT_R8G8 \_ <sup>UINT-FNS</sup> (50)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8_snormsupfnssup-51"></a>DXGI_FORMAT_R8G8 \_ <sup>SNORM-FNS</sup> (51)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 16 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8_sintsupfnssup-52"></a>DXGI_FORMAT_R8G8 \_ <sup>SINT-FNS</sup> (52)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 16 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16_typelesssuppcssup-53"></a>DXGI_FORMAT_R16 \_ TYPLOSEN<sup>PCS</sup> (53)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16_floatsupfnssup-54"></a>DXGI_FORMAT_R16 \_ <sup>FLOAT-FNS</sup> (54)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_d16_unormsupfnssup-55"></a>DXGI_FORMAT_D16 \_ <sup>UNORM-FNS</sup> (55)
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
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | \- |
| 4x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16_unormsupfnssup-56"></a>DXGI_FORMAT_R16 \_ <sup>UNORM-FNS</sup> (56)
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
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16_uintsupfnssup-57"></a>DXGI_FORMAT_R16 \_ <sup>UINT-FNS</sup> (57)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | ![Erforderlich](images/letter-r.jpg) |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16_snormsupfnssup-58"></a>DXGI_FORMAT_R16 \_ <sup>SNORM-FNS</sup> (58)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r16_sintsupfnssup-59"></a>DXGI_FORMAT_R16 \_ <sup>SINT-FNS</sup> (59)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8_typelesssuppcssup-60"></a>DXGI_FORMAT_R8 \_ TYPLOSEN<sup>PCS</sup> (60)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8_unormsupfnssup-61"></a>DXGI_FORMAT_R8 \_ <sup>UNORM-FNS</sup> (61)
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
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
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
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8_uintsupfnssup-62"></a>DXGI_FORMAT_R8 \_ <sup>UINT-FNS</sup> (62)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 8 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8_snormsupfnssup-63"></a>DXGI_FORMAT_R8 \_ <sup>SNORM-FNS</sup> (63)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 8 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8_sintsupfnssup-64"></a>DXGI_FORMAT_R8 \_ <sup>SINT-FNS</sup> (64)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 8 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_a8_unormsupfnssup-65"></a>DXGI_FORMAT_A8 \_ <sup>UNORM-FNS</sup> (65)
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
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | \- |
| Automatische Mipmap-Generierung | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r9g9b9e5_sharedexpsupfncsup-67"></a>DXGI_FORMAT_R9G9B9E5 \_ SHAREDEXP<sup>FNC</sup> (67)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_r8g8_b8g8_unormsupfncsup-68"></a>DXGI_FORMAT_R8G8 \_ B8G8 \_ UNORM<sup>FNC</sup> (68)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 16 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_g8r8_g8b8_unormsupfncsup-69"></a>DXGI_FORMAT_G8R8 \_ G8B8 \_ UNORM<sup>FNC</sup> (69)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 16 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc1_typelesssuppccsup-70"></a>DXGI_FORMAT_BC1 \_ TYPELESS<sup>PCC</sup> (70)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 4 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc1_unormsupfncsup-71"></a>DXGI_FORMAT_BC1 \_ UNORM<sup>FNC</sup> (71)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 4 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc1_unorm_srgbsupfncsup-72"></a>DXGI_FORMAT_BC1 \_ UNORM \_ SRGB<sup>FNC</sup> (72)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 4 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
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
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc2_typelesssuppccsup-73"></a>DXGI_FORMAT_BC2 \_ TYPELESS<sup>PCC</sup> (73)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 8 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc2_unormsupfncsup-74"></a>DXGI_FORMAT_BC2 \_ <sup>UNORM-FNC</sup> (74)
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
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
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
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc2_unorm_srgbsupfncsup-75"></a>DXGI_FORMAT_BC2 \_ UNORM \_ SRGB<sup>FNC</sup> (75)
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
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
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
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc3_typelesssuppccsup-76"></a>DXGI_FORMAT_BC3 \_ TYPELESS<sup>PCC</sup> (76)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 8 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc3_unormsupfncsup-77"></a>DXGI_FORMAT_BC3 \_ UNORM<sup>FNC</sup> (77)
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
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc3_unorm_srgbsupfncsup-78"></a>DXGI_FORMAT_BC3 \_ UNORM \_ SRGB<sup>FNC</sup> (78)
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
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
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
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc4_typelesssuppccsup-79"></a>DXGI_FORMAT_BC4 \_ <sup>TYPLOSEN PCC</sup> (79)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 4 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc4_unormsupfncsup-80"></a>DXGI_FORMAT_BC4 \_ UNORM<sup>FNC</sup> (80)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 4 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc4_snormsupfncsup-81"></a>DXGI_FORMAT_BC4 \_ SNORM<sup>FNC</sup> (81)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 4 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc5_typelesssuppccsup-82"></a>DXGI_FORMAT_BC5 \_ TYPLOSEN<sup>PCC</sup> (82)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 8 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc5_unormsupfncsup-83"></a>DXGI_FORMAT_BC5 \_ <sup>UNORM-FNC</sup> (83)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 8 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_bc5_snormsupfncsup-84"></a>DXGI_FORMAT_BC5 \_ <sup>SNORM-FNC</sup> (84)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 8 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_b5g6r5_unormsupfnssup-85"></a>DXGI_FORMAT_B5G6R5 \_ <sup>UNORM-FNS</sup> (85)
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
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_b5g5r5a1_unormsupfnssup-86"></a>DXGI_FORMAT_B5G5R5A1 \_ <sup>UNORM-FNS</sup> (86)
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
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_b8g8r8a8_typelesssuppcssup-90"></a>DXGI_FORMAT_B8G8R8A8 \_ TYPLOSEN<sup>PCS</sup> (90)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
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
| Gekachelte Ressource | \- |

## <a name="dxgi_format_b8g8r8a8_unormsupfnssup-87"></a>DXGI_FORMAT_B8G8R8A8 \_ <sup>UNORM-FNS</sup> (87)
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
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| Other Multisample Count RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | ![Erforderlich](images/letter-r.jpg) |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | ![optional](images/letter-o.jpg) |
| Videoprozessorausgabe | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_b8g8r8a8_unorm_srgbsupfnssup-91"></a>DXGI_FORMAT_B8G8R8A8 \_ UNORM \_ SRGB<sup>FNS</sup> (91)
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
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Last | \- |
| Anzeigen Scan-Out | ![Erforderlich](images/letter-r.jpg) |
| Cast Within Bit Layout | \- |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | ![optional](images/letter-o.jpg) |
| Videoprozessorausgabe | ![Erforderlich](images/letter-r.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_b8g8r8x8_typelesssuppcssup-92"></a>DXGI_FORMAT_B8G8R8X8 \_ TYPLOSEN<sup>PCS</sup> (92)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | \- |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | \- |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_b8g8r8x8_unormsupfnssup-88"></a>DXGI_FORMAT_B8G8R8X8 \_ <sup>UNORM-FNS</sup> (88)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | ![optional](images/letter-o.jpg) |
| Videoprozessorausgabe | ![optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_b8g8r8x8_unorm_srgbsupfnssup-93"></a>DXGI_FORMAT_B8G8R8X8 \_ UNORM \_ SRGB<sup>FNS</sup> (93)
| Ziel | Support |
| - | - |
| Bits pro Element (BPE) | 32 |
| Formatunterstützung | ![Erforderlich](images/letter-r.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabe-Assemblers | \- |
| Indexpuffer des Eingabe-Assemblers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | ![Erforderlich](images/letter-r.jpg) |
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| 8x Multisample RenderTarget | ![optional](images/letter-o.jpg) |
| Andere Multisampleanzahl RT | ![optional](images/letter-o.jpg) |
| Multisample-Auflösung | ![Erforderlich](images/letter-r.jpg) |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | \- |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | ![Erforderlich](images/letter-r.jpg) |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_ayuvsupvsup-100"></a>DXGI_FORMAT_AYUV<sup>V</sup> (100)
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
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
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
| Gemeinsam genutzte Ressource | \- |
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
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
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
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_y416supvsup-102"></a>DXGI_FORMAT_Y416<sup>V</sup> (102)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 64 |
| Formatunterstützung | ![optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung des Videodecoders | ![optional](images/letter-o.jpg) |
| Videoprozessoreingabe | ![optional](images/letter-o.jpg) |
| Videoprozessorausgabe | ![optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_nv12supvsup-103"></a>DXGI_FORMAT_NV12<sup>V</sup> (103)
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
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
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
| Gemeinsam genutzte Ressource | \- |
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
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
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
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_p016supvsup-105"></a>DXGI_FORMAT_P016<sup>V</sup> (105)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 16 |
| Formatunterstützung | ![optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
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
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_420_opaquesupvsup-106"></a>DXGI_FORMAT_420 \_ OPAQUE<sup>V</sup> (106)
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
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU-Sperrbar | \- |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Other Multisample Count RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | ![Erforderlich](images/letter-r.jpg) |
| Videoprozessoreingabe | ![Erforderlich](images/letter-r.jpg) |
| Videoprozessorausgabe | ![optional](images/letter-o.jpg) |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_yuy2supvsup-107"></a>DXGI_FORMAT_YUY2<sup>V</sup> (107)
| Ziel | Support |
| - | - |
| Bits Per-Element (BPE) | 16 |
| Formatunterstützung | ![optional](images/letter-o.jpg) |
| Buffer | \- |
| Vertexpuffer des Eingabeassemblierers | \- |
| Indexpuffer des Eingabeassemblierers | \- |
| Streamausgabepuffer | \- |
| Texture1D | \- |
| Texture2D | ![Erforderlich](images/letter-r.jpg) |
| Texture3D | \- |
| TextureCube | \- |
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
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
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_y210supvsup-108"></a>DXGI_FORMAT_Y210<sup>V</sup> (108)
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
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
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
| Gemeinsam genutzte Ressource | \- |
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
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
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
| Gemeinsam genutzte Ressource | \- |
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
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
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
| Gemeinsam genutzte Ressource | \- |
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
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU sperrbar | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Ladevorgang | \- |
| Anzeigen Scan-Out | \- |
| Umwandlung innerhalb des Bitlayouts | \- |
| Unterstützung des Videodecoders | \- |
| Videoprozessoreingabe | ![Erforderlich](images/letter-r.jpg) |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
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
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
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
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | ![Erforderlich](images/letter-r.jpg) |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
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
| Shaderbeispiel (nur Punktbeispiel) | \- |
| Shaderbeispiel (beliebiger Filter) | \- |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
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
| UAV Typed Load | \- |
| UAV Atomic Add | \- |
| UAV Atomic Bitwise Ops | \- |
| UAV Atomic Cmp&Store/Cmp&Exch | \- |
| UAV Atomic Exchange | \- |
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
| CPU Lockable | ![Erforderlich](images/letter-r.jpg) |
| 4x Multisample RenderTarget | \- |
| 8x Multisample RenderTarget | \- |
| Andere Multisampleanzahl RT | \- |
| Multisample-Auflösung | \- |
| Multisample-Last | \- |
| Anzeigen Scan-Out | \- |
| Cast Within Bit Layout | \- |
| Unterstützung für Videodecoder | \- |
| Videoprozessoreingabe | ![Erforderlich](images/letter-r.jpg) |
| Videoprozessorausgabe | \- |
| Gemeinsam genutzte Ressource | \- |
| Gekachelte Ressource | \- |

## <a name="dxgi_format_b4g4r4a4_unormsupfnssup-115"></a>DXGI_FORMAT_B4G4R4A4 \_ <sup>UNORM-FNS</sup> (115)
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
| TextureCube | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (nur Punktbeispiel) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel (beliebiger Filter) | ![Erforderlich](images/letter-r.jpg) |
| Shaderbeispiel \_ c (Vergleichsfilter) | \- |
| Shaderbeispiel (Mono-1-Bit-Filter) | \- |
| Shader gather4 | \- |
| Shader gather4 \_ c | \- |
| Mipmap | ![Erforderlich](images/letter-r.jpg) |
| Automatische Mipmap-Generierung | ![optional](images/letter-o.jpg) |
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
| UAV Atomic Signed Min oder Max | \- |
| UAV Atomic Unsigned Min oder Max | \- |
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
| Gekachelte Ressource | \- |

## <a name="format-notes"></a>Formathinweise

Der Zweck des Formats kann sich von einer Hardwarefeatureebene zur nächsten ändern.

<dl> <dt>

<sup>L:</sup> typloses Format
</dt> <dt>

<sup>PCS:</sup> teilweise typisiertes, umwandlungsfähiges und einfaches Layout
</dt> <dt>

 <sup>FCS:</sup> vollständig typisiertes, umwandlungsfähiges und einfaches Layout
</dt> <dt>

<sup>FNS:</sup> vollständig typisiertes, nicht umwandlungsfähiges und einfaches Layout
</dt> <dt>

<sup>PCC:</sup> teilweise typisiertes, umwandlungsfähiges und komplexes Layout
</dt> <dt>

 <sup>FCC:</sup> vollständig typisiertes, umwandlungsfähiges und komplexes Layout
</dt> <dt>

<sup>FNC:</sup> vollständig typisiertes, nicht umwandlungsfähiges und komplexes Layout
</dt> <dt>

<sup>V</sup> : Videoformat
</dt> </dl>

## <a name="related-topics"></a>Zugehörige Themen

[D3D12-Hardwarefeatureebenen](../direct3d12/hardware-feature-levels.md)

[Implementieren von Schattenpuffern für Direct3D-Featureebene 9](/previous-versions/windows/apps/jj262110(v=win.10))

[Zuordnen von Legacyformaten](../direct3d10/d3d10-graphics-programming-guide-resources-legacy-formats.md)

[Programmierhandbuch für DXGI](dx-graphics-dxgi-overviews.md)
