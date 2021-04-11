---
description: 'Sie können mithilfe der IDirect3DSurface9:: lockrect-Methode direkt auf den Speicher der-Oberfläche zugreifen.'
ms.assetid: ad669c22-6163-4fbb-bad0-160ced5bc558
title: Direktes Zugreifen auf den Surface-Speicher (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ed9a65265671e6509172eccd9a1b66ea91507f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342219"
---
# <a name="accessing-surface-memory-directly-direct3d-9"></a>Direktes Zugreifen auf den Surface-Speicher (Direct3D 9)

Sie können mithilfe der [**IDirect3DSurface9:: lockrect**](/windows/desktop/api) -Methode direkt auf den Speicher der-Oberfläche zugreifen. Wenn Sie diese Methode aufrufen, ist der prect-Parameter ein Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur, die das Rechteck auf der-Oberfläche beschreibt, auf das direkt zugegriffen werden soll. Um anzufordern, dass die gesamte Oberfläche gesperrt ist, legen Sie vorab auf **null** fest. Außerdem können Sie eine **Rect** angeben, die nur einen Teil der Oberfläche abdeckt. Wenn keine zwei Rechtecke überlappend sind, können zwei Threads oder Prozesse gleichzeitig mehrere Rechtecke in einer Oberfläche sperren. Beachten Sie, dass ein Multisampling-Hintergrund Puffer nicht gesperrt werden kann.

Die [**IDirect3DSurface9:: lockrect**](/windows/desktop/api) -Methode füllt eine [**D3DLOCKED \_ Rect**](d3dlocked-rect.md) -Struktur mit allen Informationen aus, um ordnungsgemäß auf den Oberflächen Speicher zuzugreifen. Die Struktur enthält Informationen über die Tonhöhe und weist einen Zeiger auf die gesperrten Bits auf. Wenn Sie den Zugriff auf den Surface-Speicher beenden, können Sie die [**IDirect3DSurface9:: unlockrect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) -Methode aufrufen, um Sie zu entsperren.

Wenn eine Oberfläche gesperrt ist, können Sie den Inhalt direkt bearbeiten. In der folgenden Liste werden einige Tipps zur Vermeidung allgemeiner Probleme beim direkten Rendern von Oberflächen Arbeitsspeicher beschrieben.

-   Gehen Sie niemals von einer Konstanten Anzeige Fläche aus. Überprüfen Sie immer die von der [**IDirect3DSurface9:: lockrect**](/windows/desktop/api) -Methode zurückgegebenen Informationen über die Tonhöhe. Diese Tonhöhe kann verschiedene Ursachen haben, z. b. den Speicherort des Oberflächen Speichers, den Anzeige Kartentyp oder sogar die Version des Direct3D-Treibers. Weitere Informationen finden Sie unter [Width vs. Pitch (Direct3D 9)](width-vs--pitch.md).
-   Stellen Sie sicher, dass Sie auf entsperrtes Oberflächen kopieren Direct3D Copy-Methoden schlagen fehl, wenn Sie auf einer gesperrten Oberfläche aufgerufen werden.
-   Beschränken Sie die Aktivität Ihrer Anwendung, während eine Oberfläche gesperrt ist.
-   Kopieren Sie Daten immer ausgerichtet, um Arbeitsspeicher anzuzeigen. Windows 98 verwendet einen Seiten Fehlerhandler (Vflatd. 386), um einen virtuellen flatframe-Puffer für Anzeige Karten mit Bank gespeichertem Arbeitsspeicher zu implementieren. Mit dem-Handler können diese Geräte Anzeigegeräte einen linearen Frame Puffer für Direct3D präsentieren. Das Kopieren von Daten, die nicht ausgerichtet sind, um Arbeitsspeicher anzuzeigen, kann dazu führen, dass das System Vorgänge anhält, wenn sich die Kopie
-   Eine Oberfläche ist möglicherweise nicht gesperrt, wenn Sie zu einer Ressource gehört, die dem D3DPOOL- \_ Standard Speicherpool zugewiesen ist, es sei denn, es handelt sich um eine dynamische Textur oder eine Oberfläche, die mithilfe von [**IDirect3DDevice9::**](/windows/desktop/api)Erstellungs Token erstellt wurde. Hintergrund Puffer Oberflächen, auf die mithilfe der [**IDirect3DDevice9:: GetBackBuffer**](/windows/desktop/api) -Methode und der [**IDirect3DSwapChain9:: GetBackBuffer**](/windows/desktop/api) -Methode zugegriffen werden kann, können nur gesperrt werden, wenn die SwapChain mit dem Flags-Member von [**D3DPRESENT- \_ Parametern**](d3dpresent-parameters.md) erstellt wurde, um D3DPRESENTFLAG \_ Lockable \_ BackBuffer einzuschließen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Oberflächen](direct3d-surfaces.md)
</dt> </dl>

 

 
