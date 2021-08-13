---
title: WINBIO_ANSI_385_FACE Konstanten (Winbio \_ types.h)
description: Geben Sie die Frontalbildtypen für die Gesichtserkennung an.
ms.assetid: 16D21E40-C158-4674-80D0-AE9494124B96
topic_type:
- apiref
api_name:
- WINBIO_ANSI_385_FACE_TYPE_UNKNOWN
- WINBIO_ANSI_385_FACE_FRONTAL_FULL
- WINBIO_ANSI_385_FACE_FRONTAL_TOKEN
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6bd8ddc173915e2bbd912a6a668c63b4be733f32357189fe6ff3365a20bacfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119410310"
---
# <a name="winbio_ansi_385_face-constants"></a>WINBIO \_ ANSI \_ 385 \_ FACE-Konstanten

Bei den folgenden Konstanten handelt es sich um **WINBIO \_ BIOMETRIC \_ SUBTYPE-Werte,** die verwendet werden können, um die beiden Typen von Frontalbildaufnahmen gemäß der Definition von ANSI INCITS 385-2004 anzugeben: "Face Recognition Format for Data Interchange": vollständige und niedrige Auflösung. In der Praxis verwendet das biometrische Framework nur Bilder mit vollständiger Auflösung für die Gesichtserkennung.



| Konstante/Wert                                                                                                                                                                                                                                                                          | BESCHREIBUNG                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WINBIO_ANSI_385_FACE_TYPE_UNKNOWN"></span><span id="winbio_ansi_385_face_type_unknown"></span><dl> <dt>**WINBIO \_ ANSI \_ 385 \_ FACE TYPE \_ \_ UNKNOWN**</dt> <dt>0</dt> </dl>    | Der Typ des Frontalbildbilds ist unbekannt.<br/>         |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_FULL"></span><span id="winbio_ansi_385_face_frontal_full"></span><dl> <dt>**WINBIO \_ ANSI \_ 385 \_ FACE \_ FRONTAL \_ FULL**</dt> <dt>1</dt> </dl>    | Der Gesichtsbildtyp "Frontal" ist eine vollständige Auflösung.<br/> |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_TOKEN"></span><span id="winbio_ansi_385_face_frontal_token"></span><dl> <dt>**WINBIO \_ ANSI \_ 385 \_ FACE \_ FRONTAL \_ TOKEN**</dt> <dt>2</dt> </dl> | Der Gesichtsbildtyp "Frontal" hat eine niedrige Auflösung.<br/>  |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (einschließlich Winbio.h)</dt> </dl> |



 

 





