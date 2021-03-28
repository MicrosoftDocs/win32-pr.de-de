---
description: Flags, die die festzulegenden oder zurück zugegenden Daten einschränken.
title: Srrf (shlwapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c9dbffd1-3b3e-4a25-89ee-1666e2812a62
api_name:
- SRRF_RT_REG_NONE
- SRRF_RT_REG_SZ
- SRRF_RT_REG_EXPAND_SZ
- SRRF_RT_REG_BINARY
- SRRF_RT_REG_DWORD
- SRRF_RT_REG_MULTI_SZ
- SRRF_RT_REG_QWORD
- SRRF_RT_DWORD
- SRRF_RT_QWORD
- SRRF_RT_ANY
- SRRF_RM_ANY
- SRRF_RM_NORMAL
- SRRF_RM_SAFE
- SRRF_RM_SAFENETWORK
- SRRF_NOEXPAND
- SRRF_ZEROONFAILURE
- SRRF_NOVIRT
api_type:
- HeaderDef
api_location:
- Shlwapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3ba36b64496413a54e6d8b8b96c16c265367d05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042416"
---
# <a name="srrf"></a>Srrf

Flags, die die festzulegenden oder zurück zugegenden Daten einschränken.



| Konstante/Wert                                                                                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SRRF_RT_REG_NONE"></span><span id="srrf_rt_reg_none"></span><dl> <dt>**Srrf \_ RT \_ reg \_ None**</dt> <dt>0x00000001</dt> </dl>                 | Geben Sie reg \_ None ein.<br/>                                                                                                                                                                                             |
| <span id="SRRF_RT_REG_SZ"></span><span id="srrf_rt_reg_sz"></span><dl> <dt>**Srrf \_ RT \_ reg \_ SZ**</dt> <dt>0x00000002</dt> </dl>                       | Geben Sie reg \_ SZ ein. REG-Erweiterungs- \_ \_ SZ-Typen werden automatisch in REG SZ konvertiert, \_ es sei denn, das srrf \_ NOEXPAND-Flag ist angegeben.<br/>                                                                                     |
| <span id="SRRF_RT_REG_EXPAND_SZ"></span><span id="srrf_rt_reg_expand_sz"></span><dl> <dt>**Srrf \_ RT \_ reg \_ Expand \_ SZ**</dt> <dt>0x00000004</dt> </dl> | Typ reg \_ Expand \_ SZ. Wenn Sie einen Wert abrufen, müssen Sie auch das srrf \_ NOEXPAND-Flag abrufen, oder " [**shreggetvalue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea) " schlägt mit einem \_ ungültigen \_ Parameter fehl.<br/>                                     |
| <span id="SRRF_RT_REG_BINARY"></span><span id="srrf_rt_reg_binary"></span><dl> <dt>**Srrf \_ RT \_ reg \_ Binary**</dt> <dt>0x00000008</dt> </dl>           | Geben Sie reg \_ Binary ein.<br/>                                                                                                                                                                                           |
| <span id="SRRF_RT_REG_DWORD"></span><span id="srrf_rt_reg_dword"></span><dl> <dt>**Srrf \_ RT \_ reg \_ DWORD**</dt> <dt>0x00000010</dt> </dl>              | Geben Sie reg \_ DWORD ein.<br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_REG_MULTI_SZ"></span><span id="srrf_rt_reg_multi_sz"></span><dl> <dt>**Srrf \_ RT \_ reg \_ \_ MultiSZ**</dt> <dt>0x00000020</dt> </dl>    | Geben Sie \_ reg \_ MultiSZ ein.<br/>                                                                                                                                                                                        |
| <span id="SRRF_RT_REG_QWORD"></span><span id="srrf_rt_reg_qword"></span><dl> <dt>**Srrf \_ RT \_ reg \_ QWORD**</dt> <dt>0x00000040</dt> </dl>              | Geben Sie reg \_ QWORD ein.<br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_DWORD"></span><span id="srrf_rt_dword"></span><dl> <dt>**Srrf \_ RT \_ DWORD**</dt> <dt>0x00000018</dt> </dl>                           | Reg \_ DWORD-und 32-Bit-reg- \_ Binär Typen. Dies entspricht srrf \_ RT \_ reg \_ Binary \| srrf \_ RT \_ reg \_ DWORD. Wenn beim Abrufen eines Werts die Binärdaten des Werts größer als 32 Bits sind, werden Sie nicht zurückgegeben.<br/> |
| <span id="SRRF_RT_QWORD"></span><span id="srrf_rt_qword"></span><dl> <dt>**Srrf \_ RT \_ QWORD**</dt> <dt>0x00000048</dt> </dl>                           | Reg \_ QWORD-und 64-Bit-reg- \_ Binär Typen. Dies entspricht srrf \_ RT \_ reg \_ Binary \| srrf \_ RT \_ reg \_ QWORD. Wenn beim Abrufen eines Werts die Binärdaten des Werts größer als 64 Bits sind, werden Sie nicht zurückgegeben.<br/> |
| <span id="SRRF_RT_ANY"></span><span id="srrf_rt_any"></span><dl> <dt>**Srrf \_ RT \_ beliebige**</dt> <dt>0X0000FFFF</dt> </dl>                                 | Alle Typen. Legen Sie dieses Flag fest, wenn kein anderer srrf \_ RT-Wert festgelegt ist.<br/>                                                                                                                                                 |
| <span id="SRRF_RM_ANY"></span><span id="srrf_rm_any"></span><dl> <dt>**Srrf \_ RM \_ beliebige**</dt> <dt>0x00000000</dt> </dl>                                 | Keine Modus-Einschränkung. Dies ist der Standardwert.<br/>                                                                                                                                                             |
| <span id="SRRF_RM_NORMAL"></span><span id="srrf_rm_normal"></span><dl> <dt>**Srrf \_ RM \_ Normal**</dt> <dt>0x00010000 bis</dt> </dl>                        | Schränken Sie den Systemstart Modus auf "normaler Start" ein.<br/>                                                                                                                                                              |
| <span id="SRRF_RM_SAFE"></span><span id="srrf_rm_safe"></span><dl> <dt>**Srrf \_ RM- \_ sicheres**</dt> <dt>0x00020000</dt> </dl>                              | Beschränken Sie den Systemstart Modus auf "Abgesicherter Modus".<br/>                                                                                                                                                                |
| <span id="SRRF_RM_SAFENETWORK"></span><span id="srrf_rm_safenetwork"></span><dl> <dt>**Srrf \_ RM \_ SafeWork**</dt> <dt>0x00040000</dt> </dl>         | Beschränken Sie den Systemstart Modus auf "Abgesicherter Modus mit Netzwerk".<br/>                                                                                                                                                |
| <span id="SRRF_NOEXPAND"></span><span id="srrf_noexpand"></span><dl> <dt>**Srrf \_ NOEXPAND**</dt> <dt>0x10000000</dt> </dl>                            | Erweitern Sie keine automatischen Erweiterungs-und Erweiterungs Zeichenfolgen \_ \_ .<br/>                                                                                                                                            |
| <span id="SRRF_ZEROONFAILURE"></span><span id="srrf_zeroonfailure"></span><dl> <dt>**Srrf \_ Zeroonfailure**</dt> <dt>0x20000000</dt> </dl>             | Wenn *pvData* beim Abrufen eines Werts nicht **null** ist, legen Sie den Inhalt des *pvData* -Puffers bei einem Fehler auf Nullen fest.<br/>                                                                                        |
| <span id="SRRF_NOVIRT"></span><span id="srrf_novirt"></span><dl> <dt>**Srrf \_ Novirt**</dt> <dt>0x40000000</dt> </dl>                                  | Wenn beim Abrufen eines Werts der angeforderte Schlüssel virtualisiert ist, wird der Fehler mit der Fehler \_ Datei \_ nicht \_ gefunden.<br/>                                                                                                            |



## <a name="remarks"></a>Bemerkungen

Diese Werte werden in "shlwapi. h" definiert.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Shlwapi. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Shregsetvalue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetvalue)
</dt> <dt>

[**Shreggetvalue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea)
</dt> </dl>

 

 




