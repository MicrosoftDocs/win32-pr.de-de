---
title: Parameter für die Kachel Ressourcen Erstellung
description: Es gibt einige Einschränkungen für den Typ der Direct3D-Ressourcen, die Sie mit dem D3D11 \_ - \_ ressourcenmisc-Kachel Kennzeichen erstellen können \_ . Dieser Abschnitt enthält die gültigen Parameter zum Erstellen von gekachelten Ressourcen.
ms.assetid: 19A0EA7F-888D-4102-A5D2-F3B54775EDE8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b912325371c59bd46a6cc4245289b2fe5d32a924
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/13/2019
ms.locfileid: "103719331"
---
# <a name="tiled-resource-creation-parameters"></a>Parameter für die Kachel Ressourcen Erstellung

Es gibt einige Einschränkungen für den Typ der Direct3D-Ressourcen, die Sie mit dem [**D3D11 \_ - \_ ressourcenmisc- \_ Kachel**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) Kennzeichen erstellen können. Dieser Abschnitt enthält die gültigen Parameter zum Erstellen von gekachelten Ressourcen.

<dl> <dt>

<span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**Unterstützter Ressourcentyp**
</dt> <dd>

Texture2D \[ array \] (einschließlich texturecube- \[ array \] , das eine Variante des Texture2D- \[ Arrays ist \] ) oder Puffer.

**Nicht unterstützt:** Texture1D \[ array \] oder Texture3D, aber Texture3D wird in Zukunft möglicherweise unterstützt.

</dd> <dt>

<span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Unterstützte Ressourcenverwendung**
</dt> <dd>

D3D11 \_ Verwendungs \_ Standard.

**Nicht unterstützt:** D3D11 \_ use \_ Dynamic, D3D11 \_ Usage \_ Staging oder D3D11 \_ Usage \_ unmutable.

</dd> <dt>

<span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Unterstützte ressourcenmisc-Flags**
</dt> <dd>

D3D11 \_ Resource \_ misc \_ (definitionsgemäß), \_ misc \_ texturecube, \_ DrawIndirect \_ args, \_ buffer \_ Allow \_ RAW \_ views, \_ buffer \_ strukturierte, \_ Resource \_ Clamp oder \_ Generate \_ mips.

**Nicht unterstützt:** \_ Freigegebene, frei \_ gegebene \_ keyedmutex-, \_ GDI- \_ kompatible, frei \_ gegebene \_ nthandle, \_ eingeschränkte \_ Inhalte, frei \_ \_ gegebene \_ Ressource einschränken, Treiber für frei \_ gegebene Ressourcen einschränken, geschützter \_ \_ \_ \_ oder \_ Kachel \_ Pool.

</dd> <dt>

<span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**Unterstützte Bindungsflags**
</dt> <dd>

D3D11 \_ Bind- \_ Shader- \_ Ressource, \_ \_ Renderziel, \_ tiefen \_ Schablone oder \_ unsortierter \_ Zugriff.

**Nicht unterstützt:** \_ Konstanter \_ Puffer: \_ Vertex \_ \[ -Puffer beachten Sie, dass die Bindung eines Kachel Puffers als SRV/UAV/RTV weiterhin in Ordnung ist \] , \_ Index \_ Puffer, \_ \_ Streamausgabe, \_ Bindungs \_ Decoder oder \_ Bind \_ Video \_ Encoder.

</dd> <dt>

<span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**Unterstützte Formate**
</dt> <dd>

Alle Formate, die für die angegebene Konfiguration verfügbar sind, und zwar unabhängig davon, ob Sie gekachelt werden, mit einigen Ausnahmen.

</dd> <dt>

<span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**Unterstützte samplede SC (Multisample count, Quality)**
</dt> <dd>

Unabhängig davon, was für die jeweilige Konfiguration unterstützt wird, mit einigen Ausnahmen.

</dd> <dt>

<span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**Unterstützte Breite/Höhe/miplevels/arraySize**
</dt> <dd>

Vollständige Blöcke, die von Direct3D 11 unterstützt werden. Bei gekachelten Ressourcen gibt es keine Einschränkung der Gesamtspeicher Größe, die für nicht gekachelte Ressourcen erhoben wird. Gekachelte Ressourcen werden nur durch die Grenzen des gesamten virtuellen Adressraums eingeschränkt. Weitere Informationen finden Sie unter [Adressraum verfügbar für Kachel Ressourcen](address-space-available-for-tiled-resources.md).

</dd> </dl>

Der ursprüngliche Inhalt des Kachel Pool Arbeitsspeichers ist nicht definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Kachel Ressourcen](creating-tiled-resources.md)
</dt> </dl>

 

 




