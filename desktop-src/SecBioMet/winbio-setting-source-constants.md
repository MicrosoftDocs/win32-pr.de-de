---
title: WINBIO_SETTING_SOURCE Konstanten (Winbio \_ types.h)
description: Bestimmen Sie, ob das Windows Biometric Framework derzeit aktiviert ist.
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
ms.openlocfilehash: 2f02a5edc80d00d098a592626ad4d9f0e1030f9f6eee119bf615375680d11842
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909318"
---
# <a name="winbio_setting_source-constants"></a>WINBIO \_ SETTING \_ SOURCE Constants

Die folgenden Konstanten werden von der [**WinBioGetEnabledSetting-Funktion**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting) verwendet, um zu bestimmen, ob die Windows Biometric Framework derzeit aktiviert ist. Die Konstanten geben an, woher die Einstellung stammt.



| Konstante                                                                                                                                                                                                        | BESCHREIBUNG                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| <span id="WINBIO_SETTING_SOURCE_INVALID"></span><span id="winbio_setting_source_invalid"></span><dl> <dt>**WINBIO \_ SETTING \_ SOURCE \_ INVALID**</dt> </dl> | Die Einstellung ist ungültig.<br/>                              |
| <span id="WINBIO_SETTING_SOURCE_DEFAULT"></span><span id="winbio_setting_source_default"></span><dl> <dt>**WINBIO \_ SETTING \_ SOURCE \_ DEFAULT**</dt> </dl> | Die Einstellung stammt aus der integrierten Richtlinie.<br/>           |
| <span id="WINBIO_SETTING_SOURCE_POLICY"></span><span id="winbio_setting_source_policy"></span><dl> <dt>**WINBIO \_ SETTING \_ SOURCE \_ POLICY**</dt> </dl>    | Die Einstellung stammt aus der Registrierung des lokalen Computers.<br/> |
| <span id="WINBIO_SETTING_SOURCE_LOCAL"></span><span id="winbio_setting_source_local"></span><dl> <dt>**WINBIO \_ SETTING \_ SOURCE \_ LOCAL**</dt> </dl>       | Die Einstellung wurde von Gruppenrichtlinie<br/>                |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientanwendungskonstanten](client-application-constants.md)
</dt> </dl>

 

 





