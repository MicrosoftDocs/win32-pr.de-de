---
title: IADsDNWithString-Eigenschaftsmethoden (Iads.h)
description: Die -Eigenschaftsmethode der IADsDNWithString-Schnittstelle legt die in der folgenden Tabelle beschriebene Eigenschaft fest. Weitere Informationen finden Sie unter Schnittstelleneigenschaftenmethoden.
ms.assetid: d3fb67b6-9f7d-4de5-bf01-f9c5b9e4f086
ms.tgt_platform: multiple
keywords:
- IADsDNWithString-Eigenschaftsmethoden ADSI
topic_type:
- apiref
api_name:
- IADsDNWithString Property Methods
- IADsDNWithString.StringValue
- IADsDNWithString.get_StringValue
- IADsDNWithString.put_StringValue
- IADsDNWithString.DNString
- IADsDNWithString.get_DNString
- IADsDNWithString.put_DNString
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51082f31aa9e456ded5498a4711d3ddcfe3c03241235aa14c39920071b110e35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082504"
---
# <a name="iadsdnwithstring-property-methods"></a>IADsDNWithString-Eigenschaftsmethoden

Die -Eigenschaftsmethode der [**IADsDNWithString-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring) legt die in der folgenden Tabelle beschriebene Eigenschaft fest. Weitere Informationen finden Sie unter [Schnittstelleneigenschaftsmethoden.](interface-property-methods.md)

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**DNString**
</dt> <dd> <dl>

Die einem Zeichenfolgenwert zugeordnete DN-Zeichenfolge.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DNString(
  [out] BSTR* retval
);
HRESULT put_DNString(
  [in] BSTR bstrDN
);
```


</dt> </dl> </dd> <dt>

**Stringvalue**
</dt> <dd> <dl>

Der einem DN eines Objekts zugeordnete Zeichenfolgenwert.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StringValue(
  [out] BSTR* retVal
);
HRESULT put_StringValue(
  [in] BSTR varBV
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsDNWithString ist als 370DF02E-F934-11D2-BA96-00C04FB6D0D1 definiert.<br/>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IADsDNWithString**](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring)
</dt> <dt>

[**ADS \_ DN \_ MIT \_ ZEICHENFOLGE**](/windows/win32/api/iads/ns-iads-ads_dn_with_string)
</dt> </dl>

 

 





