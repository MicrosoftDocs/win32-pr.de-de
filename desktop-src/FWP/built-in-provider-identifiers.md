---
title: Integrierte Anbieterbezeichner (Fwpmu.h)
description: Die Bezeichner für die Anbieter, die in die Windows Filtering Platform (WFP) integriert sind, werden jeweils durch eine GUID dargestellt.
ms.assetid: 61bc1e2d-f6ee-45db-892f-c49680d27072
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_IKEEXT
- FWPM_PROVIDER_IPSEC_DOS_CONFIG
- FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD
- FWPM_PROVIDER_TCP_TEMPLATES
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8982fe6ebbe3f4cf5135f2b67f07826ddf9d3f970ca0568c7095931c617cdce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951309"
---
# <a name="built-in-provider-identifiers"></a>Integrierte Anbieterbezeichner

Die Bezeichner für die Anbieter, die in die Windows Filtering Platform (WFP) integriert sind, werden jeweils durch eine GUID dargestellt.

Diese Bezeichner werden wie folgt definiert.

<dl> <dt>

<span id="FWPM_PROVIDER_IKEEXT"></span><span id="fwpm_provider_ikeext"></span>**\_FWPM-ANBIETER \_ IKEEXT**
</dt> <dd> <dl> <dt>

{10ad9216-ccde-456c-8b16-e9f04e60a90b}
</dt> <dt>



Wird verwendet, um alle von IKE/AuthIP hinzugefügten Filter zu identifizieren.


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_IPSEC_DOS_CONFIG"></span><span id="fwpm_provider_ipsec_dos_config"></span>**\_ \_ IPSEC-DOS-KONFIGURATION DES \_ FWPM-ANBIETERS \_**
</dt> <dd> <dl> <dt>

{3c6c0519-c05c-4bb9-8338-2327814ce8bf}
</dt> <dt>



Wird verwendet, um alle von IPsec DoS Protection hinzugefügten Filter zu identifizieren.

> [!Note]  
> Nur auf Windows 7 und Windows Server 2008 R2 verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_provider_tcp_chimney_offload"></span>**\_ \_ \_ TCP-CHIMNEY-AUSLADUNG DES \_ FWPM-ANBIETERS**
</dt> <dd> <dl> <dt>

{896aa19e-9a34-4bcb-ae79-beb9127c84b9}
</dt> <dt>



Wird verwendet, um alle Filter zu identifizieren, die von TCP Chimney Offload hinzugefügt wurden.


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_TCP_TEMPLATES"></span><span id="fwpm_provider_tcp_templates"></span>**TCP-VORLAGEN \_ DES FWPM-ANBIETERS \_ \_**
</dt> <dd> <dl> <dt>

{76cfcd30-3394-432d-bed3-441ae50e63c3}
</dt> <dt>



Wird verwendet, um alle von TCP-Vorlagen hinzugefügten Filter zu identifizieren.

> [!Note]  
> Nur auf Windows 8 und Windows Server 2012.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Fwpmu.h</dt> </dl> |



 

 





