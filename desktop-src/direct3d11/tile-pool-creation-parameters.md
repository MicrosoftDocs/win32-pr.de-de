---
title: Parameter zum Erstellen des Kachelpools
description: Verwenden Sie die Parameter in diesem Abschnitt, um Kachel Pools über die ID3D11Device-API-API zu definieren.
ms.assetid: 04290AAF-8517-4557-954E-1CAA3A0CA7F6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c22ef3acf1c7b926890d1c5867df55bea4821b90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036483"
---
# <a name="tile-pool-creation-parameters"></a>Parameter zum Erstellen des Kachelpools

Verwenden Sie die Parameter in diesem Abschnitt, um Kachel Pools über die [**ID3D11Device::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) -API zu definieren.

<dl> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Größe**
</dt> <dd>

Zuordnungs Größe, als Vielfaches von 64 KB. 0 ist gültig, da Sie später einen [**ID3D11DeviceContext2:: resizetilepool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) -Vorgang verwenden können.

</dd> <dt>

<span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Unterstützte ressourcenmisc-Flags**
</dt> <dd>

D3D11 \_ \_ ressourcenmisc- \_ Kachel \_ Pool (identifiziert die Ressource als Kachel Pool), \_ D3D11 \_ ressourcenmisc \_ Shared, \_ Shared \_ keyedmutex oder \_ Shared \_ nthandle.

</dd> <dt>

<span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Unterstützte Ressourcenverwendung**
</dt> <dd>

D3D11 \_ \_ nur Verwendungs Standard.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Kachel Ressourcen](creating-tiled-resources.md)
</dt> </dl>

 

 




