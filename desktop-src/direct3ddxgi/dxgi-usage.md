---
description: Flags für Optionen für die Oberflächen- und Ressourcenerstellung.
ms.assetid: b5026566-89b5-458e-b36d-a55e5f8c10c1
title: DXGI_USAGE (DXGI.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d7bc0773794c6c2243d8a3171cbd6ffdafbe1cdd558e1198c2c8cc0b1a3440d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117909931"
---
# <a name="dxgi_usage"></a>\_DXGI-NUTZUNG

Flags für Optionen für die Oberflächen- und Ressourcenerstellung.



| Konstante/Wert                                                                                                                                                                                                                                                                                  | Beschreibung                                                                                                                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_USAGE_BACK_BUFFER"></span><span id="dxgi_usage_back_buffer"></span><dl> <dt>**DXGI \_ USAGE \_ BACK \_ BUFFER**</dt> <dt>1L << (2 + 4)</dt> </dl>                             | Die Oberfläche oder Ressource wird als Hintergrundpuffer verwendet. Sie müssen **DXGI USAGE \_ BACK \_ \_ BUFFER** nicht übergeben, wenn Sie eine Swapkette erstellen. Sie können jedoch ermitteln, ob eine Ressource zu einer Auslagerungskette gehört, wenn Sie [**IDXGIResource::GetUsage**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) aufrufen und **DXGI \_ USAGE BACK \_ BUFFER \_ erhalten.**<br/> |
| <span id="DXGI_USAGE_DISCARD_ON_PRESENT"></span><span id="dxgi_usage_discard_on_present"></span><dl> <dt>**DXGI \_ USAGE \_ DISCARD \_ ON \_ PRESENT**</dt> <dt>1L << (5 + 4)</dt> </dl>       | Dieses Flag ist nur für die interne Verwendung.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="DXGI_USAGE_READ_ONLY"></span><span id="dxgi_usage_read_only"></span><dl> <dt>**DXGI \_ NUTZUNG \_ \_ SCHREIBGESCHÜTZT**</dt> <dt>1L << (4 + 4)</dt> </dl>                                   | Verwenden Sie die Oberfläche oder Ressource nur zum Lesen.<br/>                                                                                                                                                                                                                                                                        |
| <span id="DXGI_USAGE_RENDER_TARGET_OUTPUT"></span><span id="dxgi_usage_render_target_output"></span><dl> <dt>**DXGI \_ \_ \_ \_ VERWENDUNGSRENDERINGZIELAUSGABE**</dt> <dt>1L << (1 + 4)</dt> </dl> | Verwenden Sie die Oberfläche oder Ressource als Ausgaberenderziel.<br/>                                                                                                                                                                                                                                                              |
| <span id="DXGI_USAGE_SHADER_INPUT"></span><span id="dxgi_usage_shader_input"></span><dl> <dt>**DXGI \_ \_VERWENDUNGS-SHADEREINGABE \_**</dt> <dt>1L << (0 + 4)</dt> </dl>                          | Verwenden Sie die Oberfläche oder Ressource als Eingabe für einen Shader.<br/>                                                                                                                                                                                                                                                                 |
| <span id="DXGI_USAGE_SHARED"></span><span id="dxgi_usage_shared"></span><dl> <dt>**DXGI \_ USAGE \_ SHARED**</dt> <dt>1L << (3 + 4)</dt> </dl>                                             | Freigeben der Oberfläche oder Ressource.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="DXGI_USAGE_UNORDERED_ACCESS"></span><span id="dxgi_usage_unordered_access"></span><dl> <dt>**DXGI \_ VERWENDUNG \_ UNGEORDNETER \_ ZUGRIFF**</dt> <dt>1L << (6 + 4)</dt> </dl>              | Verwenden Sie die Oberfläche oder Ressource für ungeordneten Zugriff.<br/>                                                                                                                                                                                                                                                                    |



## <a name="remarks"></a>Hinweise

Jedes Flag wird als ganze Zahl ohne Vorzeichen definiert.

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

Diese Flagoptionen werden in einem Aufruf von [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory-createswapchain), [**IDXGIFactory2::CreateSwapChainForHwnd,**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd) [**IDXGIFactory2::CreateSwapChainForCoreWindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)oder [**IDXGIFactory2::CreateSwapChainForComposition-Methode**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) verwendet, um die Oberflächennutzungs- und CPU-Zugriffsoptionen für den Rückpuffer einer Austauschkette zu beschreiben. Sie können die **WERTE DXGI \_ USAGE \_ SHARED,** **DXGI \_ USAGE DISCARD \_ ON \_ \_ PRESENT** und **DXGI USAGE READ \_ \_ \_ ONLY** nicht als Eingabe verwenden, um eine Swapkette zu erstellen. DXGI kann jedoch **DXGI \_ USAGE DISCARD \_ ON \_ \_ PRESENT** und **DXGI USAGE READ \_ \_ \_ ONLY** für einige der Hintergrundpuffer der Swapkette im Auftrag der Anwendung festlegen. Sie können die [**IDXGIResource::GetUsage-Methode**](/windows/desktop/api/DXGI/nf-dxgi-idxgiresource-getusage) aufrufen, um die Verwendung dieser Backpuffer abzurufen. Swap chain es unterstützt nur den **DXGI \_ CPU ACCESS \_ \_ NONE-Wert** im **DXGI CPU ACCESS \_ \_ \_ FIELD-Teil** von **DXGI \_ USAGE**.

Diese Flagoptionen werden auch von der [**IDXGIDevice::CreateSurface-Methode**](/windows/desktop/api/DXGI/nf-dxgi-idxgidevice-createsurface) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DXGI.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DXGI-Konstanten](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




