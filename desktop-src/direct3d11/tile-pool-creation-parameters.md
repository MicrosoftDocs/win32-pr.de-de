---
title: Parameter zum Erstellen des Kachelpools
description: Verwenden Sie die Parameter in diesem Abschnitt, um Kachelpools über die ID3D11Device CreateBuffer-API zu definieren.
ms.assetid: 04290AAF-8517-4557-954E-1CAA3A0CA7F6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7350dc01c845542b97674189a120c0d55db95c282dc80b11fda66230618f99b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119470"
---
# <a name="tile-pool-creation-parameters"></a>Parameter zum Erstellen des Kachelpools

Verwenden Sie die Parameter in diesem Abschnitt, um Kachelpools über die [**ID3D11Device::CreateBuffer-API zu**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) definieren.

<dl> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Größe**
</dt> <dd>

Zuordnungsgröße als Vielfaches von 64 KB. 0 ist gültig, da Sie später einen [**ID3D11DeviceContext2::ResizeTilePool-Vorgang verwenden**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) können.

</dd> <dt>

<span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Unterstützte Ressourcenflags**
</dt> <dd>

D3D11 RESOURCE MISC TILE POOL (identifiziert die Ressource als \_ \_ \_ Kachelpool), \_ D3D11 \_ RESOURCE \_ MISC \_ SHARED, SHARED \_ \_ KEYEDMUTEX oder \_ SHARED \_ NTHANDLE.

</dd> <dt>

<span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Unterstützte Ressourcennutzung**
</dt> <dd>

Nur D3D11 \_ USAGE \_ DEFAULT.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von gekachelten Ressourcen](creating-tiled-resources.md)
</dt> </dl>

 

 




