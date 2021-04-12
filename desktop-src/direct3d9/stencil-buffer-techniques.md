---
description: Anwendungen verwenden den Schablonen Puffer, um Pixel in einem Bild zu maskieren. Die Maske steuert, ob das Pixel gezeichnet wird. Einige der gängigeren Effekte sind unten dargestellt.
ms.assetid: 984f0a98-4a74-44c3-a9d0-f5d3f12f7e4e
title: Techniken für Schablonen Puffer (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2dcc05475a3ddfc13e456faf60ec2d11e271a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392882"
---
# <a name="stencil-buffer-techniques-direct3d-9"></a>Techniken für Schablonen Puffer (Direct3D 9)

Anwendungen verwenden den Schablonen Puffer, um Pixel in einem Bild zu maskieren. Die Maske steuert, ob das Pixel gezeichnet wird. Einige der gängigeren Effekte sind unten dargestellt.

-   [Zusammensetzung](compositing.md)
-   [Wird abgebrochen](decaling.md)
-   [Wird aufgelöst, ausgeblendet und durchstreifen](dissolves--fades--and-swipes.md)
-   [Kontur und Silhouetten](outlines-and-silhouettes.md)
-   [Zweiseitige Schablone](two-sided-stencil.md)

Der Schablonen Puffer aktiviert oder deaktiviert das Zeichnen auf der Renderingzieloberfläche auf Pixel Basis. Auf der grundlegendsten Ebene ermöglicht es Anwendungen, Abschnitte des gerenderten Bilds so zu maskieren, dass Sie nicht angezeigt werden. Anwendungen verwenden häufig Schablonen Puffer für besondere Effekte, wie z. b. auflösen, herabsetzen und gliedern.

Schablonen Puffer Informationen werden in die z-Puffer Daten eingebettet. Die Anwendung kann die [**IDirect3D9:: CheckDeviceFormat**](/windows/desktop/api) -Methode verwenden, um die Unterstützung von Hardware Schablonen zu prüfen, wie im folgenden Codebeispiel gezeigt.


```
// Reject devices that cannot perform 8-bit stencil buffering. 
// The following example assumes that pCaps is a valid pointer 
// to an initialized D3DCAPS9 structure. 

if( FAILED( m_pD3D->CheckDeviceFormat( pCaps->AdapterOrdinal,
                                       pCaps->DeviceType,  
                                       Format,  
                                       D3DUSAGE_DEPTHSTENCIL, 
                                       D3DRTYPE_SURFACE,
                                       D3DFMT_D24S8 ) ) )
return E_FAIL;
```



[**IDirect3D9:: CheckDeviceFormat**](/windows/desktop/api) ermöglicht Ihnen die Auswahl eines zu erstellenden Geräts basierend auf den Funktionen dieses Geräts. In diesem Fall werden Geräte, die 8-Bit-Schablonen Puffer nicht unterstützen, abgelehnt. Beachten Sie, dass dies nur eine mögliche Verwendung für **IDirect3D9:: CheckDeviceFormat**; ist. Weitere Informationen finden Sie [unter Bestimmen des Hardware Supports (Direct3D 9)](determining-hardware-support.md).

## <a name="how-the-stencil-buffer-works"></a>Funktionsweise des Schablonen Puffers

Direct3D führt einen Test für den Inhalt des Schablonen Puffers auf Pixel Basis aus. Für jedes Pixel in der Ziel Oberfläche wird ein Test mit dem entsprechenden Wert im Schablonen Puffer, einem Schablonen Verweis Wert und einem Schablone-Maskenwert durchführt. Wenn der Test ausgeführt wird, führt Direct3D eine Aktion aus. Der Test wird mithilfe der folgenden Schritte ausgeführt.

1.  Führt eine bitweise AND-Operation des Schablonen Verweis Werts mit der Schablonen Maske aus.
2.  Führt eine bitweise AND-Operation des Schablonen Puffer Werts für das aktuelle Pixel mit der Schablonen Maske aus.
3.  Vergleichen Sie das Ergebnis von Schritt 1 mit dem Ergebnis von Schritt 2 mit der Vergleichsfunktion.

Diese Schritte sind im folgenden Codebeispiel dargestellt.


```
(StencilRef & StencilMask) CompFunc (StencilBufferValue & StencilMask)
```




```
StencilBufferValue
```



der Inhalt des Schablonen Puffers für das aktuelle Pixel. In diesem Codebeispiel wird das kaufmännische und-Zeichen (&) verwendet, um die bitweise AND-Operation darzustellen.


```
StencilMask
```



stellt den Wert der Schablonen Maske dar.


```
StencilRef
```



stellt den Schablonen Verweis Wert dar.


```
CompFunc
```



ist die Vergleichsfunktion.

Das aktuelle Pixel wird auf die Ziel Oberfläche geschrieben, wenn der Schablonen Test verstrichen ist, und wird andernfalls ignoriert. Das Standard Vergleichs Verhalten besteht darin, das Pixel zu schreiben, unabhängig davon, wie sich jeder bitweise Vorgang ausstellt (D3DCMP \_ Always). Sie können dieses Verhalten ändern, indem Sie den Wert des D3DRS \_ stencilfunc-renderzustands ändern und einen Member des [**D3DCMPFUNC**](./d3dcmpfunc.md) -enumerierten Typs übergeben, um die gewünschte Vergleichsfunktion zu identifizieren.

Die Anwendung kann den Vorgang des Schablonen Puffers anpassen. Sie kann die Vergleichsfunktion, die Schablonen Maske und den Schablonen Verweis Wert festlegen. Außerdem kann Sie die Aktion steuern, die Direct3D durchführt, wenn der Schablonen Test erfolgreich verläuft oder fehlschlägt. Weitere Informationen finden Sie unter [Status des Schablone-Puffers (Direct3D 9)](stencil-buffer-state.md).

## <a name="examples"></a>Beispiele

Die folgenden Codebeispiele veranschaulichen das Einrichten des Schablonen Puffers.


```
// Enable stencil testing
pDevice->SetRenderState(D3DRS_STENCILENABLE, TRUE);

// Specify the stencil comparison function
pDevice->SetRenderState(D3DRS_STENCILFUNC, D3DCMP_EQUAL);

// Set the comparison reference value
pDevice->SetRenderState(D3DRS_STENCILREF, 0);

//  Specify a stencil mask 
pDevice->SetRenderState(D3DRS_STENCILMASK, 0);
```



Der Schablonen Verweis Wert ist standardmäßig 0 (null). Jeder ganzzahlige Wert ist gültig. Direct3D führt ein bitweises and des Schablonen Verweis Werts und einen Schablonen Maskenwert vor dem Schablonen Test aus.

Abhängig vom Schablone-Vergleich können Sie steuern, welche Pixel Informationen geschrieben werden.


```
// A write mask controls what is written
pDevice->SetRenderState(D3DRS_STENCILWRITEMASK, D3DSTENCILOP_KEEP);
// Specify when to write stencil data
pDevice->SetRenderState(D3DRS_STENCILFAIL, D3DSTENCILOP_KEEP);
```



Sie können eine eigene Formel für den Wert schreiben, den Sie in den Schablonen Puffer schreiben möchten, wie im folgenden Beispiel gezeigt.


```
NewStencilBufferValue = (StencilBufferValue & ~StencilWriteMask) | 
                        (StencilWriteMask & StencilOp(StencilBufferValue))
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixel Pipeline](pixel-pipeline.md)
</dt> </dl>

 

 
