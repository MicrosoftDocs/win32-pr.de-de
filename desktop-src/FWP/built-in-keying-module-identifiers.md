---
title: Integrierte Schlüsselmodulbezeichner (Fwpmu.h)
description: Die Bezeichner für die Schlüsselierungsmodule, die in die Windows Filtering Platform (WFP) integriert sind, werden jeweils durch eine GUID dargestellt.
ms.assetid: ba3aaf0f-5524-4d61-bb74-e4714b11b2a9
topic_type:
- apiref
api_name:
- FWPM_KEYING_MODULE_IKE
- FWPM_KEYING_MODULE_IKEV2
- FWPM_KEYING_MODULE_AUTHIP
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b978832d65ab930f172c205144ba352f028c486d4d04c6f680ee963c6cf2ae2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951339"
---
# <a name="built-in-keying-module-identifiers"></a>Integrierte Schlüsselmodulbezeichner

Die Bezeichner für die Schlüsselierungsmodule, die in die Windows Filtering Platform (WFP) integriert sind, werden jeweils durch eine GUID dargestellt.

Diese Bezeichner werden wie folgt definiert.

<dl> <dt>

<span id="FWPM_KEYING_MODULE_IKE"></span><span id="fwpm_keying_module_ike"></span>**IKE DES \_ FWPM-SCHLÜSSELMODULS \_ \_**
</dt> <dd> <dl> <dt>



IKE-Exchange (Internet Key Exchange).


</dt> </dl> </dd> <dt>

<span id="FWPM_KEYING_MODULE_IKEV2"></span><span id="fwpm_keying_module_ikev2"></span>**\_FWPM-SCHLÜSSELMODUL \_ \_ IKEV2**
</dt> <dd> <dl> <dt>



Schlüsselmodul Exchange IKEv2 (Internet Key Exchange Version 2).

> [!Note]  
> Nur auf Windows Server 2008 R2 und Windows 7 verfügbar.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_KEYING_MODULE_AUTHIP"></span><span id="fwpm_keying_module_authip"></span>**AUTHIP DES \_ FWPM-SCHLÜSSELMODULS \_ \_**
</dt> <dd> <dl> <dt>



AuthIP-Schlüsselmodul.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Fwpmu.h</dt> </dl> |



 

 





