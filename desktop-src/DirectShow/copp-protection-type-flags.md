---
description: Die folgenden Konstanten werden mit dem Certified Output Protection Protocol (COPP) für bestimmte Ausgabeschutzmechanismen verwendet.
ms.assetid: a3cd63d8-22a5-473c-83c2-3499f3d32671
title: COPP-Schutztypflags (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPP_ProtectionType_Unknown
- COPP_ProtectionType_None
- COPP_ProtectionType_HDCP
- COPP_ProtectionType_ACP
- COPP_ProtectionType_CGMSA
- COPP_ProtectionType_Mask
- COPP_ProtectionType_Reserved
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 75038b22a30be41389311fd1a7cfb830f870859b01ba48fd9a791a42cee86dc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119214050"
---
# <a name="copp-protection-type-flags"></a>COPP-Schutztypflags

Die folgenden Konstanten werden mit dem Certified Output Protection Protocol (COPP) für bestimmte Ausgabeschutzmechanismen verwendet.



| Konstante/Wert                                                                                                                                                                                                                                                                                                             | BESCHREIBUNG                                                     |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="COPP_ProtectionType_Unknown"></span><span id="copp_protectiontype_unknown"></span><span id="COPP_PROTECTIONTYPE_UNKNOWN"></span><dl> <dt>**COPP \_ \_ProtectionType Unknown**</dt> <dt>0x80000000</dt> </dl>     | Unbekannter Schutzmechanismus.<br/>                        |
| <span id="COPP_ProtectionType_None"></span><span id="copp_protectiontype_none"></span><span id="COPP_PROTECTIONTYPE_NONE"></span><dl> <dt>**COPP \_ ProtectionType \_ None**</dt> <dt>0x00000000</dt> </dl>                 | Keine Schutzmechanismen.<br/>                            |
| <span id="COPP_ProtectionType_HDCP"></span><span id="copp_protectiontype_hdcp"></span><span id="COPP_PROTECTIONTYPE_HDCP"></span><dl> <dt>**COPP \_ ProtectionType \_ HDCP**</dt> <dt>0x00000001</dt> </dl>                 | High-Bandwidth Digital Content Protection (HDCP).<br/>    |
| <span id="COPP_ProtectionType_ACP"></span><span id="copp_protectiontype_acp"></span><span id="COPP_PROTECTIONTYPE_ACP"></span><dl> <dt>**COPP \_ ProtectionType \_ ACP**</dt> <dt>0x00000002</dt> </dl>                     | Analoger Kopierschutz (ACP).<br/>                        |
| <span id="COPP_ProtectionType_CGMSA"></span><span id="copp_protectiontype_cgmsa"></span><span id="COPP_PROTECTIONTYPE_CGMSA"></span><dl> <dt>**COPP \_ ProtectionType \_ CGMSA**</dt> <dt>0x00000004</dt> </dl>             | Copy Generation Management System Analog (CGMS-A).<br/> |
| <span id="COPP_ProtectionType_Mask"></span><span id="copp_protectiontype_mask"></span><span id="COPP_PROTECTIONTYPE_MASK"></span><dl> <dt>**COPP \_ ProtectionType \_ Mask**</dt> <dt>0x80000007</dt> </dl>                 | Bitmaske zum Isolieren gültiger Flags.<br/>                      |
| <span id="COPP_ProtectionType_Reserved"></span><span id="copp_protectiontype_reserved"></span><span id="COPP_PROTECTIONTYPE_RESERVED"></span><dl> <dt>**COPP \_ \_Reservierte**</dt> <dt>protectionType-0x7FFFFFF8</dt> </dl> | Reserviert. Muss Null sein.<br/>                              |



## <a name="remarks"></a>Hinweise

Einige Methoden geben ein einzelnes Flag von diesem Enumerationstyp zurück, und einige Methoden geben ein bitweises **OR** von einem oder mehreren Flags zurück.

Diese Flags werden in den folgenden COPP-Abfragen und -Befehlen verwendet.

-   Globale Schutzebene
-   Lokale Schutzebene
-   Schutztyp
-   Festlegen der Schutzebene

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Konstanten und GUIDs](constants-and-guids.md)
</dt> <dt>

[Verwenden von Certified Output Protection Protocol (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 




