---
description: Flags für Optionen zur Oberfläche und Ressourcen Erstellung.
ms.assetid: b5026566-89b5-458e-b36d-a55e5f8c10c1
title: DXGI_USAGE (dxgi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e55e99d86201c76fbe2ec229b13b5831d767ff34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353712"
---
# <a name="dxgi_usage"></a>DXGI- \_ Verwendung

Flags für Optionen zur Oberfläche und Ressourcen Erstellung.



| Konstante/Wert                                                                                                                                                                                                                                                                                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_USAGE_BACK_BUFFER"></span><span id="dxgi_usage_back_buffer"></span><dl> <dt>**DXGI \_ Verwendungs \_ Hintergrund \_ Puffer**</dt> <dt>1L <<  (2 + 4)</dt> </dl>                             | Die-Oberfläche oder-Ressource wird als Hintergrund Puffer verwendet. Sie müssen den **DXGI- \_ Verwendungs \_ Hintergrund \_ Puffer** nicht übergeben, wenn Sie eine SwapChain erstellen. Sie können jedoch ermitteln, ob eine Ressource zu einer Swapkette gehört, wenn Sie [**idxgiresource:: getusage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) aufrufen und den **DXGI- \_ Verwendungs-Back- \_ \_ Puffer** abrufen.<br/> |
| <span id="DXGI_USAGE_DISCARD_ON_PRESENT"></span><span id="dxgi_usage_discard_on_present"></span><dl> <dt>**DXGI \_ Verwendungs \_ verwerfen \_ bei der \_ aktuellen**</dt> <dt>1L- <<  (5 + 4)</dt> </dl>       | Dieses Flag ist nur für die interne Verwendung vorgesehen.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="DXGI_USAGE_READ_ONLY"></span><span id="dxgi_usage_read_only"></span><dl> <dt>**DXGI \_ Verwendung \_ \_**</dt> Schreib geschützter <dt>1L- <<  (4 + 4)</dt> </dl>                                   | Verwenden Sie die-Oberfläche oder-Ressource nur zum Lesen.<br/>                                                                                                                                                                                                                                                                        |
| <span id="DXGI_USAGE_RENDER_TARGET_OUTPUT"></span><span id="dxgi_usage_render_target_output"></span><dl> <dt>**DXGI \_ \_Ausgabe- \_ Renderziel \_ Ausgabe**</dt> <dt>1L <<  (1 + 4)</dt> </dl> | Verwenden Sie die-Oberfläche oder-Ressource als Ausgabe Renderziel.<br/>                                                                                                                                                                                                                                                              |
| <span id="DXGI_USAGE_SHADER_INPUT"></span><span id="dxgi_usage_shader_input"></span><dl> <dt>**DXGI \_ Usage- \_ \_ Shadereingabe**</dt> <dt>1L <<  (0 + 4)</dt> </dl>                          | Verwenden Sie die-Oberfläche oder-Ressource als Eingabe für einen Shader.<br/>                                                                                                                                                                                                                                                                 |
| <span id="DXGI_USAGE_SHARED"></span><span id="dxgi_usage_shared"></span><dl> <dt>**DXGI \_ Verwendungs frei \_ gegebene**</dt> <dt>1L- <<  (3 + 4)</dt> </dl>                                             | Freigeben der-Oberfläche oder-Ressource.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="DXGI_USAGE_UNORDERED_ACCESS"></span><span id="dxgi_usage_unordered_access"></span><dl> <dt>**DXGI \_ \_Ungeordneter \_ Zugriff**</dt> in der Verwendung von <dt>1L <<  (6 + 4)</dt> </dl>              | Verwenden Sie die-Oberfläche oder-Ressource für den ungeordneten Zugriff.<br/>                                                                                                                                                                                                                                                                    |



## <a name="remarks"></a>Bemerkungen

Jedes Flag wird als Ganzzahl ohne Vorzeichen definiert.

``` syntax
#define DXGI_CPU_ACCESS_NONE    ( 0 )
#define DXGI_CPU_ACCESS_DYNAMIC    ( 1 )
#define DXGI_CPU_ACCESS_READ_WRITE    ( 2 )
#define DXGI_CPU_ACCESS_SCRATCH    ( 3 )
#define DXGI_CPU_ACCESS_FIELD        15
#define DXGI_USAGE_SHADER_INPUT             ( 1L << (0 + 4) )
#define DXGI_USAGE_RENDER_TARGET_OUTPUT     ( 1L << (1 + 4) )
#define DXGI_USAGE_BACK_BUFFER              ( 1L << (2 + 4) )
#define DXGI_USAGE_SHARED                   ( 1L << (3 + 4) )
#define DXGI_USAGE_READ_ONLY                ( 1L << (4 + 4) )
#define DXGI_USAGE_DISCARD_ON_PRESENT       ( 1L << (5 + 4) )
#define DXGI_USAGE_UNORDERED_ACCESS         ( 1L << (6 + 4) )
typedef UINT DXGI_USAGE;
```

Diese Flagoptionen werden bei einem aufzurufenden [**idxgifactory-Befehl verwendet: die Methoden "anateswapchain**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain)", " [**IDXGIFactory2:: | ateswapchadetailhwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)", " [**IDXGIFactory2::**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)" und " [**IDXGIFactory2:: foateswapchadetailcomposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) ", um die Optionen für die Oberflächen Verwendung und den CPU-Zugriff für den Hintergrund Puffer einer Swapkette zu beschreiben. Es ist nicht möglich, die **\_ \_ gemeinsame Verwendung der DXGI-Verwendung**, die **DXGI- \_ Verwendung \_ verwerfen \_ \_** und die **DXGI- \_ Verwendung \_ \_** als Eingabe für die Erstellung einer SwapChain zu verwenden. DXGI kann jedoch die **DXGI- \_ Verwendungs \_ Verwerfungs \_ \_** -und **DXGI \_ - \_ Verwendung \_** für einige der Hintergrund Puffer der Swapkette im Auftrag der Anwendung festlegen. Sie können die [**idxgiresource:: getusage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) -Methode aufrufen, um die Verwendung dieser Hintergrund Puffer abzurufen. Die SwapChain unterstützt nur den **DXGI- \_ CPU- \_ Zugriff \_ None** -Wert im **Feld DXGI- \_ CPU- \_ Zugriff \_** auf die **DXGI- \_ Verwendung**.

Diese Flagoptionen werden auch von der [**idxgidevice:: kreatesurface**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface) -Methode verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DXGI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DXGI-Konstanten](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




