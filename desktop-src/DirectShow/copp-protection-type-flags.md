---
description: Die folgenden Konstanten werden mit dem Certified Output Protection Protocol (COPP) für bestimmte Mechanismen zum Schutz von-Mechanismen verwendet.
ms.assetid: a3cd63d8-22a5-473c-83c2-3499f3d32671
title: COPP-Schutztyp Flags (DXVA. h)
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
ms.openlocfilehash: 57e9ccc9420659ac09c19f2bbb7a18db519c07bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365421"
---
# <a name="copp-protection-type-flags"></a>COPP-Schutztyp Flags

Die folgenden Konstanten werden mit dem Certified Output Protection Protocol (COPP) für bestimmte Mechanismen zum Schutz von-Mechanismen verwendet.



| Konstante/Wert                                                                                                                                                                                                                                                                                                             | BESCHREIBUNG                                                     |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="COPP_ProtectionType_Unknown"></span><span id="copp_protectiontype_unknown"></span><span id="COPP_PROTECTIONTYPE_UNKNOWN"></span><dl> <dt>**COPP \_ Schutztyp \_ unbekannt**</dt> <dt>0x80000000</dt> </dl>     | Unbekannter Schutzmechanismus.<br/>                        |
| <span id="COPP_ProtectionType_None"></span><span id="copp_protectiontype_none"></span><span id="COPP_PROTECTIONTYPE_NONE"></span><dl> <dt>**COPP \_ Schutztyp \_ None**</dt> <dt>0x00000000</dt> </dl>                 | Keine Schutzmechanismen.<br/>                            |
| <span id="COPP_ProtectionType_HDCP"></span><span id="copp_protectiontype_hdcp"></span><span id="COPP_PROTECTIONTYPE_HDCP"></span><dl> <dt>**COPP \_ Schutztyp \_ HDCP**</dt> <dt>0x00000001</dt> </dl>                 | High-Bandwidth Digital Content Protection (HDCP).<br/>    |
| <span id="COPP_ProtectionType_ACP"></span><span id="copp_protectiontype_acp"></span><span id="COPP_PROTECTIONTYPE_ACP"></span><dl> <dt>**COPP \_ Schutztyp \_ ACP**</dt> <dt>0x00000002</dt> </dl>                     | Der Schutz von analogen Kopien (ACP).<br/>                        |
| <span id="COPP_ProtectionType_CGMSA"></span><span id="copp_protectiontype_cgmsa"></span><span id="COPP_PROTECTIONTYPE_CGMSA"></span><dl> <dt>**COPP \_ Schutztype \_ cgmsa**</dt> <dt>0x00000004</dt> </dl>             | Copy Generation Management System Analog (CGMS-A).<br/> |
| <span id="COPP_ProtectionType_Mask"></span><span id="copp_protectiontype_mask"></span><span id="COPP_PROTECTIONTYPE_MASK"></span><dl> <dt>**COPP \_ Schutztyp \_ Maske**</dt> <dt>0x80000007</dt> </dl>                 | Bitmaske, um gültige Flags zu isolieren.<br/>                      |
| <span id="COPP_ProtectionType_Reserved"></span><span id="copp_protectiontype_reserved"></span><span id="COPP_PROTECTIONTYPE_RESERVED"></span><dl> <dt>**COPP \_ Schutztyp \_ reserviert**</dt> <dt>0x7ffffff8</dt> </dl> | Reserviert. Muss Null sein.<br/>                              |



## <a name="remarks"></a>Bemerkungen

Einige Methoden geben ein einzelnes Flag von diesem Enumerationstyp zurück, und einige Methoden geben ein bitweises **or** von einem oder mehreren Flags zurück.

Diese Flags werden in den folgenden COPP-Abfragen und-Befehlen verwendet.

-   Globale Schutz Ebene
-   Lokale Schutz Ebene
-   Schutztyp
-   Schutz Ebene festlegen

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Konstanten und GUIDs](constants-and-guids.md)
</dt> <dt>

[Verwenden des Certified Output Protection-Protokolls (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 




