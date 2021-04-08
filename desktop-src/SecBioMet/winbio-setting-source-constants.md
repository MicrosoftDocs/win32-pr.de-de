---
title: WINBIO_SETTING_SOURCE Konstanten (winbio \_ types. h)
description: Bestimmen Sie, ob die Windows-Biometrieframework derzeit aktiviert ist.
ms.assetid: d95aa6cc-ddff-40fb-ab82-eac78dc0cb6b
topic_type:
- apiref
api_name:
- WINBIO_SETTING_SOURCE_INVALID
- WINBIO_SETTING_SOURCE_DEFAULT
- WINBIO_SETTING_SOURCE_POLICY
- WINBIO_SETTING_SOURCE_LOCAL
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54723612c7e0948e09baddf22ad4f4703ca5c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957156"
---
# <a name="winbio_setting_source-constants"></a>Winbio- \_ Einstellungs \_ Quellen Konstanten

Die folgenden Konstanten werden von der [**winbiogetenabledsetting**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting) -Funktion verwendet, um zu bestimmen, ob die Windows-Biometrieframework derzeit aktiviert ist. Die Konstanten geben an, woher die Einstellung stammt.



| Konstante                                                                                                                                                                                                        | BESCHREIBUNG                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| <span id="WINBIO_SETTING_SOURCE_INVALID"></span><span id="winbio_setting_source_invalid"></span><dl> <dt>**winbio- \_ Einstellungs \_ Quelle \_ ungültig**</dt> </dl> | Die Einstellung ist ungültig.<br/>                              |
| <span id="WINBIO_SETTING_SOURCE_DEFAULT"></span><span id="winbio_setting_source_default"></span><dl> <dt>**Standardeinstellung für winbio- \_ Einstellungs \_ Quelle \_**</dt> </dl> | Die Einstellung stammt aus der integrierten Richtlinie.<br/>           |
| <span id="WINBIO_SETTING_SOURCE_POLICY"></span><span id="winbio_setting_source_policy"></span><dl> <dt>**winbio- \_ Einstellungs \_ Quell \_ Richtlinie**</dt> </dl>    | Die Einstellung stammt aus der Registrierung des lokalen Computers.<br/> |
| <span id="WINBIO_SETTING_SOURCE_LOCAL"></span><span id="winbio_setting_source_local"></span><dl> <dt>**winbio- \_ Einstellungs \_ Quelle \_ lokal**</dt> </dl>       | Die Einstellung wurde von Gruppenrichtlinie<br/>                |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Client Anwendungs Konstanten](client-application-constants.md)
</dt> </dl>

 

 





