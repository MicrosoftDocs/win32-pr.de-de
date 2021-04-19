---
description: Die BLOB- \_ Zeichen \_ Satz-Enumeration gibt den Zeichensatz an, der vom aktuellen Konferenz-BLOB verwendet wird.
ms.assetid: 79131b84-19b5-492b-a44e-9d47c365b298
title: BLOB_CHARACTER_SET-Enumeration (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b180a8574f1643a5fc1be134be99c951faaf1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357719"
---
# <a name="blob_character_set-enumeration"></a>BLOB \_ - \_ Zeichensatz-Enumeration

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **BLOB- \_ Zeichen \_ Satz** -Enumeration gibt den Zeichensatz an, der vom aktuellen Konferenz-BLOB verwendet wird.

## <a name="syntax"></a>Syntax


```C++
} BLOB_CHARACTER_SET;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="BCS_ASCII"></span><span id="bcs_ascii"></span>**BCS- \_ ASCII**
</dt> <dd>

Standard mäßiges ASCII-Format.

</dd> <dt>

<span id="BCS_UTF7"></span><span id="bcs_utf7"></span>**BCS \_ UTF7**
</dt> <dd>

Das 7-Bit-Transformations Format von Unicode. Ausführliche Informationen zu diesem Format finden Sie unter Durchführen einer Internet Suche nach RFC 1642.

</dd> <dt>

<span id="BCS_UTF8"></span><span id="bcs_utf8"></span>**BCS \_ UTF8**
</dt> <dd>

UCS-Transformations Format 8. Ausführliche Informationen zu diesem Format erhalten Sie, wenn Sie eine Internet Suche nach ISO (das internationale Organisation für Normung) und IEC (das Internationale Elektrotechnische Kommission) Dokument ISO/IEC JTC1/SC2/WG2 N 1036, vom 1. August 1994, durch den WG2-Projekt-Editor ausführen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                               |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itdirectoryobjectconference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> <dt>

[**\_Zeichensatz erhalten**](itconferenceblob-get-characterset.md)
</dt> <dt>

[**Init**](itconferenceblob-init.md)
</dt> <dt>

[**Setconfererceblob**](itconferenceblob-setconferenceblob.md)
</dt> </dl>

 

 




