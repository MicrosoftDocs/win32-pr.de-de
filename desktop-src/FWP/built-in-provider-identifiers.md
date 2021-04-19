---
title: Integrierte Anbieter Bezeichner ("f")
description: Die Bezeichner für die Anbieter, die in die Windows-Filter Plattform (WFP) integriert sind, werden jeweils durch eine GUID dargestellt.
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
ms.openlocfilehash: 060f6d63d703d7c91e5538b7bfdd8758ee2e1cde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344089"
---
# <a name="built-in-provider-identifiers"></a>Integrierte Anbieter Bezeichner

Die Bezeichner für die Anbieter, die in die Windows-Filter Plattform (WFP) integriert sind, werden jeweils durch eine GUID dargestellt.

Diese Bezeichner werden wie folgt definiert.

<dl> <dt>

<span id="FWPM_PROVIDER_IKEEXT"></span><span id="fwpm_provider_ikeext"></span>**swpm- \_ Anbieter \_ ikeext**
</dt> <dd> <dl> <dt>

{10ad9216-CCDE-456c-8b16-e9b04e60a90b}
</dt> <dt>



Wird verwendet, um alle von IKE/AuthIP hinzugefügten Filter zu identifizieren.


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_IPSEC_DOS_CONFIG"></span><span id="fwpm_provider_ipsec_dos_config"></span>**\_ \_ IPSec- \_ DOS- \_ Konfiguration des WPM-Anbieters**
</dt> <dd> <dl> <dt>

{3c6c0519-c05c-4bb9-8338-2327814ce8bf}
</dt> <dt>



Wird verwendet, um alle vom IPSec-DOS-Schutz hinzugefügten Filter zu identifizieren.

> [!Note]  
> Nur unter Windows 7 und Windows Server 2008 R2 verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_provider_tcp_chimney_offload"></span>**\_TCP-Chimney- \_ \_ \_ Abladung des WPM-Anbieters**
</dt> <dd> <dl> <dt>

{896aa19e-9a34-4bcb-ae79-beb9127c84 B9}
</dt> <dt>



Dient zum Identifizieren aller von der TCP-Chimney-Abladung hinzugefügten Filter.


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_TCP_TEMPLATES"></span><span id="fwpm_provider_tcp_templates"></span>**TCP-Vorlagen für den WPM- \_ Anbieter \_ \_**
</dt> <dd> <dl> <dt>

{76cfcd30-3394-432D-bed3-441ae50e63c3}
</dt> <dt>



Wird verwendet, um alle von TCP-Vorlagen hinzugefügten Filter zu identifizieren.

> [!Note]  
> Nur unter Windows 8 und Windows Server 2012 verfügbar.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>"F"</dt> </dl> |



 

 





