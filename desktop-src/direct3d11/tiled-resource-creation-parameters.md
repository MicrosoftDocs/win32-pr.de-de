---
title: Parameter für die Erstellung von Gekachelten Ressourcen
description: Es gibt einige Einschränkungen für den Typ von Direct3D-Ressourcen, die Sie mit dem D3D11 \_ RESOURCE \_ MISC \_ TILED-Flag erstellen können. Dieser Abschnitt enthält die gültigen Parameter zum Erstellen von gekachelten Ressourcen.
ms.assetid: 19A0EA7F-888D-4102-A5D2-F3B54775EDE8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9668c21060cbb8f39884204780ce689b3e67196aef0bdcfef891836768f04af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279840"
---
# <a name="tiled-resource-creation-parameters"></a>Parameter für die Erstellung von Gekachelten Ressourcen

Es gibt einige Einschränkungen für den Typ von Direct3D-Ressourcen, die Sie mit dem [**D3D11 \_ RESOURCE \_ MISC \_ TILED-Flag**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) erstellen können. Dieser Abschnitt enthält die gültigen Parameter zum Erstellen von gekachelten Ressourcen.

<dl> <dt>

<span id="Supported_Resource_Type"></span><span id="supported_resource_type"></span><span id="SUPPORTED_RESOURCE_TYPE"></span>**Unterstützter Ressourcentyp**
</dt> <dd>

Texture2D \[ Array \] (einschließlich TextureCube \[ Array , das eine Variante des \] Texture2D-Arrays \[ \] ist) oder Buffer.

**NICHT unterstützt:** Texture1D \[ Array \] oder Texture3D, aber Texture3D kann in Zukunft unterstützt werden.

</dd> <dt>

<span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Unterstützte Ressourcennutzung**
</dt> <dd>

D3D11- \_ \_ NUTZUNGSSTANDARD.

**NICHT unterstützt:** D3D11 \_ USAGE \_ DYNAMIC, D3D11 \_ USAGE STAGING ODER \_ D3D11 \_ USAGE \_ IMMUTABLE.

</dd> <dt>

<span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Unterstützte Ressourcenflags**
</dt> <dd>

D3D11 \_ RESOURCE \_ MISC \_ TILED (by definition), \_ MISC \_ TEXTURECUBE, \_ DRAWINDIRECT \_ ARGS, \_ BUFFER ALLOW RAW \_ \_ \_ VIEWS, BUFFER \_ \_ STRUCTURED, RESOURCE CLAMP oder GENERATE \_ \_ \_ \_ MIPS.

**NICHT unterstützt:** \_ SHARED, \_ SHARED \_ KEYEDMUTEX, \_ GDI \_ COMPATIBLE, SHARED \_ \_ NTHANDLE, \_ RESTRICTED \_ CONTENT, RESTRICT SHARED \_ \_ \_ RESOURCE, RESTRICT SHARED RESOURCE \_ \_ \_ \_ DRIVER, \_ GUARDED oder TILE \_ \_ POOL.

</dd> <dt>

<span id="Supported_Bind_Flags"></span><span id="supported_bind_flags"></span><span id="SUPPORTED_BIND_FLAGS"></span>**Unterstützte Bindungsflags**
</dt> <dd>

D3D11 \_ BIND \_ SHADER \_ RESOURCE, RENDER \_ \_ TARGET, DEPTH \_ \_ STENCIL oder \_ UNORDERED \_ ACCESS.

**NICHT unterstützt:** \_ CONSTANT \_ BUFFER, \_ VERTEX \_ BUFFER Beachten \[ Sie, dass die Bindung eines gekachelten Puffers als SRV/UAV/RTV weiterhin in Ordnung \] ist, INDEX \_ \_ BUFFER, STREAM \_ \_ OUTPUT, BIND DECODER oder \_ BIND VIDEO \_ \_ \_ \_ ENCODER.

</dd> <dt>

<span id="Supported_Formats"></span><span id="supported_formats"></span><span id="SUPPORTED_FORMATS"></span>**Unterstützte Formate**
</dt> <dd>

Alle Formate, die für die angegebene Konfiguration verfügbar wären, unabhängig davon, ob sie gekachelt wird, mit einigen Ausnahmen.

</dd> <dt>

<span id="Supported_SampleDesc__Multisample_count__quality_"></span><span id="supported_sampledesc__multisample_count__quality_"></span><span id="SUPPORTED_SAMPLEDESC__MULTISAMPLE_COUNT__QUALITY_"></span>**Supported SampleDesc (Multisample count, quality)**
</dt> <dd>

Was auch immer für die angegebene Konfiguration unterstützt wird, unabhängig davon, ob sie gekachelt wird, mit einigen Ausnahmen.

</dd> <dt>

<span id="Supported_Width_Height_MipLevels_ArraySize"></span><span id="supported_width_height_miplevels_arraysize"></span><span id="SUPPORTED_WIDTH_HEIGHT_MIPLEVELS_ARRAYSIZE"></span>**Unterstützte Breite/Höhe/MipLevels/ArraySize**
</dt> <dd>

Vollständige Erweiterungen, die von Direct3D 11 unterstützt werden. Für gekachelte Ressourcen gelten keine Einschränkungen hinsichtlich der Gesamtgröße des Arbeitsspeichers, die für nicht gekachelte Ressourcen gelten. Gekachelte Ressourcen sind nur durch allgemeine Grenzwerte für den virtuellen Adressraum eingeschränkt. Weitere Informationen finden Sie unter [Verfügbarer Adressraum für gekachelte Ressourcen.](address-space-available-for-tiled-resources.md)

</dd> </dl>

Der ursprüngliche Inhalt des Kachelpoolspeichers ist nicht definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von gekachelten Ressourcen](creating-tiled-resources.md)
</dt> </dl>

 

 




