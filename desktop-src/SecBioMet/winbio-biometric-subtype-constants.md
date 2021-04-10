---
title: WINBIO_BIOMETRIC_SUBTYPE Konstanten (winbio \_ types. h)
description: Stellen Sie Informationen zu einer biometrischen Messung bereit.
ms.assetid: 019569A9-6184-4E75-9B82-C98F4F45F61A
topic_type:
- apiref
api_name:
- WINBIO_SUBTYPE_NO_INFORMATION
- WINBIO_SUBTYPE_ANY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba1bc25337bf49a48b54b6b2426673daf8a15bd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956690"
---
# <a name="winbio_biometric_subtype-constants"></a>Subtypkonstanten von winbio- \_ Biometrie \_

**Winbio \_ Biometrische \_ subtypkonstanten** werden im gesamten Windows-Biometrieframework verwendet, um zusätzliche Informationen zu einer biometrischen Messung bereitzustellen. Die folgenden Konstanten können verwendet werden, wenn kein Untertyp erforderlich ist oder wenn ein beliebiger Untertyp erforderlich ist.



| Konstante/Wert                                                                                                                                                                                                                                                            | BESCHREIBUNG                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span id="WINBIO_SUBTYPE_NO_INFORMATION"></span><span id="winbio_subtype_no_information"></span><dl> <dt>**Winbio \_ Untertyp \_ keine \_ Informationen**</dt> <dt>0x00</dt> </dl> | Keine Untertyp Informationen.<br/> |
| <span id="WINBIO_SUBTYPE_ANY"></span><span id="winbio_subtype_any"></span><dl> <dt>**Winbio \_ Untertyp \_ beliebiger**</dt> <dt>0xFF</dt> </dl>                                   | Ein beliebiger Untertyp.<br/>            |



## <a name="remarks"></a>Bemerkungen

Verwenden Sie die folgende Tabelle, um die verfügbaren biometrischen Untertypen für einen bestimmten biometrischen Typ zu finden:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>WINBIO_BIOMETRIC_TYPE</strong> Wert</th>
<th>Thema (e) zum Suchen nach <strong>WINBIO_BIOMETRIC_SUBTYPE</strong> Werten</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>WINBIO_TYPE_FACIAL_FEATURES</strong></td>
<td><a href="winbio-ansi-385-face-constants.md"><strong>WINBIO_ANSI_385_FACE Konstanten</strong></a>
<blockquote>
[!Note]<br />
Diese Werte gelten nur für Windows 10 und höher.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>WINBIO_TYPE_FINGERPRINT</strong></td>
<td>Eines der folgenden Themen:
<ul>
<li><a href="winbio-ansi-381-format-constants.md"><strong>WINBIO_ANSI_381_FORMAT Konstanten</strong></a></li>
<li><a href="winbio-ansi-381-img-constants.md"><strong>WINBIO_ANSI_381_IMG Konstanten</strong></a></li>
<li><a href="winbio-ansi-381-img-acq-constants.md"><strong>WINBIO_ANSI_381_IMG_ACQ Konstanten</strong></a></li>
<li><a href="winbio-ansi-381-imp-type-constants.md"><strong>WINBIO_ANSI_381_IMP_TYPE Konstanten</strong></a></li>
<li><a href="winbio-ansi-381-pixels-constants.md"><strong>WINBIO_ANSI_381_PIXELS Konstanten</strong></a></li>
<li><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>WINBIO_ANSI_381_POS Fingerabdruck Konstanten</strong></a></li>
<li><a href="winbio-ansi-381-pos-palm-constants.md"><strong>WINBIO_ANSI_381_POS_Palm Konstanten</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>WINBIO_TYPE_IRIS</strong></td>
<td><a href="winbio-iris-constants.md"><strong>WINBIO_IRIS Konstanten</strong></a>
<blockquote>
[!Note]<br />
Diese Werte gelten nur für Windows 10 und höher.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>WINBIO_TYPE_VOICE</strong></td>
<td><a href="https://www.bing.com/search?q=<strong>WINBIO_VOICE+Constants</strong>"><strong>WINBIO_VOICE Konstanten</strong></a>
<blockquote>
[!Note]<br />
Diese Werte gelten nur für Windows 10 und höher.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Weitere Informationen finden Sie unter [Client Anwendungs Konstanten](client-application-constants.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h)</dt> </dl> |



 

 





