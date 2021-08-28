---
title: WINBIO_BIOMETRIC_SUBTYPE Konstanten (Winbio \_ types.h)
description: Geben Sie Informationen zu einer biometrischen Messung an.
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
ms.openlocfilehash: 07e6dc285e1a19fab8e0363391fbd81429e931cd
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630839"
---
# <a name="winbio_biometric_subtype-constants"></a>WINBIO \_ BIOMETRIC \_ SUBTYPE Constants

**WINBIO \_ BIOMETRISCHE \_ SUBTYPE-Konstanten** werden im gesamten Windows Biometric Framework verwendet, um zusätzliche Informationen zu einer biometrischen Messung bereitzustellen. Die folgenden Konstanten können verwendet werden, wenn kein Untertyp erforderlich ist oder wenn ein Untertyp erforderlich ist.



| Konstante/Wert                                                                                                                                                                                                                                                            | Beschreibung                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------|
| <span id="WINBIO_SUBTYPE_NO_INFORMATION"></span><span id="winbio_subtype_no_information"></span><dl> <dt>**WINBIO \_ UNTERTYP \_ KEINE \_ INFORMATIONEN**</dt> <dt>0x00</dt> </dl> | Keine Untertypinformationen.<br/> |
| <span id="WINBIO_SUBTYPE_ANY"></span><span id="winbio_subtype_any"></span><dl> <dt>**WINBIO \_ SUBTYPE \_ ANY**</dt> <dt>0xFF</dt> </dl>                                   | Ein beliebiger Untertyp.<br/>            |



## <a name="remarks"></a>Hinweise

Um die verfügbaren biometrischen Untertypen für einen bestimmten biometrischen Typ zu finden, verwenden Sie die folgende Tabelle:



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th><strong>WINBIO_BIOMETRIC_TYPE</strong> Wert</th>
<th>Themen zum Suchen <strong>von WINBIO_BIOMETRIC_SUBTYPE</strong> Werten</th>
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
<li><a href="winbio-ansi-381-pos-fingerprint-constants.md"><strong>WINBIO_ANSI_381_POS Fingerabdruckkonstanten</strong></a></li>
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



 

Weitere Informationen finden Sie unter [Clientanwendungskonstanten.](client-application-constants.md)

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h einschließen)</dt> </dl> |



 

 





