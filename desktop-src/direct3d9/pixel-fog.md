---
description: Pixel Nebel erhält seinen Namen aus der Tatsache, dass Sie im Gerätetreiber pro Pixel berechnet wird.
ms.assetid: 6fcfb9fa-cacc-4dbc-bfc6-85d533dbfbf8
title: Pixel Nebel (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f62a597820fa009207d8dda7836d161cdf34c88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103859975"
---
# <a name="pixel-fog-direct3d-9"></a>Pixel Nebel (Direct3D 9)

Pixel Nebel erhält seinen Namen aus der Tatsache, dass Sie im Gerätetreiber pro Pixel berechnet wird. Dies unterscheidet sich von dem Scheitelpunkt Nebel, der durch die Pipeline während der Transformation und der Beleuchtungsberechnungen berechnet wird. Pixel Nebel wird manchmal als Tabellen Nebel bezeichnet, da einige Treiber eine vorab berechnete Nachschlage Tabelle verwenden, um den Nebel Faktor zu ermitteln. dabei wird die Tiefe jedes Pixels verwendet, das in Mischungs Berechnungen angewendet werden soll. Sie kann mithilfe jeder von Membern des [**D3DFOGMODE**](./d3dfogmode.md) -Enumerationstyps identifizierten Nebel Formel angewendet werden. Die Implementierungen dieser Formeln sind Treiber spezifisch. Wenn ein Treiber eine komplexe Nebel Formel nicht unterstützt, sollte er in eine weniger komplexe Formel herabgestuft werden.

## <a name="eye-relative-vs-z-based-depth"></a>Eye-Relative im Vergleich zu Z-basierter Tiefe

Um Nebel bezogene Grafik Artefakte zu verringern, die durch eine ungleichmäßige Verteilung von z-Werten in einem tiefen Puffer verursacht wurden, verwenden die meisten Hardware Geräte die Augen relative Tiefe anstelle von z-basierten tiefen Werten für Pixel Nebel. Die Augen relative Tiefe ist im Grunde das w-Element aus einem homogenen Koordinaten Satz. Microsoft Direct3D nimmt die gegenseitige Verwendung des Rhw-Elements aus einem Geräteraum-Koordinaten Satz an, um true w zu reproduzieren. Wenn ein Gerät Eye-relative Nebel unterstützt, wird das **D3DPRASTERCAPS \_ wfog** -Flag im RasterCaps-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur festgelegt, wenn Sie die [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) -Methode aufrufen. Mit Ausnahme des verweisrasterizers verwenden Software Geräte immer z, um Pixel Nebeleffekte zu berechnen.

Wenn Eye-relativer Nebel unterstützt wird, verwendet das System automatisch die Augen relative Tiefe anstelle der z-basierten Tiefe, wenn die angegebene Projektions Matrix z-Werte im Raum der Welt erzeugt, die w-Values im Geräteraum entsprechen. Sie legen die Projektions Matrix fest, indem Sie die [**IDirect3DDevice9:: setTransform**](/windows/desktop/api) -Methode aufrufen, indem Sie den D3DTS \_ -Projektions Wert verwenden und eine [**D3DMATRIX**](d3dmatrix.md) -Struktur übergeben, die die gewünschte Matrix darstellt. Wenn die Projektions Matrix mit dieser Anforderung nicht kompatibel ist, werden die Nebeleffekte nicht ordnungsgemäß angewendet. Ausführliche Informationen zum Erstellen einer kompatiblen Matrix finden Sie unter [Projektions Transformation (Direct3D 9)](projection-transform.md).

Direct3D verwendet die aktuell festgelegte Projektions Matrix in den w-basierten tiefen Berechnungen. Daher muss eine Anwendung eine konforme Projektions Matrix festlegen, um die gewünschten w-basierten Funktionen zu erhalten, auch wenn Sie die Direct3D-Transformations Pipeline nicht verwendet.

Direct3D überprüft die vierte Spalte der Projektions Matrix. Wenn die Koeffizienten \[ 0, 0, 0, 1 sind \] (bei einer affinen Projektion), verwendet das System die z-basierten tiefen Werte für den Nebel. In diesem Fall müssen Sie auch die Start-und endabstände für lineare Nebeleffekte im Gerätebereich angeben, die von 0,0 am nächsten Punkt bis zum Benutzer und 1,0 am äußersten Punkt liegen.

## <a name="using-pixel-fog"></a>Verwenden von Pixel Nebel

Verwenden Sie die folgenden Schritte, um Pixel Nebel in Ihrer Anwendung zu aktivieren.

1.  Aktivieren Sie die Schnebel Mischung, indem Sie den D3DRS \_ fogenable-Rendering-Zustand auf **true** festlegen.
2.  Legen Sie die gewünschte Nebelfarbe im D3DRS \_ fogcolor-Rendering-Zustand fest.
3.  Wählen Sie die zu verwendende Nebel Formel aus, indem Sie den \_ renderzustand D3DRS fogtablemode auf den entsprechenden Member des [**D3DFOGMODE**](./d3dfogmode.md) -enumerierten Typs festlegen.
4.  Legen Sie für den ausgewählten Nebelmodus in den zugeordneten renderzuständen die gewünschten Nebel Parameter fest. Dies umfasst die Start-und endabstände für linearen Nebel und die Nebeldichte des exponentiellen Nebel Modus.

Im folgenden Beispiel wird gezeigt, wie diese Schritte im Code aussehen können.


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupPixelFog(DWORD Color, DWORD Mode)
{
    float Start   = 0.5f;    // For linear mode
    float End     = 0.8f;
    float Density = 0.66f;   // For exponential modes
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if( Mode == D3DFOG_LINEAR )
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }
```



Einige Nebel Parameter sind als Gleit Komma Werte erforderlich, auch wenn die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode nur DWORD-Werte im zweiten Parameter akzeptiert. Im vorangehenden Beispiel werden die Gleit Komma Werte für **IDirect3DDevice9:: seetrenderstate** ohne Daten Übersetzung bereitstellt, indem die Adressen der Gleit Komma Variablen als DWORD-Zeiger umgewandelt und dann dereferenzierend durch umgewandelt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Nebel Typen](fog-types.md)
</dt> </dl>

 

 
