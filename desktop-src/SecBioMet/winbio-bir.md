---
title: WINBIO_BIR Struktur (winbio \_ types. h)
description: Stellt einen biometrischen Informationsdaten Satz (BIR) dar.
ms.assetid: 39cfab34-0416-4897-bf95-a1b3c3a6a7a1
keywords:
- WINBIO_BIR Struktur Windows-Biometrieframework-API
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
ms.openlocfilehash: e422bbe59414d75541127b41e5e2cc1829adaaa7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344272"
---
# <a name="winbio_bir-structure"></a>Winbio- \_ Struktur "Bir"

Die Struktur von **winbio \_ Bir** stellt einen biometrischen Informationsdaten Satz (BIR) dar. Der Informationsdaten Satz enthält Header-, Daten-und Signatur Blöcke.

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

**Headerblock**
</dt> <dd>

Eine [**winbio \_ - \_ Daten**](winbio-bir-data.md) Struktur, die die Größe, in Bytes und den Offset des BIR-Headers enthält. Der-Header enthält Informationen, mit denen der Inhalt des Informationsdaten Satzes beschrieben wird.

</dd> <dt>

**Standarddatablock**
</dt> <dd>

Eine [**winbio \_ - \_ Daten**](winbio-bir-data.md) Struktur, die die Größe, in Bytes und den Offset der verarbeiteten oder nicht verarbeiteten biometrischen Informationen enthält, die vom Windows-Biometrieframework (WBF) erstellt wurden.

</dd> <dt>

**Vendordatablock**
</dt> <dd>

Eine [**winbio \_ - \_ Daten**](winbio-bir-data.md) Struktur, die die Größe, in Bytes und den Offset der verarbeiteten oder nicht verarbeiteten biometrischen Informationen von Hersteller Sensoren und Software enthält.

</dd> <dt>

**Signatureblock**
</dt> <dd>

Eine optionale [**winbio \_ - \_ Daten**](winbio-bir-data.md) Struktur, die die Größe (in Bytes) und den Offset des Mac (Digital Signature Message Authentication Code) enthält, der zum Überprüfen der Integrität von Bir verwendet werden kann. Falls vorhanden, muss die Signatur oder der Mac den Header und die Datenblöcke abdecken.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Verwendung von Offsets anstelle von Zeigern ermöglicht die einfache Serialisierung von Bir und für eine weniger komplizierte Übersetzung zwischen 32-und 64-Bit-Umgebungen oder zwischen Benutzer-und Kernel Modus.

Der BIR ist mit dem allgemeinen CBEFF (biometrische Exchange Format Framework) kompatibel, das von NIST 6529-A definiert wurde.

Wenn diese Struktur einen *standarddatablock* -Wert enthält, muss der *Typparameter* des Headers, der vom Header *Block* -Parameter angegeben wird, auf den **\_ \_ \_ \_ Formattyp winbio ANSI 381** festgelegt werden. Dies ist das einzige Standarddatenformat, das von der aktuellen Version der Windows-Biometrieframework unterstützt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Client Anwendungs Strukturen](client-application-structures.md)
</dt> <dt>

[**winbio \_ - \_ Daten**](winbio-bir-data.md)
</dt> <dt>

[**winbio- \_ Bir- \_ Header**](winbio-bir-header.md)
</dt> </dl>

 

 





