---
title: WINBIO_BIR -Struktur (Winbio \_ types.h)
description: Stellt einen biometrischen Informationsdatensatz (BIR) dar.
ms.assetid: 39cfab34-0416-4897-bf95-a1b3c3a6a7a1
keywords:
- WINBIO_BIR Struktur Windows Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_BIR
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb9e82a27717b33bcd0e06f5cd5bc23a3c43bc3a67cf70068f1a9eeb31b08bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911093"
---
# <a name="winbio_bir-structure"></a>WINBIO \_ BIR-Struktur

Die **WINBIO \_ BIR-Struktur** stellt einen biometrischen Informationsdatensatz (BIR) dar. Der Informationsdatensatz enthält Header-, Daten- und Signaturblöcke.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WINBIO_BIR {
  WINBIO_BIR_DATA HeaderBlock;
  WINBIO_BIR_DATA StandardDataBlock;
  WINBIO_BIR_DATA VendorDataBlock;
  WINBIO_BIR_DATA SignatureBlock;
} WINBIO_BIR;
```



## <a name="members"></a>Member

<dl> <dt>

**HeaderBlock**
</dt> <dd>

Eine [**WINBIO \_ BIR \_ DATA-Struktur,**](winbio-bir-data.md) die die Größe in Bytes und den Offset des BIR-Headers enthält. Der Header enthält Informationen, die den Inhalt des Informationsdatensatz beschreiben.

</dd> <dt>

**StandardDataBlock**
</dt> <dd>

Eine [**WINBIO \_ BIR \_ DATA-Struktur,**](winbio-bir-data.md) die die Größe in Bytes und den Offset verarbeiteter oder nicht verarbeiteter biometrischer Informationen enthält, die vom Windows Biometric Framework (WBF) erstellt wurden.

</dd> <dt>

**VendorDataBlock**
</dt> <dd>

Eine [**WINBIO \_ BIR \_ DATA-Struktur,**](winbio-bir-data.md) die die Größe in Byte und den Offset von verarbeiteten oder nicht verarbeiteten biometrischen Informationen enthält, die von Sensoren und Software des Herstellers bereitgestellt werden.

</dd> <dt>

**SignatureBlock**
</dt> <dd>

Eine [**optionale WINBIO \_ BIR \_ DATA-Struktur,**](winbio-bir-data.md) die die Größe in Byte und den Offset des Authentifizierungscodes für digitale Signaturnachrichten (Digital Signature Message Authentication Code, MAC) enthält, mit dem die Integrität des BIR überprüft werden kann. Falls vorhanden, muss die Signatur oder der MAC den Header und die Datenblöcke abdecken.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Verwendung von Offsets anstelle von Zeigern ermöglicht eine einfache Serialisierung des BIR und eine weniger komplizierte Übersetzung zwischen 32- und 64-Bit-Umgebungen oder zwischen Benutzer- und Kernelmodus.

Das BIR ist mit dem Common Biometric Exchange Format Framework (CBEFF) kompatibel, das durch NIST 6529-A definiert ist.

Wenn diese Struktur einen *StandardDataBlock-Wert* enthält, muss der *Type-Parameter* des Headers, der durch den *HeaderBlock-Parameter* angegeben wird, auf **WINBIO \_ ANSI \_ 381 \_ FORMAT TYPE festgelegt \_ werden.** Dies ist das einzige Standarddatenformat, das von der aktuellen Version des biometrischen Frameworks Windows wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (einschließlich Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientanwendungsstrukturen](client-application-structures.md)
</dt> <dt>

[**WINBIO \_ \_ BIR-DATEN**](winbio-bir-data.md)
</dt> <dt>

[**WINBIO \_ \_ BIR-HEADER**](winbio-bir-header.md)
</dt> </dl>

 

 





