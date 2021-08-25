---
description: Der Adresstyp identifiziert das Adressformat, z. B. die Standardtelefonnummer oder E-Mail-Adresse. Nur Anwendungen, die TAPI Version 3.0 oder höher aushandeln, können Adresstypen verwenden.
ms.assetid: 2c32eda1-e510-40eb-ae75-fc7b9e9953cd
title: LINEADDRESSTYPE_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6555ff934ffb8c1b40b8f35d279a2071cad32b80b754af19672108f5e318a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873332"
---
# <a name="lineaddresstype_-constants"></a>LINEADDRESSTYPE-Konstanten \_

Der Adresstyp identifiziert das Adressformat, z. B. die Standardtelefonnummer oder E-Mail-Adresse. Nur Anwendungen, die TAPI Version 3.0 oder höher aushandeln, können Adresstypen verwenden.

<dl> <dt>

<span id="LINEADDRESSTYPE_PHONENUMBER"></span><span id="lineaddresstype_phonenumber"></span>**LINEADDRESSTYPE \_ PHONENUMBER**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Der Adresstyp ist eine Standardtelefonnummer.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_SDP"></span><span id="lineaddresstype_sdp"></span>**\_LINEADDRESSTYPE-SDP**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Adresstyp: Session Description Protocol (SDP)-Konferenz.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_EMAILNAME"></span><span id="lineaddresstype_emailname"></span>**LINEADDRESSTYPE \_ EMAILNAME**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Der Adresstyp ist ein E-Mail-Name.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_DOMAINNAME"></span><span id="lineaddresstype_domainname"></span>**LINEADDRESSTYPE \_ DOMAINNAME**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Der Adresstyp ist ein Domänenname.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_IPADDRESS"></span><span id="lineaddresstype_ipaddress"></span>**LINEADDRESSTYPE \_ IPADDRESS**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Der Adresstyp ist eine IP-Adresse.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




