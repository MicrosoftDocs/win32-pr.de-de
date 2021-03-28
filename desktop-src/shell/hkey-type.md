---
description: Diese Datentypen können verwendet werden, um den Typ eines Registrierungs Werts anzugeben.
title: Registrierungs Datentypen (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4185e7af-e1f0-40af-91c7-0ff7e27896ae
api_name:
- REG_BINARY
- REG_DWORD
- REG_QWORD
- REG_DWORD_LITTLE_ENDIAN
- REG_QWORD_LITTLE_ENDIAN
- REG_DWORD_BIG_ENDIAN
- REG_EXPAND_SZ
- REG_LINK
- REG_MULTI_SZ
- REG_NONE
- REG_RESOURCE_LIST
- REG_SZ
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4de4595b55716d58df04a598dd6ba298f22829d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104996594"
---
# <a name="registry-data-types"></a>Registrierungs Datentypen

Diese Datentypen können verwendet werden, um den Typ eines Registrierungs Werts anzugeben.



| Konstante                                                                                                                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_BINARY"></span><span id="reg_binary"></span><dl> <dt>**REG- \_ Binärdatei**</dt> </dl>                                          | Binärdaten in beliebiger Form.<br/>                                                                                                                                                                                                                                                                                          |
| <span id="REG_DWORD"></span><span id="reg_dword"></span><dl> <dt>**REG \_ DWORD**</dt> </dl>                                             | 32-Bit-Nummer.<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_QWORD"></span><span id="reg_qword"></span><dl> <dt>**REG \_ QWORD**</dt> </dl>                                             | 64-Bit-Nummer.<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="REG_DWORD_LITTLE_ENDIAN"></span><span id="reg_dword_little_endian"></span><dl> <dt>**REG \_ DWORD \_ Little- \_ umdian**</dt> </dl> | 32-Bit-Zahl im Little-Endian-Format. Dies entspricht " **reg \_ DWORD**".<br/> Im Little-Endian-Format wird ein multibytewert im Arbeitsspeicher vom niedrigsten Byte (dem "kleinen Ende") bis zum höchsten Byte gespeichert. Beispielsweise wird der Wert 0x12345678 als (0x78 0x56 0x34 0x12) im Little-Endian-Format gespeichert.<br/> |
| <span id="REG_QWORD_LITTLE_ENDIAN"></span><span id="reg_qword_little_endian"></span><dl> <dt>**REG \_ QWORD \_ Little- \_ umdian**</dt> </dl> | Eine 64-Bit-Zahl im Little-Endian-Format. Dies entspricht " **reg \_ QWORD**". <br/>                                                                                                                                                                                                                                   |
| <span id="REG_DWORD_BIG_ENDIAN"></span><span id="reg_dword_big_endian"></span><dl> <dt>**REG \_ DWORD Big-DWORD \_ \_**</dt> </dl>          | 32-Bit-Zahl im Big-Endian-Format.<br/> Im Big-Endian-Format wird ein multibytewert im Arbeitsspeicher vom höchsten Byte (dem "großen Ende") bis zum niedrigsten Byte gespeichert. Beispielsweise wird der Wert 0x12345678 als (0x12 0x34 0x56 0x78) im Big-Endian-Format gespeichert.<br/>                                                   |
| <span id="REG_EXPAND_SZ"></span><span id="reg_expand_sz"></span><dl> <dt>**REG \_ Expand \_ SZ**</dt> </dl>                                | NULL-terminierte Zeichenfolge, die nicht erweiterte Verweise auf Umgebungsvariablen enthält (z. b. "% Path%"). Dabei handelt es sich um eine Unicode-oder ANSI-Zeichenfolge, je nachdem, ob Sie die Unicode-oder ANSI-Funktionen verwenden.<br/>                                                                                                     |
| <span id="REG_LINK"></span><span id="reg_link"></span><dl> <dt>**REG- \_ Link**</dt> </dl>                                                | Symbolische Unicode-Verknüpfung.<br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dl> <dt>**REG \_ \_ MultiSZ**</dt> </dl>                                   | Array von auf NULL endenden Zeichen folgen, die mit zwei NULL-Zeichen beendet werden.<br/>                                                                                                                                                                                                                                      |
| <span id="REG_NONE"></span><span id="reg_none"></span><dl> <dt>**REG \_ None**</dt> </dl>                                                | Kein definierter Werttyp.<br/>                                                                                                                                                                                                                                                                                            |
| <span id="REG_RESOURCE_LIST"></span><span id="reg_resource_list"></span><dl> <dt>**REG- \_ Ressourcen \_ Liste**</dt> </dl>                    | Gerätetreiber-Ressourcen Liste.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="REG_SZ"></span><span id="reg_sz"></span><dl> <dt>**REG- \_ SZ**</dt> </dl>                                                      | Mit NULL endende Zeichenfolge. Dabei handelt es sich um eine Unicode-oder ANSI-Zeichenfolge, je nachdem, ob Sie die Unicode-oder ANSI-Funktionen verwenden.<br/>                                                                                                                                                                                          |



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WinNT. h</dt> </dl> |



 

 




